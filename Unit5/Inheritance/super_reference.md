The Super Reference Variable
============================

The super method is nice and all but does it allow us to do things like refer to a superclass instance variable or call a superclass method? No, it does not. :(

Instead, we will need to use the keyword `super` instead. This keyword acts like a reference variable to a superclass object. This means that we can continue to use dot notation to access instance variables and methods of a superclass.

For example, what if we wanted to approach part B of the Pets FRQ a little differently? We could make the loud dog bark like this:

```java
public class Main{
  public static void main(String[] args){
    LoudDog rufus = new LoudDog("Rufus");
    System.out.println(rufus.speak());
  }
}
```

```java

public class Pet{
  private String name;

  public Pet(String n){
    name = n;
    System.out.println(n + " has been instantiated!");
  }

  public String speak(){
    return "Sound";
  }
}
```

```java

public class Dog extends Pet{
  public Dog(String n){
    super(n);
  }

  public String speak(){
    return "Bark";
  }
}
```

```java

public class LoudDog extends Dog{
  public LoudDog(String n){
    super(n);
  }

  public String speak(){
    return super.speak() + super.speak();
  }
}
```

Pay close attention to the `LoudDog` class. This class overrides the speak method of its superclasses! More specifically, it calls the Dog class' speak method twice. Then, it takes the value that is returned by each of the speak method calls and adds them together. What is returned by the Dog class' speak method? The String "Bark"! So the LoudDog's version of the speak method essentially squishes together "Bark" with "Bark", making the new string "BarkBark".

You can also use the keyword super to access instance variables of a superclass. Imagine if we were to add a *public* instance variable named breed and a setBreed method to the Dog class, like so:

```java
public class Dog extends Pet{
  public String breed;

  public Dog(String n){
    super(n);
  }

  public String speak(){
    return "Bark";
  }

  public void setBreed(String b){
    breed = b;
  }
}
```
We could then override the setBreed method in our LoudDog class to ensure that the breed is indeed a loud dog:

```java

public class LoudDog extends Dog{
  public LoudDog(String n){
    super(n);
  }

  public String speak(){
    return super.speak() + super.speak();
  }

  public void setBreed(String b){
    if(b.equals("Akita") || b.equals("Labrador Retriever") || b.equals("Puggle") || b.equals("Australian Shepherd")){
      super.breed = b;
    }else{
      System.out.println("Sorry, " + b + " is not considered a loud breed.");
    }
  }
}
```

See the statement `super.breed = b`? This statement grabs the public instance variable "breed" from the Dog class and initializes it to the parameter b. You would not be able to do this if the breed instance variable were private.

I want to take a moment to examine the condition of our if statement. It uses a method named `equals` and this method is defined within the `Object` class. What does it do? It is used to compare objects! More specifically, it checks to see if two objects are the same.

I know it is really tempting to use our `==` operator, but you cannot actually compare objects using this operator; you can only compare primitive values using the `==` operator. This is one of the reasons why all classes that are defined secretly extend the `Object` class -- we need to be able to use the equals method in our program to say if two objects are equal to one another.

<iframe height="400px" width="100%" src="https://replit.com/@SoniaSpindt1/Example815?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>
