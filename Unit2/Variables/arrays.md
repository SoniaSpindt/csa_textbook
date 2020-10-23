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

Arrays
======

Take a look at this Java program:

```{code-cell} java
String sneaker1 = "Air Jordan 1";
String sneaker2 = "Buscemi 100 MM Diamond";
String sneaker3 = "Air Jordan 12 (Flu Game)";
String sneaker4 = "Air Jordan 11 'Jeter'";
String sneaker5 = "Nike Air Mag Back to the Future";
String sneaker6 = "Adidas NMD_R1 Friends and Family";
String sneaker7 = "Nike Yeezy 2 Red October";
String sneaker8 = "Solid Gold OVO x Air Jordan";
String sneaker9 = "Nike Moon Shoe";
String sneaker10 = "Air Jordan Silver Shoes";
```
<br>Is this you right now?
```{image} https://media.giphy.com/media/aMO3tYzgitW8c8u2Si/giphy.gif
:alt: Doing too much
:height: 200px
```
<br>I'm right there with you; there are SO many variables in the program above! Technically speaking, there's nothing wrong with this program, but it sure would be nice to embrace our lazy selves again. How could be streamline this a bit more? Well, we could do something like this!

```{code-cell} java
String[] sneakers = {"Air Jordan 1", "Buscemi 100 MM Diamond", "Air Jordan 12 (Flu Game)", "Air Jordan 11 'Jeter'", "Nike Air Mag Back to the Future", "Adidas NMD_R1 Friends and Family", "Nike Yeezy 2 Red October", "Solid Gold OVO x Air Jordan", "Nike Moon Shoe", "Air Jordan Silver Shoes"};
```
```{image} https://i.imgur.com/3v3NsPD.gif
:alt: SO nice
:height: 200px
```
<br>SO much better, right?

When we need to store multiple values in a single variable we use something called an <b><i>array</i></b> in Java. How are they used? Pay attention to how I declared the sneakers variable: `String[] sneakers`. It looks a lot like how we declare reference variables for Strings! However, if you squint really hard, you'll notice that there are now square brackets (`[]`) after the keyword `String`. The square brackets are how we let our computer know that we plan on initializing `sneakers` to a list of String objects, instead of single String.

Initialization is also very similar to what we have seen so far. In this case, all you need to do is list every value that you would like to use in between a pair of curly braces (`{}`). The commas are important to include within your list because they separate the values from one other. Everything else about our data types is the same; booleans are never capitalized, Strings must be contained within quotes, and your numbers are either integers or decimal values.

Here is what it would look like to declare variables of the four data types that we have seen so far, and initialize them to arrays:
```{code-cell} java
int[] ids = {0341, 2293, 7182};
double[] temps = {98.6, 95.9, 104.2};
boolean[] test_results = {false, false, true};
String[] patients = {"Robert Blah", "Jane Smith", "John Doe"};
System.out.println(patients);
```

If you haven't already executed this program, please do so now. You will notice that when we use the System.out.println statement to display the `patients` array, we see something hella weird: `[Ljava.lang.String;@b2e0fdf`.

This is how your computer tells you that there is an object stored in a chunk of memory called "b2e0fdf". In other words, this is what it looks like to display the value of a reference variable; it displays the actual reference!

You know what this also means? This means that arrays are objects! I know it's hard to tell in this case because we can't check to see if the keyword in our declaration statement is capitalized because there is no `array` keyword to look at. Instead, you will just have to memorize the fact that arrays are objects and the variables that store them are reference variables.

If it helps, this is how our computer will think about the program above:

```{image}
:alt: Notional machine arrays
:height: 300px
```

One last thing! You cannot store values of different types in a single array. Remember, Java is hella picky when it comes to the types of values that are stored in variables. This trend continues into the use of arrays. If you try to mix values together, like int and double, in a single array, your compiler will yell at you.  
