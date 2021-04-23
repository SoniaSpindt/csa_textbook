Method Overloading
==================

There is another really useful thing that we can do in our subclasses! It's called ***overloading***. This should not be confused with overriding, which says that you can define a more specific version of a method in a subclass as long as it has the method header matches the method header seen in the superclass  (i.e. same name, same return type, and the same parameters).

What is overloading? Overloading is nothing more than having two methods or constructors with the same name but different parameter lists. Overloading lets you make multiple versions of a method or constructor for convenience. For example, here is an example Overload class:

```java
public class Overloads{
  private String uniqueID;

  public Overload(){
    System.out.println("I'm a constructor without parameters");
  }

  public Overload(String id){
    System.out.println("I'm a constructor with parameters");
    uniqueID = id;
  }

  public int addNums(int a, int b){
    return a + b;
  }

  public double addNums(double a, double b){
    return a + b;
  }

  public void setUnique(String theID){
    uniqueID = theID;
  }

  public void setUniqueID(int num){
    String numString = "" + num;
    setUniqueID(num);
  }
}
```
As you can see, we have two constructors and two methods by the name of `addNums` in this class. However, they are "seen" as different because the use of parameters is different in every case. For example, one of the addNums method has parameters that are of type int and the other has parameters that are of type double. This is enough of a difference for Java to know which method it should run when a particular method is called.

Overloading can come in handy and it may show up on the exam. I won't spend a ton of time talking about it but know that it's totally possible!  
