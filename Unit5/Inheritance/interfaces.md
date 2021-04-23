Interfaces
==========

Let's build a Pet Shop program! However, I'm feeling lazy, so I want to reuse as much code from the Animal example on the previous page. Some animals are pets after all. Pets should have different behavior than Animals -- for example, we might want a `beFriendly` method or a `play` method. I'll pass on playing with animals like tigers or hippos, so not every animal should be able to implement these methods...

**Option 1:** What if we just put every method in the Animal super class?

Pro: All of the animals will instantly inherit the pet behaviors defined in the Animal class. I could define a new subclass at any moment and viola! It can do pet things.

Con: When was the last time you went to a pet shop and saw a lion? Also, it might be dangerous to give non-pets pet methods -- we don't want the ability to play with a bear!

**Option 2:** Make the pet methods in the Animal class abstract.

Pro: We force ourselves to implement an animal-specific version of each method. This makes it possible for us to ensure that animals like lions, tigers, and bears don't inherit some default version of a method like play.

Con: I still have to implement all abstract methods in every class! So I could just make the play method do nothing in the dangerous animal classes, but I still have to go through the trouble of writing those empty methods. While this solves the problem of non-pets not being able to do pet things, it still gives the illusion that these classes are able to do pet things. I imagine that will be confusing to anyone I give this program.

**Option 3:** Define pet appropriate methods in only the subclasses that need them.

Pro: Whew! Finally, an option where dangerous animals can't do pet things.

Con: If I work with anyone else on this program, I have to make sure that explicitly agree on how these methods are defined. But what if they get it just the tiniest bit wrong? Like they capitalize the first letter or they give it a String argument instead of an int? Also, I don't get to use the power of polymorphism anymore! Every class that needs pet behaviors would have to know about each and every class. In other words, you can't use Animal as the polymorphic type now because the compiler won't let you call a Pet method on an Animal reference (even if it's really a Dog object) because Animal doesn't have the method.

**Option 4:** Make two super classes? One for Pet and one for Animal?

Pro: I can consistently give each and every pet class pet behavior! They can inherit methods from both a Pet class and an Animal class, cuz pets are animals too! This also makes it so none of the non-pet animals inherit pet methods.

Con: A subclass can't inherit code from two superclasses because of something called the [diamond problem](https://www.tutorialspoint.com/what-is-diamond-problem-in-case-of-multiple-inheritance-in-java).  Short story --> Java just won't allow it. :(

SO WHAT CAN WE DO?!!!???

```{image} https://media4.giphy.com/media/3og0ISDmwZW0z7W7HW/200.gif
:alt: What can we do gif
:height: 200px
```
Don't worry! We can use something called an ***interface***! An interface solves the diamond problem by making all of its methods abstract. A subclass can extend a superclass and implement an interface at the same time. And by making all of the methods abstract, each subclass implementing the interface HAS to define its own version of the method. We won't have to worry about a friend of ours screwing everything up.

So how do you define an interface? Check this out:

```java
public interface Pet{
  public abstract void beFriendly();
  public abstract void play();
}
```

```java
public abstract class Animal{
  private String name;

  public Animal(String name){
    this.name = name;
  }

  public abstract void sound();

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

  public void sound(){
    System.out.println("Grrrrrrr!");
  }
  //Method overriding!
  public void eat(){
    System.out.println("Chomp chomp chomp");
  }
}
```
```java
public class Dog extends Animal implements Pet{
  public Dog(String name){
    super(name);
  }

  public void sound(){
    System.out.println("Bark!");
  }

  public void beFriendly(){
    System.put.println("Wag tail");
    System.out.println("Woof woof!");
  }

  public void play(){
    System.out.println("Fetch!");
  }
}
```

Isn't it beautiful? The Dog class can inherit code from the Animal class and be told what to do through the Pet interface! Now our Dog object can do pet-friendly things while our hippo gets to continue living its wild and free life.

Some important things to notice about the interfaces:
1. Your interface declaration uses the keyword "***interface***" instead of "class".
2. Interfaces do not have constructors because they cannot be instantiated. Ever.
3. All methods in interfaces are abstract.
4. When you want a subclass to be able to be told what to do by an interface, you use the keyword "***implements***" instead of "extends".
5. A subclass can extend a superclass and implement an interface at the same time.
