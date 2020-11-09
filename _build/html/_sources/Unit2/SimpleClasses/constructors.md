Constructors
=============

Wouldn't it be nice to be able to create an object from a class that you defined?

In order to do this, we will have to add something to the body of your class called a <b><i>constructor</i></b>. As the name suggests, this is a block of code that your computer will read EVERY time you attempt to construct, (*cough* <b><i>instantiate</i></b> *cough*), a new object from your class.

What does a constructor look like? Well, you will always follow the same pattern when you are adding a constructor to the body of your class: `public Name(){}`.

The keyword `public` is used to describe the visibility of your constructor; in other words, it describes what parts of your program are allowed to actually use the constructor to make a new object from your class. The keyword `public` is the most generous visibility setting you can use in Java programs because it means that every other part of your Java program is free to use it. We will learn about more restrictive visibility keywords in the future; for now, every constructor that you make will start with the keyword `public`.

The next part of a constructor is the name you have given your class. Yup, you gotta repeat yourself and you gotta make sure that the name is capitalized! Finally, you will end with a pair of parentheses and a pair of curly braces. Here is what is looks like to declare a `Student` class that contains instance variables and an empty constructor:

```java
class Student{
  String name;
  int grade;
  double gpa;

  public Student(){

  }
}
```

As you can see, the constructor is found under your class' instance variables. Although you can technically put instance variables and constructors anywhere inside the body of a class, it is a widely accepted practice to place the constructor AFTER the instance variables, which are conventionally placed at the top of your class.

What goes inside of our constructor? All of the statements that your computer needs to execute in order to create a new object! That means that you can literally put anything that we have learned about so far into your constructor!

```{image} https://media1.tenor.com/images/a0aae55a8d64861a8b669e0f69277065/tenor.gif?itemid=12708224
:alt: So many options!
:height: 200px
```

<br>Wanna add a bunch of `System.out.println` statements to your constructor? Go right ahead!

```java
class Student{
  String name;
  int grade;
  double gpa;

  public Student(){
    System.out.println("OMG!!!")
    System.out.println("A new student has been created!");
    System.out.println("I'm the king/queen of the world!");
  }
}
```

Wanna declare a variable and initialize it to 0 in your constructor? Literally, the sky is the limit!

```java
class Student{
  String name;
  int grade;
  double gpa;

  public Student(){
    int count = 0;
    System.out.println("OMG!!!")
    System.out.println("A new student has been created!");
    System.out.println("I'm the king/queen of the world!");
  }
}
```

<br>Ok...Not to rain on your parade, but in many cases, a constructor is used to initialize your instance variables to some values.

Let's imagine that you have been hired as an engineer by Jupyter to create a new grade book for high school teachers to use, and the `Student` class declared above is for this project. This means that the `Student` class will be used to create student objects, which represent teenagers that actually exist in the world!

Given this context, it might make sense to immediately initialize the instance variable `grade` to the integer 9 because most high school students begin in 9th grade. Our constructor will now look like this now:

```java
class Student{
  String name;
  int grade;
  double gpa;

  public Student(){
    grade = 9;
    System.out.println("A new student has been created!");
  }
}
```

This means that every `Student` object created with this constructor will begin in 9th grade.

```{image} https://media.tenor.com/images/46fc1dd0d3a212f4bcc7edfc73303c34/tenor.gif
:alt: Wait a minute
:height: 300px
```
<br>Yeah, I know; there are plenty of real world cases where it doesn't make sense to have every student start in 9th grade. We will learn how to initialize our instance variables on a case by case basis in our next unit. For now, you should know that a constructor is where you put the statements you need to give your computer in order for it to successfully instantiate an object.

Is that it? Will our computer be able to read our minds and instantiate a new object whenever we feel like it? HELL NO! Your computer can't read your mind. You have to explicitly state that you would like to instantiate an object from your class by writing a statement our computer can execute. BUT how?
