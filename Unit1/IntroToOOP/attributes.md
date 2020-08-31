Attributes
==========

By now you have probably noticed that objects have a set of characteristics associated with them. These facts are collectively referred to as an object's
<b><i>attributes</i></b>. You can think of attributes as the things that make an object itself! Attributes are also an important component of classes --- without attributes our objects
would be meaningless!

Still a bit confused? That's ok! Let's list all the attributes that might be found in a Vehicle class. In other words, what information do we need to make a vehicle object? In 
order to complete this thought exercise, you need to ask yourself what makes a vehicle, well, a vehicle? It's important to keep in mind that the list of attributes you come up with will
be based on your beliefs about the world. And that's ok! Remember, computers are dumb. They will believe anything you tell them. ;p

 I have included a drawing to help our discussion:

```{figure} vehicles.png
---
height: 300px
name: vehicles-figure
---
These objects are vehicles.
```
Soak it in. Try to list out all of the characteristics that the vehicles have in common. For example, I notice that all of our vehicles have some number of wheels [^*].
Can you think of anything else that they share? 
<br>

```{image} https://media.giphy.com/media/DfSXiR60W9MVq/giphy.gif
:alt: Time to think!
:height: 300px
```
<br>

Got your list? Here are some class attributes that make sense to me:

```{admonition} My Class Attributes
1. Has an engine
2. Manufacturer name
3. Number of doors 
4. Number of wheels
5. Number of passengers safely transported 
```

I hope you noticed that this list is really generic, and it doesn't account for the fact that our vehicle objects can actually look different for each of the categories listed above. This
is due to the fact that these 5 attributes are <b>class</b> attributes. They must stay generic so that our classes can make objects that are not exactly the same.

Every vehicle <b>object</b> created will then store specific nuggets of information within each attribute listed. For example, our car object might look like this:

```{admonition} Car Object
1. Has an engine = true
2. Manufacturer name = Ford
3. Number of doors = 4
4. Number of wheels = 4
5. Number of passengers safely transported = 5
```

<br>

We call this the <b><i>state</i></b> of the object! The state of an object just refers to the information that is stored within its attributes at a given moment in time. We'll talk about
how we might change the state of an object in our next section.

What might the state of the bicycle object look like?

```{admonition} State of Bicycle Object
1. Has an engine = false
2. Manufacturer name = Giant
3. Number of doors = 0
3. Number of wheels = 2
4. Number of passengers safely transported = 1
```

Remember, it's ok if your list of attributes looks different than mine! The attributes included within a class, and consequently, the possible state of a given object, is really a 
matter of personal preference. I, and many other object oriented programmers, will agree with your design choices as long as you can justify your decisions. 

[^*]: Planes have wheels. You just can't see them in the pretty picture I drew. Not convinced? Think about how planes take off and land. Wheels are involved.
