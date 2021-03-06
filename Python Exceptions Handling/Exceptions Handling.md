# Python - Exceptions Handling

An exception is an error that happens during the execution of a program.There are a number of built-in exceptions, which indicate conditions like
reading past the end of a file, or dividing by zero. You can also define your own exceptions.

## Raising an Exception

You can raise an exception in your own program by using the raise exception
statement.

Raising an exception breaks current code execution and returns the exception
back until it is handled.

## Exception Errors Examples-
The words "try" and "except" are Python keywords and are used to catch exceptions.The code within the try clause will be executed statement by statement.

If an exception occurs, the rest of the try block will be skipped and the except clause will be executed.

## Example:
```
try:
    some statements here
except:
    exception handling
    
try:
    print 1/0
except ZeroDivisionError:
    print "You can't divide by zero."
 ```
 
The error handling is done through the use of exceptions that are caught in try blocks and handled in except blocks.
If an error is encountered, a try block code execution is stopped and transferred down to the except block. 

Sometimes it is useful to find out exactly what went wrong, or to print the python error text yourself.
For example:
```
try:
    the_file = open("the_parrot")
except IOError, (ErrorNumber, ErrorMessage):
    if ErrorNumber == 2: # file not found
        print "Sorry, 'the_parrot' has apparently joined the choir invisible."
    else:
        print "Congratulation! you have managed to trip a #%d error" % ErrorNumber
        print ErrorMessage
 ```       
    
