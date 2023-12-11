A common issue of mapping API responses to success or failure is not properly handling new unknown response states that could occur.   There are several ways of handling this situation:

### Create an allowlist
Create a list of successful responses.  All other responses map the failure

### Create a blocklist
Create a list considered failures and map all other responses to success.

### Create an "unknown" response state
This raises an error, alter, or something else, to get an engineer to look at it.  This is better than the first two, in that is raises awareness of a change to the interface being worked with.