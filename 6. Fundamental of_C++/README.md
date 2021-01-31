
Material retrieved from [Udacity.com](https://classroom.udacity.com/courses/ud210/lessons/1343a461-102f-41e1-b505-bf9ec62f427b/concepts/b1e0db7a-619e-4f23-a30d-b505d84ae3bc)


## C++ Preprocessor Directives and the main function

Each C++ program consists of two parts: the preprocessor directives and the main function. 


    #include <iostream>

    int main() 
    {
        std::cout << "Hello world, I am ready for C++";
        return 0;
    }

The first line we encounter has a hash at the start of the line. Any line that has a hash sign at the start is a preprocessor directive.

    #include <iostream>

After the hash sign we have the word include. There are several preprocessor directives available in C++, but include is the one we see and use the most often.

Include means add the declarations of the given library. In this case we are adding the declarations of the iostream library.

The final detail of this line …. The brackets..

The brackets say “Look for this file in the directory where all the standard libraries are stored”. C++ also allows us to specify the library name using double quotes.

    #include "main.hpp"

The double quotes say “look in the current directory, if the file is not there, then look in the directory where the standard libraries are stored”.

If we change the brackets to double quotes, for this case, the program still compiles. We will see later in the course a situation where using the correct enclosure (Brackets or quotes) makes a difference.

The next section is the main section of the program. We will discuss this in more detail in the next concept.

    int main() 
    {
        std::cout << "Hello world, I am ready for C++";
        return 0;
    }

## How to use comment in C++:
- Comment is used to show how code is done not why it is done.

 Comments can be added in two ways:
As a comment block
As a single line
In the next node you will see the prompt for a "Hello World" program.

The prompt is enclosed in the symbols: '/*' and '*/'. This is how we signify comment block. For example:

     /*The start of a comment block.
     Everything between "/* "and " */ "
     is in the comment block.
     The end of a comment block.*/
For this course we are adding asterisks for each line of the comment block. It is not necessary, but we think it draws your attention to the comment block.

For example:

/*write a C++ program that outputs the following statement:
*** "Hello world, I am ready for C++"
*/
A comment can be added as a single line by preceding the comment with two slash marks.

For example the code snippet below has two comments. Each comment begins with two slash marks. :

int main()
{
    int year = 0;
    int age = 0;
    std::string name = " ";
    //print a message to the user <- this line is a comment
    std::cout<<"What year is your favorite? ";
    //get the user response and assign it to the year<- this line is a comment
    std::cin >> year;
    ...

## Progamming

### C++ Style Guide

As with all programming languages, there are many different ways to style the code we write. For this course, we are not using a standard style. We are trying to remain consistent throughout the course, while making the codes as readable as possible.

There are a number of style guides available, the best one is the one used by the people who are paying you.

A straightforward style guide is:
               [Modern C++ Coding Guidelines](https://github.com/Microsoft/AirSim/blob/master/docs/coding_guidelines.md)

For a more detailed guideline:
               [Google C++ Style Guideline](https://google.github.io/styleguide/cppguide.html)

### The g++ compiler:


    g++  main.cpp -o main.out

G++ for the C++ compiler. The file name is main.cpp. -o is for the name of the output. Main.out is the name of the output.

To run the output file, main.out.

We run:

    ./main.out

### Using namespace std

    using namespace std;
    int main()
    {
    }
This tells the compiler to assume we are using the standard library, so we don’t have to write std::

### sizeof
For this programming assignment, you will be printing the size of different variable types. As with other programming languages, the size a variable is allocated in memory is dependent upon its type. To determine how many bytes each variable type uses, C++ provides the function sizeof(variableType).

You will use the command :

    sizeof(variable type) ie: sizeof(int)
When printing out the variable types, you may want to print them out, one per line.
To do this, add "\n" or "endl" to the end of the text to be printed.
For example:
This is the new line character.

    cout<<"int size = "<<sizeof(int)<<"\n";
A second option is:
"endl"

    cout<<"int size = "<<sizeof(int)<<endl;
In many instances endl and "\n" will perform the same function. There are cases where they will be different.
You can read a quick discussion about their differences here:
newline and endline differences

Go here to get more information about [sizeof](https://www.tutorialspoint.com/cplusplus/cpp_sizeof_operator.htm)