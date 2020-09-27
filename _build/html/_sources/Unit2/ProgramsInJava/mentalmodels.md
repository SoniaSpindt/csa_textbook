The Notional Machine
====================
```{epigraph}
To understand a program you must become both the machine and the program.

-- Alan Perlis
```
Like Dr. Perlis, I am convinced that you need to know a little bit about how your computer works in order to better understand how to control them. I hope that by explicitly naming some of the underlying components of your computer, you will be better able to explain and predict all of its observable behavior. This ability will not only help you do really well on the AP CSA exam, but it will give you an edge in future computer science classes that you take.

CS teachers like to call this shared mental model the <b><i>Notional Machine</i></b>. Duh duh duh!!!! You can think of the Notional Machine as the collection of diagrams we will use to illustrate how your computer is reasoning about the programs you give it. The Notional Machine is not something that I can describe on a single page of our textbook; instead, it is a learning tool that we will build up and constantly refer to over time.

Today, we will begin our exploration of the Notional Machine by discussing the general lifecycle of a Java program. This lifecycle starts with you! How? Well, one day you will decide that you need a Java program in your life. In order to write this program, you must first create a new file! Think of this like opening a new Google Doc for an essay you need to write. However, instead of writing English sentences in a <b>.doc</b> file, you will write lines of code in a <b>.java</b> file.  

Now imagine that you were super productive and wrote a ton of code into your <b>.java</b> file. It looks like this[^*]:
```Java
class Greetings{  
    public static void main(String args[]){  
     System.out.println("Hello, world!");  
    }  
}  
```
Everything looks good, so you decide it's time to see if your code actually works! In other words, you decide to "run" your program by pressing enter. Go ahead! Click into the text box above and press enter! :)

As you can see, your computer instantly spits out the phrase "Hello, world!". It may feel like magic, but I swear it's not! I hope that the Notional Machine will help to make these secret, hidden steps a little more obvious for you; and in doing so, we will take a lot of the frustrating guess work out of programming.

So how does your computer make this magic happen? Spoiler alert! Go to the next page. :)
Let's examine this hidden process a bit more because I hope that this will help to take a lot of the frustrating guess work out of programming. Move to the next page!


[^*]: Don't panic! It's normal to look at this code and think it makes no sense! We will talk about the specifics of this code over the next few weeks. :)

is systematically reading each line of this program in a very specific and honestly, predictable way. Understanding a bit more about the compiler will help you make sense of the programs you write before you ever ask your computer to run them! So who is this? And what do they do?

Today, we will begin our exploration of the Notional Machine by discussing the <b><i>sequence</i></b> in which your computer <b><i>executes</i></b> lines of code within a Java program. In other words, we are going to discuss the general order in which your computer reads and interprets lines of code found within a program. Consider the following four lines of Java code:

By examining the order in which lines of code are generally executed, we will meet two important players in the world of Object Oriented programming, the <b><i>compiler</i></b> and the <b><i>Java Virtual Machine</i></b>.
