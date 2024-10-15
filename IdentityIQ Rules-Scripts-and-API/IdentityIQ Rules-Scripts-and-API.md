# SailPoint IdentityIQ Rules, Scripts and API

# Table of Contents

1. **[Rules, Scripts, and Beanshell](#rules-scripts-and-beanshell)**
	1. [Rule Arguments](#rule-arguments)
		1. [Context](#context)  
		2. [Log](#log)  
	2. [Print the BeanShell Namespace](#print-the-beanshell-namespace)  
	3. [Rule Libraries](#rule-libraries)
2. **[API Introduction](#rules-scripts-and-beanshell)**

## Rules, Scripts, and Beanshell

### Rule Arguments

All rule and script hooks are automatically provided at least two input arguments – **context** and **log**.

#### Context

The context argument is a SailPointContext object, the entry point into the SailPoint API – giving you methods for accessing other objects and interacting with the SailPoint database. 

#### Log

The log argument is a Logger object, which lets you use Log4j, the same logging utility used by the IdentityIQ core product, to generate logging messages from your rules. 

### Print the BeanShell Namespace

If you’re unsure about what variables are available to your rule or script, you can use the snippet of BeanShell shown below to figure it out.  This logic prints the name and value of each variable in the BeanShell namespace – in other words, all the variables known to BeanShell at that point in time.

The code example below is URL encoded for use within an XML file.

```java
System.out.println("Beanshell namespace:");

for (int i = 0 ; i &lt; this.variables.length ; i++) {
		String name = this.variables[i];
		if ("transient".equals(name)) { continue; } 
		Object value = eval(name);
		if (value == void)
				print(name + " = void");
		else if (value == null)
				print(name + " = null");
		else
				print(name + ": " + value.getClass().getSimpleName() + " = " + value);
}
```

```
// output 

Beanshell namespace:
bsf: BSFManager = org.apache.bsf.BSFManager@d4de53d
log: Log4jLog = org.apache.logging.log4j.jcl.Log4jLog@489edd0d
bsh: This = 'this' reference to Bsh object: NameSpace: Bsh Object (bsh.NameSpace@4b8d8ae6)
context: InternalContext = sailpoint.server.InternalContext@37edef77
```

### Rule Libraries

Many rule objects are just a single block of code, executed together as a unit. But IdentityIQ also allows you to create rule objects that contain multiple separate functions or methods. These are called rule libraries. 

Rule libraries are a way you can manage collections of methods that can be accessed from within other rules. These can help promote code re-use. 

If you find yourself continually writing the same segment of code over and over again, consider including that logic in a rule library, so you can access it from other rules. If you ever need to change it, you can change it in one place and have it changed everywhere automatically. As a best practice for artifact management, you should group related methods together in a rule library, creating as many rule libraries as you need for different logical groupings.

In this example of rule referencing a rule library method, you see a rule library called My Library that contains a public method called doSomething. 

```xml
<Rule name='My Library'>
   <Source>
      public void doSomething() { // do stuff }
      public String returnSomething() { // do stuff and return a String } 
   </Source>
</Rule>
```

To use this method in a rule, you need to include a reference to the Rule Library in the XML of that rule with a <ReferencedRules> element, then in the body of the rule itself, you can call the doSomething method and the system will find it in the rule library and execute its code. 

```xml
<Rule…>
   <ReferencedRules>
       <Reference class='Rule' name='My Library'/>
   </ReferencedRules>
   <Source>
       doSomething();
   </Source>
</Rule>
```

## API Introduction

### IdentityIQ Architecture

Because IdentityIQ is a Java application, it follows an object-oriented paradigm. When you interact with IdentityIQ’s API, you retrieve and act on objects:

- Identity objects
- Application objects
- Certification objects
- Link and bundle objects
- And more


### SailPointContext

> The SailPointContext object is a critical component for working with IdentityIQ’s API in BeanShell rules and scripts.  It is effectively the entry point to the API – the class that lets you retrieve and work with other objects. This lesson covers the key operations supported by the SailPointContext and the two objects used to direct and constrain its searching functions – the QueryOptions and the Filter objects

The SailPointContext supports object retrieval through multiple methods, and some of these support more than one signature, so they behave differently based on the arguments you provide.

#### getObjects

The `getObjects` method lets you retrieve one or more objects of a specified type. View examples below.

```java
List <SailPointObject> getObjects(class)
List <SailPointObject> getObjects(class, QueryOptions) // better performance
```

#### search

The `search` method lets you retrieve whole objects, like getObjects does, or individual attributes of objects that match your search criteria. 

```java
Iterator<SailPointObject> search(class, QueryOptions)

// Example
Iterator apps = context.search(Application.class, qo);

Iterator<SailPointObject> search(class, QueryOptions, properties) // better performance

// Example
Iterator users = context.search(Identity.class, qo, "name, status");
Iterator users = context.search(Identity.class, qo, props);
```

#### Single Object Retrieval

The SailPointContext offers two options for retrieving a single object by a unique identifier. Both require specification of the class name, either the name or GUID value as an argument – effectively, their search criteria.  

#### getObjectByName

The `getObjectByName` method requires the class name as a string.

```java
SailPointObject getObjectByName(class, String name)

// Example
Identity id = context.getObjectByName(Identity.class, "Bob.Smith");
```

#### getObjectById

The `getObjectbyId` method requires the the GUID value of the class.

```java
SailPointObject getObjectById(class, String guid)

// Example
Application app = context.getObjectById(Application.class, "ff80808161b51a2a0161b51a434a0002");
```