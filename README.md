# JavaScript-The-Good-Parts

# Chapter 1: Good parts
# 1.1 - Why is JavaScript?
   - Js is the loose typing language when compair with other language
     - As in java, when you create a function with argument is string then call that funtion and pass a number, complier with detect errors for you, but with Js...nothing happens
   - Js is an important language because of it is language of web browser
     - If you wanna develop web, There is no choice but to JS
   - Js is built on some very good ideas and have few very bad ones
     - Good ideas: function, loose typing, dynamic object, an expressive object literalnotation. (Object can be created by listing their components)
     - Bad ideas: is a programming language base on global variables, all of the top-level variables of all compilation units are tossed together in a common namespacecalled the global object (window), amazing when create file a.js have function a(), variable aVar and then create b.js, in b.js you can call a() and aVar.
> There are two answers:
>The first is that you don't have a choice. The Web hasbecome an important platform for application development, and JavaScript is the only language that is found in all browsers

> The other answer is that, despite its deficiencies, JavaScript is really good. It is lightweight and expressive. And once you get the hang of it, functional programming is a lot of fun
# 1.3 - A Simple Testing Ground
   - If you have a web browser and any text editor, you have everything you need to run JavaScript programs
> First, make an HTML file with a name like program.html:
```
<html>
    <body>
        <pre><script src="program.js"></script></pre>
    </body>
</html>
```
> Then, make a file in the same directory with a name like program.js:
```
document.writeln('Hello, world!');
```
> Open file program.html on browser

> Result: Hello, world!
