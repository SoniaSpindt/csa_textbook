The Super Method
============

What happens if you try to execute the following program? Pay special attention to the constructor found in Animal -- it has a parameter named `name`. You should also notice that the class Cat does not explicitly define its own constructor. Got any ideas?

```java
class Main{
  public static void main(String[] args){
    Cat norman = new Cat("Norman");
  }
}
```

```java
public class Animal{
  private String name;

  public Animal(String name){
    this.name = name;
  }

  public String speak(){
    return "Sound";
  }
}
```

```java
public class Cat extends Animal{
  public String speak(){
    return "Meow";
  }
}

```

We learned in the last unit that our subclass will borrow the constructor of the superclass if a constructor is not explicitly written in the subclass. However, none of those constructors required parameters.

If you instantiate a new cat object, will Java know that it needs to give the argument "Norman" to the Animal constructor? Nope!

Here is what you would see if you tried to execute the program above:
```{image} weNeedSuper.png
:alt: An example of when super is needed.
:height: 300px
```
<br>As you can see by the error message, the compiler of our program is confused because the number of arguments needed by the constructor differs from the amount that was actually passed into the statement `new Cat("Norman");`. This means that Java is actually executing the secret default constructor of the Cat class first, and this constructor has no parameters. If it helps, it would look like this;

``` java
public Cat(){

}
```
This points to a larger behavior that you should know about when objects are instantiated from subclasses that extend some superclass -- all contructors in an object's inheritance tree must run when you make a new object. This includes the secret default constructors that are found in classes that do not explicitly define a constructor.

It may help to look at this image, which represents how objects look when they are instantiated from a class that is involved in inheritance:

```{image} objectRelationships.png
:alt: What an object looks like to our computer.
:height: 400px
```

<br>This image tells us that every object holds not just its own declared instance variables, but also everything from its superclasses.

Wondering what's happening in the middle of this picture? That's the `Object` class and it is the mother of all classes. Every class built into the Java standard library extends the Object class. Every class that you define will also extend this class. We'll talk a little bit more about this class soon. For now, I want to focus on how we can solve the problem described above.

If you would like your subclass to be able to use a superclass constructor that contains parameters, you will need to call the `super` method. This method knows how to jump up one level in a class hierarchy and give information to a superclass constructor. Here's what I mean:

``` java
public class Cat{
  public Cat(String name){
    super(name);
  }

  public String speak(){
    return "Meow";
  }
}
```

Now our Cat class has an explicitly defined constructor that calls the super method! It is important to see that we have added a parameter to the constructor and passed that parameter into the super method call. This argument is then passed off to the Animal constructor, which knows how to deal with the information because it also has parameters. If you try to execute this program, you will see this:

```{image} https://media.tenor.com/images/bb4975045724ea7f452402629ead7737/tenor.gif
:alt: You're happy cuz it runs.
:height: 300px
```
<br>LOL GET IT?! It's cuz the program runs with no problems. Here is the repl just in case you want to play around with the example program:

<iframe height="400px" width="100%" src="https://replit.com/@SoniaSpindt1/Example814?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>
