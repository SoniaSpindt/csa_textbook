Nested Loops
====================

Loops are some of the most useful blocks of code you can include within your complex methods because they can be used to efficiently access and manipulate the information stored within arrays and 2D-arrays. You have already seen that a for loop can be used to loop through an array, but what does it look like to do that for 2D-arrays?

In order to traverse 2D-arrays, you need to actually use two loops; one loop to go across, and one loop to go down! More specifically, you need to use something called ***nested loops***. A nested loop is a loop that is found inside of another loop! Seems straight-forward, right?

Here is what it looks like to nest a while loop inside of another while loop:

```java
public class NestedLoopStuff{

  //No instance variables or constructor

  public static void displayXY(){
    int x = 1;
    int y = 100;

    while(x < 5){
      while(y > 95){
        y = y - x;
      }

      System.out.print(x + y);
      x++;
    }
  }
}

```
```java
public class Main{
  public static void main(String[] args){
    NestedLoopStuff.displayXY();
  }
}
```

Try to predict what the output of `displayXY()`` method will be before you continue reading. It never hurts to write down your thoughts while you're solving a problem. So if you have a pen and piece of paper nearby, try using a Memory Table to keep track of the values of x and y. Scroll down only when you have an answer:

```{image} https://media1.giphy.com/media/xT1XGLSb5E1VjIUw4E/source.gif
:alt: Waiting
:height: 250px
```
<br>If you ran the program, you would see the following output:
```{image} output10.png
:alt: Waiting
:height: 250px
```
<br>Did you get that? If not, try to figure out where you went wrong before you play with the repl found at the bottom of this page.

It's also possible to nest for loops inside of other for loops! Here is an example of what it looks like to do that:
```java
public class NestedLoopStuff{

  //No instance variables or constructor
  public static void displayIJ(){
    for(int i = 0; i != 3; i++){
      for(int j = 3; i % j != 1; j--){
        System.out.println("i: " + i);
        System.out.println("j: " + j);
      }
    }
  }
}

```
```java
public class Main{
  public static void main(String[] args){
    NestedLoopStuff.displayIJ();
  }
}
```

Again, try to determine what will be displayed as a result of calling the `displayIJ()` method before you scroll down. And don't forget about your Memory Table! Practicing this skill will be really important for success on the exam because you won't be able to test your ideas out in repl.it. So do yourself the favor and try writing out the Memory Table riiiiiight now. :)

```{image} https://media1.giphy.com/media/I1nwVpCaB4k36/giphy.gif
:alt: Please!
:height: 250px
```
<br>If you ran the program, you would see the following output:

```{image} output11.png
:alt: Output
:height: 250px
```
<br>WHAT!?!?! A run-time error!!!??? Why???????

Think about it.

Think about it some more.

What does the error message say?

```{image} https://media0.giphy.com/media/l0Iy3d2oLxKEG7NMQ/source.gif
:alt: Think think think
:height: 250px
```

<br>Your computer is able to compile the program because there's nothing wrong with the code that is written -- every semi-colon and curly brace is in the right place. However, when your computer begins to execute the compiled version of your program, it realizes it's being asked to divide i by 0. This is a no no! You can never divide by 0, not even in classes outside of math. At this moment, your computer will throw a run-time error message at you called an "ArithmiticException." Basically, this just means that the math you're trying to do is illegal and that you need to figure your life out.  


<iframe height="400px" width="100%" src="https://replit.com/@SoniaSpindt1/713Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>
