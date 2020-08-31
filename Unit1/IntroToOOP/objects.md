Objects
=======
In order to be a proficient object oriented programmer, you need to know about the term <b><i>object</i></b>. Your English teachers would have
talked about this word a lot because it's an important part of English sentences. In most cases, they probably talked about objects
as nouns, which are people, places or things. For computer scientists, objects aren't just people, places or things --- basically *everything* in the world can be an object!
And it doesn't stop there! Computer scientists even say that you have the power to create your own objects whenever you feel so inclined. 

So what are some examples of objects that you might see within object oriented programs?
 
```{figure} Whalemouse.png
---
height: 300px
name: whale-figure
---
Here is a whale object and a mouse object.
```

```{figure} Treeball.png
---
height: 300px
name: tree-figure
---
Trees, soccer balls, and blades of grass can also be considered objects.
```
```{figure} drawPeaceLove.png
---
height: 200px
name: peaceANDlove-figure
---
Even abstract concepts like peace and love can be considered objects!
```

See! I wasn't kidding when I said computer scientists will try to describe everything as objects. And they do because their official definition
of the term is super generic: an object is anything that has some <b><i>state</i></b> and <b><i>behavior</i></b>. 
<br>
<img width="400px" src="https://66.media.tumblr.com/8c81ee99c3bd4a24fb6e9f6a989ae19c/tumblr_pdt19g8dh91wmjj3po2_500.gif"><img src="https://pa1.narvii.com/5780/9ab01f3bcf61f2b2c4abc0a4f450f175e1c97187_hq.gif" width="340px"><br>
<br>
Damn. I thought I could sneak that in without you noticing. Let me rephrase; an object is a bundle of information and all the things we can do to interact with that information.
Still a bit confused?  Consider our friend the whale object. The bundle of information that makes him a whale object, as opposed to the pencil object, is quite large. This
information might include the following facts: he is blue, large and alive; he is a mammal that lives in the sea and communicates through song.  
More impressively, he can do things in this world that change some of that information (swimming makes him a tired whale while singing might make him a happy
whale).

Need another example? Let's try to conceptualize an object that is commonly used within music streaming software, the song. The characteristics that
make up a song object might include: length, artist, writer, key, number of plays, and rank in the world. Obviously, we can change the data that 
represents the number of plays by pressing the play button -- this action will increase the number of plays by 1! If the number of plays becomes
large enough, we might even be able to change the song object's rank in the world. 

As long as you understand that an object is just a collection of data that can be changed by some action, then you're good to go. But what about
our computers? How do they reason [^*] about objects? And how might we communicate the notion of an object to our computers so that they don't have a temper tantrum [^**]?

[^*]: I'm being really generous with the word "reason" here. Computers don't reason about anything. They're really dumb. Alas, it's suprisingly difficult to talk about computers without
anthropormorphizing them.  

[^**]: Look at me giving computers human characteristics again. Funnily enough, this human trait is a lot more accurate when describing computers.
