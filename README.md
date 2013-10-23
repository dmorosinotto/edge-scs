# edge-scs

## What is it

edge-scs is an extension for [edge](https://github.com/tjanczuk/edge) that allows invoking scriptcs from node.js.

## Hello edge-scs

Below is a snippet of using scriptcs from edge

```javascript
var edge = require('edge');
var hello = edge.func('scs', function() {/*
Func<IDictionary<string,object>, Task<object>> execute = p=> Task.FromResult<object>(p["value"]); 
execute
*/});
hello({"value": "Hello from scriptcs"}, function(error,result) {
    if (error) throw error;
    console.log(result.Result);
}); 
```



