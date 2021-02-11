Calling Methods within Other Methods
====================================

Some of the best statements that you can include within your method definitions are calls to other methods that you have defined. Technically, we have already seen what this looks like, but I want to formally describe the process because it can be weird to think about at first.

Consider the Line class from Unit 3:
```java
class Line{
  //See Point.java for more info on these variables.
  Point pointA;
  Point pointB;

  public Line(Point a, Point b){
    pointA = a;
    pointB = b;
  }
  /** Computes the slope of a line produced by two points.
  * @return slope. If denominator is 0,
  *   then the method will produce an error.
  */
  public double getSlope(){
    double numerator = pointA.getY() - pointB.getY();
    double denominator = pointA.getX() - pointB.getX();
    return numerator/denominator;
  }

  /** Determines the value where a line crosses the y axis.
  * @return y intercept. If the line does not cross the y-axis,
  *   the method will produce an error.
  */
  public double getYIntercept(){
    double b = pointA.getY() - (this.getSlope() * pointA.getX());
    return b;
  }

  /** Determines if a point can be found on a given line.
  * @param p is a Point object.
  * @return true if p can be found on the line in question.
  */
  public boolean onLine(Point p){
    double b = this.getYIntercept();
    double m = this.getSlope();
    // y = mx + b is used to format boolean expression below
    return (p.getY() == ((m * p.getX()) + b));
  }

  /** Determines if two given lines are parallel.
  * @param l is a Line object.
  * @return true if the slopes of the two lines are equal.
  */
  public boolean areParallel(Line l){
    double slopeLine1 = this.getSlope();
    double slopeLine2 = l.getSlope();
    return slopeLine1 == slopeLine2;
  }
}

```

In this class, there are four methods defined in the Line class: getSlope, getYIntercept, onLine, and areParallel. The areParallel, onLine, and getYintercept methods all call the getSlope method like so, `this.getSlope()`. By now, you should know that `this` means we are calling the getSlope method of the current Line object being used. However, most programmers think that `this` should be implied. AKA most Java programmers like to call methods in these cases without putting `this` out front. Here's how our Line class would look instead:

```java
class Line{
  //See Point.java for more info on these variables.
  Point pointA;
  Point pointB;

  public Line(Point a, Point b){
    pointA = a;
    pointB = b;
  }
  /** Computes the slope of a line produced by two points.
  * @return slope. If denominator is 0,
  *   then the method will produce an error.
  */
  public double getSlope(){
    double numerator = pointA.getY() - pointB.getY();
    double denominator = pointA.getX() - pointB.getX();
    return numerator/denominator;
  }

  /** Determines the value where a line crosses the y axis.
  * @return y intercept. If the line does not cross the y-axis,
  *   the method will produce an error.
  */
  public double getYIntercept(){
    double b = pointA.getY() - (getSlope() * pointA.getX());
    return b;
  }

  /** Determines if a point can be found on a given line.
  * @param p is a Point object.
  * @return true if p can be found on the line in question.
  */
  public boolean onLine(Point p){
    double b = getYIntercept();
    double m = getSlope();
    // y = mx + b is used to format boolean expression below
    return (p.getY() == ((m * p.getX()) + b));
  }

  /** Determines if two given lines are parallel.
  * @param l is a Line object.
  * @return true if the slopes of the two lines are equal.
  */
  public boolean areParallel(Line l){
    double slopeLine1 = getSlope();
    double slopeLine2 = l.getSlope();
    return slopeLine1 == slopeLine2;
  }
}

```
Basically, I want you to know that it's totally possible to call methods without using your dot operator. You will see this on the exam and in real life, so start mentally adding "this" every time you see a naked method call. What other keywords can we use to spice up our method definitions? Keep reading to find out!

Before you move on, here is the repl.it version of the Line class. Play around with method calls to confirm your thinking about not using `this`:

<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/ThisExampleOutsideConstructor?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>
