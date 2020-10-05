---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Java
  language: java
  name: java
---
Expressions
===========

That was quite the cliffhanger! :p Let me put you out of your misery and say that the answer is "hell yah, we can!"

We can combine numbers and variables with mathematical operators like `+` (addition), `-` (subtraction), `*` (multiplication) and `/` (division). Here is an example of a variable that is declared and initialized to something that is more complex:

```Java
  1. int example = (3 + 12) / 5;
```

Here is what our computer's memory will look like after our computer reads this line of code:

```{image} https://media.giphy.com/media/zFK7sPYUpw4k36izxD/giphy.gif
:alt: Notional Machine variables 5
:height: 200px
```
<br>WHAT?! It's not storing all of `(3 + 12) / 5`? Nope. Your computer will always try to simplify these things because it takes up less space in memory and our computer only has so much of that to use. Consequently, your computer will store the value that you would get if you actually did the math [^*].

And as always, we have a name for this! The lines of code that can be evaluated by our computer and turned into a single value are called <b><i>expressions</i></b>. Your programs will be filled with expressions because they allow us to describe abstract concepts and relationships with code.

Need another example? Let's see how a Java program can be used in medicine to help doctors diagnose patients who might be having a heart attack. One thing that doctors do when they suspect their patient is having a heart attack is draw their blood every few hours. They do this because the heart will release a special protein called Troponin into the blood if it is experiencing a heart attack.

Guess what! Doctors use computers to determine the concentration of these proteins in the blood (computer science really is everywhere these days)! You can imagine that if a patient has a lot of Troponin in his/her/their blood, then their heart is really struggling! Here is a simple program that can determine if someone is having a heart attack.

```{code-cell} java
double enzymesHour0 = 2.0;
double enzymesHour6 = 320.0;
double rateOfChange = (enzymesHour6 - enzymesHour0) / (6 - 0);
System.out.println(rateOfChange);
```
Take a moment to read this program, line by line. See if you can predict what your compiler and consequently, your computer will do once this program is compiled and executed. Once you are done, press the run button to see if you are right!

Again, here is how your computer might make sense of these 4 lines of code:

```{image} https://media.giphy.com/media/RX82QdG4dT725vnwSt/giphy.gif
:alt: Notional Machine variables 6
:height: 200px
```
I want to explicitly name that there are <b>TWO</b> expressions in this program. The first one is more obvious than the other. Can you figure out where they are?

```{image} https://d.wattpad.com/story_parts/498804209/images/14f9e6d1b4ec938a73803243043.gif
:alt: Thinking hard
:height: 200px
```

<br>The first expression is found on line 3 of the program above, and it is `(enzymesHour6 - enzymesHour0) / (6 - 0)`. Like we saw before, your computer will try to turn this into a single value. That means it will grab the values that are stored in `enzymesHour6` and `enzymesHour0` and plug them into the expression where ever it sees these variable names [^**]. Then, it will complete the subtraction and division necessary to arrive at the number 53.0. The variable `rateOfChange` is then assigned to this number. I know that was hard to follow, so here's a little diagram I drew to help you see how your computer substitutes values in for variables used within expressions:


The second expression is found on line 4 of the program, and it is `rateOfChange`. I know it looks like a single value already but it's actually one step away from becoming the simple value it has always wanted to become! Why? Well, your computer has to actually retrieve the value from memory before the `System.out.println` statement tells our computer to display the value in an output window.

```{admonition} TL;DR
:class: warning
1. Expressions are the combination of one or more values that our computer can evaluate in order to produce a new value.
2. Variables can be assigned to expressions, like complex math equations or other variables!
3. Expressions are always evaluated by your computer and turned into their simplest form.
```

[^*]: Computers also care about PEMDAS! They will follow the order of operations described in your Algebra classes, so use parentheses if you're ever unsure about how execution will occur. Parentheses takes the highest priority!
[^**]: Algebra strikes again! This is very much like the algebraic concept of substitution.
