Defining Methods
================

In order to create a method in Java, you must ***define*** the method first. Think of this as actually writing down the steps of your recipe. It doesn't mean that you're going to use that recipe right then and there; it just means that you will be ready to get to work when the time comes.

It's the same idea when defining methods! And you will ALWAYS follow this pattern when defining a new method:

```java
modifier returnType name(parameter list){

  /* Body of method */

}

```

As you can see, this is a vocabulary nightmare! Every piece of the pattern illustrated above contains a new word used to describe a very specific concept in Java programs (again, vocabulary is important). Let's break it down a bit more so that we can learn to customize this pattern for our own needs.

***Modifier:*** This is a special keyword that your compiler uses to determine what parts of your Java program can actually use this method. For now, the modifier that you should use when defining a new method is `public`, which just means that the method can be used by any part of your Java program.


***Return Type:*** Like a recipe, your methods will produce some output when followed. Sometimes your methods will produce an integer, other times it will produce a new object from a class that you defined! In any case, your compiler needs you to be explicit about what kind of information is produced by your method. For now, the return type that you should use when defining a new method is `void`. This return type just means that your method will not return any specific type of information. You can assume your method should have a return type of `void` if the body of your method does not contain the keyword `return`. We will talk about what this looks like in our next lesson.

***Name:*** This one is self-explanatory; it's the name of your method! You can choose the name that you give a method but you really should choose something that relates to what the method does. So if you define a method that somehow bakes the best cookies ever, you should consider naming your method `BakeBestCookiesEver`. Notice that the name contains no spaces! Don't include spaces in your method names because this will result in a compile-time error. Also, don't start your method names with a number --- this will also result in a compile-time error.

***Parameter List:*** This is the ingredient list of method definitions. This lists all of the information that your computer needs to successfully follow the recipe contained within the body of your method (*cough all of the statements and expressions found in between of the curly braces cough*). For now, your parameter list will be empty (some recipes don't need any ingredients to work).  

Examine this example Java program, which contains a `Character` class.

<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/61-Defining-Methods?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

As you can see, the `Character` class contains a method that increases a video game character's experience level. Its visibility is `public` and its return type is `void`. The name of the method is `addExperience` and its parameter list is empty. The body of the method contains a single statement which is used to increase the value of the attribute `experience` by one every time the method is used.
