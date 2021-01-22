Constructors With Parameters
============================

Take a look at this simple `Celebrity` class:

```Java
class Celebrity{
  String name;

  public Celebrity(){
    System.out.println("A new celebrity has been created!");
  }

  public void setName(String n){
    name = n;
  }
}
```

I bet you noticed that there are a lot of similarities between the structure of the constructor and our method `setName`.
For example, I notice that both of them start with the modifier `public`. I also notice that both of them have a name, followed by
a set of parentheses. Does that mean it's possible to include parameters in our constructors too?

```{image} https://i.pinimg.com/originals/f5/af/0b/f5af0b0ac3ade19b8af88afa25e8e2ab.gif
:alt: Beyonce - You know it
:height: 200px
```
<br>You betcha! In fact, in many cases you will want to include parameters in your constructor because it makes instantiating an object
with a specific state a lot easier. For example, I could assign our `name` instance variable to a value of my choosing if I write my constructor like
this:

```Java
class Celebrity{
  String name;

  public Celebrity(String n){
    name = n;
    System.out.println("A new celebrity has been created!");
  }

  public void setName(String n){
    name = n;
  }
}
```

Think of what this allows me to do. I can now make as many Celebrity objects as I would like, all with different states! Don't believe me? Take a look at this
main method where I instantiate three very different Celebrity objects using the Celebrity class defined above:

```Java
class Main{
  public static void main(String[] args){
    Celebrity bey = new Celebrity("Beyonce");
    Celebrity rihrih = new Celebrity("Rihanna");
    Celebrity juice = new Celebrity("Juice WRLD");
  }
}
```

If we didn't include parameters within our constructor, we would have to write a lot more code. Remember our dot operator?

```Java
class Main{
  public static void main(String[] args){
    Celebrity bey = new Celebrity();
    bey.name = "Beyonce";
    Celebrity rihrih = new Celebrity("Rihanna");
    rihrih.setName("Rihanna");
    Celebrity juice = new Celebrity("Juice WRLD");
    juice.setName = "Juice WRLD";
  }
}
```
```{image} https://media.tenor.com/images/e589a33608b6f9621e9135a611ad31e3/tenor.gif
:alt: Rihanna - Doing too much
:height: 200px
```

<br>You can add as many parameters to your constructors as you would like! Here is an example of a Celebrity constructor that contains
all the parameters:

```Java
class Celebrity{
  String name;
  int age;
  String type;
  boolean isAlive;

  public Celebrity(String n, int a, String t, boolean d){
    name = n;
    age = a;
    type = t;
    isAlive = d;
    System.out.println("A new celebrity has been created!");
  }
}
```
```Java
class Main{
  public static void main(String[] args){
    Celebrity bey = new Celebrity("Beyonce", 39, "Singer", true);
    Celebrity rihrih = new Celebrity("Rihanna", 32, "Singer", true);
    Celebrity juice = new Celebrity("Juice WRLD", 21, "Rapper", false);
  }
}
```

Once thing is bothering me about my constructor's parameters though; their names suck! If I look at this code 5 years from now,
I'm probably not going to remember what I was thinking when I wrote "n", "a", "t", and "d". I know that I can name parameters whatever I would like but
I gotta think about what makes my program easier to read, both for me and other programmers reviewing my code.

But honestly, it feels like I already chose the best names when I declared the instance variables of this class. Is there a way that I
can name my parameters the same thing and not confuse my computer?
