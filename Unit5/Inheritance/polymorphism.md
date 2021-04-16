The Power of Polymorphism
=========================

Ok, ok, why do we actually care about being able to have a subclass inherit code from a superclass?

When you define a superclass for a group of subclasses, *any subclass of that superclass can be substituted wehere the superclass is expected*. Read that sentence again.

WHAT!?

```{image} https://media.tenor.com/images/55e0be5740070be4293a7ab976691a90/tenor.gif
:alt: Say what?
:height: 200px
```

<br>Let's break this statement down with an example:

```java
class Main{
  public static void main(String[] args){
    Dog rufus = new Dog("Rufus");
    Bird blue = new Bird("Blue");
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

public class Dog extends Animal{
  public Dog(String n){
    super(n);
  }

  public String speak(){
    return "Bark";
  }
}
```
```java

public class Bird extends Animal{
  public Bird(String n){
    super(n);
  }

  public String speak(){
    return "Tweet";
  }
}
```

Hopefully, nothing is too shocking to see. Even the declaration and assignment of the Dog and Bird objects in the Main class looks pretty straightforward. What if we did this in the main method instead:

```java
class Main{
  public static void main(String[] args){
    Animal rufus = new Dog("Rufus");
    Animal blue = new Bird("Blue");
  }
}
```

This is totally legal! We can make the reference of the object different than the type of the object instantiated as long as the reference is a superclass type. When you declare a reference variable, any object that passes a IS-A test for the declared type of the reference variable can be assigned to that reference. In other words, anything that extends the declared reference variable type can be assigned to the reference variable.

This highlights the power of a very important concept in object-oriented programming called ***polymorphism***. Polymorphism essentially decribes the ability to access objects of different types through the same interface. This is just fancy CS talk for an object passing multiple "IS-A" tests.

When I was first learning Java, I really struggled to wrap my head around this idea until someone showed me what happens when we throw arrays or ArrayLists into the mix:

```java
class Main{
  public static void main(String[] args){
    Animal[] animals = new Animal[3];

    animals[0] = new Dog("Rufus");
    animals[1] = new Bird("Blue");
    animals[2] = new Dog("Taco");

    for(int i = 0; i < animals.length; i++){
      animals[i].speak();
    }
  }
}
```

Polymorphism essentially allows us to get around the fact that arrays and ArrayLists must contain values of the same type. In the eyes of Java, a Dog and a Bird are the same type -- they're both Animals!

There's more! You can also have polymorphic arguments and return types. If you can declare a reference variable of a superclass type, say Animal, and assign a subclass object to it, say Dog, think of how that might work when the reference is an argument to a method:

```java
public class Vet{
  public static void giveShot(Animal a){
    //Something happens that makes the animal speak
    a.speak();
  }
}
```
```java
class Main{
  public static void main(String[] args){
    Animal rufus = new Dog("Rufus");
    Animal blue = new Bird("Blue");
    Vet.giveShot(rufus);
    Vet.giveShot(blue);
  }
}
```

Ultimately, polymorphism makes it possible for us to avoid changing code when we need to introduce new subclasses to an inheritance tree. Think about the Vet class above to understand this statement. If you write a Vet class using arguments declared as type Animal, your code can handle any Animal subclass. That means if others want to take advantage of your Vet class, all they have to do is make sure their new subclass extends the class Animal. The Vet methods will still work, even though the Vet class was written without any knowledge of the new subclasses, the Vet methods will still be able to work without any changes needing to be made.
