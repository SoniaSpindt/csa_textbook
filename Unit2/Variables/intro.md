Variables
==================

It's time to learn how to create attributes within our Java programs! The way we do this is with a programming concept called <b><i>variables</i></b>. Does this term sound familiar to you? It's possible that you heard about it in your Algebra class, which is a class all about variables! The variables you learned about in your Algebra class are very similar to the variables that you will see and create in this class; in both cases, <b><i>they are the names we give values</i></b>.

For example, you may have seen a simple equation in your Algebra class that looks like this:

```Java
  x = 3
```

If I asked you "What is x?" you would (hopefully) answer with "3". See, the name `x` is given to the value `3`! We will do the same thing in this class, except it will look something like this:
```Java
  1. int x = 3;
```
As you can see, this line of code is a statement that was written on line 1 of our program[^*]! This means we are asking our computer to do something on line 1. But what exactly are we asking it to do? Well, we are asking our computer to associate the name `x` with the value `3`. So, when I ask you what `x` is in this class, you can respond with "x is 3", or "x gets 3", or "3 is assigned to x". All of these responses are valid and they all mean the same thing.

I prefer the last response, "3 is assigned to x", because this secretly refers to the name computer scientists give the equal sign; they call it the <b><i>assignment operator</i></b>. The assignment operator is responsible for actually telling our computer that you ship a particular name and value.

```{image} https://media.giphy.com/media/HkA9xsCxJCRWw/giphy.gif
:alt: Shipping variables
:height: 200px
```
<br>Remember how I said it was important to know a little bit about how your computer works when learning to program? We want to keep thinking about this as we learn new stuff because it will help make your prediction skills sharp[^**]. Most of the time, this involves me drawing pretty pictures. :P So here's a picture of how your computer might "think" about the variables created in the following Java program:
```Java
  1. int x = 3;
  2. int y = 4;
```
```{image} https://media.giphy.com/media/BmsLYXlBAbDgLzBtye/giphy.gif
:alt: Notional Machine variables 1
:height: 200px
```
<br>As you can see, our computers are super organized; they love to put all of the information they come across in boxes that are clearly labeled! That label is super important to include because it helps our computer easily find important bits of information later on. This is also why many people say that variables "store" values in them. If it helps you to think of a variable as a little box used to store a value, then cool! You do you, boo. :)

```{admonition} TL;DR
:class: warning
Variables are names that store values!
```

[^*]: You can tell it's a statement because it ends in a semi-colon.
[^**]: It's also important to be able to do this because "predict the output" questions will make up a large part of the AP CSA exam.
