Arguments
=========

Calling methods that contain parameters is very similar to calling methods that do not contain parameters. The only difference between the two is found inside of the parentheses! In fact, you have already seen the difference when we called the ArrayList method `add` in section 6.8 -- you had to write the value that you wanted to add to the ArrayList inside of the parentheses.

Still confused? Let's take a look at our Goodreads example again. This time you will see the following call statement on line 9 of the `Main` class:

```java
stamped.setTitle("Stamped from the Beginning");
```

<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/612Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

<br>This call statement does the same thing as `stamped.title = "Stamped from the Beginning"`, though in our next unit, we will see why the method call is preferred. For now, just know that when you are calling methods that contain parameters, you must ***pass*** a value into the method call. In other words, you need to write some value inside of the parentheses.

More specifically, we call the value that is passed into a call statement an ***argument*** in Java. In the example above, the String *"Stamped from the Beginning"* is the argument being passed into the method call. When you pass in an argument to any call statement, your computer will check to see if the type of that argument matches the type you listed in your method definition. Remember, Java is a picky betch that demands you are careful about the values you throw around in your programs.

If the types don't match, your compiler will complain. Don't believe me? Change "Stamped from the Beginning" to the boolean value `true` in the example above and try to execute the program -- see, your computer yells at you!

Don't worry if this happens to you though; even professional engineers make this mistake from time to time. Instead, you should practice making sense of the error messages that pop up because your compiler will tell you how to fix your mistake. For example, here is the error message I see when I pass a boolean value into the `setTitle` call statement:

```{image} errormessage.png
:alt: Error message
:height: 250px
```

<br>Focus on the sentence that starts with `Main.java:9`. This is telling you the name of the file and the line number that you need to fix. In this case, the mistake can be found on line 9 of `Main.java`. The next part of the error message is `error: incompatible types`. This is your compiler's way of describing what it thinks is wrong; in this example, our compiler is telling us that are types don't match.

Now that you know what it looks like to add one parameter to a method, let's take a look at a few methods that utilize many parameters.
