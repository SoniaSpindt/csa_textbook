Private Modifier
========================

Up until now, you have only seen the `public` modifier when defining methods. Remember, this is a word that basically makes our methods down for anything.

The `public` modifier is useful in some contexts, though it is a little dangerous to haphazardly throw around because it gives anyone the power to interact and change whatever top-secret information you are storing within your program.

I recognize that it can be hard to understand this problem because you rarely write programs that deal with sensitive information in this class. That's why it's important to take a step back and think about why Java was created. Java is an "enterprise language", which means it was invented to be used by businesses. These businesses need to build software for all kinds of information, that if leaked or changed, would make a lot of people upset. For example, most banks use Java to write their bank account software. I know I would be HELLA MAD if someone accessed my savings account information and changed the balance to $0.00.

```{image} https://i.pinimg.com/originals/3a/4e/ec/3a4eecc97f6e07c3ae83a37bf6c0d8c1.gif
:alt: That's not fair!
:height: 200px
```

<br>Furthermore, people make mistakes when writing code. Especially, when you're writing code with a team. Java needed to include features that made it possible for groups of people to contribute to a single project without accidentally f*$%ing everything up.

So how do we protect ourselves from accidents or vendettas? We can use a modifier called `private` for both our method definitions and our instance variable declarations. The keyword `private` makes instance variables and method definitions only visible to the class that they were defined within. Consider the following example:

```java
class NuclearBomb {
  int launchCode;

  public NuclearBomb(){
    System.out.println("Uh oh! A new bomb was created. That's no bueno.");
  }

  /** Assigns launchCode to a value
  *@param newLC is an integer value that launchCode will be assigned to
  */
  private void setLaunchCode(int newLC){
    launchCode = newLC;
  }
  /** Assigns launchCode to a value
  *@return launchCode if launchCode has been assigned to a value
  */
  private int getLaunchCode(){
    return launchCode;
  }
}
```
```java
class Main{
  public static void main(String[] args){
    NuclearBomb bomb = new NuclearBomb;
    //This statement results in an error because the method getLaunchCode is private.
    bomb.getLaunchCode();
  }
}
```

If you try to compile and execute this program, you would see the following error in the console:

```{image} VisibilityError.png
:alt: Compile-time error
:height: 250px
```

<br>Whew! A nuclear holocaust has been avoided just by adding a little word in front of our getter and setter methods. OR WAS IT??? What happens if I do this instead?

```java
class Main{
  public static void main(String[] args){
    NuclearBomb bomb = new NuclearBomb;
    //This statement does not result in an error.
    System.out.println(bomb.getLaunchCode);
  }
}
```

Notice that I'm using our dot operator to access the launchCode instance variable directly? YUP! That is totally legal, which means our launch code is still accessible to prying eyes. It's much better to write something like this:

```java
class NuclearBomb {
  private int launchCode;

  public NuclearBomb(){
    System.out.println("Uh oh! A new bomb was created. That's no bueno.");
  }

  /** Assigns launchCode to a value
  *@param newLC is an integer value that launchCode will be assigned to
  */
  private void setLaunchCode(int newLC){
    launchCode = newLC;
  }

  /** Assigns launchCode to a value
  *@return launchCode if launchCode has been assigned to a value
  */
  private int getLaunchCode(){
    return launchCode;
  }
}
```
```java

class Main{
  public static void main(String[] args){
    NuclearBomb bomb = new NuclearBomb;
    //This statement results in an error because the attribute launchCode is private.
    System.out.println(bomb.getLaunchCode);
  }
}
```

Here, I have added the `private` modifier to the very beginning of line 2. This makes the variable's contents only visible to the NuclearBomb class. Everything besides the constructor is private in this example, which means that it's fairly locked down and hard to use by anyone. Instead, you would most likely see a mix of `public` and `private` being used like so:

```java
public class NuclearBomb {
  private int launchCode;

  public NuclearBomb(){
    System.out.println("Uh oh! A new bomb was created. That's no bueno.");
  }

  /** Assigns launchCode to a value
  *@param newLC is an integer value that launchCode will be assigned to
  */
  private void setLaunchCode(int newLC){
    launchCode = newLC;
  }

  /** Assigns launchCode to a value
  *@return launchCode if launchCode has been assigned to a value
  */
  public int getLaunchCode(){
    return launchCode;
  }
}
```
```Java
class Main{
  public static void main(String[] args){
    NuclearBomb bomb = new NuclearBomb;
    System.out.println(bomb.getLaunchCode());
  }
}
```
Try changing the private and public modifiers in the NuclearBomb class to help you wrap your head around how they work:
<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/71Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>
