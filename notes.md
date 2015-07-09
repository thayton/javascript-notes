```javascript
f = function() {};
f.prototype.name = 'rob';

x = {};
x.__proto__ = f.prototype;
x.name = 'todd';

y = {};
y.__proto__ = f.prototype;
y.name = 'allen';

z = {};
z.__proto__ = f.prototype;
```

What are the values of x.name, y.name, z.name?

```javascript
delete x.name;
```
Now what's the value returned by x.name?

Now add the following code:

```javascript
f.prototype.say_my_name = function() { return this.name; };
```

What do the following return?

```javascript
f.prototype.say_my_name();

x.say_my_name();

b = f.prototype.say_my_name;
b();
```

http://dmitrysoshnikov.com/ecmascript/javascript-the-core/

Given the following code:

```javascript
y = { name: 'y', getName: function () { return this.name; }};
x = { name: 'x'};
x.__proto__ == y;
window.name = 'window';
```

What will the following calls display?
```javascript
y.getName();
x.getName();

f = y.getName;
f();
```

Read the following, then answer the below questions:

http://stackoverflow.com/questions/133973/how-does-this-keyword-work-within-a-javascript-object-literal

Describe four different ways a function can be called? Or to put it another way, what are the
four patterns of function invocation in Javascript?

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