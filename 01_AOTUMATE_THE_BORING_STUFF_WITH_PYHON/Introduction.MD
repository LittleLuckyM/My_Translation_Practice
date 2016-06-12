Introduction
==

“You’ve just done in two hours what it takes the three of us two days to do.”
你用两个小时就干完了我们三个人要花费两天才能完成的任务.

My college roommate was working at a retail electronics store in the early 2000s. 

Occasionally, the store would receive a spreadsheet(电子表格) of 
thousands of product prices from its competitor(竞争者).

A team of three employees would print the spreadsheet onto a thick stack of paper(厚厚的一摞纸) 
and split it among themselves. 

For each product price, they would look up their store’s price
and note all the products that their competitors sold for less. 
It usually took a couple of days.

“You know, I could write a program to do that if you have the original file(原始文件) for the printouts,” 
my roommate told them, when he saw them sittingon(无名指) the floor with papers scattered(散落一地) 
and stacked(堆积) around them.

After a couple of hours, he had a short program that read a competitor’s price from a file, 
found the product in the store’s database, and noted whether the competitor was cheaper. 

He was still new to programming, and he spent most of his time looking up documentation in a programming book.

The actual program took only a few seconds to run. 
My roommate and his co-workers took an extra-long lunch that day.

This is the power of computer programming. 
A computer is like a Swiss Army knife(瑞士军刀) that you can configure for countless tasks. 
Many people spend hours clicking and typing to perform repetitive tasks, 
unaware that the machine they’re using could do their job in seconds 
if they gave it the right instructions(指令).

whom is this Book for?
--

Software is at the core of so many of the tools we use today: 
Nearly everyone uses social networks to communicate, 
many people have Internet-connected computers in their phones, 
and most office jobs(办公室工作) involve interacting with a computer(涉及与电脑的互动) to get work done. 

As a result, the demand for people who can code has skyrocketed(编程人员的需求量暴涨). 
Countless books, interactive web tutorials(交互式网络教程), 
and developer boot camps(培训机构) promise to turn ambitious beginners(野心勃勃的初学者) into software engineers 
with six-figure salaries(6位数的薪水).

This book is not for those people. It’s for everyone else.

On its own(就其本身而言), this book won’t turn you into a professional software devel-oper any more 
than a few guitar lessons will turn you into a rock star(几节吉他课将你变成摇滚明星). 

But if you’re an office worker, administrator, academic(大学生), or anyone else 
who uses a computer for work or fun, you will learn the basics of programming 
so that you can automate simple tasks such as the following:

    •  Moving and renaming thousands of files and sorting them into folders()
    •  Filling out online forms, no typing required
    •  Downloading files or copy text from a website whenever it updates
    •  Having your computer text you custom notifications
    •  Updating or formatting Excel spreadsheets(更新或者是格式化你的Excel表格)
    •  Checking your email and sending out prewritten responses(预先写好的答复)
These tasks are simple but time-consuming(简单却耗时) for humans, 
and they’re often so trivial or specific that there’s no ready-made software to perform them. 
(如此繁琐或者是特别,但却没有现成的软件来完成他们)
Armed with(拥有) a little bit of programming knowledge, you can have your computer do these tasks for you.

Conventions
--

This book is not designed as a reference manual(参考手册); 
it’s a guide for begin-ners. 

The coding style sometimes goes against best practices(违背最佳实现方式) (for example,
some programs use global variables), but that’s a trade-off(权衡取舍) to make the code simpler to learn.

This book is made for people to write throwaway code(一次性代码), 
so there’s not much time spent on style and elegance(风格和优雅). 

Sophisticated program-ming(复杂的规划) concepts—like(概念) object-oriented programming(面向对象免除), 
list comprehensions(列表推导), and generators—aren’t covered(生成器也不包含) 
because of the complexity they add(因为他们增加的难度).

