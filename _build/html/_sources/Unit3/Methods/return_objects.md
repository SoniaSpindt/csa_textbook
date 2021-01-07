Returning Objects
=================

In many cases, your methods will need to return objects. This is really useful when we are creating Java programs that contain a ton of new classes. For example, let's imagine that you were just hired by <a href="https://www.goodreads.com/?ref=nav_home">Goodreads</a> to help maintain their database of books.

You begin by examining their `Book` class, which can be used to instantiate `Book` objects. While looking at the body of this class, you notice that there are a handful of methods that return String objects (open the `Book.java` file if you haven't done so already!).

<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/67Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

Pay attention to what all of these methods have in common -- they all use `String` as their return type and they all contain the keyword `return`. In other words, the pattern that we followed in order to return primitive data types works for objects too!

Don't worry, you will always follow this pattern when defining methods that return a value, no matter how complex it seems. For example, take a look at our `Book` class again; it now contains the `awards` attribute, which is an ArrayList of String objects.

<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/67Example2?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

If we wanted to define a method that returns the `awards` attribute of a `Book` object, we would write the following code:

```Java
public ArrayList<String> getAwards(){
  return awards;
}

```
Notice that the return type of the `getAwards` method is `ArrayList<String>`. We chose this as our return type because the instance variable `awards` is an ArrayList of String objects. In other words, the return type must match the type of the value being returned, even if it is a really scary looking value.

```{image} https://149363654.v2.pressablecdn.com/wp-content/uploads/2014/03/scared-gif.gif
:alt: Scared!
:height: 200px
```

<br>If you have read "Stamped from the Beginning", then you may know that this biography has won a few awards. However, you may have noticed that our program returns an empty ArrayList when the `getAwards` method is called. That's not right! We must fix this!
