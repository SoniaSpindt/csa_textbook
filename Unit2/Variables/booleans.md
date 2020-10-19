Booleans
========

So far, we have seen that we can store integers and decimals in our variables. Sweet! However, this is not all we can store in our variables. Today, we are going to discuss a new value <i>type</i> called <b><i>booleans</i></b>. Ignore the weird sounding name! These values are really useful when programming because they allow our computers to communicate the idea of something being <i>true</i> or <i>false</i>. In my opinion, the boolean is one of the most powerful data types that we can use in our programs because it allows our computers to make decisions!

Like I said, <b><i>booleans</i></b> are the values <i>true</i> and <i>false</i>. That's it! These two little words make up this super awesome data type. If we wanted to declare a variable that stores a boolean value, we might write something like this:

```Java
1. boolean answer;
2. boolean result;
```
Here is how our computer would think about these lines of code:

```{image} https://media.giphy.com/media/O5xj7zzJQU2pmYfYWV/giphy.gif
:alt: Notional machine boolean variable.
:height: 200px
```
<br>Notice that the type of these variables is `boolean`. What if we wanted to initialize these variables to boolean values? Well, it might looks something like this:

```Java
/* Declare boolean variables */
1. boolean answer;
2. boolean result;
/* Initialize variables to boolean values */
3. answer = true;
4. result = false;
```
Our computer would think about this program like so:
```{image} https://media.giphy.com/media/6vwrVSwUyI1RDm0s6j/giphy.gif
:alt: Notional machine boolean variable.
:height: 200px
```
<br>Need to declare and initialize a boolean variable all in a single line? That will look something like this:

```Java
1. boolean gameWon = false;
```
```{image} https://media.giphy.com/media/kef9klv146Wv5oS0fl/giphy.gif
:alt: Notional machine boolean variable.
:height: 200px
```

```{admonition} TL;DR
:class: warning
1. A boolean value can be either true or false. That's it!
2. When declaring boolean variables, you must use the keyword `boolean` for its type.
```
