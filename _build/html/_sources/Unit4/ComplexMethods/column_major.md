Column-Major Traversals
=======================

Sometimes you want to traverse a 2D-array like this instead:

```{image} columnMajor.png
:alt: Column-Major Traversal
:height: 300px
```
<br>How would we write a nested for loop to accomplish this? BAM!

```java
public class Main{
  public static void main(String[] args){
    String[][] alphabet = {
      {"A", "a"},
      {"B", "b"},
      {"C", "c"}
    };

    for(int i = 0; i < alphabet[i].length; i++){

      for(int j = 0; j < alphabet.length; j++){
        System.out.print(alphabet[j][i]);
      }

    }
  }
}

```

Notice how the conditions of our nested for loop have changed -- it's like they have flipped! The condition of the outer loop is now `alphabet[i].length`, which means that we are determining the length of the internal arrays. In this case, it's 2 because these arrays contain String objects like "A" and "a". This also means that the outer for loop will execute 2 times because `i` will become equal to 2 after only two loops.

The condition of the inner loop is now the length of the array that contains the internal arrays. In this case, 3! This will allow the internal loop to repeat three times, every time the outer loop repeats. In total, the internal loop will repeat 6 times.

Last but not least, it is important to notice that the print statement has also changed. We have reversed the order of the row and column indices. This is needed to make sure that we are accessing the correct element of the internal arrays.

It's ok if you're having a hard time wrapping your head around these differences! I still second guess myself when thinking about column-major traversals. However, I continue to push myself to draw as many pictures as I can to illustrate what's going on under the hood of a program. I challenge you to draw a picture of the above program so that you can internalize how nested loops are used to iterate through 2D-arrays.

<iframe height="400px" width="100%" src="https://replit.com/@SoniaSpindt1/714Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>
