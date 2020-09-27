Execution
=========

Once your compiler is happy, it will turn your <b>.java</b> file into a <b>.class</b> file. This new file contains the compiler's translation of your Java code, and this is what is executed by your computer when you press that shiny "run" button in your text editor[^*].

So what does your computer do? Well, your computer will begin to read the translation from the very top of the file, just like the compiler did. It will work it's way to the very bottom of the file, <b><i>executing</i></b> each translated statement that it encounters along the way. In other words, your computer will do everything that you (correctly) asked it to do!

However, there are a few types of errors that can pop up after the compiler has finished compiling your Java code. These mistakes happen when your computer runs the <b>.class</b> file, and are collectively referred to as <b><i>runtime errors</i></b>. Runtime errors are a lot rarer than compile-time errors in this class. Why? Novice programmers simply make more compile-time errors when learning to code. :p In other words, novice programmers are more likely to forget things like semi-colons at the end of statements, and these kinds of mistakes are caught by the compiler. You and your compiler are going to become the best of friends this year!

How can you tell if you're experiencing a compile-time error or a runtime error? Well, most IDEs (the place programmers code) will be nice and tell you. In fact, the IDE that we're using this year has done just that. See if you can tell the difference:

```{figure} runtime.png
---
height: 200px
name: runtime-figure
---
Mystery error message 1.
```
```{figure} compiletime.png
---
height: 200px
name: compiletime-figure
---
Mystery error message 2.
```
If you're thinking most of that looks like complete gibberish, then you're not alone --- I still want to pull my hair out when trying to decipher error messages. For now, I want you to focus on the glaring red letters. What do they say? Did you notice that mystery message 2 actually includes the word "compiler" in it? If you did, then you're right! Error message 1 is the runtime error and error message 2 is the compile-time error.

If you're feeling really brave, you can try and figure out what went wrong. Hint, the specific description of the mistake is found right above the red letters. <br> <img src="https://i.imgflip.com/4g76nd.jpg" title="made at imgflip.com"/>



[^*]: I'm leaving out a few additional steps here. Don't worry, they're not terribly important to know for this class, so I'm going to skip over them. However, if you're curious about this step, google "Java Virtual Machine".
