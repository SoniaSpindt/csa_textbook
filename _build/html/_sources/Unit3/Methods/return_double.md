Returning Decimals
==================

Let's see what it looks like to return a decimal from a method. Take a look at our `Actor` class again, but notice that there is a new method! It's named `getNetWorth` and it returns the total amount of money that an actor has earned.

<iframe height="400px" width="100%" src="https://repl.it/@SoniaSpindt1/65Example1?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>

As you can see, the value stored in the attribute `netWorth` is being returned by the method `getNetWorth` every time it is called. In other words, the call statements found within the `Main` class are literally being replaced by the value stored in each object's `neWorth` attribute. This allows us to use the dot operator in new and useful ways because this allows us to embed function calls wherever we need to plug in a specific value related to the state of an object.

Can we do the same thing for booleans? Keep reading to find out!
