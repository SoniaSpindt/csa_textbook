Dot Notation
============

In order to call a method on a specific object, you must use something called ***dot notation***. Dot notation is a really powerful way of accessing and using both the instance variables and methods of a class.

More specifically, the various things an object contains--—its instance variables and its methods--—are called the ***members*** of that object. The members of an object are accessed using dot notation, which looks like this:

```Java
objectReference.memberName
```

The objectReference is the name of the reference variable that points to the object in question. The memberName is the instance variable or method name that we are trying to access within the class.  

In our previous example with BTS, we were able to use (*cough call cough*) our `recordAlbum` method because of dot notation. We can even check that the state of our BTS object was correctly updated by continuing to use dot notation within our Java program like so:

<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/63Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

As you can see on lines 12 and 13, we are using dot notation to access the `numberOfRecords` attribute for both the BTS and GLAM objects. The state is different for these two objects because we only called `recordAlbum` on the BTS object, not the GLAM object.

This also means that we can use dot notation to assign instance variables to new values. For example, we could have also written the following line of code to increase the number of records BTS has made to 1:

```Java
BTS.numberOfAlbums = 1;
```

This accomplishes the same thing as our method `recordAlbum`, though it requires more knowledge of the current state of the object by the programmer. This is obviously less preferable than defining the method because mistakes are more likely to be made this way  --- what if this statement was written after BTS released their second album? Then the state of the object would no longer be correct because the programmer simply forgot to write 2 instead of 1. On the other hand, `recordAlbum` can easily just add 1 to whatever value is currently stored within the `numberOfAlbums` attribute, regardless of what the programmer knows.

Don't get me wrong! You're still going to need to use dot notation to access attributes all the time. Developing this intuition simply takes a bit time and practice. But I promise that over the course of the new few weeks, you will become a dot notation master!
