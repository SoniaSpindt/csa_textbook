Else If Statements
==================

What if we wanted our computer to check more than one condition? Don't worry, there's a statement we can use for that and it's called the ***else if statement***.

An else if statement is used along side the if statement to check if a second boolean expression is true. When you are using else if statements in your programs, you should follow this pattern:
```java
if(condition1){
  //statements
}else if(condition2){
  //different statements
}
```
An else if statement cannot stand alone! In other words, you must always start with an if statement if you are going to use an else if statement. Secondly, you can use as many else if statements as you want; all you need to do is stack them, like so:
```java
if(condition1){
  //statements
}else if(condition2){
  //different statements
}else if(condition3){
  //more statements
}else if(condition4){
  //other statements
}
```
Finally, the body of your else if statement will only be executed if the if statement's condition evaluates to false AND the else if statement's condition evaluates to true. Check out what I mean by examining this example:

```java
class Main {
  public static void main(String[] args) {
    int y = 5;

    if(y < 0){
      System.out.println("y is negative.");
    }else if(y > 0){
      System.out.println("y is positive.");
    }
  }
}
```
We would see the following output if we ran this program:
```{image} output4.png
:alt: Output 4
:height: 200px
```
Your computer starts at the top of the program and works its way down, asking itself if the if statement's condition is true. Because it is false, it skips over the body of the if statement and checks to see if the condition of the else if statement is true. Because it is true, the body of the else if statement is executed.

Need a more complex example? Here yah go:
```java
class Main {
  public static void main(String[] args) {
    String word = "CAT";

    if(word.indexOf("B") == 0){
      System.out.println("The word is probably BAT.");
    }else if(word.indexOf("C") == 0){
      System.out.println("The word is probably CAT.");
    }
  }
}
```
```{image} output5.png
:alt: Output 5
:height: 200px
```
<br>In the example above, we are using another method found in the String class called `indexOf()`.

```{image} https://media4.giphy.com/media/3HxxgzWNNlHeuOPtZN/giphy.gif
:alt: What the hell is that?
:height: 200px
```
This method utilizes an idea that is really important to understand for Strings, arrays, and ArrayLists called an ***index value***. An index value is a number we use to talk about the position of a character in a String or an item in an array or ArrayList.

If we consider the word seen above, "CAT", the index of the character "C" is 0, the index of "A" is 1 and the index of "T" is 2. Notice a pattern? Our index values always start at 0 and increase in value as we talk about characters that are found farther to the right. Here is a picture of what I mean:

```{image} IndexExample.png
:alt: Diagram of index.
:height: 200px
```
<br>The method `indexOf()` returns the index of the first character it finds in the String that matches the character passed into the method call. In the example above, the condition of the if statement uses the `indexOf()` method to see if a letter "B" can be found at index 0 of the word "CAT". Obviously, "CAT" does not start with the letter B, so the condition becomes false. More specifically, indexOf() returns a -1 because "B" cannot be found in the word "CAT" at all. The condition of the else if statement becomes true because "C" is found at index 0 of the word "CAT".

Play around with the repl.it to test your understanding of else if, index values, and the method indexOf().
<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/75Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>
