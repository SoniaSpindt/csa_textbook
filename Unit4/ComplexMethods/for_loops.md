For Loops
=========

There's another type of loop that you will need to use in your programs. This loop is called a ***for loop***. A for loop is a loop that repeats a specific number of times. More specifically, it takes a lot of the guess work out of using a while loop because a counter variable is built into the structure of the for loop itself. Here is an example of a while loop and a for loop. Both loops do the same thing:

```Java
class Main{
  public static void main(String args[]){
    int i = 0;
    while(i < 3){
      System.out.println(i);
      i++;
    }

    for(int j = 0; j < 3; j++){
      System.out.println(j);
    }
  }
}
```

As you can see, the for loop is a little more concise than the while loop because you can declare and initialize a counter variable in the for loop itself. This makes it much harder to accidentally create an infinite loop!

More specifically, when you are using a for loop in your program, you want to follow this pattern:

```java
for(initialize; condition; update){
  // Statements
}
```
***Initialize:*** This is where you will declare and initialize a variable  to a value of your choosing. Your computer executes variable_setup once, at the very beginning of the for loops execution. In the example above, int `j = 0`; is an example of a variable_setup statement in a for loop.

***Condition:*** A boolean expression your computer will evaluate to determine if the loop should continue to execute.  The condition of the example above is `j < 3`;. If the condition evaluates to true, then any statements found in between the curly braces will be executed. We refer to the collection of statements that is found in between the curly braces of a for loop as the body of the for loop. The loop will continue as long as the condition evaluates to true.

***Update:*** This is where you update the variable that you declared within your initialization statement. This statement is executed every time the statements found in the body of the for loop are executed. In the example above, the variable_update statement is `j++`, which is equivalent to writing `j = j + 1`.

Let's use a for loop to manipulate ArrayList objects. We are also going to use more methods found within the ArrayList class. More specifically, this is set of ArrayList methods you will need to know for the AP exam.

```{image} ArrayListMethods.png
:alt: ArrayList Methods
:height: 250px
```
Here's the program:

```java
import java.util.ArrayList;

class ManipulateArrayLists{
    /** Adds together all of the values found in an ArrayList.
    * @param arrayList is the ArrayList of integers to be added together.
    * @return an Integer object if the ArrayList is not empty.
    */
    public static Integer sumNumbers(ArrayList<Integer> arrayList){
      if(arrayList.size() == 0){
        System.out.println("Gah! Your ArrayList is empty");
        return null;
      }

      Integer sum = new Integer(0);
      for(int i = 0; i < arrayList.size(); i++){
        sum = sum + arrayList.get(i);
      }
      return sum;
    }

    /** Adds a range of integers an ArrayList.
    * @param finalValue is the final integer found in the ArrayList.
    * @return an ArrayList of Integers once the Integers have been added to the ArrayList.
    */
    public static ArrayList<Integer> addNums(int finalValue){
      /*
      Remember, we can also have Integer and Double objects!
      This is important because ArrayLists cannot store primitive
      values within them.
      */
      ArrayList<Integer> numbers = new ArrayList<Integer>();

      int count = 0;
      while(count <= finalValue){
        numbers.add(new Integer(count));
        count++;
      }

      return numbers;

    }
}
```
```Java
class Main{
  public static void main(String args[]){
    ArrayList<Integer> numbers = ManipulateArrayLists.addNums(3);
    System.out.println(ManipulateArrayLists.sumNumbers(numbers));
  }
}
```

There is a lot going on in the program above! First of all, we are using the ArrayList method named `size` in order to make sure that the ArrayList being passed into the method is not empty. We want to perform this check because you cannot add together numbers that aren't there! If our ArrayList is non-empty, then we are safe to execute the for loop.

The for loop seen in the method above is used to loop over an ArrayList. More specifically, it starts at the beginning of the ArrayList and uses the `get()` method to retrieve the item found at index 0. That's right, ArrayLists use index values too! Once it grabs the value found at index 0, it adds it to the current value of `sum` and updates the value of the variable `i`. The for loop will continue to loop until the value of i is equal to the size of the ArrayList passed into the function.

Confused? Take a look at how I would use a memory table to figure out what this sumNumbers method does:

<iframe width="560" height="315" src="https://www.youtube.com/embed/FZEj0ILGRk0" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Whew! That's it for loops right now. Practice using loops, index values, and ArrayLists by playing around with the following repl:
<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/78Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>
