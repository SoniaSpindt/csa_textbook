Parameters
==========

By now, you have probably noticed that method names are always followed by a set of parentheses. Defining a method? Gotta use parentheses after the name. Calling a method? Still gotta use parentheses. But whyyyy????

```{image} https://media4.giphy.com/media/jokkaWkMRp3MklZBxm/200.gif
:alt: Why tho?
:height: 200px
```
<br>Parentheses are used to contain something computer scientists call ***parameters***. Parameters are all of the information that you need to give a method in order for it to find a solution to the problem it was designed to solve. You can think of this like the ingredient list of the recipe we saw for the "Best Cookies Ever":

```{image} https://csatextbook.soniaspindt.com/_images/cookieRecipe.png
:alt: Cookie recipe
:height: 400px
```

<br>Without listing things like "1 cup of salted butter" or "2 cups of chocolate chips" at the top of the recipe, no one would actually be able to make the best cookies ever.

Obviously, not every method that you define will utilize parameters. However, with time and a little practice, I bet that you will find that parameters are pretty dang useful. Why? Parameters make our methods a lot more generic in nature, which means that a single method can be used to solve problems that are slightly different from one another.

Think of our cookie recipe from above! What if someone asked you to bake the "Best Cookies Ever" for 500 people. Do you think that 2 cups of chocolate chips and 1 cup of salted butter would be sufficient to make enough cookies for this number of people? No! But we're not going to write a new recipe every time someone asks you to do something different. Instead, you would probably just do some mental math to figure out how to scale this recipe to meet the demands of this crazy person.

And guess what! We can do the same when defining our methods. So let's take a look at how we can include a few parameters within a method definition.
