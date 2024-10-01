# SailPoint IdentityIQ Rules, Scripts and API

## Rule Arguments

All rule and script hooks are automatically provided at least two input arguments – **context** and **log**.

### Context

The context argument is a SailPointContext object, the entry point into the SailPoint API – giving you methods for accessing other objects and interacting with the SailPoint database. 

### Log

The log argument is a Logger object, which lets you use Log4j, the same logging utility used by the IdentityIQ core product, to generate logging messages from your rules. 