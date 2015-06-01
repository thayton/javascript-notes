http://stackoverflow.com/questions/133973/how-does-this-keyword-work-within-a-javascript-object-literal

In the following code, why do we save a reference to `this` in variable `that`?
What does variable `that` point to when function `bar()` is called?

```javascript
var foo = {};
foo.someMethod = function (){
    var that=this;
    function bar(){
        alert(that);
    }
}
```



