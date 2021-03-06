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

Strings
=======

Before we begin talking about a new data <i>type</i>, I want us to take a quick second to admire the data <i>types</i> that we have seen so far. They are:

```{admonition} Data Types
1.  `int`
2. `double`
2. `boolean`
```

It is important to notice that these three data <i>types</i> have a few things in common. First of all, the keywords that represent all of these data types begin with a lowercase letter. I know this doesn't seem particularly special or important, but this fact can help you determine if a type is considered a "primitive data type". I like to think of the primitive data types as the fundamental building-blocks of programming in Java; they are like a single brick in a giant building or a single atom found in an insanely complex molecule!

Secondly, these data types are relatively small in size! This means they can be stored directly in variables. Consider the following Java program that declares and initializes three variables, one of each data type that we have seen so far:

```Java
1. int airPodsPurchased = 1;
2. double price = 124.99;
3. boolean wireless = true;
```

Here is how our computer would think about these three lines of code:
```{image} https://media.giphy.com/media/polVkhmJJmfO8OexvP/giphy.gif
:alt: Notional machine primitive data types.
:height: 300px
```

<br>As you can see, these values sit directly in the boxes that represent each variable. They can do this because they are primitive data types. This is important to remember because the data type that we are learning about today does not do this. Why? Because it's secretly an object. GASP!!!

```{image} https://media3.giphy.com/media/3oEjHKvjqt5pssL99C/giphy.gif
:alt: Shock and awe gif.
:height: 200px
```
<br>This new and improved data type is called a <b><i>String</i></b>, and it represents all of the characters you can find on your computer's keyboard. Here's what it would look like to declare and initialize a variable of <i>type</i> <b>String</b>:

```{code-cell} java
/* Declare a variable of type String */
String brand;

/* Initialize the variable to a String value */
brand = "Ford";

System.out.println(brand);
```

Notice how the keyword `String` begins with a capital letter? This tells us that the type is an object. More specifically, it's an object created from the String class. You should also notice that the variable `brand` is initialized to the value `"Ford"`, which is a collection of letters found on your keyboard, surrounded by quotation marks. The quotation marks MUST be placed around all String values. It doesn't matter what characters you put inside; as long as you surround those characters with quotation marks it will be seen by your compiler as <i>type</i> `String`.

This isn't all you should know about Strings! Keep reading to see how our computer thinks about Strings stored in variables.

```{admonition} TL;DR
:class: warning
1. The data type `String` is an object, not a primitive.
2. All Strings need quotation marks!
```
