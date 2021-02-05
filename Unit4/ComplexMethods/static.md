Static Modifier
===============

Have you ever noticed that you need to instantiate objects of a class before you can call the methods you defined? Sometimes you will want to be able to call methods before you instantiate an object. In order to do that, you will need to use the `static` modifier, which makes it possible to execute the body of a method without creating an object first. Here is an example of a static method you might use without instantiating objects first:

```java
public class DoMath(){
  /** Returns the sum of two numbers.
  * @return the sum of two decimal values that are passed into the method call.
  */
  public static double absoluteValue(double num1, double num2){
    return num1 + num2;
  }
  /** Returns the product of two numbers.
  * @return the product of two decimal values that are passed into the method call.
  */
  public static double multiplyTogether(double num1, double num2){
    return num1 * num2;
  }
}
```
```java
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

How do you define a static method? It's pretty straightforward. All you need to do is add the keyword `static` after you write either `public` or `private`. Not too bad right?


Static methods are so popular that there are a few pre-defined classes in Java that you can use in your own programs. One of them is the `Math` class, which contains the following static methods.

```{image} StaticMathMethods.png
:alt: Math Class Documentation
:height: 300px
```

All you have to do to use these methods is write `Math.methodName(arguments)` because Math is the name of the class that contains these methods.

You can also have static instance variables in your classes! When a variable is declared as static, then a single copy of variable is created and shared among all objects of the class. Here is an example of what I mean:

```Java
import java.lang.Math;

class BankAccount{
  private static int totalAccounts = 0;
  private String name;
  private int accountNumber;

  public BankAccount(String name){
    this.name = name;

    /* Notice the naked function calls?
    These lines have a secret "this" out front.*/
    accountNumber = generateAccountNum();
    updateAccountTotal();
  }

  /** Generates a random account number that is 6 digits long.
  * @return a six digit integer once Math.random and Math.random have been called.
  */
  private int generateAccountNum(){
    //Math.random generates a random decimal found between 0 and 1.
    double tempNum = Math.random();

    /* Math.round rounds a decimal to the nearest whole number.
    In order to store a number that used to a be a decimal in a variable of type int, we need to do something called "casting." Casting allows us to convert one type to another.*/
    int accountNum = (int)Math.round(tempNum);
    accountNum = accountNum * 100000;
    return accountNum;
  }

  /* Adds one to totalAccounts
  */
  private static void updateAccountTotal(){
    //This is equivalent to totalAccounts = totalAccounts + 1;
    totalAccounts++;
  }

  /* Returns the total number of BankAccount objects that have been instantiated.
  * @return non-zero integer if at least one bank account has been opened.
  */
  public static int getTotal(){
    return totalAccounts;
  }
}
```
The `totalAccounts` number is a variable that is shared across all objects created from the BankAccount class. Any method that acts on this instance variable must be static as well, which is why you see the static modifier in both `updateAccountTotal` and `getTotal`.

It's also important that this class calls static methods from the Math class in the `generateAccountNum` function. Notice that "Math" class name out front? Never forget it! It's really important when calling methods found in the Math class.

You may have also noticed a weird line of code in `generateAccountNum` that looks like this: `int accountNum = (int)Math.round(tempNum);`. Most of this should look familiar except the `(int)`. This is called "casting", which is necessary when you are converting primitive types into other primitive types. In order to cast, you just need to put the type of the value you would like to convert to in a set of parentheses. That's why we see (int) out front.

Want to play around with this class in repl.it? Check this out:

<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/73Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

WHEW! That was a lot. But I promise that these are all the modifiers and keywords that you will need to know when defining and calling complex methods. Practice using them all the time because I can guarantee that you will see a mix of them on the AP exam.