Veteran programmers(编程老手) may point out ways the code in this book 
could be changed to improve efficiency(提高效率), 
but this book is mostly concerned with(关心) getting programs to work with the least amount of effort(最少的工作).

what is Programming?
--
Television shows and films often show programmers furiously typing 
cryptic streams of 1s and 0s on glowing screens(发光的屏幕上疯狂的输入什么0和1的数据流), 
but modern(现代的) programming isn’t that mysterious(如此神秘). 

Programming is simply the act of entering instructions(简单的输入指令的行为) for the computer to perform. 

These instructions might crunch some numbers(处理一些数字),modify text, look up information in files, 
or communicate with other computers over the Internet.

All programs use basic instructions as building blocks(以简单的指令为基石). 
Here are a few of the most common ones, in English:(下面是一些最常见的问题)

    “Do this; then do that.”
    “If this condition is true, perform this action; otherwise, do that action.”
    “Do this action that number of times.”
    “Keep doing that until this condition is true.”

You can combine(结合) these building blocks to implement(实现) more intricate decisions(复杂的决策), too. 

For example, here are the programming instructions, called the source code, 
for a simple program written in the Python programming language. 

Starting at the top, the Python software runs each line of code
(some lines are run only if a certain condition is true or else Python runs some other line) 
until it reaches the bottom.
```python
passwordFile = open('SecretPasswordFile.txt')
secretPassword = passwordFile.read()
print('Enter your password.')
typedPassword = input()
if typedPassword == secretPassword:
    print('Access granted')
if typedPassword == '12345':
    print('That password is one that an idiot(白痴的) puts(字符串输出) on their luggage(行李).')    
else:
    print('Access denied')
```

You might not know anything about programming, but you could probably make a reasonable guess 
at what the previous code does just by reading it.

First, the file SecretPasswordFile.txt is opened, and the secret password in it is readed. 

Then, the user is prompted(提示) to input a password (from the keyboard) .
These two passwords are compared, and if they’re the same,
the program prints Access granted(授权) to the screen . 

