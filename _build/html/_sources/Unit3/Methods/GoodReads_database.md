Goodreads Database Example
===========================

What does it mean to be a database? Well, a database is just a fancy term we use to talk about a collection of data. Companies, like Goodreads, really care how this data is organized because it can impact other parts of their products. For example, a database that features very little organization might make it hard for software engineers to define methods that retrieve specific pieces of data within that database because there would be no obvious and consistent way to access said data. It would be like asking someone to grab "your socks with the cats on them" from your bedroom if you put your clothes away by literally throwing them on the ground. You could argue that you have a system to putting your clothes away, but your mom would probably say there are better ways to do it. :P

The act of storing data in a database is such an important component of computer science that there are people who have dedicated their entire careers to thinking about the best way to structure these collections of data. In fact, if you continue taking computer science courses, you will spend half of your time as a student learning about all of the ways you can structure data within a program (this is like learning about all of the ways you can organize your closet).

In most cases, there is more than one way to structure data within a Java program. Keep this in mind as we explore our Goodreads example -- it is very possible that there is another way to write this program; it just depends on your needs.

For example, I think we need a way to keep track of the reviews that people write about each book. What information is connected to that review? Off the top of my head, I think about the number of stars that was listed in that review, the text of that review, the date that it was written, and the name of the person who wrote the review. We could haphazardly throw all of this information into our Book class, but that's starting to feel a lot like throwing our clothes on the floor.

Let's create a `Review` class so that we can be a bit more organized about this information.
<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/69Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

Take a second to explore all of the files found in this Java program, making sure to notice the new attribute in our `Book` class named `reviews`. What is the type of this instance variable?

```{image} https://64.media.tumblr.com/66f0a0b36ccdca1654d9864ae04c35d6/tumblr_inline_pkhgfpSVnA1qijzwz_250.gifv
:alt: Thinking hard!
:height: 200px
```

It's an ArrayList of Review objects!!! This is not the only example of a class that utilizes elements of another class in this program. Where else do you find that our classes are reliant on one another? Is there another way that you would have structured this database? Feel free to fork the repl found above and play around with some of your ideas. :)
