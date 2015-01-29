# setTimeout and setInterval
Ways to do tasks/functions/things asynchronously at a set delay or set interval.
##setTimeout(function, ms)
- This means that 'x' milliseconds from now, place the contained function in the execution queque.  The amount of time set will not be exact.  
- This can be used to prevent the user interface (UI) from being blocked while a browser is processing.  ex: setTimeout (function, 0)

##setInterval(function, ms)
- This means that this function will be repeated every 'x' milliseconds.  
- Use clearInterval to stop the call.
