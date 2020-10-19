Reference Variables
===================

Let's take a look at a Java program that contains both a String and a boolean:

```Java
1. boolean amIRight = true;
2. String praise = "Yussssss!";
```

Our computers will think differently about the String stored in the variable `praise` than the boolean stored in the variable `amIRight` because Strings are objects and booleans are not. Take a look at the following animation to see how this differs:

```{image} https://media.giphy.com/media/iyS29c9WJcLUMl6k8I/giphy.gif
:alt: Notional machine primitive vs. reference variables.
:height: 300px
```
<br>Really different thought process, right? When you are storing a value in a variable that is an object, we say that the variable is a <i>reference variable</i>. This is because the actual object is not stored in the variable itself; instead, a reference to that object is stored in the variable. The giant green dot and arrow represent how our computer <i>references</i> a value found elsewhere in its memory. I like to use a dot and arrow in my diagrams because they are related to how engineers talk about the act of referencing objects; they say "the variable `praise` <i>points to</i> the String 'Yusssss!'." Get it? Arrows point to things! :)

Let's take a look at another example that will help you see why it might be beneficial for variables to point to objects:

```Java
1. String dolly = "llama";
2. String como_se = dolly;
```
```{image} https://media.giphy.com/media/JuF4q52QC3XhQXpirn/giphy.gif
:alt: Notional machine referencing the same object.
:height: 300px
```

Woah! They point to the same object? Yup! This is a preferable system for our computers because it allows them to reuse objects that have already been created; this saves our computers some time and effort because they don't have to go through the act of creating a copy of an object. This process is especially awesome when our objects contain a lot more information than just a string of characters.

What happens if we assign `dolly` to a new String object, like so?
```Java
1. String dolly = "llama";
2. String como_se = dolly;
3. dolly = "Parton";
```
Will the variable `como_se` point to the new String "Parton"? Or will it continue to point to the String "llama"?

Let's see what happens!

```{image} https://media.giphy.com/media/TBALqHr9P8tWEQOKi7/giphy.gif
:alt: Notional machine referencing a new object
:height: 300px
```

<br>It continues to point to the String object "llama"! Now, what if we were to do this?

```Java
1. String dolly = "llama";
2. String como_se = dolly;
3. dolly = "Parton";
4. como_se = dolly;
```

If we were to assign the variable `como_se` to `dolly` again, then the String object "llama" would disappear, like so:

```{image} https://media.giphy.com/media/ejk0RCkE5B5sY3zo1S/giphy.gif
:alt: Notional machine garbage collection
:height: 300px
```

<br>Why? Once an object is no longer referenced by any variables in a program, your computer will clean things up at runtime and get rid of any values that are not actively used. This keeps your computer's memory free and available for future use. This is also really useful for me when drawing these diagrams; I would run out of room for drawing if your computer wasn't a clean freak. :)


```{admonition} TL;DR
:class: warning
1. Strings are not stored directly in variables because they are objects.
2. Variables <i>point to</i> objects that are found elsewhere in our computer's memory.
```
