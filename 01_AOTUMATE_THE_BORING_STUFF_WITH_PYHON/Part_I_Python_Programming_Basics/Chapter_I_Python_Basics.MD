Py thon BASiCS
==

The Python programming language has a wide range of(多种多样的) syntactical constructions(语法结构),
standard library functions(标准库函数), and interactive development environment features(交互式的开发环境特性). 

Fortunately(幸运的是), you can ignore most of that; you just need to learn enough to write some handy(方便的 ) little programs.

You will, however, have to learn some basic programming concepts(概念) before you can do anything. 

Like a wizard-in-training(翻译结果), you might think these concepts seem arcane and tedious(神秘而乏味), 
but with some knowledge and practice, you’ll be able to command your computer like a magic wand(魔法杖) to perform incredible feats(完成惊世壮举).

This chapter has a few examples that encourage(鼓励) you to type into the interactive shell, 
which lets you execute Python instructions one at a time and shows you the results instantly(立即).

Using the interactive shell is great for learning what basic Python instructions do, so give it a try as you follow along(当你往下看的时候都尝试一下).
 
You’ll remember the things you do much better than the things you only read.(做过的事情比只是简单的看更能深入记忆)


Entering expressions into the interactive Shell
--

You run the interactive shell by launching IDLE, which you installed with Python in the introduction. 

On Windows, open the Start menu, select All Programs > Python 3.3, and then select IDLE (Python GUI). 

On OS X, select Applications > MacPython 3.3 > IDLE. 

On Ubuntu, open a new Terminal window and enter  idle3 .

A window with the  >>> prompt(提示) should appear; that’s the interactive shell. 
Enter  2 + 2 at the prompt to have Python do some simple math.


errorS Are okAy!
--

Programs will crash if they contain code the computer can’t understand, which will cause Python to show an error message . 

An error message won’t break your computer, though, so don’t be afraid to make mistakes .

A crash just means the program stopped running unexpectedly(出乎意料的) .

If you want to know more about an error message, you can search for the exact message text online to find out more about that specific error . 

You can also check out the resources at http://nostarch.com/automatestuff/ to see a list of common Python error messages and their meanings .

There are plenty of other operators(大量的其他操作) you can use in Python expressions, too. 
For example, Table 1-1 lists all the math operators in Python.

