This
====

Don't worry, I'm not the only Java programmer to ask this question. In fact, this is such a common problem in object oriented programming that the Java standard library contains a special word that engineers can use when they are trying to differentiate their class attribute names from their constructor or method parameter names.

This keyword is called `this`. As the name suggests, `this` is used to describe the current object in a constructor or a method. Here is our `Celebrity` class again:

```Java
class Celebrity{
  String name;
  int age;
  String type;
  boolean isAlive;

  public Celebrity(String name, int age, String type, boolean status){
    this.name = name;
    this.age = age;
    this.type = type;
    isAlive = status;
    System.out.println("A new celebrity has been created!");
  }
}
```
```{image} https://i.pinimg.com/originals/23/2e/f8/232ef8934380ee248c30a9f06ca5a76b.gif
:alt: Shocked!
:height: 200px
```
<br>Gasp! The dot operator strikes again! In this case, `this` is being used as the "objectReference" and is explicitly referring to the object that is actively being made by the constructor. We know that this object has attributes `name`, `age`, `type` and `isAlive`, and that we are initializing them to the values passed in for our parameters `name`, `age`, `type` and `status`.

If we did not use `this` for the assignment of our first three attributes, our computer would not know which `name`, `age`, or `type` you are referring to; is it the attribute or the parameter? This is not a problem for the attribute `isAlive` because the parameter we are using within the assignment statement is `status`, not `isAlive`. We're lucky that I was able to come up with a more appropriate name for this last parameter! It may help to know that our compiler secretly plugs in the keyword `this` for our final assignment statement, even though it wasn't explicitly written. You can add `this` yourself if you'd like, though programmers prefer to only break out `this` when there are naming conflicts between class attributes and the parameters of a constructor a method.  

```Java
class Celebrity{
  String name;
  int age;
  String type;
  boolean isAlive;

  public Celebrity(String name, int age, String type, boolean status){
    this.name = name;
    this.age = age;
    this.type = type;
    this.isAlive = status;
    System.out.println("A new celebrity has been created!");
  }
}
```
The keyword `this` can be used in other situations, though the problem described above is by far the most common use in this course.
