Else Statements
===============

It sure would be nice to have a backup plan just in case all of our conditions are false. Don't sweat! Java has a solution for you and it's called an ***else statement***.

An else statement is a statement that will be executed if the condition of an **if** statement and an **else if** statement evaluate to false. Here is the pattern you should follow when using an else statement:
```java
if(condition1){
  //statements
}else if(condition2){
  //different statements
}else{
  //some other statements
}
```
Here, the else statement comes at the very end and it acts as a backup plan -- if everything evaluates to false then the body of the else statement will automatically be executed, no questions asked. You do not have to use an else statement if you don't want to but you cannot use an else statement without an if statement. Here is the bare minimum code you need to write if you are going to use an else statement in your program:

```java
if(condition){
  //statements
}else{
  //some other statements
}
```

Let's take a look at an example of what this looks like in practice:
```java
class Main {
  public static void main(String[] args) {
    String word = "CAT";

    if(word.indexOf("B") == 0){
      System.out.println("The word is probably BAT.");
    }else if(word.indexOf("H") == 0){
      System.out.println("The word is probably HAT.");
    }else{
      System.out.println("Honestly, I have no idea what this word could be.");
    }

  }
}
```
```{image} output6.png
:alt: Output 1
:height: 200px
```
<br>The condition of the if statement evaluates to false because the letter "B" is not found at index 0 of the word "Cat". The condition of the else if statement also evaluates to false because the letter "H" is not found at index 0 of the word "Cat". Because both of these conditions evaluated to false, our computer will execute the body of the else statement.

Let's take a look at a much larger example. This example will show you how if, else if, and else statements can be used within a class:
<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/76Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

Pay attention to the use of the method `substring()` in the method `mixUpWord()`. The substring() method is another method found within Java's String class. This method can take 1 or 2 arguments, depending on your needs. In the example, we are passing in two arguments that represent the index values. The first argument is the index of the character where you would like to start your smaller String, while the second argument is where you would like the smaller String to end. Try changing the statements found in the example to test your understanding of if/else if/else statements as well as the String methods length(), indexOf(), and substring().
