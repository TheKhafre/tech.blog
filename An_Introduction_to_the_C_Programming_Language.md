---
title: "An Introduction to the C Programming Language"
seoTitle: "how to code in C programming language"
seoDescription: "learn the beginner practice on how to code with the C programming language. explore the syntax, and structure of C language."
datePublished: Fri Jul 07 2023 08:52:38 GMT+0000 (Coordinated Universal Time)
cuid: clkax01f9000q09mq2ej118wd
slug: an-introduction-to-the-c-programming-language
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/z5bgBKdTRA4/upload/beca4824f5ca1efde5c8fd376cd0b6c7.jpeg
tags: c, beginners, programming-languages, technical-writing-1, programming-tips

---

```c
#include <stdio.h>

int main(void)
{
    printf("hello world!\n");
}
```

Before I jump right into it, here are a few things you need to know instantly:

* C is a compiled language
    
* C is a low-level language
    
* C is a support language
    
* C is case sensitive
    
* It has just 32 keywords
    

Now, let's get into it!

## C Process:

The C Programming language (as mentioned earlier) is a compiled language i.e. this language requires you to first write your code in a file (also known as a source and ends with a .c). Once you're done writing your code in this file it will then be passed to what is known as a compiler which will now produce a new executable file.

However, the process of C file compilation passes through a few crucial steps which are described below.

**Preprocessor**: the preprocessor imports the header file into the code to run the important functions we might be using in the code (such as scanf, printf, getchar, putchar etc) and then turns the source code to a `.i` file.

**Compiler**: the first thing the compiler looks for is syntax error i.e. is there any error in the code? are the syntaxes correctly written? Once all these conditions have been met, the compiler then begins an extensive compilation process by parsing it to the assembler.

**Assembler**: the assembler is a packager i.e. it packages the code into a format that is readable for the machine which is basically 1s and 0s. Once this assembling process is completed, it turns the code into a .obj file which is a format the machine can now read to understand your code. However, in some machines like Windows, the object file is created on the system alongside the executable file. whereas, in some others such as Ubuntu (and other Linux machines) this .obj file is merged with the executable.

**Linker**: Just as the saying goes that "C is machine dependent programming language" i.e. although all C source code can work on all machines, the executable files are machine specific. what this essentially means is that the executable file from a source code compiled on Windows can not work on another machine that is not Windows. Whereas, same goes for those compiled on other machines as well.

Technically, the linker is the last point of compilation for a c program, however, the machine still checks two other processes.

**Execute Process**: once the compilation is completed, the program can now be used. however, whether or not it will work as intended is dependent on two conditions; Logic error (an error in the writing of the conditions of the code) or Data error (error from the data the user enters at a run time e.g typing an integer where a character is expected).

**Output**: Now, this is the final stage where the result is given after it has satisfied all the required conditions to make it work well.

## C Fundamentals

### **Header**

Header files are the files containing the meaning of the important functions which will be used in the code. the most popular and important header file in a C program is the "`#include <stdio.h>`". This header file is particularly important because it helps out with the input and output functions in the program by handling functions such as the printf, scanf, gets, getchar, putchar etc.

### Format Specifier

When printing output to the console using a formatted input and output, there are some special characters that we can use to specify the kind of output or input format we want. some of the most common and rather more important specifiers include:

`%d` = int i.e whole numbers (e.g 1, 2, 3 etc);

`%f` = float (0.2000, 2.670000 etc);

`%c` = char ('a', '1', ' ');

`%s` = string ("tobiloba");

`%x` = hexadecimal

### Comment

***Single-line***: for single line comments, we use a double forward slash //

***Double-line***: multiline comments are used for writing more than one line of comment. for multiline comments, we use a forward slash followed by a star and when we are done with the comment, we end it with a star followed by a forward slash (`/* COMMENT ON MULTIPLE LINES */`).

***Tip***: Here is the format for writing a betty compliant comment; you can just edit accordingly to your preference:

```c
/**
* main - you can write anything here
* Description: a brief description of the project
* Return: 0 (this is the most common return type)
*/
```

### Main

In C, the main section is where your code starts from i.e. the compiler understands the code statements within the "int main(void)" as the most important blocks of code. PLEASE NOTE: everything written before the main block is known as global code therefore, if a variable is declared before the main block, it will be known as the global variable which can be used everywhere within the code.

### Return

this is simply a statement of what happens to the code you want, let's simply call it a status report. therefore the success is mostly attributed to zero, and all unsuccessful code processes are attributed to a non-zero return type.

### Variable

Variables are simply containers in all programming languages (C inclusive). In C, variables are used to store data both during compilation and run time. To declare variables in C we follow the simple format as follows:

`datatype variable_name = value`;

e.g

```c
int age = 29;
```

A variable can be declared uninitialized i.e. you can declare a variable at compile time without assigning value to it yet and let the user decide the value. here is a code example of how to do that:

```c
#include <stdio.h>

int main(void)
{
    int age;
    
    printf("please enter your age:\t");
    scanf("%d", &age);

    printf("you have entered %d years\n", age);
}
```

What we simply did was that we declared a variable name age with type int (i.e. we want the user to enter a number) and then told the user to enter their age using the printf function.

The scanf function is used to save whatever the user entered in the variable we declared before i.e. age. however, to save something into a variable during run time, we need to use the `&` symbol followed by the variable we have declared. what this means is that when we declared the variable, we gave it a memory location and told it that we will be saving an int into it. So, by using the ampersand (i.e &) we told the computer to look for wherever we have saved the variable and now save the data the user entered into it.

### Datatype

The following are the most popular data types in C and the memory/space they take up in C:

* int (4bytes);
    
* char(1byte(s));
    
* float (4bytes);
    
* long(8bytes);
    
* double(8bytes);
    
* Long double(16bytes)
    

### ASCII

I really don't know how to explain this but, there is something called ascii table that assigns number to all the supported characters in C. This is essentially important to know for use with character datatype and other important functions.

This is not even up to 2% of everything in C, this is just to get you started. I'll advise you to take your time to read more on this for more understanding of the immense power of the C programming Language.

*with love,*

Oluwatobiloba Ezekiel ([Khafre](https://github.com/TheKhafre))
