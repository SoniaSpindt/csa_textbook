---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Java
  language: java
  name: java
---
Instance Variables
==================

The first thing that you should include in the body of a class are attributes. Remember those? Attributes are the characteristics that we use to describe objects of a class. The way that we create attributes within our classes is by declaring variables at the very top of our class definition. These are special variables, so they have a special name; they are called <b><i>instance variables</i></b>. Are you putting two and two together right now? Where have you seen the word <b><i>instance</i></b> before? Hmmmmmm?

```{image} https://media.tenor.com/images/cc2e5bc3bbe230320ed6eaa74f259c23/tenor.gif
:alt: Hmmmmmm
:height: 200px
```
<br>We saw the word <b><i>instance</i></b> when we learned that the keyword `new` tells our computer to create a new object from a class. In other words, these variables will be used to store information that is specific to the objects that we create. And that makes sense because instance variables are attributes! We're coming full circle now! :D

What does it look like to actually add instance variables (*cough* attributes *cough*) to our class definitions? Here's our `Dog` example again, except now it contains three instance variables:

```{code-cell} java
class Dog{
  String name;
  String breed;
  int age;
}
```
And here is our `Song` class:

```{code-cell} java
class Song{
  String[] artists;
  double length;
  String genre;
}

```
You may be wondering why we are only declaring the instance variables, instead of declaring and initializing them to a value. Although it is totally possible to initialize our instance variables to values at the top of our class definition, we often save that for later in our Java programs. Think about why that may be.
```{image} https://media.giphy.com/media/1jl173guBKkbvC03rQ/giphy.gif
:alt: Hmmmmmm
:height: 200px
```
<br>If we were to initialize an instance variable to a particular value at the top of our class, then every object instantiated from the class would have that value for said attribute. If we wait to initialize these variables until later, then we can be specific about what object gets what piece of information. Don't worry if this isn't terribly clear right now -- we will continue to examine cases where we see both. Here is an example of a class where it might be more appropriate to initialize an instance variable right away:

```{code-cell} java
class Game{
  int score = 0;
  boolean hasWon = false;
  String characterChosen;
}
```
In this example, any Game object instantiated from the Game class will have a `score` attribute that is initially set to 0 and a `hasWon` attribute that is set to false. This intuitively makes more sense because most games start where no one has won and everyone's score is 0. It does not make sense for every dog to be named "Fido" or for every Song to be 2 minutes and 45 seconds long.

I would also like to say that it's ok to disagree with the attributes that I have chosen to list within any of the examples above. This is where programming becomes really personal. For example, if you believe that dogs are more than a name, breed, and age, then your class will look different than mine and that's totally ok. :)
