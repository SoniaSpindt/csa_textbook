Abstract Classes
================

There are some classes that should not be instantiated. Consider the Animal class, Bird class and Dog class we defined in section 8.6. It makes sense to create a Dog object or a Bird object, but what exactly *is* an Animal object? What shape is it? What color? Size? It simply doesn't make sense to actually create an object from the Animal class.

That being said, we still need an Animal class for inheritance and polymorphism. We just want programmers to instantiate only the subclasses of Animal, not Animal itself.

Thankfully, there is a simple way to prevent a class from ever being instantiated while still maintaining its role in inheritance and polymorphism. The way we do that is through something called ***abstract*** classes.

An abstract class is a class that cannot be instantiated. You must extend it in order to use any of the code found within its body.

How do you make an abstract class? It's pretty easy. All you have to do is put the keyword "abstract" at the beginning of your class declaration:

```java
public abstract class Animal{
  private String name;

  public Animal(String name){
    this.name = name;
  }

  public void eat(){
    System.out.println("Nom nom nom");
  }
}
```

```java
public class Hippo extends Animal{
  public Hippo(String name){
    super(name);
  }

  //Method overriding!
  public void eat(){
    System.out.println("Chomp chomp chomp");
  }
}
```
An abstract class, like Animal, means that nobody can ever make a new instance of that class. You can still use that abstract class as a declared reference type and for the purpose of polymorphism, but you don't have to worry about somebody making objects of that type. The compiler guarantees it!

Don't worry, I didn't just lie to you -- abstract classes aren't instantiated! So why then does the Animal class have a constructor? In this case, the subclass Hippo needs it. We can still build out constructors and methods in our abstract classes as long as it makes sense for our subclasses to use that code.

If it's a little less clear that our subclasses should use an exact method defined in the abstract class, then you should really use something called an ***abstract method***. An abstract method guarantees that a method will be overridden. You might decide that all or some of behaviors in an abstract class don't make any sense unless they are implemented by a more specific subclass. In other words, if you can't think of any possible way to generically implement some method, then you should make it abstract, like so:

```java
public abstract class Animal{
  private String name;

  public Animal(String name){
    this.name = name;
  }

  public abstract void eat();
}
```

```java
public class Hippo extends Animal{
  public Hippo(String name){
    super(name);
  }

  //Method overriding!
  public void eat(){
    System.out.println("Chomp chomp chomp");
  }
}
```
Notice that our abstract method `eat` does not have a body! This is because you have decided that there isn't any code that you could put in this method that makes sense. You also cannot have abstract methods in a class that is not abstract. So if you decide that you need an abstract method, you gotta throw that abstract keyword at the beginning of your class declaration. Feel free to mix abstract and non-abstract methods in an abstract class though!

Just in case it wasn't clear, you **MUST** implement every abstract method in a subclass. If you don't, your compiler will yell at you. You have to do this when abstract classes extend each other too (yes, an abstract class can extend another abstract class).he first non-abstract class in the inheritance tree will have to implement all of the abstract methods defined in the tree. Here's what I mean:

```java
public abstract class Animal{
  private String name;

  public Animal(String name){
    this.name = name;
  }

  public abstract void sound();
}
```

```java
public abstract class Pet extends Animal{
  public Pet(String name){
    super(name);
  }

  public abstract void play();
}
```

```java
public abstract class Dog extends Pet{
  public Dog(String name){
    super(name);
  }

  public String sound(){
    return "Bark!";
  }

  public String play(){
    return "Fetch";
  }
}
```
