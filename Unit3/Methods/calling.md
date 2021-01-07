Calling Methods
======================

Imagine it's the early 2000s and you're living in South Korea as a software engineer. Although Java has only been out for a few years, it is a tool you use everyday at your job at Big Hit Entertainment, managing the database of artists working under the label.

On the first day of the job, you begin by declaring a dope `Artist` class that can be used when a new artist signs with the label:

<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/62Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

As you cans see, you use the constructor to initialize `numberAlbums` and `earnings` to 0 because you think it is safe to assume that every artist newly signed will not have had a chance to record an album and consequently, has made no money.

The artist will eventually record an album though, so you know you will need to be able to change the value that `numberOfAlbums` is assigned to. You believe its best to handle this with a public method that increases the value of `numberOfAlbums` by one every time it is used.

You decide to define the method `recordAlbum` in your `Artist` class, like so:

```Java

public void recordAlbum(){
  numberAlbums = numberAlbums + 1;
}  
```

You do good work, so Big Hit Entertainment keeps you around well into the 2000s, long enough to see the creation of the world-famous BTS.

<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/62Example2?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

As soon as they sign, you instantiate the BTS object and wait until they produce their first album.

When "2 Cool 4 Skool" debuts, you immediately jump into your Java program and ***call*** the BTS Object's `recordAlbum` method, like so:

```Java
BTS.recordAlbum();
```

This will update the state of the BTS object to reflect the current state of the band in real life, making it easier for high-level managers to quickly assess the overall performance of the company. A job well done!

More importantly, this story illustrates how methods can be use to selectively update the state of an object, while leaving the state of other objects unchanged. Let's examine this pattern a little more deeply on the next page.
