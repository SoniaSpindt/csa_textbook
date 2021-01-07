Defining Methods
================

In order to create a method in Java, you must ***define*** the method first. Think of this as actually writing down the steps of your recipe. It doesn't mean that you're going to use that recipe right then and there; it just means that you will be ready to get to work when the time comes.

You will ALWAYS follow this pattern when defining a new method:

```java
modifiers returnType name(parameter list){

  /* Body of method */

}

```

As you can see, this is a vocabulary nightmare! Every piece of the pattern illustrated above contains a new word used to describe a very specific concept in Java programs (again, vocabulary is important). Let's break it down a bit more so that we can learn to customize this pattern for our own needs.

***Modifiers:*** These keywords are used to describe special characteristics of a method. The list of modifiers is quite long, but don't panic! You have already seen one in action before, `public`. This is specifically known as an *access modifier* because it describes what files in your program can access and use the method in question. The modifier `public` is the least restrictive of the access modifiers; you can use a `public` method anywhere within your program!

***Return Type:*** Like a recipe, your methods will produce some output. And because Java is a HELLA picky language, you must be be explicit about what kind of information is produced by your method or else your compiler will yell at you (it really doesn't like surprises). This week, we will practice defining methods whose return type is `void`. This just means that your method will not *return* any specific type of information when it is used. Don't worry, we will spend the next few weeks examining cases that require other return types.   

***Name:*** This one is self-explanatory; it's the name of your method! You can choose the name that you give a method but you really should choose something that relates to what the method does. So if you define a method that somehow bakes the best cookies ever, you should consider naming your method `BakeBestCookiesEver`. Notice that the name contains no spaces! Don't include spaces in your method names because this will result in a compile-time error. Also, don't start your method names with a number --- this will also result in a compile-time error.

***Parameter List:*** This is the ingredient list of method definitions. This lists all of the information that your computer needs to successfully follow the recipe contained within the body of your method (*cough all of the statements and expressions found in between of the parentheses cough*). For now, your parameter list will be empty (some recipes don't need any ingredients to work).  

Examine this example Java program, which contains a `Character` class.

<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/61-Defining-Methods?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

As you can see, the `Character` class contains a method that increases a video game character's experience level. Its visibility is `public` and its return type is `void`. The name of the method is `addExperience` and its parameter list is empty. The body of the method contains a single statement which is used to increase the value of the attribute `experience` by one every time the method is used.

You may have noticed that the method definition comes after the class constructor. Although you can technically put methods anywhere within the body of a class, it is a widely accepted practice within the Java programming community to always place method definitions after the constructor. The AP exam will follow this industry trend, so it is important to internalize the following class structure:
1. Declare instance variables (attributes) at the top.
2. Define constructors in the middle.
3. Define methods at the bottom.
