If Statements
=============

I hope you haven't forgotten about boolean expressions because we are going to use them all the time within our complex methods.  More specifically, our computer programs make decisions based on logic: if a statement is true, do something, otherwise, do something else. We need boolean expressions, and something called ***if statements***, to build this style of logic within our programs. What does an if statement do exactly? And how can we add them to our programs?

An if statement allows a specific block of code to be executed if a boolean expression evaluates to true. When you are adding an if statement to a program in Java, you must follow this pattern:

```java
if(condition){
	//statements
}
```

The ***condition*** of an if statement is the boolean expression your computer will evaluate. The condition of an if statement should always be placed inside of the parentheses. And in case it wasn't obvious, you ALWAYS have to put a boolean expression in your if statements; all other types of expressions, like 2 + 2, cannot be conditions in your if statements.

If the condition evaluates to true, then any statements found in between the curly braces will be executed. We refer to the collection of statements that is found in between the curly braces of an if statement as the ***body*** of an if statement. If the condition evaluates to false, then the body of the if statement will not be executed; your computer will skip over the body of the if statement and continue executing any lines of code that are found after the closing curly brace.

Take this if statement for example:
```java
class Main {
  public static void main(String[] args) {
    int x = 10;

    System.out.println("Hi!");

    //The condition is: x > 0
    if(x > 0){
      System.out.println("x is positive");
    }

    System.out.println("Bye!");
  }
}
```
The condition of the if statement above is `x > 0`. This condition will evaluate to true because x is 10 and 10 is greater than 0. When we execute this entire program, we see the following output:
```{image} output1.png
:alt: Output 1
:height: 200px
```
<br>Notice how we see "Hi!", "x is positive" and "Bye!" in the output window? Our computer made the decision to execute every line of code in this program because the condition evaluated to true.

However, if we were to change the value of x to -10, we would only see the following output:
```java
class Main {
  public static void main(String[] args) {
    //x is now -10!
    int x = -10;

    System.out.println("Hi!");

    //The condition is: x > 0
    if(x > 0){
      System.out.println("x is positive");
    }

    System.out.println("Bye!");
  }
}
```
```{image} output2.png
:alt: Output 2
:height: 200px
```
<br> In this case, our computer makes the decision to skip the body of the if statement because the condition now evaluates to false.

Let's spice things up and complicate our condition a bit by playing around with some String objects. Strings, as you know, are a sequence of characters contained within quotation marks. This is a string: "oas123 idhao982 idha". So is this: "". And like all objects, Strings have methods associated with them. For example, all String objects have a `length()` method. The `length()` method tells us how many characters are found in between those quotation marks, and like all public methods, we can call them anywhere we want by using the dot operator. So what if I wrote this program instead?

```java
class Main {
  public static void main(String[] args) {
    String word = "aofinfibnawiufageraewudpauidb";

    System.out.println("Hi!");

    //The condition is: word.length() > 7
    //Your computer will simplify this condition to true.
    if(word.length() > 7){
      System.out.println("The length of the word is " + word.length() + " characters long.");
      System.out.println("Geesh. That's a long word.");
    }

    System.out.println("Bye!");
  }
}
```
What would the output be? It would be this:
```{image} output3.png
:alt: Output 3
:height: 200px
```

<br>Not convinced? Run the repl.it version of this program before turning the page:
<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/74Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>
