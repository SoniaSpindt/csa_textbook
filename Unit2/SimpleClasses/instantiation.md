Instantiation
============
```{image} https://media1.tenor.com/images/47485a5099343f3922ea6194b593c4a4/tenor.gif?itemid=15610644
:alt: Guess who's back!
:height: 300px
```
<br>THE MAIN CLASS! :D

```{image} main.png
:alt: Main class
:height: 300px
```

<br>The Main class is important to include in every Java program that you write because it's where you instantiate objects!

In order to instantiate objects in the Main class, you must write a statement that looks like this: `new Name();` Look familiar? It should look a lot like how we created ArrayLists! Now, imagine that we want to instantiate three new `Student` objects from our Student class. We would need to write code that looks like this:

<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/Section54Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

These statements are asking our computer to jump into the Student class and execute the contents of its constructor[^*]. Press the run button to see what happens! You can see that your computer executed all of the lines of code found in the constructor because we see "A new student has been created!" in the output window. However, in the example above, we don't do anything with those Student objects once they are created; they are created and then instantly forgotten by our computer. Lame.

It would be much more useful to couple the instantiation of these objects with the declaration and initialization of a reference variable. That way, we can indirectly tell our computer that we would like the objects to be saved for later. It also means that we can refer to a particular, unique Student object by its variable's name. So instead of wasting space like we did above, consider doing something like this instead:

<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/Section54Example2?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

Like always, we have to list the type of data we plan on pointing to with our reference variables `a`, `b`, and `c`. However, instead of it being a standard Java data type, like String or int, it's a type that we created by declaring a new class! The variables `a`, `b`, and `c` are of type `Student`! The rest of the statement should look familiar --- write the keyword `new` and then the name of the constructor that you would like your computer to use, followed by a set of parentheses and a semi-colon.

If it helps, this is how our computer would think about this program:

```{image} https://media.giphy.com/media/N25Ns7oZ8t5V4KZM1g/giphy.gif
:alt: Notional Machine Example
:height: 300px
```

<br>And that's essentially it! We will expand our understanding of instantiation in future classes, but it will always boil down to the major ideas discussed in this section.

[^*]: You can find the `Student` class in the file named `Student.java`. All you have to do is click the "file" button found in the example above.
