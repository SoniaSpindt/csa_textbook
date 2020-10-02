Declaring Variables
====================================

Sometimes you know you will need a variable in your program but you won't have a value to give it right away. That's ok! Your computer is totally down for you to create a variable that doesn't have a value associated with it just yet.

When you create a variable for the first time, regardless of whether or not you assign it to a value right away, we say we are <b><i>declaring</i></b> a variable. Here's an example of what it looks like to <b>declare</b> two different variables, both of which are not assigned to any values.

```Java
  int score;
  double percentChange;
```
Again, these are statements[^*]. We are telling our computer that we would like to create two variables, one with the name `score` and one with the name `percentChange`. Here is how these variables might look in your computer's memory:

```{image}
:alt: Notional Machine variables in memory 2
:height: 200px
```
<br>Notice that there isn't any value in the box yet? That's because we haven't told our computer to assign a value to either of these names.

Now, in your Algebra class, it's kind of assumed that the values that variables can store are numbers --- makes sense, it is a math class after all. However, in computer science, the collection of values that a variable can store is much larger. We will learn about all of these values over the next few weeks. For now, we're going to stick with what we know, numbers!

I want you to notice the strange little `int` word in the example above. This keyword tells our computer what <b><i>type</i></b> of value can be found in the variable. In this example, we are telling our computer that it can expect an integer to be assigned to the variable `score`.

The second variable has the keyword `double` out front and this is how we tell our computer that we plan to store a decimal value in a variable.

Java is a HELLA picky language, so we ALWAYS have to list the <b>type</b> of the value we plan on storing in a variable [^**]. You cannot change your mind later or try to slyly store a different value type in the variable; once a variable is declared, it will forever be that type! Need a different type? Well tough; you're gunna need to declare a new variable with a different type.

What happens when you're ready to give your variable a value? Keep reading to find out. :D

[^*]: Notice the semi-colons at the end?
[^**]: Computer scientists call hella picky languages like Java "statically typed" languages. I guess it sounds a little more professional that way. :P
