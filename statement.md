# C# Tutorial - Part 1: Intro

C# (pronounced "C sharp") is a high-level general-purpose, compiled, managed, object-oriented programming languaged developed by Microsoft, with default libraries now managed under the .NET Foundation.

What does all that mean?
* C# can create all sorts of programs: Games, websites, servers, apps, databases, you name it! The code for almost anything that isn't an operating system or driver can be written entirely in C# (although even some projects find a way!). 
* C# is "compiled", meaning that another program (known as a compiler) takes the code that you can read, and changes it into a form the computer can read. This is different than an "interpreted" language like Python or JavaScript, which is are scripts that the computer reads the text the moment you run them. 
* C# uses the concept of "objects". We see objects in real life all the time, like the screen you may be reading this on. But computers don't understand what an "object" is. Luckily, we programmers can create our own objects, and have the computer pretend they exist. It makes it easier for us to make them interact with each other in programs, and for us to organize them.
* C# has managed memory. This means the program picks up after itself. If you are done using a piece of memory, it becomes garbage. As with any garbage, it needs to be collected. A "Garbage Collector" process runs to give memory back to the computer when your program is done with it. This will slightly slow down the computer and make it use a bit more memory, but it lets you focus on doing what you care about, instead of managing that pesky memory.
* C# uses the ".NET" libraries in its most core functionality. If you've ever used a higher-level programming language, you find out pretty quickly that you don't make the computer do everything! You instead ask the computer to do something, and if you are allowed to do it, you can! .NET gives you all the things you need to make C# work on any modern operating system (not just Windows, like in the good old days)!

# World's Smallest C# Program™

Here is the smallest C# program possible. We shall be expanding this ever-so-slowly over time. Before long, you can create the next big thing on your own! (Legal note: The next big thing is in limited supply, and cannot be guarenteed to every student)
```C# runnable
static class Program {
    static void Main() {}
}
```
Wow. That is... boring! No namespaces, no .NET, no variables, no objects, no input. It doesn't even say "Hello"! We shall be there soon enough.
First, let's discuss what we have so far:
* In C#, by default, all code starts with a "Main" function. There are going to be many classes in a large project, but only one place tp start. "Main" in this case is going to mark the beginning of it all.
* In C#, all code is inside of a class (or a "struct", which we shall get to another time). Objects are going to exist, whether we like it or not. Many early languages didn't have this luxury. In this case, a class named "Program" is used to store our Main function.

We see other things here, such as "void" and "static", as well as those unusal curly brackets, "{" and "}". We will go into detail later, but now, a simple explanation for each:
* "void" means the function doesn't return ANYTHING. It just stops when it's done, and doesn't give the computer any data to work with when it's done. This will be important later when you write your own functions.
* "static" means 'THERE CAN BE ONLY ONE!!!'™. Basically, if something is "static", don't bother creating an object for it (it won't let you). This is good, because you only need one Main function for a program.
* The curly brackets indicate to the computer that whatever is in between belongs to the line it is on. Fun fact: In C#, you could write that whole program on one line! But it would look really ugly and be hard to read, so we put those there to help programmers write long programsd with many lines. They are required in many cases as well.

That's a LOT to go over and remember, but don't worry about it! You will get used to it over time, and learn the value of many of these options.
Before moving on, let's add onto this program:
```C# runnable
using System;

static class Program {
    static void Main()
    {
        Console.WriteLine("Hello World!");
    }
}
```
Here, we have done something pretty significant: We imported a .NET library. By saying "using System;" we asked the computer to give us access to more classes and function to use in our program. There are quite a lot of them, but fortunately, we only need one of them: The "Console" class. This class represents the command prompt (or teerminal, if you use MacOS or Linux). Inside that class, there is a piece of code called "WriteLine". This tells the Console on your computer to write a piece of text and end it with moving to the next line. In this case, whatever is inside the quotation marks gets written. I told it to say "Hello World", but any texts will do!

It's important to note that programming languages like C# are very strict in how you type them. If you remove any one of the lines (except for the blank one), or make typos, it's over! The compiler won't know how to change it into the computer's language for it to run. It isn't very good at guessing either, but it will often tell you some ways it could be fixed!

Next lesson, we will go over variables, a core part of any programming language, and how you can use them to do math, as well as to collect and use data!