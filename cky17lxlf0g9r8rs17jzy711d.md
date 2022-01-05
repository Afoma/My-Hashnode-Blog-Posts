## How to troubleshoot JavaScript ReferenceError "x" is not defined

Ever been writing code and then you notice that your code isn't giving any or the desired result even after you save your code and refresh your browser page? On checking the console, you see an error that reads ` ReferenceError x is not defined `. 

` ReferenceError "x" is not defined ` is an error that is given by the JavaScript engine when the identifier "x" cannot be found within the scope it is being referenced in.
This tutorial shows you the potential causes of the error and how to resolve it when the problem arises. 

## Reproducing the error

Here are instances of the error message.

### Not Yet Existing Variable 

This error happens when a variable that has not yet been declared is trying to be used. For example:

```
x.toUpperCase();

``` 

Notice that the string "x" has not been declared before we command the JavaScript engine to convert it to an uppercase letter. This will throw an error ` Uncaught ReferenceError: x is not defined `.

<hr/>

```
"use strict";
x=[1,2,3];'

``` 
This particular instance only throws the ` Uncaught ReferenceError: x is not defined ` as long as the `use strict` is employed. 

### Wrong Scope

This same error can also be a result of trying to access the variable in a totally different scope.

```
function minus(){
    let x=6;
    let y=4;
    return x-y;
}
console.log(x);

``` 
Trying to log `x` to the console will throw the ` Uncaught ReferenceError: x is not defined ` because it is not within the function scope.

### Typo

The JavaScript engine throwing this error could also be a result of some typographical error in naming the variable.

```
let tear="EAR";
x.toLowerCase();

``` 
This would also throw the error message ` Uncaught ReferenceError: x is not defined ` because `x` is not `tear`, hence the JavaScript engine doesn't recognize it.

## Solutions

Now that we have seen how the error is produced, let's see solutions to the error.

### Declaring a variable before accessing a variable

```
let x="Ear";
x.toUpperCase();

``` 
Notice here the variable `x` was already declared before we tried to access it. This will convert the string in the variable `x` to upper case letters.

### Right Scope

Another solution would be to access the variable within the scope it was declared.


```
function minus(){
    let x=6;
    let y=4;
    console.log(x);
}

``` 
Logging the variable `x` to the console will display `6` and wouldn't throw any error.

Declaring the variable by using the `var` keyword only and not the `let` or `const` keyword makes the variable accessible from anywhere in the code. For example:

```
var x=8;
function alert(){

}
console.log(x);

``` 
Logging the variable `x` to the console will display `8` and wouldn't throw any error.

### Ensure the variable's spelling corresponds with the variable name

Sometimes we could be in a rush when coding and accidentally mistype the already declared variable name. So we make sure to ensure the correct spelling of the variable name. 

```
let song="just dance";
song.toUpperCase();

``` 
This will convert the string in the variable `song` to capital letters.

## Learn more

Search across open-source JavaScript repositories that have the `ReferenceError` to understand the message more.
