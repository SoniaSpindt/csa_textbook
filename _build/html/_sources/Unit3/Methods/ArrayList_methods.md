ArrayList Methods
=================

In order to add String objects to our `awards` ArrayList, we will need to call a method that can be found in the <a href="https://www.w3schools.com/java/java_arraylist.asp">ArrayList class</a>. The name of this method is `add`. And just like we have seen before, we must use the dot operator to call this method on a specific object.

Take a look at the `Main` class of our Goodreads program again.
<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/68Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

There is a new statement on line 12 that looks like this:
```Java
stamped.awards.add("National Book Award for Nonfiction");
```

This statement probably looks a little funny to you because the dot operator is being used twice instead of once.

```{image} https://media.tenor.com/images/b0b5b750ca8db524e47cbe9cc3b72314/tenor.gif
:alt: Shocked
:height: 200px
```
<br>This is a totally valid statement in Java; you can pile on as many dot operators as you would like as long as you are using it to refer to progressively more specific components of an object.

Let's break this statement down further. We know that the word on the left side of a dot operator is the object reference. If we look all the way to the left, we will see that the object reference is `stamped`. This means that we are going to be acting on the object referenced by the variable `stamped`.

Not so fast! We have another word that is found to the left of a dot operator, `awards`, in this statement. This is secretly another object reference! Why? The attribute `awards` is an instance variable of our `stamped` object. It's also a reference variable because it points to an ArrayList object.  

Finally, we know that the word on the right side of a dot operator is the member name. In this case, our member name is `add` and it refers to a member (*cough* a method *cough*) of the `ArrayList` class, not the `Book` class. It is important that you understand that now we have two objects in play and that we are operating on the ArrayList object with this statement. 

This also speaks to a much larger, cooler idea in Java! Your classes can contain references to objects instantiated from other classes. Let's examine this powerful tool by expanding our understanding of the Goodreads book database.
