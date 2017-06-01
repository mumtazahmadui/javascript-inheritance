# JavaScript Inheritance

How to “Achieve Inheritance”in JavaScript?

There are two ways

1. Pseudo classical Inheritance
2. Prototype Inheritance

<b>Pseudo classical Inheritance</b> is the most popular way. In this way, create a constructor function using the new operator and add the members function

Example as,

```javascript
// Create a helper function.
if (typeof Object.create !== 'function') {

        Object.create = function (obj) {
            function fun() { };
            fun.prototype = obj;
            return new fun();
        };
}

//This is a parent class.
var parent = {
        sayHi: function () {
            alert('Hi, I am parent!');
        },
        sayHiToWalk: function () {
            alert('Hi, I am parent! and going to walk!');
        }
};

//This is child class and the parent class is inherited in the child class.
var child = Object.create(parent);

child.sayHi = function () {
    alert('Hi, I am a child!');
};
```

```javascript 
<button type='submit' onclick='child.sayHi()'> click to oops</button>
```

```
The output is : Hi, I am a child!
```
