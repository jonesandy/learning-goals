# Ruby to JavaScript

```

    ____          __                                          
   / __ \ __  __ / /_   __  __                                
  / /_/ // / / // __ \ / / / /                                
 / _, _// /_/ // /_/ // /_/ /                                 
/_/ |_| \__,_/||.___/ \__, /                                  
   (_)____   / /_ ___/____/                                   
  / // __ \ / __// __ \                                       
 / // / / // /_ / /_/ /                                       
/_//_/ /// \__/ \____/        _____              _         __ 
      / /____ _ _   __ ____ _/ ___/ _____ _____ (_)____   / /_
 __  / // __ `/| | / // __ `/\__ \ / ___// ___// // __ \ / __/
/ /_/ // /_/ / | |/ // /_/ /___/ // /__ / /   / // /_/ // /_  
\____/ \__,_/  |___/ \__,_//____/ \___//_/   /_// .___/ \__/  
                                               /_/            
```

***

The purpose of this document is to convert basic syntax and functionality of Ruby to JavaScript. This will help me take concepts I've learnt in Ruby and **translate** them in JavaScript.   

## Ruby

Making a list of Ruby code I want to find out the equivilant in JavaScript.

* Variables -  How to create them and use them.
* Numbers - How to use them.
* Loops - Type of loops available.
* Functions - How to declare and use them.

## JavaScript

### Variables

Variables exist in JavaScript. They are used similarly to how they are used in Ruby. They have to be defined using the ```var``` keyword:

```javascript
var name = "Andy"
```

JavaScript allows it's variables to be **untyped** which means you don't have to tell it what *type* of data it will store in that variable.  That variable can also change type during the course of it's lifespan.

```javascript
// initialise variable to be number
var myContainer = 42;
// same variable now assigned a string value
myContainer = "Andy";
// same variable now holds an array
myContainer = ['One', 2, 'Three', false];
```

Variables also have **scope** like in Ruby.  Variables in JavaScript either exist locally(inside a function or method) or in the global scope.

```javascript
// global variable
var secret = 42;

function foo() {
    // local variable to function foo
    var superSecret = "bar";
};
```

This allows the use of namespacing to stop variables clashing and causing unexpected behaviour.

```javascript
//global variable set
var life = 42;

function meaning() {
    // local varible set
    var life = "Is a precious gift";
    console.log(life);
};

// console log in global scope
console.log(life) //  42

//console log inside function
meaning(); // "Is a precious gift"
```

### Numbers

Numbers work the same way and can have mathimatical operations done on them.

```javascript
1 + 1 // 2
```

Interstingly in JavaScript if you try and add a string to a number it doesn't flag an error. It will try and convert and give an answer.

```javascript
1 + "1" // "11"

"1" + "1" // "11"

"1" - "0" // 1
```

### Loops

There are many different types of loops in JavaScript. Loops work similar but certain loops need conditions set inside the loop and then iterate afterwards. A for loop is written like so.

```javascript
var total = 0;

for (var i = 0; i < 10; i++) {
    total++;
};
```

There is also a while loop.

```javascript
while (i < 10) {
    console.log(i);
    i++
};
```

