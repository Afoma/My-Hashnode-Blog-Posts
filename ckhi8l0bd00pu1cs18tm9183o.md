## Stand in Line

<figure>
<img src="https://media.giphy.com/media/M76XI0UYkJkys/giphy.gif" alt="sound of music farewell song gif">
</figure>
Exercise: <br>
Write a function `nextInLine` which takes an array (`arr`) and a number (`item`) as arguments.<br>
Add the number to the end of the array, then remove the first element of the array.<br>
The `nextInLine` function should then return the element that was removed.<br>
<h2>Brief Summary</h2><br>
```
1. A brief explanation of functions and array
2. Solving the question
``` 
<h3>A brief explanation of functions</h3>
<p>An array is a special variable, whose length is not fixed [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array) , and which can hold more than one value at a time - [Wikipedia](https://www.w3schools.com/js/js_arrays.asp) .</p>
<p>A function is a set of instructions compiled into a block of code. Everything in the block of code will be executed when you call the function.</p>
Solution:<br>

A breakdown of the question<br>
- Write a function, with `arr` and `item` as parameters<br>
- Add the number to the end of the array<br>
- Remove the first element of the array<br>
- Return the element that was removed from the array<br>
<h3>Write a function, with `arr` and `item` as parameters</h3>

```
function nextInLine(arr, item) {

}
``` 
<h3>Add the number to the end of the array</h3>

```
function nextInLine(arr, item) { 
   arr.push(item);
}
``` 
<h3>Remove the first element of the array</h3>

```
function nextInLine(arr, item) { 
   arr.push(item);
   arr.shift();
}
``` 
<h3>Return the element that was removed from the array</h3>

```
function nextInLine(arr, item) { 
   arr.push(item);
   return arr.shift();
}
``` 
Calling the function with an argument of `[2]` and `8`, returns `2`.<br>
I screenshot the image below from my Console.
![nextInLine function.PNG](https://cdn.hashnode.com/res/hashnode/image/upload/v1605277557103/aGEC2rzLA.png)

<h3>The wrong answer that kept me stuck for a while</h3>

```
function nextInLine(arr, item) { 
   arr.push(item);
   arr.shift();
   return arr.shift();
}
``` 
<p>By writing this code this way, I thought the code will return the removed element of the array, but it gives a wrong answer because the code simply interprets that the removal of the first element of the array took place twice. Hence, removing the first element, which will make the former second element to be the first element, removing the former second element, and returning the recently removed value.</p>
<p>Looking at this question now, I feel embarrassed to have found this question difficult some time ago. I really hope it is useful to some people who need help with finding the solution to this question.</p>
<p>I am not yet done with my exercises on freecodecamp, so I will be updating this series as I figure more questions out.</p>
<p>Thank you for taking out your time to read this article. I look forward to getting feedback from you.</p>
<p>This article was inspired by @[Chris Bongers](@dailydevtips) session at the Hashnode Technical Writing Bootcamp.</p>
