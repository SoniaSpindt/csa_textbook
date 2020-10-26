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

ArrayLists
==========

The creators of Java heard everyone's pleas and decided to create a class that every programmer could use, and they called it <b><i>ArrayLists</i></b>. ArrayLists are very similar to arrays, except their size can change depending on how much information that you need to store within them.

Here is an example of how you would declare and initialize a variable to an ArrayList instead of an array.

```{code-cell} java
/* Import the ArrayList class */
import java.util.ArrayList;

/* Declare and initialize the variable brands to an ArrayList of Strings. */
ArrayList<String> brands = new ArrayList<String>();
```

Because ArrayLists were added later on, they are not a part of the standard Java library. This means our computers will have no idea what you're talking about until you import the ArrayList class. Importing classes gives your program access to them, which means that you can use them in your program. When you want to use ArrayLists, you write the statement `import java.util.ArrayList` at the very top of your program. This line of code will always live at the top of your program, and once you add it, you can <b><i>instantiate</i></b> as many ArrayList objects in your program as you would like (Yup, ArrayLists are objects!).

Just like arrays, you cannot mix data types in ArrayLists. In fact, Java is especially picky when it comes to naming the types of values to be stored within an ArrayLists; in a perfect world, you are able to name it twice, once on either side of the assignment operator[^*]. The type of values stored within an ArrayList will always go within angle brackets (`<>`). In the example above, String objects are found in the `brands` ArrayList. I know this because the keyword `String` is contained within the angle brackets. This also means, that `brands` will only ever contain String objects. However, if you were to leave this blank (aka not include the keyword `String` inside of the angle brackets), then your compiler will assume that you wanted to use the most generic type possible in the Java programming language, `Object`. Here is an example of what I mean:

```{code-cell} java
/* Import the ArrayList class */
import java.util.ArrayList;

/* Declare and initialize the variable brands to an ArrayList of Strings. */
ArrayList brands = new ArrayList<>();
```
In this case, the type of objects stored in `brands` will be `Object`, not `String`. The 'Object' class is the mother of all object types in Java; every class (like the ArrayList class and the String class) are derived from the 'Object' class. Although your compiler won't yell at you for leaving the type blank in this case, many professional Java programmers will! It's always best to be as specific and explicit as possible because this will result in fewer errors on your part.  

Also, have you noticed that I didn't provide an example of what it looks like to store values of type `int`, `double`, or `boolean` in an ArrayList? That's because you can't actually do this!!! ArrayLists can only store object types. :(

```{image} https://www.picgifs.com/gifs/movies-and-series/lord-of-the-rings/lord-of-the-rings-5zXkpf.gif
:alt: Nervous
:height: 200px
```

<br>Don't be too sad because the creators of Java created a loophole for our numeric primitive types --- they created a class called `Integer` and a class called `Double`, both of which can be used to instantiate Integer and Double objects [^**]. You don't have to worry about importing these classes because they are a part of the Java standard library. Here is an example of what it would look like to declare and instantiate an ArrayList that contains Integer and Double objects:

```{code-cell} java
/* Import the ArrayList class */
import java.util.ArrayList;

/* Declare and initialize the variable brands to an ArrayList of Strings. */
ArrayList<Integer> integers = new ArrayList<Integer>();
ArrayList<Double> decimals = new ArrayList<Double>();
```

As you can see, the pattern for declaring and initializing variables to ArrayLists is consistent: `ArrayList<Object Type> name = new ArrayList<Object Type>();`. For now, I want you to memorize that these statements need to end with a set of parentheses. We will talk about why this is needed within our next unit. We will also wait to talk about how we can add values to an ArrayList. Until then, our ArrayLists will remain empty.

```{admonition} TL;DR
:class: warning
ArrayLists are like arrays except they can change in size! However, you cannot store primitive types in ArrayLists. You should use Integer objects or Double objects instead!
```

[^*]: There's actually a reason for this. We'll learn more about why in the second half of the class! For now, just memorize, memorize, memorize. :)
[^**]: These are also derived from the <a href="https://www.javatpoint.com/object-class">Object Class</a>.
