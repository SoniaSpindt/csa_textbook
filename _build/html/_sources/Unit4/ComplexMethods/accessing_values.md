Accessing and Modifying Values in 2D Arrays
===========================================

Think back to the letter example from the previous page:

```java
String[] a = {"A", "a"};
String[] b = {"B", "b"};
String[] c = {"C", "c"};
String[][] alphabet = {a, b, c};
```
It's important to think about the index of each element found within each array. In order to talk about a single value in this 2D-array, we need to refer to two separate index values! We need one index to tell us what row to look at and another index to tell us what column to look at. Here's what I mean:

```{image} index2darray.png
:alt: 2D-array
:height: 300px
```
<br>If I wanted store the letter "B" in a separate variable, I would need to write the following statement:

```java
String letter = alphabet[1][0];
```
This is our index operator on steroids! More specifically, we have to specify the row and the column of the value that we are trying to access. In the example above, we are targeting row 1 and column 0 (remember, we start counting at 0 instead of 1 in computer science!!!).

What would you need to write in order to access the letter "c"?

```{image} https://i.pinimg.com/originals/dd/49/5e/dd495e07229445a7f028c3253217f146.gif
:alt: Thinking
:height: 200px
```

<br>Did you say `alphabet[2][1];`?!

You can use the index operator to change values in a 2d-array as well. Imagine we wanted to change "a" to "Z". Then, we would write:
```java
alphabet[0][1] = "Z";
```

The index operator is very useful when accessing or modifying values found within arrays. It's also definitely going to show up on the exam, so you might as well practice using it a bit right now. Take a look at the 2D-array named `pattern` in repl.it. What lines of code would you need to write in order to get this pattern to show up instead:
```java
**
**
**
**
```
There's a catch though! You cannot change any lines of code in this program -- you can only add new lines! :)
<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/712Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>
