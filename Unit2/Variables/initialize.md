Initializing Variables
======================
When you're ready to give your variable a value for the very first time in your program, you will need to <b><i>initialize</i></b> it to said value. We can initialize the `score` and  `percentChange` variables to values using the assignment operator (cough the equal sign cough). Now, our program will look like this:

```Java
  1. int score;
  2. double percentChange;
  3. score = 100;
  4. percentChange = 45.7;
```

<br> As you can see, we are declaring the variables `score` and  `percentChange` on line 1 and 2 of our program, and initializing them to the numbers 100 and 45.7 on lines 3 and 4 of the program. Here's how your computer might interpret this program:

```{image} https://media.giphy.com/media/qd4KyIfroda2Tt1QeT/giphy.gif
:alt: Notional Machine variables 3
:height: 200px
```
<br>What if you want to change the value that is stored in your variable? No problema! We can change our minds by <b><i>assigning</i></b> our variables to new values (cough use the equal sign again cough). Our computer is happy to chuck the old value and replace it with a new one. Here's what it might look like to <b><i>assign</i></b> our variables to new values[^*]:

```Java
  1. int score;
  2. double percentChange;
  3. score = 100;
  4. percentChange = 45.7;
  5. score = 200;
  6. percentChange = 11.2;
```
```{image} https://media.giphy.com/media/QrAP7jWVHbpGkeb58x/giphy.gif
:alt: Notional Machine variables 4
:height: 200px
```
<br>I REALLY need you to notice that the values stored in `score` and `percentChange` are the MOST RECENT values assigned to the variables. What makes something the most recent value? That's decided by our compiler, and remember, our compiler reads from top to bottom. So, the most recent assignment is the assignment which occurs last. In this case, that is line 5 and 6 of the program above. All other values are instantly forgotten by our computer because they no longer occupy any space in our computer's memory.

Ok, ok, so we can store numbers in our variables. Big deal. Can we store anything a little more complex in variables?

```{admonition} TL;DR
:class: warning
 You will always follow this pattern when you need to initialize or assign your variable to a value:
 <br>`name = value;`
 <br>If you want to declare and initialize in a single line, you will follow this pattern:
 <br>`type name = value;`
```

[^*]: <i>Initialize</i> is only used to refer to the first value that is given to our variables. <i>Assign</i> is used to generally talk about giving variables values. It's very much like the math saying of "every square is a rectangle but not every rectangle is a square." Initialization is a form of assignment. Assignment is not a form of initialization.
