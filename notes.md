http://dmitrysoshnikov.com/ecmascript/javascript-the-core/


Read the following, then answer the below questions:

http://stackoverflow.com/questions/133973/how-does-this-keyword-work-within-a-javascript-object-literal

Describe four different ways a function can be called?

What is the `this` variable bound to in each of the four different ways a function can be called?

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

In the following code snippet, what will be displayed? 

```javascript
var foo = {};
foo.someMethod = function() {
    function standAlone() {
        console.log(this == foo);
    }

    console.log(this == foo);
    standAlone();
};
```

Given the following code snippet:

```javascript
var a = {
    func: returnThis
};

var b =	a.func;
var c = { func: a.func };
```

What will `a.func() == a` return?

What will `b() == a` return?

What will `b() == b` return?