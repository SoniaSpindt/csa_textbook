Row-Major Traversals
====================

What about all that 2D-array magic we talked about? Don't worry, we're getting to that right now!

Although you can use whatever nested loop configuration you would like, the most common way to loop over a 2D-array is through a nested for loop.

Here's what I mean:

```java
public class Main{
  public static void main(String[] args){
    String[][] alphabet = {
      {"A", "a"},
      {"B", "b"},
      {"C", "c"}
    };

    for(int i = 0; i < alphabet.length; i++){

      for(int j = 0; j < alphabet[j].length; j++){
        System.out.print(alphabet[i][j]);
      }

    }
  }
}

```
Notice the condition of the outer loop? It is `alphabet.length`. Why is this ok? By its definition, a 2D-array is just an array of arrays. When we access the length of an array object, we are simply asking the question "How many items are in the array?". Yes, these items happen to be other arrays, but they are still items! Just a little more complex than usual.

Now look at the condition of the inner for loop. This condition is `alphabet[j].length`. What does this even mean? Start working from the left side of the dot operator. In this case, we are accessing the item found at index `j` What is j when the inner loop begins? It's 0! So what item is found at index 0 of the alphabet array? It's the array that looks like this: `{"A", "a"}`. Now the condition is {"A", "a"}.length. What's that simplify to? 2! Cuz there are two String objects in this array.

Ultimately, we call this type of traversal a ***row-major traversal*** because it does this:



Do we always have to traverse a 2D-array like this? Nope! Keep reading to see how we can switch it up.