The order of operations (also called precedence(优先级) of Python math operators is similar to that of mathematics(数学). 
The  ** operator is evaluated first; 
the  * ,  / ,  // , and  % operators are evaluated next, from left to right;
and the + and  - operators are evaluated last (also from left to right). 

You can use parentheses to override the usual precedence if you need to. 
Enter the following expressions into the interactive shell:

In each case, you as the programmer must enter the expression, but Python does the hard part of evaluating it down to a single value(的到一个结果值). 

Python will keep evaluating parts of the expression until it becomes a single value, as shown in Figure 1-1.

These rules for putting operators and values together to form expressions are a fundamental part(一个基本单元) of Python 
as a programming language, just like the grammar rules that help us communicate(帮助我们沟通的语法规则). 

Here’s an example:

**This is a grammatically correct English sentence.**
**This grammatically is sentence not English correct a.**

The second line is difficult to parse(语法分析) because it doesn’t follow the rules of English. 
Similarly(类似的), if you type in a bad Python instruction, Python won’t be able to understand it 
and will display a  SyntaxError error message, as shown here:

You can always test to see whether an instruction works by typing it into the interactive shell. 

Don’t worry about breaking the computer: The worst thing that could happen is that Python responds(回复) with an error message.
Professional software developers get error messages while writing code all the time.

The integer, floating-Point, and String data types
--
Remember that expressions are just values combined with operators, and they always evaluate down(求值) to a single value. 

A data type is a category for values(值的类型), and every value belongs to exactly(精确地分类) one data type. 
The most common data types in Python are listed in Table 1-2. 
The values  -2 and  30 , for example, are said to be integer values.

The integer (or int) data type indicates(表明) values that are whole numbers. 
Numbers with a decimal point(小数点), such as 3.14 , are called floating-point numbers (or floats). 

Note that even though the value  42 is an integer, the value  42.0 would be a floating-point number.

Python programs can also have text values called strings, or strs (pronounced(发音) “stirs”). 

Always surround your string in single quote ( ' ) characters (单引号) (as in  'Hello' or  'Goodbye cruel world!(再见了残酷的世界!)' ) 
so Python knows where the string begins and ends. 

You can even have a string with no characters in it,  '' , called a blank string(空字符串). 

Strings are explained in greater detail(更详细的说明) in Chapter 4.

If you ever see the error message  SyntaxError: EOL while scanning string literal(), 
you probably forgot the final single quote character at the end of the string, such as in this example:

String concatenation(连接) and replication(复制) 
--
The meaning of an operator may change based on the data types of the values next to it. 

For example,  + is the addition operator when it operates on two integers or floating-point values. 

However, when  + is used on two string values, it joins the strings as the string concatenation operator. 
Enter the following into the interactive shell:

The expression evaluates down to a single, new string value that combines(结合) the text of the two strings. 

However, if you try to use the  + operator on a string and an integer value, 
Python will not know how to handle(处理) this, and it will display an error message.

The error message  Can't convert(转换) 'int' object to str implicitly(隐式地) means  that 
Python thought you were trying to concatenate an integer to the string 'Alice' . 

Your code will have to explicitly(显式的) convert the integer to a string, because Python cannot do this automatically. 
(Converting data types will be explained in “Dissecting Your Program(剖析程序)” on page 22 
when  talking about the  str() ,  int() , and  float() functions.)

The  * operator is used for multiplication when it operates on two integer or floating-point values. 

But when the  * operator is used on one string value and one integer value, it becomes the string replication operator. 
Enter a string multiplied by a number into the interactive shell to see this in action.

The expression evaluates down to a single string value that repeats the original(原始的字符串) a number of times equal to the integer value. 
String replication is a useful trick(有用的技巧), but it’s not used as often as string concatenation(但是却不是经常被用来做字符串的连接).

The  * operator can be used with only two numeric values (for multiplication 乘法) or 
one string value and one integer value (for string replication).

Otherwise(否则), Python will just display an error message.

It makes sense that(是有道理的) Python wouldn’t understand these expressions: 
You can’t multiply two words, and it’s hard to replicate an arbitrary string(任意字符串) a fractional number(小数) of times.

Storing Values in Variables(在变量里面存储值)
--

A variable is like a box in the computer’s memory where you can store a single value. 

If you want to use the result of an evaluated expression later in your program, you can save it inside a variable.

**Assignment Statements**

You’ll store values in variables with an assignment statement(赋值语句). 
An assignment statement consists of a variable name, an equal sign (called the assignment operator), 
and the value to be stored. 

If you enter the assignment statement spam = 42 , then a variable named  spam will have the integer value  42 stored in it.

Think of a variable as a labeled box(贴了标签的盒子) that a value is placed in, as in Figure 1-2.

For example, enter the following into the interactive shell:

A variable is initialized (or created) the first time a value is stored in it.

After that, you can use it in expressions with other variables and values.
When a variable is assigned a new value(赋新值), the old value is forgotten, 
which is why  spam evaluated to  42 instead of  40 at the end of the example. 

This is called overwriting the variable. 
Enter the following code into the interactive shell to try overwriting a string:

Just like the box in Figure 1-3, the  spam variable in this example stores 'Hello' until you replace it with  'Goodbye' 

**Variable Names**

Table 1-3 has examples of legal(合法的) variable names. You can name a variable anything as long as it obeys the following three rules:
    1. It can be only one word.
    2. It can use only letters, numbers, and the underscore ( _ ) character.
    3. It can’t begin with a number.


Variable names are case-sensitive(区分大小写), meaning that  spam ,  SPAM ,  Spam , and  sPaM are four different variables.

It is a Python convention(约定) to start your variables with a lowercase letter(小写字母).

This book uses camelcase(驼峰拼写法) for variable names instead of underscores(而不是下划线拼写法);
that is, variables  lookLikeThis instead of  looking_like_this . 

Some experienced programmers may point out that the official(官方的) Python code style, PEP 8,
says that underscores should be used. 

I unapologetically(不客气的表示) prefer camelcase(更喜欢驼峰) and point to(指出) 
“A Foolish Consistency Is the Hobgoblin of Little Minds(愚蠢的一致性是头脑狭隘人士的心魔)” in PEP 8 itself:

    “Consistency with the style guide is important(一致性的代码风格指南是很重要的). 
    But most importantly:(但是最重要的是) 
    know when to be inconsistent—sometimes(某些时候的差异性) the style guide just doesn’t apply(). 
    When in doubt(有疑问时), use your best judgment(适合自己的才是最好的).”

A good variable name describes the data it contains. 
Imagine that you moved to a new house and labeled all of your moving boxes as Stuff. 
You’d never find anything! 

The variable names  spam ,  eggs , and  bacon are used as generic names for the examples in this book and 
in much of Python’s documentation (inspired by(受启发) the Monty Python “Spam” sketch(插画), but in your programs, 
a descriptive(描述性的) name will help make your code more readable.

Your first Program
--

While the interactive shell is good for running Python instructions one at a time, 
to write entire Python programs(完整的python程序), you’ll type the instructions into the file editor. 

The file editor is similar to text editors such as Notepad or TextMate, but it has some specific features(特点) for typing in source code. 

To open the file editor in IDLE, select File > New Window.

The window that appears should contain a cursor(光标) awaiting your input,
but it’s different from the interactive shell, which runs Python instructions as soon as you press  enter . 

The file editor lets you type in many instructions, save the file, and run the program. 

Here’s how you can tell the difference between the two:

    •  The interactive shell window will always be the one with the  >>> prompt.
    •  The file editor window will not have the  >>> prompt.

Now it’s time to create your first program! When the file editor window opens, type the following into it:

Once you’ve entered your source code, save it so that you won’t have to retype it each time you start IDLE. 

From the menu at the top of the file editor window, select File > Save As. 

In the Save As window, enter  hello.py in the File Name field and then click Save.

You should save your programs every once in a while as you type them.

That way, if the computer crashes or you accidentally exit(意外退出) from IDLE, you won’t lose the code. 

As a shortcut, you can press  ctrl -S on Windows and Linux or  z -S on OS X to save your file.

Once you’ve saved, let’s run our program. Select Run > Run Module or just press the F5 key. 

Your program should run in the interactive shell window that appeared when you first started IDLE. 

Remember, you have to press F5 from the file editor window, not the interactive shell window.

Enter your name when your program asks for it. The program’s output in the interactive shell should look something like this:


When there are no more lines of code to execute, the Python program
terminates; that is, it stops running. (You can also say that the Python pro-
gram exits.)
You can close the file editor by clicking the X at the top of the window.
To reload a saved program, select File4Open from the menu. Do that now,
and in the window that appears, choose hello.py, and click the Open button.
Your previously saved hello.py program should open in the file editor window.
dissecting your Program
With your new program open in the file editor, let’s take a quick tour of the
Python instructions it uses by looking at what each line of code does.


Comments
The following line is called a comment.
u # This program says hello and asks for my name.
Python ignores comments, and you can use them to write notes or
remind yourself what the code is trying to do. Any text for the rest of the
line following a hash mark ( # ) is part of a comment.
Sometimes, programmers will put a  # in front of a line of code to tem-
porarily remove it while testing a program. This is called commenting out
code, and it can be useful when you’re trying to figure out why a program
doesn’t work. You can remove the  # later when you are ready to put the line
back in.
Python also ignores the blank line after the comment. You can add as
many blank lines to your program as you want. This can make your code
easier to read, like paragraphs in a book.
The print() Function
The  print() function displays the string value inside the parentheses on the
screen.
The line  print('Hello world!') means “Print out the text in the string
'Hello world!' .” When Python executes this line, you say that Python is
calling the  print() function and the string value is being passed to the func-
tion. A value that is passed to a function call is an argument. Notice that
the quotes are not printed to the screen. They just mark where the string
begins and ends; they are not part of the string value.
n o t e You can also use this function to put a blank line on the screen; just call  print() with
nothing in between the parentheses.
When writing a function name, the opening and closing parentheses at
the end identify it as the name of a function. This is why in this book you’ll
see  print() rather than  print . Chapter 2 describes functions in more detail.
The input() Function
The  input() function waits for the user to type some text on the keyboard
and press  enter 

This function call evaluates to a string equal to the user’s text, and the
previous line of code assigns the  myName variable to this string value.

You can think of the  input() function call as an expression that evalu-
ates to whatever string the user typed in. If the user entered  'Al' , then the
expression would evaluate to  myName = 'Al' .
Printing the User’s Name
The following call to  print() actually contains the expression  'It is good to
meet you, ' + myName between the parentheses.

Remember that expressions can always evaluate to a single value. If  'Al'
is the value stored in  myName on the previous line, then this expression evalu-
ates to  'It is good to meet you, Al' . This single string value is then passed to
print() , which prints it on the screen.
The len() Function
You can pass the  len() function a string value (or a variable containing a
string), and the function evaluates to the integer value of the number of
characters in that string.

Enter the following into the interactive shell to try this:

Just like those examples,  len(myName) evaluates to an integer. It is then
passed to  print() to be displayed on the screen. Notice that  print() allows
you to pass it either integer values or string values. But notice the error that
shows up when you type the following into the interactive shell:

The  print() function isn’t causing that error, but rather it’s the expres-
sion you tried to pass to  print() . You get the same error message if you type
the expression into the interactive shell on its own.

Python gives an error because you can use the  + operator only to add
two integers together or concatenate two strings. You can’t add an integer
to a string because this is ungrammatical in Python. You can fix this by
using a string version of the integer instead, as explained in the next section.
The str(), int(), and float() Functions
If you want to concatenate an integer such as  29 with a string to pass to
print() , you’ll need to get the value  '29' , which is the string form of  29 . The
str() function can be passed an integer value and will evaluate to a string
value version of it, as follows:

Because  str(29) evaluates to  '29' , the expression  'I am ' + str(29) +
' years old.' evaluates to  'I am ' + '29' + ' years old.' , which in turn
evaluates to  'I am 29 years old.' . This is the value that is passed to the
print() function.
The  str() ,  int() , and  float() functions will evaluate to the string, inte-
ger, and floating-point forms of the value you pass, respectively. Try con-
verting some values in the interactive shell with these functions, and watch
what happens.

The previous examples call the  str() ,  int() , and  float() functions
and pass them values of the other data types to obtain a string, integer,
or floating-point form of those values.
The  str() function is handy when you have an integer or float that you
want to concatenate to a string. The  int() function is also helpful if you
have a number as a string value that you want to use in some mathematics.
For example, the  input() function always returns a string, even if the user
enters a number. Enter  spam = input() into the interactive shell and enter  101
when it waits for your text.

The value stored inside  spam isn’t the integer  101 but the string  '101' .
If you want to do math using the value in  spam , use the  int() function to
get the integer form of  spam and then store this as the new value in  spam. 

Now you should be able to treat the  spam variable as an integer instead
of a string.

Note that if you pass a value to  int() that it cannot evaluate as an inte-
ger, Python will display an error message.

The  int() function is also useful if you need to round a floating-point
number down.

In your program, you used the  int() and  str() functions in the last
three lines to get a value of the appropriate data type for the code.

The  myAge variable contains the value returned from  input() . Because
the  input() function always returns a string (even if the user typed in a num-
ber), you can use the  int(myAge) code to return an integer value of the string
in  myAge . This integer value is then added to  1 in the expression  int(myAge) + 1 .
The result of this addition is passed to the  str() function:  str(int(myAge)
+ 1) . The string value returned is then concatenated with the strings  'You
will be ' and  ' in a year.' to evaluate to one large string value. This large
string is finally passed to  print() to be displayed on the screen.
Let’s say the user enters the string  '4' for  myAge . The string  '4' is con-
verted to an integer, so you can add one to it. The result is  5 . The  str() func-
tion converts the result back to a string, so you can concatenate it with the
second string,  'in a year.' , to create the final message. These evaluation
steps would look something like Figure 1-4.

text AnD numBer equivAlenCe
Although the string value of a number is considered a completely different
value from the integer or floating-point version, an integer can be equal to a
floating point .
Python makes this distinction because strings are text, while integers and
floats are both numbers .

Summary
You can compute expressions with a calculator or type string concatena-
tions with a word processor. You can even do string replication easily by
copying and pasting text. But expressions, and their component values—
operators, variables, and function calls—are the basic building blocks
that make programs. Once you know how to handle these elements, you
will be able to instruct Python to operate on large amounts of data for you.
It is good to remember the different types of operators ( + ,  - ,  * ,  / ,  // ,  % ,
and  ** for math operations, and  + and  * for string operations) and the three
data types (integers, floating-point numbers, and strings) introduced in this
chapter.
A few different functions were introduced as well. The  print() and  input()
functions handle simple text output (to the screen) and input (from the key-
board). The  len() function takes a string and evaluates to an int of the num-
ber of characters in the string. The  str() ,  int() , and  float() functions will
evaluate to the string, integer, or floating-point number form of the value
they are passed.
In the next chapter, you will learn how to tell Python to make intelli-
gent decisions about what code to run, what code to skip, and what code to
repeat based on the values it has. This is known as flow control, and it allows
you to write programs that make intelligent decisions.






