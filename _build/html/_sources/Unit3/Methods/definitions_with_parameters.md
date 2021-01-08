Defining Methods with Parameters
=================================

Reexamine the `Main` class found in last week's Goodreads example:
<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/611Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

<br>On line 8 of `Main.java`, we use the dot operator to initialize the `title` attribute of our `stamped` Book object to the String, *"Stamped from the Beginning"*. We can accomplish the same result by using a method with parameters instead! How?

Jump into the `Book.java` file of this example and you will see a new method defined on line 24 named `setTitle` that looks like this:
```java
public void setTitle(String name){
  title = name;
}
```
Notice that most of the pattern we previously followed to define methods has not changed; we still need a modifier, a return type, a name, and a body filled with valid Java statements.

However, there are now two words inside of the parentheses! More specifically, we see `String name`. `String` is the type of the value that will be ***passed*** into the parentheses and `name` is just a generic word we used to represent said value. You can literally pick whatever words you would like for your parameters, though most programmers would argue that it should be related to the context of the problem you are defining a method to solve. In this case, I chose to represent my parameter with the word `name` because I will be passing the *name* of a book into this method. Heads up! Just like variables, your parameter names cannot contain spaces or begin with numbers.

Another really important thing to notice about this example is the fact that the parameter `name` is being used within the body of the method. This is an important step to follow and yet, many students forget to do it! So, if you are attempting to include parameters in your method definitions, please make sure that you ALWAYS follow these steps:

```{admonition} TL;DR
:class: warning
1. First, list the type of your parameter.
2. Then, give your parameter a name.
3. Finally, use your parameter somewhere inside the body of your method.
```

Continue reading to see how we can call our new `setTitle` method.
