Enhanced For Loops
==============

Although it is perfectly fine to use a while loop or a for loop to iterate through an array or ArrayList, many programmers prefer to use something called an ***enhanced for loop***. An enhanced loop is a modified for loop that looks like this:

```java
for(type item: array){
  //Statements
}
```

The enhanced for loop is specifically used when you are working with arrays or ArrayLists in a program. Let's take a look at a real example before we break it down a bit further:

```java
int[] numbers = {3, 9, 5, -5};
for(int number: numbers){
  System.out.println(number);
}
```
Output:
```{image} output7.png
:alt: Enhanced loop example
:height: 250px
```
<br>Most of this should look familiar to you. On line 1, we are declaring a variable named `numbers` and initializing it to an array that contains the numbers 3, 9, 5 and -5. The for loop itself should also look pretty familiar; the type of value that is found in our array is placed out front and the name of the array we are iterating through is found after the colon. The weird thing in this example is the word `number`. Where'd that come from and what does it mean?

This word generically represents each item found in the array. You can choose whatever word you would like to represent the values in an array; your computer will know what it means as long as it follows the pattern seen above. This means I could have written the same enhanced loop like this:

```java
int[] numbers = {3, 9, 5, -5};
for(int cheese: numbers){
  System.out.println(cheese);
}
```
Output:

```{image} output7.png
:alt: Enhanced loop example
:height: 250px
```
<br>Now the word `cheese` represents each number in the array. Obviously, this makes the code a bit harder to understand because people are going to be like "why are we talking about cheese when we're dealing with numbers?" Try to come up with descriptive names that help you and other viewers make sense of what is happening; your future self will thank you for it!

Let's take a look at a more complicated example about cars:

```java
public class Car{
  private double milesDriven;

  public Car(double miles){
    milesDriven = miles;
  }

  /** Returns the current value of milesDriven
  * @return milesDriven if a value was passed into the constructor when instantiating a new Car object.
  */
  public double getMilesDriven(){
    return milesDriven;
  }
}
```

```java
import java.util.ArrayList;

public class CarFleet{
  private ArrayList<Car> allCars;

  public CarFleet(){
    allCars = new ArrayList<Car>();
  }

  /** Adds a new car to the ArrayList allCars.
  * @param c is the new Car to be added.
  */
  public void addNewCar(Car c){
    allCars.add(c);
  }

  /** Sums the miles driven for each car found in allCars.
  * @return the sum of miles driven if at least one car has been added to allCars.
  */
  public double getTotalMiles(){
    double sum = 0.0;
    for(Car c: allCars){
      sum += c.getMilesDriven();
    }

    return sum;
  }
}
```

```java
public class Main{
  public static void main(String[] args){
    CarFleet fleet = new CarFleet();
    Car a = new Car(4500.7);
    fleet.addNewCar(a);

    Car b = new Car(109827.2);
    fleet.addNewCar(b);

    Car c = new Car(0.0);
    fleet.addNewCar(c);

    System.out.println("Total miles: " + fleet.getTotalMiles());
  }
}
```
Output:
```{image} output8.png
:alt: Enhanced loop example
:height: 250px
```

<br>Focus on reading the method named `getTotalMiles()` in the `CarFleet` class. As you can see, it uses an enhanced loop to iterate through the ArrayList `allCars`. I first want to highlight this operator `+=`, which is the lazy way of writing `sum = sum + c.getMilesDriven();`. If it were up to me, I would not include little differences like this on the AP exam but alas, I don't write the exams. You will occasionally see this operator, as well as it's counterparts on the exam:

```{image} shorthand.png
:alt: Operators short hand.
:height: 300px
```
<br>The other thing I want to point out is the fact that we see `c.getMilesDriven();`. Remember, `c` represents each item found in the ArrayList. In this case, `c` represents each Car object found in the ArrayList. Every Car object has a getMilesDriven() method that you can call that returns the miles driven for that car.

Again, it is really important that you understand how to use loops to manipulate arrays and ArrayLists, so please take a moment to play around with the program above. Try to change something in the code, see if it breaks, and ask yourself why! This is exactly what the exam is going to do. Might as well practice before then, right?

<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/710Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>
