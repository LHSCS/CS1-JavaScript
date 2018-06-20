# JavaScript Text 2018

## Chapter 1 - What's JavaScript?

> Any sufficiently advanced technology is indistinguishable from magic.
> 
> *--Arthur C. Clarke*

### 1.1 What's a Computer Program?

Everyday you interact with computers.  If you use your cell phone, ride in a car, use a microwave, swipe a credit card, or, of course, use a computer to word process a paper, you are interacting with a computer.  Nearly every aspect of our lives from the clothes we wear to the food we eat, from medical treatements to sporting events, typically involve and sometimes depend on computers.

We have all told computers what to do, in the sense of telling our phones who to call or what music to play or telling our cars how fast to go, but in each of those cases we are really interacting with a program that is designed to listen for precisely the kind of thing you are telling it and nothing else.  The computers in your car, for instance, don't know how to make coffee, and the computers in the machines that made the fabric in your clothes, don't know how to stream your favorite music. But the computer in your coffee maker and one of the computers in your car may in fact be very similar computers with very similar capacities, but what is different is the program that they are running.

A computer program is a set of instructions that the computer must follow.  Without a program, a computer just sits and does nothing.  When you run an app on your phone, you are choosing to run a program.  Where to the programs come from? Programmers write them and that is what you will learn how to do in this course.

People write programs using vocabulary (commands) and grammar (syntax) that makes sense to people.  Just like there are different human languages in the world, there are different computer languages that can be used to write programs, each having their own commands and syntax.  In this course, we will study a language called JavaScript.  

Our computers though, don't know JavaScript or any other human language.  Computers really are sets millions of carefully arranged [switches (transistors)](http://www.explainthatstuff.com/howtransistorswork.html).  Switches can be either on or off. One or more switches can be connected to other switches to turn them on or off.  By creatively configuring these switches, computer scientists have found ways of getting them to do mathemtical calculations like adding.  Furthermore, they have found ways of getting them to do logical calculations, such as `IF A > B, then do C`.  

> In one sense a computer is only the transistors and the connections between them, but describing it like this loses something in the process. You can't really understand the computer unless you understand its functional relationships, what it's trying to accomplish, and the purpose that it serves to its human creators.
> 
> *--Bill Newsome*
> 
Using the building blocks of mathematical and logical calculations, computer scientists have found ways to get switches to do amazing things, but since it all comes down to switches being on or off, we have to program computers in on's and off's.  We often call these on's and off's 1 and 0 and refer to them as **binary** language.

