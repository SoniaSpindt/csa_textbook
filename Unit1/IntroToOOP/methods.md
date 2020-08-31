Methods
=======

So objects have state. Cool.

However, if we want our objects to be like objects in the real world, we need to be able to do two things:

1. Interact with our objects. 
2. Change the state of our objects. Think about it. Does anything in the real world truly stay
the same forever [^*]? NOPE.

Computer scientists recognized these needs too, so they included a way to do both within their object oriented programs. We won't talk about the specifics of 
the code needed just yet. All I want you to know is that we can satisfy both of these needs with something called <strong><em>methods</em></strong>. 

A method is just a set of directions our computer can follow to do something. That something is entirely up to you and your needs as an object oriented programmer, but most of the time these methods will be applied to the objects that you create within your programs. It's important to know that we give each method in our 
program a unique and fabulous name. The name you choose is up to you but it should point to what the method is used to accomplish because this
makes it easier for other people to make sense of your code. 

Still a little unsure of what this looks like? Let's go through an example, start to finish. Imagine you want to create a class that makes movie objects. 

```{image} https://media.giphy.com/media/dY0U0MLyUvblHItQsK/giphy.gif
:alt: Avenger meme
:height: 300px
```
<br>

After you come up with a name for your class, you need to think about the attributes you will need. I will use the following attributes, but remember, this is a matter of personal preference.

```{admonition} Movie Class Attributes
1. Director
2. Genre
3. Length
4. Title
5. Actors
6. Has jump scares
7. Money earned to date
```
Now let's create our first movie object! Keeping with the theme of gifs here, I'm going to create a movie object for Avengers: Endgame. 

```{admonition} Avengers: Endgame Object
1. Director = Anthony Russo, Joe Russo
2. Genre = Action
3. Length = 181
4. Title = Avengers: Endgame
5. Actors = Robert Downey Jr., Chris Evans, Mark Rufflo, Chris Hemsworth, Scarlett Johansson, Jeremy Renner, Don Cheedle, Paul Rudd, Brie Larson, Bradley Cooper, Gwyneth Paltrow
6. Has jump scares = false
7. Money earned to date = 2,800,000,000.00 
```

Here's the state of our object! Isn't it nice? The state of this object is relatively steady too; we aren't going to recast the movie now that it has been filmed after all. However, there are a few
attributes that stand out to me as something we may want to interact with and change. In order to do this, we will need to use methods because, as I said above, methods allow us to operate on the
internal state of our objects. Here are three methods that I envision needing for my Movie class:

```{admonition} Methods for Movie Class
:class: tip
1. getGenre
2. convertMinsToHours
3. addEarnings
```

Yes, yes. I know. The names of my methods look a bit strange. I want you to get into the habit of not using any spaces in your method names because computers HATE spaces in names with a passion.
These names are great because they also secretly tell you what each method does. For example, the first method probably allows you to retrieve the genre of the movie object in question.
If we apply this method to our Endgame object, then we will be given "Action" because this is the value we stored within the genre attribute. The second method sounds like it's going to do some math for us and the third method will probably change the value stored within the "Money earned to date" attribute. 

As you can see, methods are really powerful because they allow us to utilize the state of our objects in limitless ways! :D


[^*]: Inflation is real, [Knuth](https://en.wikipedia.org/wiki/Knuth_reward_check)! I will give you 5 bucks if you can give me an example of something that stays the same forever in the
real world.