Next, the program checks to see whether the password is 12345 and hints(提示) that 
this choice might not be the best for a password
{. If the passwords are not the same, the program prints Access denied to the screen.

What Is Python?
--

Python refers to(是指) the Python programming language (with syntax rules for writing 
what is considered valid(合法有效) Python code) 
and the Python interpreter(解释器) software that reads source code 
(written in the Python language) and performs its instructions(执行指令). 

The Python interpreter is free to download from http://python.org/, 
and there are versions for Linux, OS X, and Windows.

The name Python comes from the surreal British comedy group Monty Python
(超现实主义的英国喜剧组Monty Python), not from the snake(而不是蛇...这是真的么). 

Python programmers are affectionately(亲切地) called Pythonistas(专有词汇:python支持者), 
and both Monty Python and serpentine references(蛇形图案的引用) usually pepper(经常布满) Python tutorials and documentation(教程和文档).


Programmers Don’t Need to Know Much Math
The most common anxiety(顾虑) I hear about learning to program is that 
people think it requires a lot of math. 

Actually, most programming doesn’t require math beyond basic arithmetic(除了最基本的运算). 

In fact, being good at programming isn’t that different from being good at solving Sudoku puzzles(数度谜题).

To solve a Sudoku puzzle, the numbers 1 through 9 must be filled in for each row, each column, 
and each 3×3 interior square(小(内)方块) of the full 9×9 board.

You find a solution by applying deduction(通过推演推演) and logic from the starting numbers. 

For example, since 5 appears in the top left(左上角) of the Sudoku puzzle shown in Figure 0-1, 
it cannot appear elsewhere in the top row, in the leftmost column, or in the top-left 3×3 square. 

Solving one row, column, or square at a time will provide more number clues(线索) for the rest of the puzzle.

Just because Sudoku involves numbers doesn’t mean you have to 
be good at math to figure out the solution. 

The same is true of programming. Like solving a Sudoku puzzle, writing programs involves 
breaking down a problem into individual(将问题拆分成很多个独立的个体), detailed steps. 

Similarly(同样的), when debugging programs (that is, finding and fixing errors), 
you’ll patiently observe(耐心的观察) what the program is doing and find the cause of the bugs. 

And like all skills, the more you program, the better you’ll become(编码也讲究熟能生巧).

Programming Is a Creative Activity(一个富有创造性的活动)
--

Programming is a creative task, somewhat(有点) like constructing a castle out of LEGO bricks. 
(用乐高积木构建城堡)

You start with a basic idea of what you want your castle to look like 
and inventory your available blocks(清点可使用的积木). 

Then you start building.
Once you’ve finished building your program, you can pretty up(美化) your code
just like you would your castle(动词省略,表示对城堡进行美化).


The difference between programming and other creative activities is that 
when programming, you have all the raw materials(原材料) you need in your computer; 
you don’t need to buy any additional(额外的) canvas(帆布), paint(油漆), film(胶卷), yarn(线),
LEGO bricks(乐高积木), or electronic components(电子元器件).

When your program is written, it can easily be shared online with the entire world(全世界). 
And though you’ll make mistakes when programming, the activity is still a lot of fun(犯错同样是极富乐趣的).

About this Book
--

The first part of this book covers basic Python programming concepts, and
the second part covers various tasks you can have your computer automate.
Each chapter in the second part has project programs for you to study. Here’s
a brief rundown of what you’ll find in each chapter:
Part I: Python Programming Basics
Chapter 1: Python Basics Covers expressions, the most basic type of
Python instruction, and how to use the Python interactive shell soft-
ware to experiment with code.
Chapter 2: Flow Control Explains how to make programs decide
which instructions to execute so your code can intelligently respond to
different conditions.
Chapter 3: Functions Instructs you on how to define your own func-
tions so that you can organize your code into more manageable chunks.
Chapter 4: Lists Introduces the list data type and explains how to
organize data.
Chapter 5: Dictionaries and Structuring Data Introduces the diction-
ary data type and shows you more powerful ways to organize data.
Chapter 6: Manipulating Strings Covers working with text data
(called strings in Python).
Part II: Automating Tasks
Chapter 7: Pattern Matching with Regular Expressions Covers how
Python can manipulate strings and search for text patterns with regular
expressions.
Chapter 8: Reading and Writing Files Explains how your programs
can read the contents of text files and save information to files on your
hard drive.
Chapter 9: Organizing Files Shows how Python can copy, move,
rename, and delete large numbers of files much faster than a human
user can. It also explains compressing and decompressing files.

Chapter 10: Debugging Shows how to use Python’s various bug-
finding and bug-fixing tools.
Chapter 11: Web Scraping Shows how to write programs that can
automatically download web pages and parse them for information.
This is called web scraping.
Chapter 12: Working with Excel Spreadsheets Covers programmati-
cally manipulating Excel spreadsheets so that you don’t have to read
them. This is helpful when the number of documents you have to ana-
lyze is in the hundreds or thousands.
Chapter 13: Working with PDF and Word Documents Covers pro-
grammatically reading Word and PDF documents.
Chapter 14: Working with CSV Files and JSON Data Continues to
explain how to programmatically manipulate documents with CSV and
JSON files.
Chapter 15: Keeping Time, Scheduling Tasks, and Launching
Programs Explains how time and dates are handled by Python pro-
grams and how to schedule your computer to perform tasks at certain
times. This chapter also shows how your Python programs can launch
non-Python programs.
Chapter 16: Sending Email and Text Messages Explains how to write
programs that can send emails and text messages on your behalf.
Chapter 17: Manipulating Images Explains how to programmatically
manipulate images such as JPEG or PNG files.
Chapter 18: Controlling the Keyboard and Mouse with GUI Automation
Explains how to programmatically control the mouse and keyboard to
automate clicks and keypresses.



