---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Java
  language: java
  name: java
---

Compilation
===========

Before we continue discussing the life-cycle of a Java program, it's time for a history lesson!

In the early days of computer science (late 1940s/early 1950s), programmers had to memorize patterns of 0s and 1s to get their computers to do anything. It was paradise for any computer because they all understood these 0s and 1s perfectly; however, it SUCKED for the engineers because it was impossible to learn.

Things got a little better when programmers were able to convert these sequences of 0s and 1s into Hexadecimal --- hey, at least it was shorter --- but it still was close to impossible to learn. Not convinced? Here's how you would get the phrase "Hello world" to display on the monitor of your computer using these Hexadecimal codes [^*].

```{image} machinecode.png
:alt: Machine Code example
:height: 300px
```
<br>Obviously, most programmers of the time felt like this:

```{image} https://thumbs.gfycat.com/WiltedCourteousAzurevase-max-1mb.gif
:alt: Machine Code programmers
:height: 300px
```
<br>Eventually, a computer scientist by the name of David J. Wheeler[^**] suggested an idea to his colleague, Maurice Wilkes. I imagine the conversation went a little something like this:

Wilkes:
```{image} https://media0.giphy.com/media/ZKZiW6GSx8eSA/200.gif
:alt: Frustrated programmer
:height: 300px
```
<br><b>Wilkes</b>: <i>...I can't keep doing this...there must be a better way!!!!</i>
<br><b>Wheeler</b>: <i>Here me out...whaaaaat if we just made up some English-esque words to represent this gobbledygook?</i>
<br><b>Wilkes</b>: <i>Do it. Anything to stop this madness.</i>

And he did! Wheeler created a language called Assembly that made it a bit easier for programmers to write programs because it incorporated English. Don't get me wrong, it was still pretty difficult to learn, but this idea would shape many of the modern programming languages that we see today (aka if it looks like English, it will be easier to use and learn).

Fast forward to today and you will see that most modern programming languages look even more like English. Remember the Java statement from the previous page that displays the phrase "Hello, world!"?

```Java
  System.out.println("Hello, world!");  
```

I bet you notice some English words in there! For example, the words "out" and "print" stand out to me. Obviously, this can help programmers who are fluent in English to remember what code is needed within their programs [^***]. These English words can also help you make sense of the code you write because the words embedded within each code block were not chosen at random; they point to what each statement does! For example, `System.out.println(some_value);` <b>prints</b> a value <b>out</b> for users to see!

Computer scientists across the world instantly fell in love with these "high-level languages" for their ease of use but they ultimately had a problem --- computers couldn't make sense of any of them! So, in an effort to turn these languages back into those pesky 0s and 1s, Grace Hopper built something called a <b><i>compiler</b></i> [^****]. A compiler simply reads programs written in a high-level language, like Java, and turns it into something our computer understands. AND a compiler can do this without any human intervention. WHAT?

More specifically, the compiler starts by reading the first line of code found in your .java file. This line of code is found near the top of your program. Then, your compiler starts to make its way down, reading each line of code as it goes. As it reads, it notices the code snippets it was trained to notice:

```{admonition} Keywords
These are special words like <b><i>class</i></b> or <b><i>if</i></b>.
```
```{admonition} Operators
These are symbols like <b>+</b> and <b>*</b>.
```
```{admonition} Literals
These are values like the number 3 or the sentence "Hello, world!".
```
```{admonition} Identifiers
These are the names you give things like attributes and methods.
```
```{admonition} Special Characters
These are a small list of keys found on your keyboard. They include characters like the semi-colon and parentheses.
```

With just these 5 things, you can create incredibly complex programs that get your computer to do some pretty complex things. This also highlights why it is really important for you to be really careful when writing code; if you forget a semi-colon, or you spell a method name incorrectly, your computer's compiler will FREAK OUT because it wasn't trained to recognize anything outside of the list mentioned above. We call mistakes like this <b><i>compile-time errors</i></b>. And when you do make these mistakes, your compiler will do it's best to let you know what's wrong. Don't believe me? Try to <b><i>compile</i></b> the statement below.  

```{code-cell} java

System.out.println("Hello, world!");

```

See it doesn't work! But the compiler does let you know what it thinks is wrong. See if you can fix the mistake based on the error message that is displayed. Once you're done, move to the next page!

[^*]: These weird and random characters are collectively referred to as Machine Code. Computers LOVE it. Humans HATE it.
[^**]: David J. Wheeler was actually the first person to ever receive a PhD in computer science, the highest degree you can get in the field. He got the degree in 1951 from the University of Cambridge.
[^***]: Yup, this totally gives native English speakers a bit of an edge when programming. However, there are some programming languages that are built with other spoken languages in mind! <a target="_blank" href = "https://en.wikipedia.org/wiki/Non-English-based_programming_languages">Check em out if you're curious!</a>
[^****]: Move over Wheeler, Grace Hopper is in the building! She built the first compiler, and is generally thought of as one of the most distinguished and accomplished computer scientists in the world.
