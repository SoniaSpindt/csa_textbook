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

Strings in Expressions
======================

Years of math classes have probably convinced you that it's possible to add numbers together. What about Strings? Can we add them together? Yup! However, it's not as fancy a process as adding numbers together; when we add Strings together, we simply squish the strings together, so they become one giant String.  

Take a look at this program and try to predict what will be displayed as a result of executing this program (don't press run until you're ready to check your answer!):

```{code-cell} java
String firstName = "Greatest";
String lastName = "Ever";
String fullName = firstName + " " + lastName;

System.out.println(fullName);
```
Take a look at the third line of the program. This statement contains the expression, `firstName + " " + lastName`. Your computer will simplify this expression by first grabbing the Strings that are referenced by the variables `firstName` and `lastName`. Then, your computer will add all of the Strings together to make a new String object. It's this String that is assigned to the variable `fullName`.

To summarize, your computer might process this program like so:

```{image} https://media.giphy.com/media/2dzz7dRZaiOPoJVOci/giphy.gif
:alt: Notional machine String concatenation.
:height: 300px
```


[^*]: " " is a String because it uses the quotation marks! I know that it doesn't look like there's anything there, but there is! It's a space character. You can even have an empty String that looks like this "".
