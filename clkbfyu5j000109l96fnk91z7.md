---
title: "The C Programming Structure"
seoTitle: "step by step guide to write a c program"
seoDescription: "The c program is divided into different function, all of which serve important purpose. the first part is called the header section."
datePublished: Thu Jul 20 2023 17:44:00 GMT+0000 (Coordinated Universal Time)
cuid: clkbfyu5j000109l96fnk91z7
slug: the-c-programming-structure
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/m_HRfLhgABo/upload/0fdb69888fa03560427308d38625f58f.jpeg
tags: c, programming-blogs, learning, beginners, technical-writing-1

---

## Preprocessor

Preprocessors deal with the initial instruction that have been given in the code before it passes the file to the compiler. This instructions are passed in a part of the c source code known as header section (the .h section at the top of the code). To use an header file in C, we use the command `⁠#include`⁠.

The header section is a part that links to a file also known as header files. This files contain important information about the functions we will be using in the code. You are the one who understands what `printf` mean, a computer does not. However, the instructions about this function is thus contained in the header which is imported (or better said linked to) during preprocessing. 

The most popular header file is the `<stdio.h>`⁠ which directly translates to "standard input/output". This header file contains instruction for the most important output and input functiona. Notable functions in the stdio.h header file include formated and unformated input/output functions such as`printf`, `scanf`, `gets`, `putchar`⁠. To use the stdio.h header file, we write it in the first part of our code as follows:

```c
#include <stdio.h>
```

  
## Comments

```c
/*
* This code will print hello world!
* To the console (screen) using the
* printf function in the stdio.h header
* file
*/
```

Comments are instructions about what the program does and what challenge might be involved in using the code. This is not only for other developers who will be using your code, but at time to ones future self as well. 

Programming is a funny journey which means, whatever you learn today and you think you already mastered it, could pose a very serious challenge in the future. This is especially important in the future when you need to understand the reason you wrote a particular code the way you have written it.

## Functions

Functions are chunks of codes that can be used together from one single function call. One thing that makes function in C more interesting is the fact that they make our code efficient in the sense that once function are called they get freed automatically immediately after use. This method make the program runs faster and reduce clutter in our code hence making it a lot easier to read.  

In C, every program has at least one function known as the main function which is mostly written as follows:

```c
int main(void)
```

