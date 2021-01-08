Many Parameters
===============

Sometimes we will need more than one parameter in our methods. No problema! All we have to do is separate our parameters with a comma or two.

Again, take a look at the `Books` class in our Goodreads example:
<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/613Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

<br>There is a new method defined on line 31 named `setAuthorName`. This method utilizes two parameters, `firstName` and `lastName`. We know that there are two parameters in this method because there is a comma that separates them from each other; this is how the compiler knows that there are two parameters in play.

If you forget the comma, your compiler will no longer be able to tell where one parameter ends and the next begins (and it will display an error message telling you that this is a "no no"!).

You can include as many or as few parameters in your methods as you would like! Just make sure that you use your commas in the cases where you use more than one.

What does it look like to call our new method? You could do something like this in `Main.java`:

```java
stamped.setAuthorName("Ibram X.", "Kendi");
```
Or this:
```java
stamped.setAuthorName("Ibram", "X. Kendi");
```
You can even tweak the `setAuthorName` definition so that it uses three parameters instead of two; one for first name, one for a middle name, and one for a last name. In either of the examples above, it is important to notice the use of commas. Again, a comma is used to separate one argument from the next.

Remember, our computer cannot infer what you intend to happen; instead, it is simply plugging in values based on their position within the method call. Don't think that our computers can tell that "Ibram" is the author's first name and "Kendi" his last. Our computer would easily make "Kendi" the author's first name if you wrote your call statement like this instead:

```java
stamped.setAuthorName("Kendi", "Ibram");
```
Our computer only does what it is told, so be very careful about how you pass in your arguments -- it could mean the difference between generating the right output instead of the wrong one!
