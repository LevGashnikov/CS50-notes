## C
**Source code** - it's a code, that we, humans, can understand with some training and some practice. A special program, called **compiler**, transforms source code into **machine code**, or **binary code**. Compilers are built-in **Graphical User Interface (GUI)**, such as **VS Code**, Wing or PyCharm.
There is a terminal inside them, generally known as **Command-Line Interface (CLI)**
Here goes an example of code in C:
`#include <stdio.h>`
`int main(void)`
`{`
    `printf("hello, world\n");`
`}`
It must be written in **GUI**, but if you want this code to work you have to write
`make hello` in **CLI**. This command activates compiler, and after you need to write `./hello`
to activate whole program.
## Libraries
**Header files** - files that end with **.h**, and contain code written by other people for you to use in your own programs. Such files are collected into **libraries**. To connect library to your program you can use `#include <library>`, as we did before. CS50 has its own manual page for libraries to use: https://manual.cs50.io/, where you can find almost all useful libraries. 
One of the most common and frequently used things in coding are **functions**. They are stored in **libraries**, but they also can be created by your hands, using another function. Here are some examples of functions:
`printf()`,`scanf()`,`getchar()`, etc. As we can see functions are always used with ().
Let's talk about **CLI**. There we use special funny commands that help us to interact with our device and operating system:
#### For interacting with files
**`pwd`** - show current folder  
**`ls`** - show files in current folder  
`**cd folder**` - go to folder  
**`cd...`** - go up a level  
**`mkdir`** - make a directory(a new folder)
**`rm`** - remove a directory or a file
**`mv`** - move a file
**`cp`** - copy a file
**`touch`** - create a file
#### For interacting with your code
**`make hello`** - compilate **hello.c** 
`**./hello**` - run the program **hello**  
#### For CS50 only
**`check50` ...** - check the solution
**`submit50` ...** - send the solution
#### For VS Code only
**`code hello.c`** - open file in VS Code
One more thing: after you run **make hello**, thereby compiling the code, the **compiler** creates one file, **hello**, but without the **.c** extension in the end. Please, don't confuse executable **hello** with source code file **hello.c**.
## Conditionals in C
Conditionals are essentially Boolean expressions, complicated and long, but they are. Here goes an example: 
`if (x < y)`
`{`
	`printf("x is less than y\n")`
`}`
`else`
`{`
	`printf("x is not less than y")`
`}`
## Variables in C
Variables are named locations in memory, used to store data. There are a lot of different types of them. Here they go:
**`bool`** - stores either `true` or `false` - we usually use true/false.
**`char`** - variable stores **one character** - `%c`
**`double`** - stores a floating-point number. It uses **64 bits** and provides greater precision and a much larger range than `float` - `%f`
**`float`** - stores a floating-point number. It uses **32 bits** and provides less precision and a smaller range than `double` - `%f`
**`long`** - stores an **integer** with a larger range than `int`. It is used when `int` is not large enough. - `%li`
**`int`** - stores an **integer (whole number)**. It typically uses **32 bits.** - `%i` or `%d`
**`string`** - stores a **sequence of characters (text)** - `%s`
## Loops in C
Loop is a structure that **repeats a block of code**. Here are some of the **most popular and basic loops**, which are used everywhere.
#### `For` loop
Used when **we know how many times the loop should be repeated**
`for (int i = 0; i < 5; i++)`
`{`
    `printf("hello\n");`
`}`

`int i = 0` - countdown **begins with 0**
`i < 5` - countdown **continues until it gets to the 5**
`i++` - **step** when counting
#### `While` loop
Used when **we don't know how many times the loop should be repeated**
`while (x > 0)`
`{`
    `printf("%i\n", x);`
    `x--;`
`}`
#### `Do while`
Used when **we don't know how many times the loop should be repeated**, but we know that it should be repeated **at least one time**
`do`
`{`
    `printf("Try again.\n");`
`}`
`while (answer != 'y');`

Also there are some special constructions, called **keywords** used in language.
**`break`** - ends **the loop immediately**
**`continue`** - ends **iteration immediately**
**`void`** - later
One more interesting fact - do, while, if, etc. - are **all keywords**! And there are one more **extremely interesting and important fact** - if you **declare a variable inside the loop, it exists only inside that loop.** So you need do declare your variables outside the loop?=, if you want to use it not only in the loop

## Void
When you use **keyword** **`void`**, you literally **transform all your code written between `{}` into a function**. It is **only one of the keywords** that transform code into function. Now it sounds weird, but in a few weeks everything is going to be clear.
`void hello(void)`
`{`
	`printf("meow\n");`
`}`
**`void`** - means that it returns nothing
**`hello`** - name of function we just created
**`(void)`** - means that it takes no inputs
And the function i just created literally **doesn't take any inputs, and it doesn't return anything - it just print `meow` on the screen** - it is called **side effect function**.
## (int n)
**If you want your function to be able to take an input - you have to use `(int n)`**
`void hello(int n)`
`{`
	`for (int i = 0; i<n, i++)`
	`{`
		`printf("meow\n");`
	`}`
`}`
**`void`** - means that it returns nothing
**`hello`** - name of function we just created
**`(int n)`** - means that function take an input
## Prototype
If you want to use your own function you have to define it above the code, where you use it. BUT! To avoid cluttering the code, you can put `void hello(int n)` above the code, and the body of `hello` under the main function.