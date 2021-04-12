Visualizing Inheritance
=======================

I bet you have taken a class where your teacher has asked you to make a family tree. It may have looked something like this:

```{image} https://i.pinimg.com/originals/71/c4/16/71c416b4c9e68c96e11d2c00d19fa5fe.png
:alt: Star Wars Family Tree
:height: 500px
```
<br>Each character in Star Wars is represented by a box. The relationship between two characters is illustrated by both by a line and their position on the page; parents are found above their children, not under them.

Java programmers borrowed this idea when showing how classes can inherit instance variables and methods from one another. Here is an example of what I'm talking about:

```{image} https://ars.els-cdn.com/content/image/3-s2.0-B9780750661232500049-f04-27-9780750661232.jpg
:alt: Java Inheritance Tree Example
:height: 300px
```
<br>This inheritance tree illustrates how three classes -- Picture, Photograph and Painting -- are related to one another. Each class is represented by a box. In this box, you will find the the name of the class, as well as the names of its instance variables and methods. How can you tell if you're looking at a variable name or a method name? Look to see if there are parentheses at the end! If it has parentheses, then it is a method name. ;)

A line is used to represent how each class is related to one another. In the example above, the Picture class is the ***parent class*** of the Photograph and Painting classes, and the Photograph and Painting classes are ***child classes*** of the Picture class. You can also see this relationship by how each box is positioned on the page; the parent classes are above the child classes!

Some people prefer to say that the Picture class is the ***superclass*** to the Photograph and Painting classes, while the Photograph and Painting classes are ***subclasses*** to the Picture class. Why? These terms are more generic than the terms parent and child. Think about where it might be confusing to use "parent" to describe a relationship between classes.

What if you wanted to talk about the parent class of a parent class? Would that be a grandparent class? No. lol We don't actually have a term to describe grandparents or great-grandparents in Java. Instead, it we can describe multi-generational relationships with the term "super".

You may be wondering what it actually means for a class to inherit code from another class. Well, it just means that a subclass has access to the instance variables, constructors, and methods found within the parent class. We'll take a look what this looks like over the next few sections of this chapter.
