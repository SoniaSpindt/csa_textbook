Methods
=======

You may have noticed that computer scientists are very specific about the language they use to describe different components of a Java program. See, there's a reason why I ask you to complete those really long vocabulary activities every week! :P. I know that it probably felt a bit excessive at first and maybe a tad unnecessary at times, but I promise, it will payoff to learn these words.

Why? First of all, the AP CSA exam is a vocabulary test in disguise. Plain. And. Simple. You will be asked to complete tasks that can be perceived as quite difficult only because they are filled with exotic-sounding terminology. If you work to memorize and make sense of the words we encounter in this class, you will instantly know what these questions are asking for, and thus, you will be more likely to provide a sensible response. Uh, do I smell a 5 in your future? I think I do. :)

More importantly, having a shared language will allow you to communicate your thoughts and ideas in a way that helps others expand upon them. Without this mastery of vocabulary, you will be left trying to describe your plans in a way that often leave your peers and instructors really confused.

```{image} https://www.missmalini.com/wp-content/uploads/2015/10/tumblr_nudj0f6f0e1r91uyxo1_500.gif
:alt: What do you mean?
:height: 200px
```

<br>So, make our lives easier by continuing to internalize the following five terms:

```{admonition} Really Important Vocab
:class: note
1. Class
2. Object
3. Attribute
4. State
5. Method
```

We saw these terms at the very beginning of the year, and will continue to learn about them because they are at the heart of being able to create beautiful and sophisticated object oriented programs. So let's recap a little:

A <b><i>class</i></b> is the blueprint that your computer follows in order to make an <b><i>object</i></b>. Objects, in turn, have a <b><i>state</i></b>, which is described by class <b><i>attributes</i></b> (*cough instance variables cough*).

In many cases, the state of your object is not static; it changes over the lifetime of your Java program! We can act on or make changes to an object's state using <b><i>methods</i></b>.

Methods are blocks of code that can be used over and over again to perform a specific action. Think of methods as the recipes of computer science! In the recipe, there are steps that need to be followed, and each step is specific about what needs to happen. Consider the following recipe for “the best chocolate chip cookies ever”:

```{image} cookieRecipe.png
:alt: What do you mean?
:height: 300px
```

<br>Notice that this recipe, like most recipes, lists the ingredients that are needed at the top, and the steps that need to be performed at the bottom. And if you actually want to make the “best cookies ever”, you can’t just haphazardly perform the steps that you feel like completing, with whatever ingredients that you feel like using that day; you have to follow the recipe EXACTLY as it is written.

Computers treat methods the same way! They want to make the “best cookies ever”, so they carefully grab the ingredients listed at the top and execute each step in the recipe EXACTLY as it is written, from top to bottom (wouldn’t make sense to follow a recipe from bottom to top now, would it?)

Obviously, our computers won’t be used to bake cookies this term (boo!). Instead, we will ask our computer to use recipes (*cough methods cough*) to interact with the objects found in our Java programs. Over the next few weeks, we will learn how to add increasingly more complex methods to our Java programs because this will allow us to manipulate the state of our objects in incredibly useful ways[^*].

So how do you actually add a method to your Java program? Keep reading to find out!

```{admonition} TL;DR
:class: warning
Vocab is reaaaaaally important in this class, so learn your words!
```
[^*]: If you're feeling a little freaked out right now, you're not alone! Methods represent a generally scary time in a programming class because their implementation is heavily dependent on your willingness to experiment. That's a really uncomfortable sensation for many students to embrace because most of your education has taught you that there's no time to just see what happens --- there is a right answer and a wrong answer, and you better be right because your grade depends on it. This way of thinking is not useful when trying to add a method to your Java program simply because there are so many solutions to the same problem when programming! It's like asking someone to come up with a recipe for the "best cookies ever" -- do you reaaaally think there's only one recipe that accomplishes this goal? Mmmm probably not. So keep this in mind moving forward; method design and implementation is flexible.
