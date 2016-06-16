函数 Function
==
    you’re treating the function as a “black box .”

    As you get more programming experience, you’ll often find yourself deduplicating code(删除重复代码), 
    which means getting rid of duplicated or copy-and- pasted code.
    Deduplication makes your programs shorter, easier to read, and easier to update.

def Statements with Parameters
--
return Values and return Statements
--
the none Value
--
keyword Arguments and print()
--
    Most arguments are identified by their position in the function call.
    print('Hello', end='')
    >>> print('cats', 'dogs', 'mice', sep=',')
    cats,dogs,mice

local and global Scope(范围)
--
    local variable
    global variable

Scopes matter for several reasons:

    •  Code in the global scope cannot use any local variables.
    •  However, a local scope can access global variables.
    •  Code in a function’s local scope cannot use variables in any other local scope.
    •  You can use the same name for different variables if they are in different scopes. 
           That is, there can be a local variable named  spam and a global variable also named  spam .

Local Variables Cannot Be Used in the Global Scope

Local Scopes Cannot Use Variables in Other Local Scopes

Global Variables Can Be Read from a Local Scope

Local and Global Variables with the Same Name

    Since these three separate variables all have the same name, it can be confusing to keep track of 
    which one is being used at any given time. 
    This iswhy you should avoid using the same variable name in different scopes.

the global Statement
--
There are four rules to tell whether a variable is in a local scope or global scope:
    1. If a variable is being used in the global scope (that is, outside of all functions), then it is always a global variable.
    2. If there is a  global statement for that variable in a function, it is a global variable.
    3. Otherwise, if the variable is used in an assignment statement in the function, it is a local variable.
    4. But if the variable is not used in an assignment statement, it is a global variable.

异常处理 exception handling
--
    You can put the previous(以前的) divide-by-zero code in a  try clause and 
    have an  except clause(除此之外的子句) contain code to handle what happens when this error occurs.
    
    def spam(divideBy):
    try:
        return 42 / divideBy
    except ZeroDivisionError:
        print('Error: Invalid argument.')

A Short Program: guess the number
--

Summary
--
    Functions are the primary way to compartmentalize your code into logical groups.(函数是将代码按逻辑划分组的主要途径)
 
    def collatz(number):
        if number%2 ==0:
            number = number // 2
            print(number)
            return number
        else:
            number = number * 3 + 1
            print(number)
            return number

    if __name__ == '__main__':
        try:
            numInput = int(input())
            collatz(numInput)
        except :
            print('Incrrect input'











Words study
--
    addition 除了
    noninteger 非整数
    Validation 验证 
    sequence 顺序
    even 偶数 --> odd 奇数
    areallyourpetsnamederic
    advantageous 优点
    directly affect 直接影响
    compartmentalize 
    concatenate 连接
    hint 暗示
    generate 生成-->generator生成器
    comment 注释
    occur in 存在
    potentially 潜在的,可能的
    ZeroDivisionError 0做除数错误
    detect errors 检测错误
    therefore 因此
    declared 声明
    rely on 依靠,依赖,信赖
    track down 追查到
    narrows down 使缩小
    interacts 交谈    
    a particular 个别的
    parameters 参数
    a newline character 换行符
    respectively 分别地
    specify 指定
    optional parameters 可选参数
    Behind the scenes 在幕后
    originally 最初的
    what a function’s local scope is 函数的局部
    parameter 参数
    context 上下文,语句环境
    In general 总之,通常,一般来讲
    parentheses 圆括号
    avoid duplicating code 避免复制代码




