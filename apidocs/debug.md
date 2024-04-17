# Notes for module dflib.debug
The debug module provides a few functions to facilitate generating debugging messages. The messags are output to stderr with some colorizing. 

## function dflib.debug.set_debug(boolean)
turn debugging on and off with boolean 

## function dflib.debug.get_debug()
get debug state as boolean 

## function dflib.debug.debug(*args)
print *args as debug message with caller 

## dflib.debug.error(*args)
print *args as message message with caller 

## function dflib.debug.dpprint(object)
debug wrapper for pprint. Each line is output as a debug message. 