![Translating a High Level Language Into Binary](http://www.cs.uah.edu/~rcoleman/CS121/ClassTopics/Images/ProgLanguages06.jpg "Figure 1.A")
*Figure 1.A*

We will write programs in JavaScript using English words and mathematical symbols that we are familiar with. JavaScript is called a high level language since it is far removed from the actual 1's and 0's. Our JavaScript program will be handed off to another program that turns it into binary for the computer to actually execute.  For more information on this process, there's a wide ranging but very interesting article on coding/programming by Paul Ford [here](http://www.bloomberg.com/graphics/2015-paul-ford-what-is-code/#grabbag). Chapter 2 is the most relevant part.

![Dilbert - Scott Adams - Universal Features Syndicate, Inc. 1992](https://lyndenmath.org/CSAssets/dilbert1.png "Dilbert - Scott Adams - Universal Features Syndicate, Inc. 1992")

### 1.2 Writing a Computer Program

> **TARGET**: Be able to use the Repl.it IDE to write and run simple JavaScript programs.

Follow your teacher's instructions and login to Repl.it and enter the JavaScriptA course. Repl.it is a software environment that allows you write programs in JavaScript.  It then turns your program into binary, runs the code and gives the results back to you. The REPL in the name Repl.it stands for Read Eval Print Loop. REPL's are simple programming tools that programmers use, and while Repl.it started out as being fairly simple, it has developed into an integrated development environment (IDE).  It is quite possible to write programs with just a text editor, but programmers typically prefer the added features of REPL's and IDE's.

Repl.it will give you 3 windows.  On the right you will find the assignment instructions from your teacher. The left top window is the *editor* where you write your program, and the left bottom window is called the *console* and it is where you get information back from your program.

![repl.it interface](https://lyndenmath.org/CSAssets/replit_helloworld.jpg "Figure 1.B")
*Figure 1.B*

The 3 veritcal dots (elipsis) menu in the upper left gives you choices mostly about how your screen looks. The green submit button at the upper right is what you press when you are done with your assignment.

It is traditional for a first program to be something called the "Hello World" program. Type the following statement in the console.

```javascript
"Hello" + " " + "World";
```

This is a program. It doesn't do much, but it's a start. Please note that in this book, code examples like `"Hello" + " " + "World";` will be set in a monospaced font similar to what is used in Repl.it and also placed in a light grey box. It will make the examples easier to follow and it will make it easier to copy and paste examples.

Also note that every statement in JavaScript should end in a semicolon. Although the JavaScript language itself is smart enough to add in missing semicolons for you when it is reading what you have written, it doesn't always do it the way you might expect, so you need to always put semicolons at the end of each statement. The semicolon goes at the end of the entire statement.

Now type the same code in the editor window and press run.  While you can type code directly into the console, you will typically type it into the editor and then run it to see results in the console.  In order for your teacher to see and test the code that you write when you submit an assignment, it needs to be typed into the editor.

After submitting your completed Hello World program, take some time and play around with the program.  You can break it, in the sense that it may not work, but you can't break it, in the sense that it isn't fixable.

Try typing 1 + 1 in the console after the prompt (>) and hit return. Try some other math with minus, times (\*) and divide (/). Now try "green" + 1. Make sure you use the quotes around green. Did you correctly predict the outcome? As you can see, the computer understood the plus sign to mean "string together" (*concatenate*) rather than "add" in a mathematical sense. Try other combinations of words (with and without quotes) or numbers with the + operator and then try some combinations with the * (*asterisk*).

You may sometimes get errors in red, which means that your code isn't understood. That's OK, see if you can fix the error.

Finally, since computer programs are read not only by computers but by people, we often need to add information for people that makes our programs easier to understand, but which isn't written in the computer language.  To do this we use comment symbols.  Anything on a line after two forward slashes is a comment for people which is ignored by the computer.  For instance:

```javascript=
//This is a comment line
"Print this " + "to the console"; //The code on this line will run
//This line will be ignored: "Print this";
```

Only line 2 of the program will show up in the console, but not the comment at the end of line 2.  Only things after 2 forward slashes are ignored.

### 1.3 Variables

> **Target**: Be able to create proper variables and understand the necessity of input and output. 

To this point we've been poking around at a computer as though it is some sort of calculator with a full [QWERTY](http://gizmodo.com/why-we-still-use-qwerty-keyboards-even-though-theyre-a-1643855077) keyboard and a big screen. Not too useful. In order to write useful programs, we need **variables**. Variables in computer programs are pretty much like variables in algebra. They "contain" values and those values can change. It is perhaps a better metaphor in computer science to say that the variable *points to* a value rather than to say it *contains* a value, but for an introductory programming course, "contains" works just fine and it keeps it consistent with your math class concept of variables.

In JavaScript programming there are a variety of ways to create variables. This is the standard way:

`var firstNumber = 7;`

`var` is a **reserved** word that JavaScript uses to indicate that the word after it is a variable name. Don't try to use `var` for anything else. It is a reserved word and JavaScript will complain if you do. The "=" puts the number 7 into the variable `firstNumber`. If you don't assign a value to the variable, JavaScript will assign the value `undefined`. It is much better to assign an initial value because it tells us what type of variable you intend it to be and it helps us find errors as we read through the program. Let's take it a little farther with the four line program below. Go to Ex.1.3c in Repl.it and paste the first 4 lines below into the editor.

```javascript=
var firstNumber = 7;
var secondNumber = 6;
var sumNumber = firstNumber + secondNumber;
sumNumber;
    
    >>13
```

I will use the >> symbol to indicate what the computer produces in the console as a result of running the program. Can you follow what is going on?

You might be concerned that the assigning seems to be going the wrong direction. You might feel like we should use 7 = firstNumber to put 7 into the variable rather than the other way around, but that isn't how it's done, so you'll have to get used to it. Just think of it like x = 7 in algebra, the 7 goes into the x.

You should always make variable names reflect their purpose, but keep in mind that they can't start with numbers, can't contain non-alphanumeric characters (except \$ and _ ), can't be reserved words like var, and can't contain spaces. We can kind of get around the no spaces rule by using the "_" character or by interspersing capital letters. Both first_name and firstName are valid and slightly more readable versions of our variable firstname and yet don't break the no spaces rule. Interspersing is the most common technique used in JavaScript programming. It is usually referred to as *CamelCase*.

![Camel Case](https://storage.googleapis.com/codeavengers.appspot.com/cloud/lesson-plans/intro-to-coding/camelcase.png)

With multiple line programs like this, we can make programs that do a bit more for us. Try making a similar 4 line program using the variables firstName, lastName and fullName. Hint: put quotes around strings of letters like "Bob". Can you figure out from the variable names what the program should do?
    
### 1.4 Input & Output I/O

We've made some progress, but there are still some important pieces needed to make useful programs. We can work with strings and do some math and **output** results to the console, but what if we wanted our program to ask a user for something, process that information somehow, and then give the new result back to the user. We can already do output, but we need a way of getting information from the outside world into our program. We need **input**. Input and output are often abbreviated I/O.

> On two occasions I have been asked,
> 
> Pray Mr. Babbage, if you put into the machine wrong figures, will the right answers come out?
> 
> I am not able rightly to apprehend the kind of confusion of ideas that could provoke such a question.
> 
> *--Charles Babbage (1864)*

Copy and paste the following in the Repl.it program window for Ex.1.4c:

```javascript=
var age = prompt("What is your age?");
var nextAge = 50 + age;
alert("In fifty years you'll be " + nextAge);
```
Notice that the colors are not the same between this text and Repl.it. There is no standard color scheme for *syntax highlighting*, you just have to get used to however your environment does it, unless you are allowed to personalize it.  At present, Repl.it does not let you choose how to do the syntax highlighting. Run the program, but first, try to predict what it will do.

Repl.it shows you a dialog box asking for your age. If you respond, the program will continue and tell you that in 50 years you will be `nextAge`. But it will say you are over 5000 years old! What is going on here?

We have some new commands that I'm going to call **methods**. The `prompt()` method displays a box for the user to type something into and then takes what they type and sticks it into the variable age. The `alert()` method also displays a box with info, but doesn't ask any questions.

So we've got input from `prompt()` and we've got output from the `alert()` and it is no longer in the console, so we're heading toward our goal, but something is wrong with the math. We are expecting `50 + age` to be put into the variable `nextAge`, but instead we get 50xx with the xx being whatever age the user enters. The + is doing a concatenation rather than an addition, as though `age` is text and not a number. And that is the problem. In JavaScript any input from a `prompt()` is considered to be text, what we call a **string**, that is a string of letters. Fortunately there is a way to turn strings that look like numbers into actual numbers. It's the `Number()` method. Its **syntax** or proper usage, can be seen in the first line below and note that it *must* start with a capital N:

```javascript=
var actualNumber = Number("10");
var finalResult = actualNumber + 5;
finalResult;

>> 15
```
Here `Number()` turns the string value "10" into the number 10 that we use to do arithmetic. That will solve our programming problem.

As your programs get longer and more complex, it is a good practice to *declare* all your variables at the top of the program rather than along the way. We can use a single `var` statement and separate each variable with a comma as follows:

```javascript=
var age = 10,
    color = "green",
    life = true;
```
While I could have put all three lines on a single line, notice how the *indenting* improves readability. There are often multiple ways to do something. The goal of our various decisions is readability and error avoidance. We may not choose the most convenient way but we should always choose the most readable way. Using descriptive variable names, declaring them at the beginning of a program and assigning initial values has over decades of programming proven to be the best way to do things.

### 1.5 Types of Values and Operators 

> **Target**: Be able to describe and use different value types and explain type coercion.

In the previous section you saw that in JavaScript some types of values are treated differently than others. For instance in the situation "green" + 1; the 1 is treated differently than in the situation 2 + 1. JavaScript (or more precisely the JavaScript interpreter) will make its best guess as to what you mean. In the situation "green" + 1; it assumes that you want the 1 to be a character, not a number, since it doesn't have any simple way of turning "green" into a number. But in the situation 2 + 1, it assumes that you want both the 2 and the 1 to be numbers, although you could force them to be understood as characters by putting quotes around them.

The issue goes back to the fact that everything a computer deals with is ultimately binary. In binary, 00000001 is 1, but it can also mean "true". How does the computer know the difference? In binary, 01000001 is 65, but it also stands for the letter 'A'. In binary, the number 5 that we can do math with is 000000101, but the character '5' is 00110101, which is also the number 53. This could be very confusing even for a computer. The way the computer keeps all this straight is by requiring that we tell it what **type** of a value something is before we ask it to do some work with it.

#### Numbers

JavaScript understands several types of values. The first type of value is **number**. You have already worked with numbers like 1, 0.3 and -47. You can use positive or negative numbers up to about 16 digits, with or without a decimal point. You can also use scientific notation: 1.23e4 means 1.23 x 10^4^. With numbers, you can add, subtract, multiply, and divide. You can also use parentheses and you can expect JavaScript to obey the normal PEMDAS order of operations from your Algebra class. There is one more operator that frequently comes in handy called the remainder operator, or **modulo** and it is represented by the % symbol. It gives the remainder after dividing the first number by the second as follows: 5%2 is 1, 8%3 is 2, etc. You should play with these in your editor to make sure you understand how they work.

#### Strings

The second type of value is called a **string**. A string is indicated by putting quotes around something, even a number. "Red" is a string and "2" is also a string. Almost anything can be put between quotes and JavaScript will see it as a string. You can't do math with a string, but you can **concatenate** strings using the + operator as you've already seen.

But what if you need to use a string with a quote symbol inside it like:

`"The " symbol is called a double quote."`

JavaScript won't like it because it doesn't know how to interpret the three quote symbols - it is expecting only two. The way around it involves using a backslash symbol ( \ ). Notice that it is tilting the opposite direction from a division symbol ( / ) and the comment symbol (//). The backslash symbol inside a string alerts JavaScript and tells it that whatever comes right after it is special. So to fix the situation above we would type:

`"The \" symbol is a double quote."`

and it would give us what we want. You should experiment in your editor to see how it works. This process of using a backslash to get out of the normal meaning of a character and into a different meaning is called **escaping**, or using an escape sequence.

#### Boolean Values

There is another type of value called a **Boolean** value. A Boolean value can be either true or false. Something like

`3>2;`

will produce the value true and

`3<2;`

will produce the value false. The symbols < and > are called **logical** operators and they can be used with strings as well as numbers. The statement

`"Adam" < "Eve";`

will produce the value true. Why? Experiment in Repl.it to see if your reasoning is correct. There are other logical operators such as >= which is "greater than or equal to", and != which is "not equal to", and == which is "equal to". The reason for the double equal sign will become clear in the next section. Try making some true or false statements with those operators.

There are also some operations that can be applied to the Boolean values, true and false. The operations are AND, OR and NOT and their operator symbols are &&, || and ! respectively. According to Boolean logic, a statement is only true if it is entirely true. For instance,

`true && true && false && true && true;`

would produce the value false, but

`true && true;`

would produce the value true. Try some experiments with the other Boolean operators to make sure you understand how they work.

#### Type Coercion

JavaScript tries hard to make sense out of your programs, even to the point of changing the type of your values. This is called *type coercion*. For example

`"5" - 1;`

produces the number 4, which is nice because that is probably what you intended anyway, but

`"5" + 1;`

produces the string "51", which may or may not be what you wanted. This feature of JavaScript cuts both ways. Sometimes it helps you, but just as often it produces results that you didn't expect or intend and it can make it difficult to find errors in your program.

### 1.5 Questions

1.  Given that "A" < "B" is true, what about "a" < "B"? Explain. You should refer to the ASCII Code in your explanation. You may need to do some research. 
2.  Boolean values are either true or false.  Why is this especially suitable for our binary computers?
3.  Why is true && false || true; *true*? 
4.  There is another operator called typeof. The syntax is:`typeof "word";` What does it do? Give other examples with each of the other types of values described in this section.
5.  Nan error.


## Chapter 2 - Control and Structure

### 2.1 The IF Statement

We need our program to be able to make decisions based on user input or other conditions. To accomplish this, JavaScript has reserved words like if and that allow us to build in that decision making capacity. Consider the following code:

```javascript=
var birthYear = prompt("Give year of birth");
birthYear = Number(birthYear);
var age = 2015 -- birthYear;
if (age < 16) alert("You are too young to be kissed");
else alert("You are more than 16 years old.");
```

The `if` statement in line 4 sets up a decision. If ``(age < 16)`` is true, then the `alert` that immediately follow is executed. Otherwise the `alert` after the `else` statement is executed. Every `if` statement needs a **conditional** inside parentheses that is either true or false. If true, the code that follows runs, if not, then it runs the `else` code if it is present. The `else` is optional. Using the `if` statement allows the program to do different things depending on the user input. It makes the program just a little bit intelligent.

Please note that in the first line, birthYear is a string variable, but in the second line it turns into a number variable. This is OK to do in JavaScript, because it is a *dynamically typed* language, but most other programming languages are not dynamically typed, so we will usually avoid having variables switch between different types in this course.

Also note that we only use the reserved word var when we first introduce (*declare*) a variable name, never after that.

A programmer puts two glasses on her bedside table before going to sleep. A full one, in case she gets thirsty, and an empty one, in case she doesn't.

In Repl.it, open a new document and paste the previous code. Use this code as a template. Make your own variations on the program that ask the user for input and respond in different ways depending on what input the user gives. Pay attention to the location of the semicolons. The program won't work if they aren't where they are supposed to be.

Note that Repl.it is now making suggestion, highlighting, coloring and giving other clues about your code as you write it. Try leaving out a double quote. Does it notice?

### 2.2 The WHILE Statement

Another way to control programs is by using a while statement. Suppose in the previous example, we were concerned that the user might not put in a reasonable year of birth. We could use a while and an if statement combination to check and repeat until the user gave a reasonable year. For example see Figure 2.2 below.

![ Figure 1.C Repl.it sample program](https://lyndenmath.org/CSAssets/fig2.2sample.jpg "Figure 1.C")

*Figure 1.C*

Carefully type the program from Figure 2.2 into a Repl.it window. Pay attention to the colors. If they aren't similar to what is in the example, you've typed something wrong. Run the program and respond that you were born in 2016, then respond that you were born in 1776, then respond with your actual year of birth.

The first new thing you encounter in this program is the `while` loop. It is called a *loop* because it keeps looping between the curly braces { . . . } *while* its conditional statement is true. In this case, as long as the birth year the user enters is after 2015 (which is not possible) or before 1915 (which would make them over 100), the while loop will keep running. It will keep asking them what year they were born and keep converting their response to a number and putting it in the variable `birthYear`. As soon as they enter a reasonable year of birth during the last 100 years, the conditions will no longer be met and the while loop will not be executed. The program will move on to the next line which subtracts their birth year from 2015 to get their current age.

The curly braces are also new. In JavaScript if you want to group a set of statements together, you put them inside curly braces. You would typically use curly braces for `if` statements as well as shown below:

```javascript
if (school == "lynden") {
    alert("Your colors are green and yellow");
    alert("Your mascot is a lion");
}
```
Put the first { on the same line as the `if` statement as I did in this example and put the closing } on it's own line below the `if` statement. Everything between the braces should be indented. Indenting is very important for making your code readable and for helping you avoid errors. While the code will run without the indenting, it will be unacceptable, sort of like writing a letter without punctuation. The reason that braces were not needed in Figure 2.2 is that there was only a single line of code between them. It is good practice, however, to ALWAYS use curly braces, even if you have only one line of code since you will often need to come back and add more lines in. So in this respect, Figure 2.2 is an example of what not to do.

Here's another example of a while loop with proper curly brace placement:

```javascript
var counter = 0;
while (counter <= 5) {
    counter = counter + 1;
}
```
A variable called `counter` is set to 0. Then we begin a `while` loop which adds 1 to `counter` each time through the loop and outputs the value. Eventually `counter` becomes 6 at which point the loop condition is no longer true and the program is finished. If you paste this program into a webpage and run it, it doesn't seem to do anything. That's because there is no output. There is no `alert()` for instance. If you want to see the program as it is progressing, you'll need to change it a bit. Insert this line of code into the `while` loop above `counter = counter + 1`:

`console.log("Counter = "+counter);`

What this `console.log()` method does is to send the value of `counter` to the console, which means we have now designated a place for the output to go. You should see the numbers 0 thru 5 printed out for each time the program went through the `while` loop. When you want to see what is going on in a program as it progresses, the `console.log()` method is very useful.

Finally, it should be noted that if the condition of the `while` is never false, the loop will never stop. For instance in our example, if we had mistakenly written:

`counter = counter - 1;`

then `counter` would always be less than or equal to 5 and always true, so the loop would never end. This is called an *infinite loop*. Everybody writes one by accident sometime, but they should be avoided. If you create an infinite loop in Repl.it, you may be able break it by clicking the ****stop**** button, but more likely you will need to refresh the page, in which case you will lose your changes since the last save, so save often.

### 2.3 The FOR Loop

The next kind of control statement we will consider is the for loop. The for loop is a convenient way to do what we did with the previous while loop: repeat the loop with a counter determining the number of times we do it. The syntax of the for loop is as follows, according to the Mozilla Developer Network:

```
for ([initialization]; [condition]; [final-expression]) statement
```

Rather than give you a specific example of code, they've given you a general statement. As you learn to program, you'll frequently be looking up how different commands work so you'll need to get used to these general statements. But they also give you an explanation of terms and at least one example:

-   The *initialization* is where we set our counter to its starting value. -   The *condition* is where we put a conditional statement that needs to stay true for as long is we want to loop to run. -   The *final-expression* is where we add whatever we want to the counter each time the loop is completed. -   The *statement* is any single statement or set of statements { . . . } to be carried out during each loop.

```javascript
for (var i = 0; i < 9; i++) {
    console.log(i);
    // more statements
}
```
There are some new things here. Their counter is the variable i, which is a common variable name for a counter. i is short for *iterate* which means to change repeatedly. It starts out at zero and the loop will run so long as i is less than 9. Then comes i++? The *++* is called the increment operator and its effect is to add one to whatever variable it comes after, so it has the same effect as i = i + 1; This operator was developed around 1969 and is found in most computer languages related to the programming language C, like JavaScript. While we're on the topic, there is another short way of incrementing a counter:

`counter += 1;`

This statement also does the same thing as `counter = counter + 1;` and `counter ++;` The reason for these shortcuts is that incrementing counters is a common programming task. Note that statements like `i++` are falling out of favor and your code would be considered higher quality if you used the preferred `i += 1` form.

Now back to the example from Mozilla. The final surprise is the third line:

`//more statements`

The two forward slashes tell the computer to ignore anything else on that line. These lines are for human eyes only. We call them comments and we will spend more time on comments in the next section.

![ FoxTrot - Bill Amend -- Universal Press Syndicate](https://lyndenmath.org/CSAssets/nicetry.jpg "Fox Trot comic")

The [Mozilla Developer Network (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript) is a great source of information about JavaScript. Another good place is [w3schools.com](http://www.w3schools.com/js/default.asp), and you may find some other source you prefer. Get used to using a reference site because this book barely scratches the surface of all the commands available in JavaScript.

### 2.4 The SWITCH/CASE Statement

The `switch` and `case` statements aren't used for looping, rather they work like a multi-branched `if` statement. Here is an example:

```javascript
var answer = prompt("What is your favorite color?");
    switch (answer) {
	case "red":
	    alert("hearts, strawberries");
	    break;
	case "blue":
	    alert("ocean, jeans");
	    break;
	case "green":
	    alert("grass, go");
	    break;
	default:
	    alert("nice color");
    }
```
Paste it into a webpage script. See if you can predict how it will work before you run it and then run it to see if you were right. Now put a couple of forward slashes // before each of the break commands. This will turn those lines into comments which the computer will ignore and it is a quick way to turn a line off and on without retyping the whole line. Now run it with the breaks commented out. You should now be able to describe what break does. Why don't we need a break in the default section? Always make sure you include a default case to handle unexpected situations without crashing your program. If you want, you can think of a switch case as a series of if statements with default being like an else for all of the if's.

### 2.5 Commenting Revisited

Of course commenting isn't just for turning lines of code on and off, commenting is primarily to explain your code. It is important that computer programs can be read and understood at least by other people who know the particular language being used. But as our programs get more complex, grasping what the program is doing and how it works can be difficult to see. Even if you are the one who writes a program, if you return to look at it 6 months later, you might forget how it worked. It would be helpful if we had some explanatory information along with the program so that if we later need to make modifications we will be less likely to mess up something important. This is what we use comments for. Here's an example program that we will put comments into:

```javascript=
/* CS1 - 2.B.1 - Jeff Seely - 9/28/15 3 digit
 *  Armstrong numbers 
 * This program finds the 3 digit Armstrong numbers. 
 * An Armstrong number, such as 153, is a number in which 
 * each digit is cubed (1 + 125 + 27 = 153) and the sum 
 * equals the number itself.
*/

var possible = 0,
    cubedNum = 0,
    d1 = 0,
    d2 = 0,
    d3 = 0;
	
console.log("The 3 digit Armstrong numbers are:");
for (d1 = 1; d1 <= 9; d1+=1) {
    for (d2 = 0; d2 <= 9; d2+=1) {
        for (d3 = 0; d3 <= 9; d3+=1) {
	    possible = d1*100+d2*10+d3;
	    cubedNum = d1*d1*d1+d2*d2*d2+d3*d3*d3;
	    if (possible==cubedNum) {
		console.log(possible);
	    }
	}
    }
}
console.log("done");
```
At the top of the program is a heading set off by /* and \*/ marks. This is one way to set off a comment. The computer ignores anything between /* and \*/ no matter how many lines it takes. This is the sort of heading that you will use in this course. Without the heading comment (and line 3 of the program), it would be very hard to know what this program was about. While the /\* . . . */ style comments can be used anywhere in a program, more commonly you will use the single line comments that you have already seen, where the comment line simply starts with //. Finally, you can add blank lines and indentations to make sections of the program more obvious.

The following is what a better commented program would look like:

```javascript=
/* CS1 - Jeff Seely - 7/13/15 3 digit Armstrong numbers.
 *  This program finds the 3 digit Armstrong numbers. 
 * An Armstrong number, such as 153, is a number in which 
 * each digit is cubed (1 + 125 + 27 = 153) and the sum 
 * equals the number itself. For 2 digit numbers, the digits 
 * would be squared and for 4 digit numbers the digits would 
 * be taken to the 4th power, etc.
*/

var possible = 0, //initialize variable for possible Armstrong number
    cubedNum = 0, //and the digits of the number cubed
    d1 = 0, d2 = 0, d3 = 0; //loop incrementers

//set up for the results
console.log("The 3 digit Armstrong numbers are:");

//loops for the 100s, 10s and 1s places: d1,d2,d3 respectively so
//that all three digit numbers are generated.
for (d1 = 1; d1 <= 9; d1+=1) {
    for (d2 = 0; d2 <= 9; d2+=1) {
        for (d3 = 0; d3 <= 9; d3+=1) {
            possible = (d1*100)+(d2*10)+d3;//calculate possible
            cubedNum = (d1*d1*d1)+(d2*d2*d2)+(d3*d3*d3);//calc cubedNum
            if (possible==cubedNum) {//see if they are the same
                console.log(possible);//if so, display
            }
        }
    }
}
console.log("done");
```
Clearly this commented version takes up more room and takes longer to write, but it contains useful information that helps the reader figure out what's going on. Even the addition of unnecessary parentheses in the lines calculating `possible` and `cubedNum` can make it easier for the reader to follow. But even though it takes up more space, the computer is ignoring all the extra and so the program runs just as quickly.

What do you mean it needs comments!? If it was hard to write, it should be hard to understand. Why do you think we call it code???

Another thing that you can do in comments is say where you got code from if you didn't write it from scratch. It is very common for programmers to copy and paste bits of code and one of the reasons this text is in digital format is so that you can easily do that. Trivial bits of code, say two or three lines, need not be attributed to a source, but if problems are solved and coded by someone else, you can't just copy and paste the code and call it yours. There are many law suits currently in the courts between software companies on specifically this matter. Plagiarism in programming languages is still plagiarism, and in most cases you can't use significant pieces of someone else's code without their permission even if you do credit them in your comments. In this course, if someone comes up with a nifty chunk of code that we want to make available to the class, we'll discuss it in class and agree to comment it if we use it. Otherwise, your code should be your own.

### 2.6 Nested Loops

The Armstrong number program uses what is called **nested** for loops, that is, a for loop inside of another for loop. In this case, three for loops are nested.

Can you sort out how the nested for loops work together to generate all the 3 digit numbers? Try *being* the computer and keep a list of the values of the variables as you go through each loop. Three nested loops is not very common but two loops are frequently nested. Notice that we needed to be able to cube each digit separately which lent itself to this structure. This was one possible algorithm, there are others.

### 2.7 Questions

1.  What do the different colors of words in Brackets correspond to? Refer to Figure 2.2.

3.  You've seen the increment operator ++, what do you suppose the -- operator does? Look it up using MDN or w3schools and give it's name and function.

4.  Write a program to prompt the user for a number. In response your program prints in the browser console a kitty face however many times their number was. Consider this =\^.\^= for your kitty face, but you can be creative and design your own as well. This sort of thing is called *ASCII art* and the most amazing example is probably found at [Asciimation](http://www.asciimation.co.nz/). For an extension you can try doing a kitty that is more than one line long or that uses / or \\, but you will have to read up on how to use **escape** characters.

5.  Write a program with a loop to print the following design in the Pico/WIDE console:

	?

	??

	???

	????

	?????

5.  JavaScript has very few mathematical operators. It has no power operator (\^), no factorial operator (!) and no square root (√), for instance. Write a looping program that uses the operators from section 3 to calculate the factorial of a number provided by the user. The result should be displayed in the console. Factorial, as you may remember, is calculated by multiplying together all the numbers less than or equal to the number given. For instance, 5! = 5 x 4 x 3 x 2 x 1 = 120.

7.  An infamous programmer interview question is called Fizz Buzz. The prospective employee is asked to write a program that prints all the numbers from 1 to 100 in the console, with three exceptions. For numbers divisible by 3, print "Fizz" instead of the number. For numbers divisible by 5 (and not 3), print "Buzz" instead. For numbers that are divisible by both 3 and 5 (like 15), print "Fizz Buzz". *Hint: use looping and the % operator from Section 1.C. If you are successful, just maybe Google is looking for you.* 

8.  Write a program to prompt what a user's favorite day of the week is and to respond to that information in some day-specific and sensible way using a switch case statement.

9.  Write a well commented program to print to the console all the 4 digit binary numbers in order, along with their decimal and [hexadecimal](https://learn.sparkfun.com/tutorials/hexadecimal) equivalents on each line. You can use whichever console you prefer. The output should look something like this:

		0001				1				1
		  .
		  .
		  .
		1011				11				B
		1100				12				C


### 2.8 Simple Function

In JavaScript, a function is commonly used to group together a set of statements that accomplish a task. Once the function is written it can be used anywhere in the program that it is needed by just *calling* its name instead of rewriting the code every time. As with loops, we have parentheses and curly brackets.

```javascript
var square = function(x) {
    return x * x;
};
console.log(square(12));

>>144
```

The function has been assigned to the variable square and we created (*declared*) it just like we do with variables, but instead of assigning the variable a number or string value, we assign it a function. This syntax is called a *function expression*. The function itself, in this case, has no name. It is said to be an *anonymous function*, but since we assigned it to the variable square, we can refer to the anonymous function as square. This is not the only syntax we can use to declare a function, but it is the one we will most commonly use in the first half of this book. The keyword function requires parentheses and inside the parentheses is a variable that will contain the value that the function will work on. This variable is called a *parameter*. In this case, we are going to *pass* the value 12 into our function and it will take the 12, assign it to the variable x and then multiply x by x, which in this case is 12 times 12. The keyword return determines what the value of the function will become when the function is finished. In this case, the function will become x times x or 144 which is then assigned to the variable square. Functions can contain as many statements as needed within the curly brackets. If no value is given in the return statement, or if there is no return statement, the value of the function will become undefined. At whatever point the return keyword is encountered, the function is exited, so be careful where you put return.

The following example shows how we could use our square() function multiple times in one program:

```javascript
var square = function(x) { return x * x; };
len = prompt("Enter a length");
len = Number(len);
areaSquare = square(len);
areaCircle = square(len)\*3.14;
alert("Area of square = " + areaSquare);
alert("Area of circle = " + areaCircle);
```

By writing our function for squaring, we can use it to calculate the area of a square and the area of a circle without rewriting the code in the function. While the amount of code in our function is trivial, the idea is easy to grasp. If we had a 30 line algorithm that we needed to use a dozen times in our program, writing a function would be very efficient.

Functions can have more than one parameter and can contain loops or any of our other programming components, but they only return one value. Next we look at a function that takes 2 parameters and calculates powers of a given base. Can you follow how it works? Remember from math class that powers are just repeated multiplication.

```javascript
var power = function(base, exponent) {
    var result = 1;
    for (var count = 0; count<exponent; count++)
        result *= base;
        return result;
    };
console.log(power(2, 10));

>>1024
```

Remember it is good programming practice to declare all variables at the top, and this includes at the top of a function.

Try to keep in mind that a function always equals a value, or is undefined. Since a function equals a value, a function can be passed into another function as a parameter, just as if it was a value, which it is.

### 2.9 Scope & Global Variables

An important thing to note about functions is that whatever variables are declared using a `var` statement within the function only exist within the function. For instance in the previous example, the variable x only exists inside the `square()` function. Add the line `alert(x);` at the end of the program. While the value of x should be whatever you typed into the prompt, JavaScript tells you it is undefined. On the other hand, if you put the `alert(x);` line inside the function, it gives you the information you expect. Why do you have to put the `alert(x)` before the `return`? The part of a program where a variable is available is called its *scope*. The scope of a variable declared inside a function is the function itself. It is not available outside the function. If you need multiple functions to have access to a single variable you can pass that variable around as a parameter. This is the preferred strategy, however sometimes it is simpler just to declare the variable outside of all of the functions. These sorts of variables that are available to all the functions are called *global* variables. It is common to put the names of these global variables in all caps. We will make use of global variables later when we do some simple animations.

Using global variables is considered something to be avoided, particularily if more than one programmer is involved. Programs often get changed and have bits of code added from numerous sources. You can imagine that it would be easy for different programmers to use the same variable name and if those variables are globals it would likely break the code. The way we avoid global variables is by wrapping most of our final code inside a function statement. We control the scope of our variables by wrapping them in functions. Note that it is not the curly braces that control the scope, it is the function statement itself. The curly braces inside a `for` or `while` loop do not restrict the scope of a variable declared inside them.

One final note about global variables. If you declare a variable without using `var`, that is, if you just start using a variable without formally declaring it, JavaScript makes it a global variable. This is true even inside of a function. Since this would produce very unpredictable behavior, you should ALWAYS make sure to declare variables with a `var` statement.

Another interesting property of functions is that they can call themselves. This is called *recursion*. For instance, the following function calculates the factorial of the number passed as its parameter.

```javascript
var factorial = function(num) {
    if (num == 0) return 1;
    else return (num * factorial(num - 1));
};
var result = factorial(6);
console.log(result);

>>720
```

While recursion is a useful and common technique, there are some potential memory problems with its current implementation in JavaScript so we won't be working with it further. These problems are likely to be addressed in future versions of JavaScript.

### 2.10 Methods

In JavaScript, *methods* and *functions* are very similar. While they both have attached parentheses, the most apparent difference is that methods have a dot in the name as in the `console.log()` method. We have already been using several methods: `console.log()`, `window.alert()` and `window.prompt()` although the window part hasn't been necessary for our previous uses. The words to the left of the dot give us additional information about what sort of method it is and are usually necessary for the proper function of the method. The `log()` method belongs to something called the console object and the `alert()` and `prompt()` methods belong to something called the window object. Objects will be one of the topics of Chapter 3.

There are many built in methods in JavaScript, in contrast to relatively few built in functions. Functions are mostly custom written by programmers whereas most programmers make considerable use of built in methods. In our exploration of built in methods we will begin with Math.methods.

### Math Methods

It would be a pain if we needed to create all the normal math functions like powers, roots and trig functions by writing our own functions using only arithmetic operators. Fortunately there is a nice set of math methods that we can call whenever we need them. Below is a sample of some of the most commonly used math methods. Many more are available. If you need something that isn't listed, look it up and it will probably be there.

**Math.abs(x)** Returns the absolute value of a number.

**Math.ceil(x)** Returns the smallest integer greater than or equal to a number.

**Math.cos(x)** Returns the cosine of a number.

**Math.floor(x)** Returns the largest integer less than or equal to a number.

**Math.pow(x, y)** Returns base to the exponent power, or xy.

**Math.random()** Returns a pseudo-random number between 0 and 1.

**Math.round(x)** Returns the value of a number rounded to the nearest integer.

**Math.sqrt(x)** Returns the positive square root of a number.

**The Math.random()** method is often used in games to simulate dice, spinners, cards or any other random element of a game. Let's start with flipping a coin.

```javascript
var flip = function() {
var coin = "idle";
if (Math.random() > 0.5) coin = "heads";
else coin = "tails";
return coin;
};

console.log(flip());
```

Since the `Math.random()` method generates numbers between 0 and 1 and we need to split them into two equal groups, we can just check to see if they are greater or less than the half way point of 0.5. When we call the `flip()` function, coin is returned to us with a value of heads or tails. In this case, we don't need an argument since we don't need any information from the user for the function to work.

![XKCD #221](https://lyndenmath.org/CSAssets/xkcd.png "XKCD #221")

Try out some of the other Math methods in your editor to see how they work. Make sure you capitalize the M in Math.

### String Methods

Another set of built in methods are available for working with strings. A sampling of some of the many methods available are listed:

**charAt()** returns the character at a specified index. The index of the first letter is 0, the second letter is 1, etc.

**charCodeAt()** returns the Unicode value of the character at the specified index.

**indexOf()** returns the index of the first occurrence of the specified character, or -1 if it doesn't occur.

**slice()** returns a string from the first index up to but not including the second index.

**substr()** returns the characters of a string beginning at the specified index and continuing through the specified number of characters.

**toUpperCase()** returns the string in upper case.

Some of the methods like `toUpperCase()` have no arguments, while others like `charAt()` require one argument, and others like `slice()` require two. Next is some example code to demonstrate the syntax:

```javascript
var myString = "JavaScript";
console.log(myString.toUpperCase());
console.log(myString.charAt(2));
console.log(myString.slice(4,9));

>>"JAVASCRIPT"
>>"v"
>>"Scrip"
```

Try the other string methods in your editor to see how they work. You may need to look some up.

### Number Methods

In addition to the Math methods, there are also a few Number methods that take numbers as parameters and do something with them. For instance the `isNAN()` method returns true if the parameter is Not A Number. The `toString()` method turns a number into a string. You should take a look at a list of number methods so you have an idea what is available. They come in handy from time to time.

### String & Math Properties

Along with methods, we have properties. Properties are different from functions and methods in that they don't act on anything, they don't process data, rather they simply report on something that already exists. Properties don't have arguments. For instance we have the string property `.length` and Math properties `.PI` and `.E` with syntax as follows:

```javascript
var myString = "JavaScript";
console.log(myString.length);
console.log(Math.PI);
console.log(Math.E);

>>10
>>3.141592653589793
>>2.718281828459045
```

Try to keep in mind that JavaScript is *case sensitive*, that is `Math.PI` is not the same as `math.pi`. The first way works, the second way produces an error. As we will see in the next chapter, other languages, like HTML, are not case sensitive. These differences just mean you have to pay attention.



### Section 2.11 Questions

1.  Write a function that calculates the factorial of a number passed to it. Write it using the Pico and call the function with a console.log. After you have a working function, you can call it directly on the black side of the editor. Try it with several numbers. Do not use recursion in your program. 
2.  Using a webpage, write a function to roll 1 die that randomly returns a number between 1 and 6 to the console. 
3.  Use your function to write a program in which the user sees the value of each of two dice that are "rolled" in an alert() and then the program tells the user whether they win or lose. A win happens if the user rolls doubles, or some other combination that you specify. Put the rules to the game on an alert at the beginning and make sure that it isn't too hard to win or nobody will get addicted to your game and you won't make megabucks.
4.  Add to your dice game by asking the user for their first and last names in a prompt(). Then use string methods so that your program can refer to them by either their first name or their last name in some of your output. 
5.  Leet originated as a letter substitution system employed by computer bulletin board users, but now in various forms it is common in all sorts of text based communication from phone texting to graffiti. A few simple examples would be to substitute @ for A, 3 for E, 6 for G, \$ for S and + for T, yielding words like 6@\$ and \$33LY. Using at least the 5 substitutions given, make a Leet translator that prompts a user for a phrase and returns the phrase in Leet and all caps. You will need to use string methods and program control structures. A fuller implementation of a Leet translator can be found [here](http://www.albinoblacksheep.com/text/leet). 
6.  Research the Caesar cypher and see if you can make an encoder and decoder. 
7.  Write a program to find and list all the 3 digit happy numbers. Note that the calculation of the 3 digit happy numbers will never require more than 3 digits. Be careful of the 0 case.

![Dr. Who "42" Season 3 Episode 7](https://lyndenmath.org/CSAssets/who3.jpg "Dr. Who")

Relevance: Dr. Who once needed 4 happy numbers to save a spaceship from crashing into a star!