This function is where the machine enter our code. Note, most of the information written before the main function are most known as **global declarations** (we'll get to that later).  

Functions have 3 parts to it to work efficiently:  
_**return\_type**_ **funtion\_name****(**_input\_argument**)**_  
A typical example of this is the main function

```c
int main(void)
```

Which is explained as follows:

- _Return\_type:_ this is declared as an integer value (int). That is, when the program runs, it should give a status report which is represented by an integer value. Most commonly, this is usually `0 when it is successful` and a non-zero value `(1 - 9) when it is unsuccessful`_._  

- _Variable\_name:_ _main__⁠__⁠_ _⁠_is the defined standard for the beginning of the program. However, C gives us all the liberty to define our own functions as well. Which means, we can define a function and give it whatever name we so desire and prototype it to be used in our program. Note: this is a bit of an advance concept though and will be discussed later in the future.  

- _Input\_argument:_ oftentimes, you will see void in the main functions. The input argument is only useful when we have a function call that we can simply pass argument to to get a result. e.g assume we have declared a function which returns the sum of two numbers in a function declaration as follows

```c
int sum(int a, int b)
```

Now, it will make a lot of sense when we call the function and we also pass an argument to it. Assuming we want to sum two integers 5 and 6, we can use the function this way

```c
int sum(5, 6);
```

Now, this will easily return the sum of the two numbers. However, if our function is not one that returns such integer values or any other data, instead of leaving it blank it is good practice to simply put ⁠void

**

## Variables

**

The number one thing you need to keep at the back of your mind at all times is that "C has a problem ofn garbage values." Now, here's what that means. When you declare a variable in C without assigning a value to it, the compiler automatically gives it a value from the system memory. This value is what we call garbage value. For practice, go ahead and try it out with the uninitialized code below:

```C
#include <stdio.h>

/* This code will automatically assign
* A value to our variable because
* We left the variable uninitialized
*/

int main(void)
{
    int a; //declaration

    printf("the automatic value is %d\n", a);
    printf("end of program!");
}
```

The interesting thing that will happen to this code is that, even though we haven't assigned a value to a at declaration, it will still print out a value for us.

**_Let me know the value you got when you run the code._**  

In a C program, variables can be assigned a value on two ways:

1. Compile-time declaration
2. Run-time declaration  

**Compile-time Declaration** 

This is a method of assigning value directly to a variable before compilation. This can be because we want it to give a constant output at all times. However, one of the most popular way this is used is in loops. Here is an example of a loop that simply prints "hello world!" 5 times.

```c
#include <stdio.h>

/* This program will print hello world
* 5 times using the while loop.
* The code is simply an example to
* Show the working of a compile-time
* Variable declaration.
*/

int main(void)
{
    int i;
    i = 5;

    while(i > 0)
    {
        printf("hello world!");
        i--;
    }
}
```

Here are the workings of the code:

We started by declaring `i` as an integer datatype (`⁠int`⁠), then we initialized `i` with the value `⁠0`⁠. The condition of the whole loop says that while i is greater than zero it should print zero whereas `⁠i--`⁠ means that it should decrease the value of i after everytime it prints "hello world!" However, since we've initialized i with 5, this means that the condition will be true 5times.

**_Try out the code and let me know if you run into an error._**  

**Run-time Declaration**

Unlike compile time declaration, run time declaration requires just declaring the variable leaving the value assignment to the user. That is, we want the user to enter a value which will then be saved into the variable we have declared.  

To show an example of how this can be done, let's use the same example we used for compile time declaration but this time we won't give it a value. We will ask the user to enter a value which will then be saved in the variable hence the number of time the loop will print the "hello world!".  

```c
#include <stdio.h>

/* This program will print hello world
* 5 times using the while loop.
* The code is simply an example to
* Show the working of a compile-time
* Variable declaration.
*/

int main(void)
{
    int i;
    
    printf("please enter a number:\t");
    scanf("%d", &i);

    if(i == 0)
        printf("you have entered an invalid number\n");

    while(i > 0)
    {
        printf("hello world!\n");
        i--;
    }
    printf("end of loop\n");
}
```

The other additions we added to the code includes the following:

  _scanf:_ this is a formated input function that is used to save users input in a specified memory location. In this example, `⁠i`⁠ is the memory location, but to access it we need to use the "addressof" operator `⁠&`⁠.    

  _if statement:_ this is a conditional statement used to check the degree of truthfulness or false of a statement. In this program, we have passed a statement which checks if `⁠i`⁠ is the same as `⁠0`⁠.  

**Please note:** `⁠=`**⁠** and `⁠==`⁠ are not the same. The first is an assignment operator used to assign a value to a variable, while the latter is an operator used to check for equality i.e used to check if two values are the same.  

**

## Statements & Expression

**

**Formated input and output** (they use format specifier) this are the `printf` (formated output) and `scanf` (formated input). To use formated input and output, we use the following specifier according to the data type:

    `%d` for integer values i.e numbers

    `⁠%c`⁠ for character values i.e single character such as 'a' '2' '-' etc

    `⁠%f`⁠ for float values i.e numbers with point e.g 23.100009

    `⁠%s`⁠ for strong value e.g "hello world"

  

**unformatted input and output** (they only print characters values). _**unformatted output**_ functions include `putchar`, `putch`, `puts`  
**_unformatted input_**: `getchar`, `getch`, `gets`, `getc`  

## Pseudocode

Pseudocode are used to write out the logic of a program in a direct human readable language. This practice makes it easy to see error with logic and makes program order more meaningful.  

Let's work with an example pseudocode for a code that prints the multiple of 10 from a user's input:

_what the code does: multiply the users input by 10._    

1. Declare variables (let's say variable a and b)
2. assign 10 to one of the declared variable (lets say a = 10)
3. ask user for input (using printf function)
4. save user's input in the other declared variable (let's say this will be saved in b) (using scanf function)
5. multiply a \* b and save the result in a declared variable "result"
6. Prints the result on the screen.  

* * *  

lesson source code you can play around with:

```c
#include <stdio.h>

/* This code will print hello world
* Using the printf function that is
* Included in the studio.h header file
*/

int main(void)
{
    //char *a = "Moyinoluwa my sugar mommy";
    char b;
    /* int a = 10;
    int b;
    int result = 0;

    printf("please enter a number:\t");
    scanf("%d", &b);
    result = a * b;

    printf("the result is %d\n", result); */
    printf("please enter a character:\t");
    b = getchar();

    printf("you have entered %c\n, b);
    //puts (a);
}
```

  

_With love_,

Oluwatobiloba Ezekiel **(**[TheKhafre](https://github.com/TheKhafre)**)**