---

</p>
<p align="center">
<img src="https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/159025572_1135466283557135_3615568362222306434_n.jpg" width="500">
<p/>

---

</h3>

<p align=center>

</p>
<i>"The world, even the smallest parts of it, is filled with things you don't know."</i>
</p>

---

## Summary


- <a href="#1337">1337</a>
- <a href="#libft">libft</a>
- <a href="#coding">Coding</a>
- <a href="#Webdev">Webdev</a>
- <a href="#Robotics">Robotics</a>
- <a href="#Security">Security</a>
- <a href="#News and Articles">News and Articles</a>
- <a href="#Linux">Linux</a>
- <a href="#Useful Github Repos">Useful Github Repos</a>
- <a href="#Fun Stuff">Fun Stuff</a>

---

## 1337

---

</p>
<p align="center">
<img src="https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/accretion-disk-black-hole-diagram-NASA.png" width="500">
<p/>

----

There are no teachers but a pedagogic team that ensure that students do not harm the material and provide a cursus syllabus to follow. What is learned is hence mainly achieved through peer-to-peer project review and [RTFM](https://en.wikipedia.org/wiki/RTFM).

![RTFM meme](https://i.kym-cdn.com/photos/images/newsfeed/000/017/668/Mao_RTFM_vectorize_by_cmenghi.png?1318992465)

---

### 3 Mandatory tips to succeed in 1337 :

> 1 - WORK AND DUNNOT LET THE BLACK HOLE ABSORB YOU.

> 2 - WORK MORE, WORK EVEN MOAR!

> 3 - RTFM. (READ THE FUCKING MANUAL).

---

## Libft

---

### :coffee: Artistic view of your LIBFT :

---

</p>
<p align="center">
<img src="https://www.iamsterdam.com/media/locations-ndtrc/museums/rijksmuseum-library-cc-bynd-20-hans-splinter-via-flickr.jpg?w=977" width="800">
</p>

---

### Subject :

---

:book: [ENGLISH PDF](https://github.com/alaamimi/LIBFT-42/blob/main/en.subject.pdf)

---

### :information_source: What exactly is LIBFT ?

---

</p>
<p align="center">
<img src="https://github.com/ablaamim/libft/blob/main/ressources/Libft.png" width="500">
</p>

---

>This project aims to code a C library regrouping usual functions that you’ll be allowed to use in all your other projects.

---

## ~ Coding simple C programs / General knowledge with examples :

> **시작이 반이다** ― *The beginning is half of the way (Korean proverb)* 

### First by installing a C compiler on your computer

* On Windows it is a bit tricky, you will have to install [Mingw](http://www.mingw.org/)
* On Linux it is pretty straightforward since it is only installed and if not ```apt-get``` will make it easy.
* On MAC it is not much more difficult, i will mention it bellow.

---

### Structure of a code in C

* C code is written in a file with the extension .c . It can be modified with any text editor ( emacs , vim , etc).
* C code is executed by following line-by-line instructions in functions .
* A function consists of several parts:

> Declaration of the variables used

> Instructions

> Value returned at the end of the function (optional)

> The first function called is the main function . There must always be one in a C program.

> A function is declared as follows:

```c
	type_of_returned_variable 	function_name ( type_argument1 name_argument1 , type_argument2 name_argument2 )  
	{
		statement1;
		statement2;
		statement1;
		statement2;
		return (return_value);
	}
```

* A function can call other functions in one statement:
```c
		return_value = my_function(argument1, argument2);
```
* The "return" statement returns a value and stops the execution of the function. If we put instructions after a return, they will never be executed.
* A function must be declared before it is called. So the main must be at the very bottom of the file.

---

### C Data Types

Instructions use variables.
These variables have types allowing to define their size (in bytes).
In a variable, we can only store a number, whose lower and upper limit depends on the type.

* I will only list the main ones :

|Data Type|Bytes|Description|
|-|-|-|
|char|1|Used for text
|bool|1|Used to return true or false, you will need the header <stdbool.h>
|short|2|Half the size of an integer, used to optimize memory
|int|4|Loop Counter, operations on integers
|long|8|Twice the size of an integer, used when overflow is a problem
|float|4|Used for computer graphics
|double|8|Used for computer graphics, more precised than float but takes more memory
|unsigned|.|Apply to char, short, int and long, means than it cannot have negative values

(This table is not necessarily correct, it depends on the architecture of your machine. It is, for example, not valid in 64 bits.)
* char, short, int, long and their respective unsigned can only contain integers (2, 6, 42, 254, ...).
* float, double and long double can contain floating point numbers (2.0, 6.21, 42.5694, -3.457, ...).
* The keyword void signifies the absence of a variable, for example, if a function returns nothing or if it does not take a parameter.

* There are pre-defined types that have a name allowing you to know their roles.
For example, size_t contains the size of an array (see what an array is later.)
ssize_t will be used to iterate over an array.

* To use a variable, you must declare it by giving it a name:
```c
	type 		name ;
```
* In a function, we declare all the variables before using them.
Function names should contain only lowercase letters, numbers, and underscores ("_").
They must be in English and self- explanatory . Thanks to the name of the variable, we must understand what it contains, what it is used for in the program.
The variable name i is often used for a counter.
* Variables are internal to functions. A variable declared in a function does not exist anywhere else than in this one.
* It is possible to declare so-called global variables by declaring them outside of any function. It is not recommended, it is better to avoid them as much as possible.

#### An example...

... is better than a long speech!
```c
	int subtraction ( int  a , int  b )
	{
		int 	result;

		result = a - b;
		return (result);
	}

	int main ( void )
	{
		int	i;

		i = 3;
		i = i + 5;
		i = subtraction(i, 2);
		return (0);
	}
```

#### Here's what's going on here :

* The program begins its execution with the main function (it takes no parameters).
* In it, we declare a variable of type int and name " i ".
* We then assign a value to the variable i using the " = ".
--> i = 3.
* The next statement takes the value of i (3) and adds 5 to it. It then puts that result into i, which overwrites its old value.
--> i = 8.
* The following statement calls a function to which it gives two arguments: i (8) and 2.
* We then enter the subtraction function. We see that it takes 2 arguments of int type (a and b) as parameters. That's good, that's what we sent him during the call!
--> a = 8 and b = 2.
* We then declare a new variable of type int named "result".
--> a = 8, b = 2 and result = unknown value (/!\ not necessarily = 0)
* We perform the calculation of a - b, ie 8 - 2, and we put this value in "result".
--> a = 8, b = 2 and result = 6
* The return statement returns the value of result and we return to the main function.
* The value that the function returned is placed in i.
--> i = 6. (a, b and result no longer exist: they were specific to the subtraction function).
* The main function has then completed its instructions and is therefore the last instruction that returns a value.
* The value 0 means that the execution of the program went well. Another value means there was an error.
* Now, to test this program, we will compile it and launch it. We will realize that it does not display anything.

You should then try to recode basic C functions

### Pointers

> [In computer science, a pointer is a programming language object that stores a memory address.](https://en.wikipedia.org/wiki/Pointer_(computer_programming))

**Pointer is a fundamental concept of C programming**.

**You can think of your computer's memory as a contiguous array of bytes**. Each time that you make an innocent declaration and assignation such as **`int a = 5`**, this value is written into your computer's memory on 4 bytes (integer size).
This value will be written at a specific memory address, the **stack** (fast access to memory) if no memory allocation, else it will be stored deeper in the **heap**. This address also has a value!


*Example illustrating the difference a pointer - a memory address pointing to value - and a value:*

```c
#include <stdio.h>

int main(void) {
	int a = 5;	// declaring an integer variable and assigning the value of 5
	int *ptr;	// declaring a pointer to integer
	int b;		// declaring an integer variable
    printf("ptr's value: %2d, ptr's address: %p\n\n", *ptr, ptr);

	ptr = &a;	// pointer ptr points to what is stored at the memory address of variable a
	b = a;		// b will take the value and not the address
	a = 42;		// b is still equal to 5, but ptr will return 42, which is the value now stored at a's location;
	printf("  a's value: %2d,   a's address: %p\n", a, &a);
	printf("ptr's value: %2d, ptr's address: %p\n", *ptr, ptr); // you will get the same as above, notice that you have to dereference the pointer with * to get the value, and using the pointer alone (ptr) will give you the memory address.
	printf("  b's value: %2d,   b's address: %p\n", b, &b);
	//printf("Size of ptr: %zu\n", sizeof(ptr)); // size of ptr in bytes, 8 on my system.
	return 0;
}
```

You will get this kind of output:
```
ptr's value:  1, ptr's address: 0x7ffd99493000

  a's value: 42,   a's address: 0x7ffd99492f08
ptr's value: 42, ptr's address: 0x7ffd99492f08  <-- they now match thanks to ptr = &a
  b's value:  5,   b's address: 0x7ffd99492f0c
```

**NB: On the second printf you will get the value that you got for `a`, notice that you have to dereference the pointer with * to get the value, and using the pointer alone (ptr) will give you the memory address.**


#### [About Endianness](https://en.wikipedia.org/wiki/Endianness).

Values are stored differently depending on the kind of system you are using.

Little endian means that the value is stored in memory from left to right, big endian means it is stored from right to left.

*[See this example with int a = 9](https://stackoverflow.com/questions/12791864/c-program-to-check-little-vs-big-endian/12792301#12792301):*

```
little endian: 

       higher memory
          ----->
    +----+----+----+----+
    |0x09|0x00|0x00|0x00|
    +----+----+----+----+
    |
   &x = 0xff


big endian:
    +----+----+----+----+
    |0x00|0x00|0x00|0x09|
    +----+----+----+----+
    |
   &x
```

*To find out if your system is big or little endian you can use the [following function](https://stackoverflow.com/questions/4181951/how-to-check-whether-a-system-is-big-endian-or-little-endian/4181991):*
```c
int x = 9;

if (*(char *)&x == 0x09) // we cast x as a byte to get its very first byte, it will return true (meaning little endian) if the first byte is equal to 9.
```

### ft_putchar

*A minimalist c program that will puzzle beginners, write it in a file named a.c and create a.out with ```gcc a.c && ./a.out```*

The following program will print a char by making use of [write](http://man7.org/linux/man-pages/man2/write.2.html)

```c
#include <unistd.h>

void	ft_putchar(char c) // void because the function does not return any value, it writes directly, char is the type of the variable c that is given as parameter to the function ft_putchar by the main function.
{
	write(1, &c, 1);			// ssize_t write(int fd, const void *buf, size_t count); or in human language: write count letters of buf (which is a pointer) to fd (if fd = 1 this is your terminal, stdout)
}

int	main(void)
{
	ft_putchar(42);				// will print a star
	// ft_putchar(42 + '0');	// will only print 4
	// ft_putchar("4");			// will not work, you are using " instead of ', so C language think it is a char array.
	return 0;
}
```

Once you understand well how to print a character, you should try to return the length of many together (it is called a [string](https://en.wikipedia.org/wiki/String_(computer_science)))

### ft_strlen

```c
#include <unistd.h>

int		ft_strlen(char *str)
{
	int i = 0;					// set variable i to 0
	while (str[i] != '\0')		// while the char array does not reach a NULL character
		i++;					// increment i, equivalent of i = i + 1;

	return i;					// return i variable to the caller function
}

int main(void) {
	int i = ft_strlen("1337 is the answer");	// declare i, call the function ft_strlen, and assign its output to i
	printf("%d", i); // remember that it is forbidden to submit a function with printf during the Piscine
	return 0;
}
```
*NB: remember that it is forbidden to submit a function with printf during the Piscine*

### ft_putstr

Then print a whole string by recoding the libc function 'puts':
```c
#include <stdio.h> // header for puts

int main(void)
{
	puts("1337 is the answer");
	return 0;
}
```

This can be achieve by using and index that starts on the first character and is progressively incremented until NULL as string are NULL terminated:
```c
#include <unistd.h>

void	ft_putstr(char *str) {
	int i = 0;

	while(str[i] != '\0')
		write(1, &str[i++], 1);
}
```

Along with the main function slightly modified to make use of your code:
```c
int main(void) {
	ft_putstr("You are the answer\n");
	return 0;
}
```

You can also use only the pointer since you do not care of the return value (the function type being void)
```c
#include <unistd.h>

void	ft_putstr(char *str)
{
	while(*str)
		write(1, s++, 1);
}
```

Or even use the length of the string to print the whole string at once, hence avoiding many *[system calls](https://en.wikipedia.org/wiki/System_call) (write)* that are costly for the program execution:

```c
void	ft_putstr(char *str)
{
	write(1, str, ft_strlen(str));
}
```
*NB: You have to include ft_strlen in the same file AND above the function to make it work.*

Next you should **study the different concepts in programming**, especially spend time understanding the different [C data types](https://en.wikipedia.org/wiki/C_data_types), [the concept of pointers](https://en.wikipedia.org/wiki/Pointer_(computer_programming)) and [arrays](https://en.wikipedia.org/wiki/Array_data_type), because it is what you have been using up to now and it will only get more complicated.

---

## Coding 

<p align="right">
  <b><a href="#summary">⏫ Back To Top</a><b>
</p>

#### Some quotes : 

> “Everybody should learn to program a computer, because it teaches you how to think.” - Steve Jobs, former CEO and creator of Apple

> “Any fool can write code that a computer can understand. Good programmers write code that humans can understand.” – Martin Fowler

> First, solve the problem. Then, write the code.” – John Johnson

> “Coding, it's an endless process of trial and error, of trying to get the right command in the right place, with sometimes just a semicolon making the difference between success and failure. Code breaks and then it falls apart, and it often takes many, many tries until that magical moment when what you're trying to build comes to life.” - Reshma Saujani, Entrepreneur, founder of Girls Who Code

> “Sometimes it pays to stay in bed on Monday, rather than spending the rest of the week debugging Monday’s code.” – Dan Salomon

> “Fix the cause, not the symptom.” – Steve Maguire

> “Simplicity is the soul of efficiency.” – Austin Freeman

</p>
<p align="center">
<img src="https://image.myanimelist.net/ui/_3fYL8i6Q-n-155t3dn_4hksVs3MIJxHadG7A7FI_oTy9pL-UqrC-cycJtDkuZzC" width="500">
<p/>

---

### Miscellaneous :

---

</p>
<p align="center">
<img src="https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/hqdefault.jpg" width="500">
<p/>


> In computer engineering, computer architecture is a set of rules and methods that describe the functionality, organization, and implementation of computer systems. The architecture of a system refers to its structure in terms of separately specified components of that system and their interrelationships. Some definitions of architecture define it as describing the capabilities and programming model of a computer but not a particular implementation. In other definitions computer architecture involves instruction set architecture design, microarchitecture design, logic design, and implementation.

- :computer: Computer Architecture :
  - [Computer Science From The Bottom Up](https://www.bottomupcs.com/?fbclid=IwAR1Jn989dGlZ1e6J3Fer3LA8USDpGKV29b5s1kxW5K_mbNojbqazgdAyJPI)
  - [Carnegie Mellon Computer Architecture](https://www.youtube.com/watch?v=zLP_X4wyHbY&list=PL5PHm2jkkXmi5CxxI7b3JCL1TWybTDtKq)
  - [Computer Architecture part 1 (FR)](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/Poly_Archi_1.pdf)
  - [Computer Architecture part 2 (FR)](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/Poly_Archi_2.pdf)
  - [Saylor.org CS301: Computer Architecture](https://learn.saylor.org/course/CS301)

---

</p>
<p align="center">
<img src="https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/maxresdefault%20(3).jpg" width="500">
<p/>

> If an individual wants to grow and solve projects for a team then they should be proficient in algorithms. As a developer, your everyday work is to solve problems and algorithms solve problems very efficiently. Practicing algorithms will increase you skill and your visibility at work.

- :black_nib: Algorithms and data structures :

  - [Algo visualizer](https://algorithm-visualizer.org/)
  - [MIT Open Course](https://www.youtube.com/watch?v=HtSuA80QTyo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
  - [CS50 Data Structures](https://www.youtube.com/watch?v=2T-A_GFuoTo)
  - [Algorithms part 1 ENSIAS course (FR)](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/Algo%20Cours%202018%20Partie1%20Ettalbi.pdf) : Mr. Ahmed Ettalbi is an Ensias professor, it is always okay to follow academical courses, as well as they only concern abstraction and theory (lack of practice).
  - [Algorithms part 2 ENSIAS course (FR)](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/Algo%20Cours%202018%20Partie2%20Ettalbi.pdf)

---

> Complexity of an algorithm is a measure of the amount of time and/or space required by an algorithm for an input of a given size (n).

- Complexity :

  - [Al fihriya Academy (darija)](https://www.youtube.com/watch?v=tgeF91zLMzQ&list=PLXH8lluXIxcyf5Th7tiDOL1465UJ6GvCP&index=3)
  - [A Gentle Introduction to Algorithm Complexity Analysis](https://discrete.gr/complexity/)
  - [CS DOJO](https://www.youtube.com/watch?v=D6xkbGLQesk)
  - [Orders Of growth](https://www.ccs.neu.edu/home/jaa/CS7800.12F/Information/Handouts/order.html)
  - [Know Thy Complexities!](https://www.bigocheatsheet.com/)

---

</p>
<p align="center">
<img src="https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/maxresdefault%20(1).jpg" width="500">
<p/>

<p align="right">
  <b><a href="#summary">⏫ Back To Top</a><b>
</p>

- Vim
  - [Luke smith : Vim hacking](https://www.youtube.com/watch?v=GJ_v31qktSk&list=PL-p5XmQHB_JSTaEPygu1DZjuFfb704Uv7)
  - [Missing semester : Editors (vim)](https://www.youtube.com/watch?v=a6Q8Na575qc)

---

</p>
<p align="center">
<img src="https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/maxresdefault.jpg" width="500">
<p/>

<p align="right">
  <b><a href="#summary">⏫ Back To Top</a><b>
</p>

> “Unlike most computer languages, C allows the programmer to write directly to memory. Key constructs in C such as structs, pointers and arrays are designed to structure, and manipulate memory in an efficient, machine-independent fashion.”

- C
  - [The C cheat Sheet](https://sites.ualberta.ca/~ygu/courses/geoph624/codes/C.CheatSheet.pdf)
  - [LearnC.org](https://www.learn-c.org/)
  - [Pointers : ADEI ENSIAS](https://www.youtube.com/watch?v=f8bstCNctdU&list=PLSWu0SUaMe5gppCgnnZHJh8zIGVUxyWY3) : E-lasse9 is an ensias's students initiative, it aims to simplify programming concepts.
  - [CS50 : Memory](https://www.youtube.com/watch?v=NKTfNv2T0FE)
  - [Mr. Karim Baina Prof ENSIAS : Techniques de programmation (FR)](https://www.youtube.com/watch?v=zsgMH2kVI-4&list=PLjYgQBp0uQYeXmHPqLt5TIMKYHDxiZOfR) : I highly recommend this playlist, it is purely theorical and it covers most of the basics.
  - [Mr. Jacques Olivier Lapeyre : Programmation en C inclut Gamedev SDL (FR)](http://www.multiparadigme.org/) : This is my actual mentor.
  - [C-math](https://www.javatpoint.com/c-math) : The functions defined in <math.h> header file.
  - [Stanford : Signals / Processes / Threads and multithreading / Mutex](https://www.youtube.com/watch?v=_LFGjZ0Sc6I&list=PLai-xIlqf4JmTNR9aPCwIAOySs1GOm8sQ)
  - [Unix Processes](https://www.youtube.com/watch?v=cex9XrZCU14&list=PLfqABt5AS4FkW5mOn2Tn9ZZLLDwA3kZUY)
  - [Unix Threads](https://www.youtube.com/watch?v=d9s_d28yJq0&list=PLfqABt5AS4FmuQf70psXrsMLEDQXNkLq2)
  - [Dark Corners of C : For the fun of it](https://docs.google.com/presentation/d/1h49gY3TSiayLMXYmRMaAEMl05FaJ-Z6jDOWOz3EsqqQ/edit#slide=id.gec7eb408_3500) : If you feel bored, check this out !
  - Makefile :
    - [Learn Makefiles](https://www.youtube.com/watch?v=GExnnTaBELk)

---

> The assembly language isn’t like other higher-level programming languages such as Java, Python, C#, etc. The language syntax is symbolically much close to machine code as you’re working directly with memory locations and addresses inside the processor. 
- :game_die: Assembly

 - [Assembly 68000 ENSIAS COURSE (FR)](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/Ass%20Cours%202018.pdf)
 - [Nasm Assembly](https://www.tutorialspoint.com/assembly_programming/index.htm)
 - [RipTutorial](https://riptutorial.com/assembly)

---

- :coffee: Java/JEE
  - [Paradigme Objet ENSIAS course Lecture01(FR)](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/M.2.5.1_Lec%2001_Du%20proc%C3%A9dural%20%C3%A0%20l%E2%80%99Objet.pdf)
  - [Paradigme Objet ENSIAS course Lecture02(FR)](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/M.2.5.1_Lec%2002_Concepts%20objet.pdf)
  - [Paradigme Objet ENSIAS course Lecture03(FR)](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/M.2.5.1_Lec%2003_Cr%C3%A9ation%20d_objets%20Java.pdf)
  - [Paradigme Objet ENSIAS course Lecture04(FR)](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/M.2.5.1_Lec%2004_Cr%C3%A9ation%20d_objets%20Java.pdf)
  - [LearnJAVA](https://www.learnjavaonline.org/)
  - [Mr. Toufik Zniber : Java (FR)](https://www.youtube.com/watch?v=8WY3eG68O4U&list=PLVizoH4F7kiJY8RRe0hpbBT4_AhyVgPbM)
  - [Mr. Jacques Olivier Lapeyre : Programmation Java (FR)](http://www.multiparadigme.org/)

---

- Graph Theory
  - [Don Sheehy Lectures](https://www.youtube.com/watch?v=r5qBFm6O5_4&list=PLVqjIisMyo_9h78itHVS2hZzkthxFHoT7)
  - [Ensias Course chapter 00 (FR)](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/trspeltsro09-10-ch0.pdf) Mr. MOHAMMED ABDOU JANATI IDRISSI academical course.
  - [Ensias Course chapter 01 (FR)](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/trspeltsro09-10-ch1.pdf)
  - [Ensias Course chapter 02 (FR)](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/trspeltsro09-10-ch2.pdf)
  - [Ensias Course chapter 03 (FR)](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/trspeltsro09-10-ch3.pdf)

---

</p>
<p align="center">
<img src="https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/maxresdefault%20(2).jpg" width="500">
<p/>

<p align="right">
  <b><a href="#summary">⏫ Back To Top</a><b>
</p>

- HTML/CSS
  - [The net Ninja](https://www.youtube.com/watch?v=hu-q2zYwEYs&list=PL4cUxeGkcC9ivBf_eKCPIAYXWzLlPAm6G)
  - [LearnHTML.org](https://www.learn-html.org/)
  - [Khan Academy](https://fr.khanacademy.org/computing/computer-programming#html-css)

---

- PHP
  - [LearnPHP.org](https://www.learn-php.org/)
  - [Awesome PHP](https://github.com/ziadoz/awesome-php#readme)

---

- Symphony
  - [Awesome Symphony](https://github.com/sitepoint-editors/awesome-symfony)
  - [Symphony Certification Guide](https://github.com/raulconti/symfony-3-certification-guide)

---

- JavaScript
  - [FreeCodeCamp](https://www.freecodecamp.org/learn/javascript-algorithms-and-data-structures/) 

---

- Databases
  - [LearnSQL](https://www.learnsqlonline.org/)

---

## WebDev 

<p align="right">
  <b><a href="#summary">⏫ Back To Top</a><b>
</p>

> Web development gives you the opportunity to express yourself creatively on the internet. ... Fortunately, the high demand, easy-to-learn, fun-to-experience life of a web developer is always a great choice for someone ready to have an exciting career in code.

</p>
<p align="center">
<img src="https://i.giphy.com/3o7TKEwsOvJ0niDsBi.gif" width="500">
<p/>

---

- Youtube Channels
  - [FreeCodeCamp.org](https://www.youtube.com/c/Freecodecamp)
  - [JavaScript Mastery](https://www.youtube.com/c/JavaScriptMastery)
  - [James Q Quick](https://www.youtube.com/c/JamesQQuick)
  - [Edureka](https://www.youtube.com/c/edurekaIN)
  - [DevEd](https://www.youtube.com/c/DevEd)
  - [Web Dev Simplified](https://www.youtube.com/c/WebDevSimplified)
  - [Traversy Media](https://www.youtube.com/c/TraversyMedia)
  - [Programming with Mosh](https://www.youtube.com/c/programmingwithmosh)

---

## Robotics 

<p align="right">
  <b><a href="#summary">⏫ Back To Top</a><b>
</p>

> Robotics is an interdisciplinary branch of computer science and engineering. Robotics involves design, construction, operation, and use of robots. The goal of robotics is to design machines that can help and assist humans. Robotics integrates fields of mechanical engineering, electrical engineering, information engineering, mechatronics, electronics, bioengineering, computer engineering, control engineering, software engineering, mathematics, etc.
</p>
<p align="center">
<img src="https://image.myanimelist.net/ui/_3fYL8i6Q-n-155t3dn_4mq2XAl-hbQDfittmCbnYuROq8Fs2ckcpXlCJs9-hM1b" width="500">
<p/>

---

- Youtube Channels
  - [Oujador](https://www.youtube.com/c/oujadortube)
  - [NorthWestern Robotics](https://www.youtube.com/watch?v=jVu-Hijns70&list=PLggLP4f-rq02vX0OQQ5vrCxbJrzamYDfx)
  - [Arduino Projects & Robotics](https://www.youtube.com/watch?v=pwwVOpXrazs&list=PL4g1oAdmuCfqmYvURLzVFkMMUI7839biN)
  

---

## Security 

<p align="right">
  <b><a href="#summary">⏫ Back To Top</a><b>
</p>

</p>
<p align="center">
<img src="https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/maxresdefault%20(5).jpg" width="500">
<p/>

---

- Youtube Channels
  - [The Cyber Mentor](https://www.youtube.com/c/TheCyberMentor)
  - [Stanford CyberSecurity](https://www.youtube.com/watch?v=J2txSFdQWIY&list=PLoROMvodv4rPIdnIoOMmjjxZRqM1pPkLT)
  - [John Hammond](https://www.youtube.com/c/JohnHammond010)
  - [LiveOverflow](https://www.youtube.com/c/LiveOverflow)

---

## Markdown 

<p align="right">
  <b><a href="#summary">⏫ Back To Top</a><b>
</p>

</p>
<p align="center">
<img src="https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/4be0f23a59_122541_markdown.jpg" width="500">
<p/>

---

> Markdown Articles Tool is a free command line utility designed to help you manage online Markdown documents (e.g., articles). You can download text with images using deduplication and convert to the different formats. The Markdown Articles Tool is available for macOS, Windows, and Linux. It’s written in Python — if you want to use separate functions, you can just import the package.

- Ressources 
  - [Markdown CheatSheet](https://www.markdownguide.org/cheat-sheet/)
  - [DaringFireball](https://daringfireball.net/projects/markdown/syntax)
  - [Github Doc](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

- Youtuve vids & Channels
  - [Writing beautiful readme using markdown](https://www.youtube.com/watch?v=XuPg3l6MiEk)
  - [Mise en page Markdown (FR)](https://www.youtube.com/watch?v=4lg3YyugRZQ)
  - [Crash Course](https://www.youtube.com/watch?v=HUBNt18RFbo)
  - [Memory-Helper md syntax](https://www.youtube.com/watch?v=bpdvNwvEeSE)

---

## :octocat: Git/Github 

<p align="right">
  <b><a href="#summary">⏫ Back To Top</a><b>
</p>

</p>
<p align="center">
<img src="https://octodex.github.com/images/daftpunktocat-guy.gif" width="500">
<p/>

---

- Youtube Vids & Channels
  - [Git/Github](https://www.youtube.com/watch?v=3fUbBnN_H2c) : This Video is my special recommendation to learn git.
  - [Al fihriya Academy](https://www.youtube.com/watch?v=b5J8sBlHd1Y&list=PLXH8lluXIxcwnVQhwVJlbuwhkwc0E8CBW)
- Resources
  - [Github Official Website](https://git-scm.com/)
  - [Git Cheat Sheet](https://ohshitgit.com/)

---

## Linux 

<p align="right">
  <b><a href="#summary">⏫ Back To Top</a><b>
</p>

</p>
<p align="center">
<img src="https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/maxresdefault%20(4).jpg" width="500">
<p/>

---

- Lessons & Articles
  - [ExplainShell](https://explainshell.com/) : A tool that provides good explanation to every Linux command.
  - [Bash Reference Manual](https://www.gnu.org/savannah-checkouts/gnu/bash/manual/bash.html)
  - [LearnShell.org](https://www.learnshell.org/) : Good website to learn shell scripting with exercises.

---

## News and Articles 

<p align="right">
  <b><a href="#summary">⏫ Back To Top</a><b>
</p>

</p>
<p align="center">
<img src="https://c.tenor.com/NYrgLNGuy7YAAAAC/the-c-programming-language-uncle-dane.gif" width="500">
<p/>

---

- [The Overflow Blog](https://stackoverflow.blog/)
- [MIT Technology Review](https://www.technologyreview.com/magazines/the-computing-issue/)

---

## Useful Github Repos 

<p align="right">
  <b><a href="#summary">⏫ Back To Top</a><b>
</p>

</p>
<p align="center">
<img src="https://c.tenor.com/2nKSTDDekOgAAAAC/coding-kira.gif" width="500">
<p/>

---

- [Tech Resources](https://github.com/andou/tech-resources)
- [42 CheatSheet](https://github.com/agavrel/42_CheatSheet)

---

## Books

</p>
<p align="center">
<img src="https://animesher.com/orig/1/111/1119/11198/animesher.com_book-gif-read-1119852.gif" width="500">
<p/>

---

| Book | Impression | Author(s) |
|--- |--- |--- |
| [Introduction to Algorithms](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/Introduction%20to%20algorithms%20by%20Thomas%20H.%20Cormen%2C%20Charles%20E.%20Leiserson%2C%20Ronald%20L.%20Rivest%2C%20Clifford%20Stein%20(z-lib.org).pdf) | :star::star::star::star::star: |  Thomas H. Cormen, Charles E. Leiserson, Ronald Rivest, Clifford Stein |
| [21st Century C](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/21st%20Century%20C.pdf) | :star::star::star: | Ben Klemens |
| [Computer Science Bottom to Up](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/Computer%20Science%20From%20Bottom%20up.pdf) | :star::star::star::star::star: | Ian Wienand |
| [The Linux programming interface a Linux and UNIX system programming handbook](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/The%20Linux%20programming%20interface%20a%20Linux%20and%20UNIX%20system%20programming%20handbook%20by%20Michael%20Kerrisk%20(z-lib.org).pdf) | :star::star::star::star: | Michael Kerrisk |
| [Write Great Code, Volume 2 Thinking Low-Level, Writing High-Level](https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/Write%20Great%20Code%2C%20Volume%202%20Thinking%20Low-Level%2C%20Writing%20High-Level%20by%20Randall%20Hyde%20(z-lib.org).pdf) | :star::star::star::star: | Randall Hyde |
---

## Fun Stuff 

<p align="right">
  <b><a href="#summary">⏫ Back To Top</a><b>
</p>

</p>
<p align="center">
<img src="https://github.com/ablaamim/1337-STUDENT-REFERENCE/blob/master/srcs/t%C3%A9l%C3%A9chargement.jpg" width="500">
<p/>


---

- Spotify Music Channels
  - [AngerFist](https://open.spotify.com/artist/4sQNUQjOYj9rV2sdfJ8laS?si=lU3KgaeKQqKNHyj64LhXPQ)
  - [Piano](https://open.spotify.com/playlist/2q7U9Dh7buTnrwHEWxcxiq?si=292bf27d43764565)
- Youtube Music Vids & Channels
  - [My Playlist](https://www.youtube.com/watch?v=BqnG_Ei35JE&list=PLc11zrc3DKEnLmW4jYv84KNC3Y9wk5oh-&index=1)
  - [Coding](https://www.youtube.com/watch?v=M5QY2_8704o)
    -Podcasts
  - [Geeks BlaBla](https://web.facebook.com/geeksblabla/)
  - [Al fihriya academy](https://www.youtube.com/watch?v=_T7wMjirnEk&list=PLXH8lluXIxcyUUo3NEUnY66uWEOajHE5S)

---
