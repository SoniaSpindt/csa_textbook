Expressions
===========

That was quite the cliffhanger! :p Let me put you out of your misery and say that the answer is "hell yah, we can!"

We can combine numbers and variables with mathematical operators like `+` and `-`. Here is an example of a variable that is declared and initialized to a more complex value:

```Java
  int example = (3 + 12) / 5;
```

Here is what our computer's memory will look like after our compiler reads this line of code:
```{image}
:alt: Notional Machine variables in memory 4
:height: 200px
```
<br>WHAT?! It's not storing all of `(3 + 12) / 5`? Nope. Your computer will always try to simplify these things because it takes up less space in memory (and our computer only has so much of that to use). Consequently, your computer will store the value that you would get if you actually did the math [^*].

And as always, we have a name for this --- the chunks of complex code that can be turned into simple values are called <b><i>expressions</i></b>. Your programs will be filled with expressions because they allow us to describe much more complex ideas with code. Here is a program that a doctor might use to determine if someone is having _____:

```Java
int
double rateOfChange

[^*]: Computers also know about PEMDAS! So they will follow the order of operations described in your Algebra classes.
