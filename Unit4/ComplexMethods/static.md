Static Modifier
===============

Have you ever noticed that you need to instantiate objects of a class before you can call the methods you defined? Sometimes you will want to be able to call methods before you instantiate an object. In order to do that, you will need to use the `static` modifier, which makes it possible to execute the body of a method without creating an object first. Here is an example of a static method you might use without instantiating objects first:

```
public class DoMath(){
  public static double absoluteValue(double num1, double num2){
    return num1 + num2;
  }

  public static double multiplyTogether(double num1, double num2){
    return num1 * num2;
  }
}

public class Main{
  public static void main(String[] args){
    DoMath.addTogether(3.5, 999.99);
    DoMath.multiplyTogether(5.9, -2.0);
  }
}
```
Take a look at the Main class. Here, you will notice that our dot operator is making an appearance, except instead of an object reference out front, we see the class name. In other words, in order to call static methods, you need to follow this pattern:

```
className.methodName(arguments);
```

And to define static methods, you just need to add the keyword `static` after you write either `public` or `private`. Not too bad right?


Static methods are so popular that there are a few pre-defined classes in Java that you can use in your own programs. One of them is the `Math` class, which contains the following static methods.

```{image} StaticMathMethods.png
:alt: Math Class Documentation
:height: 300px
```

All you have to do to use these methods is write `Math.methodName` because Math is the name of the class that contains these methods.
