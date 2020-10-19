Boolean Expressions
===================

It may be hard to imagine how two little words can be so powerful. I promise this will become more obvious as we use booleans within more complex statements. For now, let's focus on how booleans can be used within expressions. YUP. You heard me correctly; booleans can be used within expressions!

Remember, an expression is the combination of one or more values that our computer can evaluate in order to produce a new value. The value that our computer produces will be the simplest version of that particular data type. When we are looking at a mathematical expression, like ((25 * 3) - (62 / 4)) + 587, our computer will perform the math and reduce this expression to a single numeric value, in this case 646.5. In the case of mathematical expressions, the integer and double data types are the simplest values a mathematical expression can become.

What about expressions that contain booleans? It's the same idea, except instead of simplifying the expression to an integer or a decimal, our computer simplifies these expressions to either `true` or `false`.

However, it's a little less obvious that an expression will turn into a boolean value because these expressions often contain values of <i>type</i> int and double. The trick is to see if the expression in question contains one or more of the following special operators:

```{admonition} Comparison Operators
1.  `>` (Greater than)
2.  `<` (Less than)
3.  `>=` (Greater than or equal to)
4.  `<=` (Less than or equal to)
5.  `==` (Equal to)
6.  `!=` (Not equal to)
```
```{admonition} Logical Operators
1.  `&&` (AND)
2.  `||` (OR)
3.  `!` (NOT)
```

As soon as you see one of these operators used in an expression, then you know your computer will turn that expression into `true` or `false`. Here is an example of an expression that will produce the value `true`:

```Java
(5 + 2) == 7;
```
Notice the <i>equal to (`==`)</i> comparison operator? It's important that you're especially careful with this operator because it looks A LOT like our assignment operator (`=`). Don't confuse the two! They do very different things --- the comparison operator (`==`) compares two values and the assignment operator (`=`) assigns a value to a variable.

If we were to translate this expression into English, we would be asking our computer, "Is the sum of 5 and 2 equal to 7?" The answer to this question is "yes" in English. The word for "yes" in Java is "true"!

Here is an example of an expression that will produce the value `false`:

```Java
((5 + 2) != 7) && ((10 - 5) >= 1);
```
This expression is definitely a bit extra because it contains a bunch of smaller expressions inside of the overall expression. Let's break it down piece by piece to really see what's going on here.

First of all, we know our computers follow the standard order of operations [^*]. This means our computers will begin by evaluating the smaller expression found on the left side of the `&&` operator, ((5 + 2) != 7), because this is contained within multiple sets of parentheses. In fact, our computer will start on the inside of this expression because 5 + 2 is technically contained within TWO sets of parentheses and that takes higher priority than just one set of parentheses. Once our computer performs this evaluation, our expression will be simplified to this:

```Java
(7 != 7) && ((10 - 5) >= 1);
```
What subexpression do you think our computer will tackle next?

```{image} https://thumbs.gfycat.com/DemandingFrighteningKinglet-max-1mb.gif
:alt: Fresh Prince thinking
:height: 200px
```
<br>If you chose (10 - 5) then you're right [^**]! Once our computer performs this evaluation, our expression will be simplified to look like this:

```Java
(7 != 7) && (5 >= 1);
```
Now, our computer will evaluate the expressions found in just a single set of parentheses, working its way from left to right. The expression found to the left of the `&&` operator, 7 != 7, is how we ask our computer the question, "Is 7 not equal to 7?" in Java. Obviously the answer to this question is "no", so (7 != 7) becomes `false`. The expression found to the right of the `&&` operator is how we ask our computer the question, "Is 5 greater than or equal to 1?" in Java. The answer to this question is "yes", so the expression becomes `true`. Now our expression looks like this to our computer:

```Java
false && true;
```
WHAT THE HELL DOES THAT MEAN??? This is where the `&&` logical operator kicks in. Logical operators (`&&`, `||`, `!`) allow us to combine multiple boolean expressions in a single line of code. The logical operators actually represent how electricity flows through your computer's circuitry, but understanding how this works is outside the scope of this class; instead, you should just memorize what happens when our computer stumbles upon a logical operator:

```{image} truthTable.png
:alt: Truth Table for AND/OR
:height: 233px
```
```{image} truethTable2.png
:alt: Truth Table for NOT
:height: 100px
```
<br>Please notice that the `&&` and `||` logical operators have TWO boolean inputs, one on either side, while the `!` operator only has ONE boolean input.

If you take a look at the first table, you'll be able to see how our giant boolean expression is simplified to `false` --- if one of the boolean inputs for `&&` is false, then the entire expression becomes false! The AND operator is picky like that; the OR operator is a little more forgiving.

The NOT operator is fun because it has the power to turn a boolean into its opposite value; true becomes false, and false becomes true. Make sure you memorize these tables! This information ALWAYS shows up on the exam. :/

Check your understanding of how boolean expressions are evaluated by reasoning through the program found below. As yourself, "what will be displayed as a result of executing this program?" Take it line by line, and don't forget about PEMDAS!

```Java
1. boolean gotIt;
2. gotIt = !(((3 + 3 == 9) || (150 / 50 != 3)) && (2 * 2 >= 8));
3. System.out.println(gotIt);
```

When you're ready, scroll down to see if you're right. :)

```{image} https://media.giphy.com/media/uODr8dOfe9kU8cnrC8/giphy.gif
:alt: Example complex boolean expression
:height: 200px
```

```{admonition} TL;DR
:class: warning
1. Boolean expressions turn into either `true` or `false`.
2. Our comparison operators are: `>`,`<`, `>=`, `<=`, `!=`, `==`
3. Our logical operators are: `&&`, `||`, `!`
```

[^*]: PEMDAS alert!
[^**]: The reason why is because this expression is in encased within two sets of parentheses. The more parentheses you use, the more our computer will want to evaluate these expressions first.
