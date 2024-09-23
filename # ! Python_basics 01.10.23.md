# <center><ins>Python Basics!</center>

<div class="alert alert-success alertsuccess" style="margin-top: 20px">
    <font size="5">Authors Note</font><br><br>This notebook is an <strong>ongoing project</strong>, and as such, while every effort has been made to ensure the accuracy and completeness of the information, no guarantee is given nor responsibility taken for errors or omissions.<br><br>The notebook is designed as a <strong>reference for quickly finding correct syntax and structure paired with examples.</strong><br>Please see my other notebook (Python quick reference) which is cleaner and easier to read, but has no examples included.<br><br>I hope this comes in useful to whoever finds it.<br>Andy Taison 28/04/2022
</div>

|<td colspan=3> <center><bold><h3>**Table of contents**<center>|||
|---|:---|:---:|
|**1.**|[**Useful Links**](#-Useful-Links;)||
|**2.**|[**Useful information**](#Useful-information;)||
|**3.**|[**Operator precedence rule in Python**](#Operator-precedence;)||
|**4.**|[**Mutable or Immutable**](#Mutable-or-Immutable;)||
|**5.**|[**Strings/Variables, Operators and Basics**](#Strings/Variables-and-Basics;)|types, operators, comparisons,<br>escape sequences, basic methods,<br>user inputs,<br>formatting strings, f-strings, formatting types,<br>zfill( )|
|**6.**|[**Regular Expressions (Regex)**](#Regular-Expressions-(Regex);)|Metacharacters<br>Special Sequences, sets<br>RegEx functions<br>Match objects, flags|
|**7.**|[**Tuples**](#Tuples;)|( )<br>immutable, ordered|
|**8.**|[**Lists**](#Lists;)|[ ]<br>mutable, ordered|
|**9.**|[**Dictionaries**](#Dictionairies;)|{ : , }<br>keys are mutable and unique|
|**10.**|[**Sets**](#Sets;)|{ }<br>unordered and unique elements,<br>mutable|
|**11.**|[**Branching**](#Branching;)|if( ): else( ): elif( ):|
|**12.**|[**Logic Operators**](#Logic-Operators;)|not or and|
|**13.**|[**Loops**](#Loops;)|for :<br>parallel iteration<br>[ list comprehension ], { dictionary comprehension }<br>while :<br>break, continue, pass|
|**14.**|[**Exception Handling**](#Exception-Handling;)|built-in exceptions,<br>try except statement,<br>raise exception<br>custom exception<br>traceback<br>assert|
|**15.**|[**Useful Built-in Functions**](#-Useful-Built-in-Functions;)|range( ), enumerate( ),<br> .count( ), sum( ),<br>isnumeric( ), isinstance( ),<br>zip( ),<br>map( )|
|**16.**|[**Building Functions**](#-Building-Functions;)|define, call and help on functions,<br>global / local scopes,<br>lambda functions|
|**17.**|[**Classes, Objects and Methods**](#Classes,-Objects-and-Methods;)|define class, create objects,<br>inheritance,<br>access / change attributes,<br>create / call methods,<br>special methods,<br>get/set with @property decorator<br>dir command,<br>duck typing|
|**18.**|[**Command line arguments**](#Command-line-arguments;)|using sys<br>argparse|
|**19.**|[**PIP**](#PIP;)|list installed packages,<br>install / uninstall packages|
|**20a.**|[**Working with Files<br>Opening and Reading Files**](#Opening-and-Reading-Files;)|open function,<br> .name, .mode, .close( ), .closed methods,<br> with statement,<br> .read( ), .readline( ), .readlines( ) methods|
|**20b.**|[**Working with Files<br>Writing to Files**](#Writing-to-Files;)|.write( ) method,<br>with statement,<br> .seek( ), .tell( ) methods,<br>writting from a list, copying files|
|**21.**|[**CSV Files**](#CSV-Files;)|reading csv files<br>reading to a dataset<br>using csv library<br>writting to csv files|
|**22.**|[**Excel Files**](#Excel-Files;)|read Excel files to dataframe<br>ExcelFile<br>sheet_names, parse( )<br>writting to Excel from dataframe<br>ExcelWriter<br>writting formula to Excel|
|**23.**|[**Simple APIs**](#Simple-APIs;)|| 
|**End**|[**End of Notebook / Notes**](#Notes;)||

---

---

---

## <center> Useful Links;</center>

[Python Quick Reference](https://www.python.org/ftp/python/doc/1.1/quick-ref.1.1.html)

[Python3 cheat sheet](https://perso.limsi.fr/pointal/_media/python:cours:mementopython3-english.pdf)

[Python.org](https://www.python.org/)

[Python Standard Library](https://docs.python.org/3/library/index.html)

[Python Functions](https://docs.python.org/3/library/functions)

[Python Pandas](https://pandas.pydata.org/)

[Python NumPy](https://numpy.org/)

[Matplotlib (PyPlot)](https://matplotlib.org/stable/index.html#)

[W3schools Python](https://www.w3schools.com/python/default.asp)

[Beginnersbook](https://beginnersbook.com/2018/03/python-tutorial-learn-programming/)

[GeeksForGeeks](https://www.geeksforgeeks.org/python-programming-language/)

[Syntax in Python](http://rigaux.org/language-study/syntax-across-languages-per-language/Python.html)

[Wiki - Python syntax and semantics](https://en.wikipedia.org/wiki/Python_syntax_and_semantics)

[For beginners](https://www.python.org/about/gettingstarted/)

[Quiz and practice](https://app.finxter.com/learn/computer/science/) 

[Pointers to the best information available about working with Excel files in the Python](https://www.python-excel.org/)

---

---

## <center>Useful information;</center>

>Python is an interpreted, object-orientated, high-level programming language with dynamic semantics. It interprets script line by line as it executes and will stop the entire program when it encounters an error unless error was expected and handled by the programmer.  
Python is coded in C/C++ meaning C/C++ code can be created and used within Python.  

<div class="alert alert-success alertsuccess" style="margin-top: 20px">
    [Tip:] When learning a <code>new library</code>, always start by checking out the developers website and begin with the quick start.
</div>


```python
# check the python version

import sys
print(sys.version)
```

    3.9.7 (default, Sep 16 2021, 16:59:28) [MSC v.1916 64 bit (AMD64)]
    

<div class="alert alert-success alertsuccess" style="margin-top: 20px">
    [Tip:] <code>sys</code> is a built-in module that contains many system-specific parameters and functions, including the Python version in use. Before using it, we must explictly <code>import</code> it.
</div>

**Help** on operations, types, methods and functions

**`help(A)`**
* Would give help on a list and variable `A`

**print all variables and function names of a module**:  

**`print(dir(moduleName))`**  
* This will print all the variables and function names from the module given  

**Get Unicode code**:  

**`ord(character)`**  
* Returns the unicode of given character  


```python
ord("A")
```




    65



**tab prompt**:  


* Use tab to autocomplete when typing variable names and functions  
* Can also be used after **"."** to get a prompt list of availiable functions and methods  

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>Operator precedence;</center>

|**Operator precedence rule in Python:**||
|---|---|
|( )| Parentheses|
|**| Exponent|
|+x, -x, ~x| Unary plus, Unary minus, Bitwise NOT|
|*, /, //, % |Multiplication, Division, Floor Division, Modulus|
|+, - |Addition, Subtraction|
|<<, >> |Bitwise shift operators|
|& |Bitwise AND|
|^ |Bitwise XOR|
|\|| Bitwise OR|
|==, !=, >, >=, <, <=, is, is not, in, not in       |Comparisions, Identity, Membership operators|
|not |Logical NOT|
|and |Logical AND|
|or |Logical OR|

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>Mutable or Immutable;</center>

|**Mutable:**|**Immutable:**|
|:---|:---|
|List|Int|
|Dictionary|Float|
|Set|Long|
|User-Defined Classes<br>(depending on the defined attributes by the user)|Complex|
|Byte Array|Boolean|
||String|
||Tuple|
||Frozenset|
||Unicode|

**Python** is Pass by **object reference**  

Pass by **reference** = The variable is passed directly (by reference) to a function. Any operation performed by the function on the variable will change the original object as it is the same object.  

Pass by **value** = A copy of the object is passed to the function. Any operation performed by the function will not affect the original object.  

Pass by **object reference** = A reference to the original object is passed, however the function will create a new variable. In essence, the object is the same, but now has two names in which to reference the object. If contents of the object is changed by the function (modified in place and can only be done with mutable objects), the contents of the original are updated too (similar to pass by reference). However if the reference/variable name is changed in the function, then the original object will not be affected (similar to pass by value).  


```python
# Function modifying a list (mutable) in place
def try_to_change_list_contents(the_list):
    print('Function received: ', the_list)
    the_list.append('four')
    print('Function changed to by append: ', the_list)

outer_list = ['one', 'two', 'three']

print('Before, outer_list: ', outer_list)
try_to_change_list_contents(outer_list)
print('After, outer_list: ', outer_list)
```

    Before, outer_list:  ['one', 'two', 'three']
    Function received:  ['one', 'two', 'three']
    Function changed to by append:  ['one', 'two', 'three', 'four']
    After, outer_list:  ['one', 'two', 'three', 'four']
    


```python
# Function modifying a list and changing reference
def try_to_change_list_reference(the_list):
    print('Function received: ', the_list)
    the_list = ['and', 'we', 'can', 'not', 'lie']
    print('Function changed to with new reference: ', the_list)

outer_list = ['we', 'like', 'proper', 'English']

print('Before, outer_list: ', outer_list)
try_to_change_list_reference(outer_list)
print('After, outer_list: ', outer_list)
```

    Before, outer_list:  ['we', 'like', 'proper', 'English']
    Function received:  ['we', 'like', 'proper', 'English']
    Function changed to with new reference:  ['and', 'we', 'can', 'not', 'lie']
    After, outer_list:  ['we', 'like', 'proper', 'English']
    


```python
# Function modifying an immutable string
def try_to_change_string_reference(the_string):
    print('Function received: ', the_string)
    the_string = the_string + ' in a kingdom by the sea'
    print('Function changed to with new reference (unable to modify a string in place): ', the_string)

outer_string = 'It was many and many a year ago'

print('Before, outer_string: ', outer_string)
try_to_change_string_reference(outer_string)
print('After, outer_string: ', outer_string)
```

    Before, outer_string:  It was many and many a year ago
    Function received:  It was many and many a year ago
    Function changed to with new reference (unable to modify a string in place):  It was many and many a year ago in a kingdom by the sea
    After, outer_string:  It was many and many a year ago
    

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>Strings/Variables and Basics;</center>

#### **Types**

A type is how Python represents different types of data:  

* **`int`** (this is the type) = Integers: whole numbers e.g., 6 (this is the expression)  
can be positive or negative, finite range  
* **`float`** = Float: real numbers with decimal point e.g., 6.986  
* **`complex`** = Complex numbers: imaginary numbers are written with a j e.g., 5j or 1 + 3j etc.
* **`str`** = String: sequence of characters e.g., Hello  
* **`bool`** = Boolean: True or False, must be capitalized. True contains the int or float value of 1, False is 0  

**`None`**  - absence of data  

The type of a variable can be viewed using the type function
e.g., **`type(6)`** or **`print(type(var))`**


```python
# example of type function
type(6)
```




    int




```python
# system settings about float type

sys.float_info
```




    sys.float_info(max=1.7976931348623157e+308, max_exp=1024, max_10_exp=308, min=2.2250738585072014e-308, min_exp=-1021, min_10_exp=-307, dig=15, mant_dig=53, epsilon=2.220446049250313e-16, radix=2, rounds=1)




```python
# example of a complex number

myComplex = 8j + 1

print(type(myComplex))
```

    <class 'complex'>
    

The type of expressions can be converted, this is called typecasting or to cast
* int to float: **`float(6)`**: **6.0**
* float to int: **`int(6.8)`**: **6** *caution as info is lost*
* str to int (or float) if contains an integer value: **`int('6')`**: **6**
* A string with a non-interger value would produce an error: **`int('A')`**: **error**
* int or float to a string: **`str(6.9)`**: **'6.9'**
* boolean to int or float: **`int(True)`**: **1**
* int or float to boolean: **`bool(0)`**: **False** 

>Expressions are operations Python performs, for example basic arithmetic which is known as an operation.
The numbers are the operands 
The maths symbols are operators 

Can get help on operations, types, methods and functions using following:  
**`A`**=[1, 2]  
**`help(A)`**
Would give help on a list object  

**Type hinting**:  

**`variable/parameter: type`**  
**`-> output type`**  
* Used to **hint** at what types are expected  
* Note this is **not enforced**  


```python
def say_hi(name: str) -> str:
    return f'Hi {name}'
```


```python
# Showing type hinting is not enforced
say_hi(float(5.0))
```




    'Hi 5.0'



**Operators**

**`/`** Single forward slash will **divide** and give result as **float** (real number, answer) e.g., 10/5=2.0 OR 6/4=1.5  
**`//`** Double forward slash = **floor division**, will give result as **int** (loss of decimal information) note that if type isn't specified and there is a float as an operand that the answer will be calculated as an int but given in float format. This is always rounded down. e.g., 6//4=1  
**`**`** **Exponentiation** will give the **power of**, e.g., 2\*\*8=8  
**`%`** **Modulus** will give **remainder** of a division, e.g., 6%4=2   
**`*`** Will **multiply**  e.g., 2"*"4=8   

**`+=`** **Increment assignment** will add a value and a variable and assign it to the variable  
**`-=`** **Decrement assignment** will subtract a value from a variable and assign it to the variable  
**`/=`** **Division assignment** divides the variable by a value and assigns the result to that variable  
**`*=`** **Multiplication assignment** multiplies the variable by a value and assigns the result to that variable  
**`%=`** **Modulus assignment** computes the modulus of the variable and a value and assigns the result to that variable  
**`//=`** **Floor division assignment** floor divides the variable by a value and assigns the result to that variable  
**`**=`** **Power assignment** raises the variable to a specified power and assigns the result to the variable  
  

---

**Comparison Operators**  
* Compares some values, operands or variables including strings

**`==`** **Equality operator** Gives result "True" when both sides are equal  
**`!=`** **Inequality operator** Gives result "True" when both sides are **Not** equal  
**`<`** **Less than operator** Gives result "True" when operand on left side is less than operand on right side  
**`>`** **Greater than operator** Gives result "True" when operand on left side is greater than operand on right side  
**`<=`** **Less than or equal to operator** Gives result "True" when operand on left side is less than or equal to the right side  
**`>=`** **Greater than or equal to operator** Gives result "True" when operand on left side is greater than or equal to the right side  


```python
# example of using comparison operators
a=6 # setting variable a
a<8
```




    True




```python
# example of using comparison operators
"AC/DC"=="Micheal Jackson"
```




    False



---

#### **Escape sequences**

**`\`** Proceeds the escape sequence - This will allow you to spread lines of code over multipul lines  

**`\n`** For new line


```python
# example of new line escape sequence
print("Double space: Micheal  Jackson") # double space only work in Markdown, not Python
print("No space, with escape \\n:\nMicheal\nJackson")
```

    Double space: Micheal  Jackson
    No space, with escape \n:
    Micheal
    Jackson
    

**`\t`** For tab  
**`\\`** To insert a single **`\`** in string    
**`r`** To display as raw string (placed before the quotation mark)   


```python
# example of raw string
print(r"With r: Micheal\nJackson")
print("Without r: Micheal\nJackson")
```

    With r: Micheal\nJackson
    Without r: Micheal
    Jackson
    

**Line continuation in code**  

**`( )`**  parentheses is the prefered method  
**`\`**  backslash can sometimes look better, and with some lines of code is the only way for it to work  
* **ENSURE** to indent continuing line of code  



 ---

#### **Operations**

Assignment operator **`=`**   
Assigns values to variables  
Or results to an expression  
  
**`print(var)`** Enter variable to be output,  can be entered as a string when put in quotes,  or multiple entries separated by a comma

**`print blank line`**:
* print( )
* print(" ")
* print(\n)

Can perform operations on a variable and assign it to a new variable  
**`x`**=5  
**`y`**=10/**`x`**  
  
Or we can perform operations on the same variable which will change its stored value  
**`x`**=160  
**`x`**=**`x`**/60 **`x`**=2.66666...   

---

#### **Strings & Indexing**

* Strings are immutable 
* Contained within two quotes, either single 'a' or double "b" but not a mixture  
* **Multi line / long strings** are with **3 double or single quotes `"""`** before and after the string  
* Can contain characters, digits, spaces or special characters  
* Strings can be added when digits or characters, **beware** this will be done as text not numbers e.g., ="1" + "4" : "14"  
* Each element of a string can be accessed with an index represented by array of numbers, first character will be 0 and counting up to the right.
  Or from the end starting at -1 and counting down to the left   


```python
# long strings

myString = """
        Hello,
        this is a
        long string
        """

print(myString)
```

    
            Hello,
            this is a
            long string
            
    

Note **square brackets** for indexing  
**indexing**:  

**`var[index]`**


```python
# define variable, "name"
name = "Micheal Jackson"
print(name)
```

    Micheal Jackson
    


```python
# example of indexing from the left
name[4]
```




    'e'




```python
# example of indexing from the right
name[-3]
```




    's'



**slice**:  

**`var[start point : end point]`**  
* Think of points between the characters 


```python
# example of a slice
name[0:4]
```




    'Mich'



**stride**:  

**`var[start : end : places to jump]`**  
* If no start/end entered, it will start from beginning


```python
# example of a stride without start or end point
name[::2]
```




    'McelJcsn'




```python
# another example with start point
name[3::3]
```




    'hlas'



**len** function:  

**`len(var)`**  
* Function returns length of string  
* Note this starts at 1 as its **number of elements** NOT index numbers


```python
# example of len function
len(name)
```




    15



**concatenate** and combine strings:  

**`new_var = var1 + var2`**


```python
# showing string concatenate
# note space before "is"
statement= name + " is the best"
print(statement)
```

    Micheal Jackson is the best
    

Be aware that concatenating strings with digits will be treated as strings, see example:


```python
# example of concatenating strings with digits
digitString = "1" + "1"
print(digitString)
print("type:", type(digitString))
```

    11
    type: <class 'str'>
    

**replicate** strings:  

**`#timesToRep* var`**


```python
# example of replicating a string
3*name
```




    'Micheal JacksonMicheal JacksonMicheal Jackson'



---

#### **Methods**

Strings are sequences and can use the same sequence methods as lists and tuples, they also have string methods which just work on strings.  

**upper**:  

**`var.upper()`**  
* To make everything upper case, **must assign a variable to keep the change** 


```python
# example of `upper` method
name.upper()
```




    'MICHEAL JACKSON'




```python
# showing changes do not affect original variable unless reassigned
name = "Micheal Jackson"
name.upper()  # upper change made temporarily, but not assigned to a variable 
print(name)  # will print original - lower case
name = name.upper()  # reassigning to original variable, could be a new variable
print(name)
name = "Micheal Jackson" # resetting variable
```

    Micheal Jackson
    MICHEAL JACKSON
    

**replace**:  

**`var.replace("what", "with")`**  
* Assign a variable to save change and denote the variable the change is being made to before the ' `.` '  
* Note this is **Case sensitive**


```python
# example of `replace` method
name.replace("Jack", "HEHE")
```




    'Micheal HEHEson'



**find**:  

**`var.find("what")`**  
* Would output the **first index** of the sequence  
* Will return **`-1`** if not found


```python
# example of `find` method
name.find("ck")
```




    10




```python
# another example of `find` method ... no hit
name.find("HE")
```




    -1



---

**strip** method:  

**`var.strip()`**  
* **Removes white spaces** and **escape characters** at the **beginning** and **end** of a string  
* Ensure to save to a new variable to save the changes  


```python
stringExample = "         an example of strip           "
print(stringExample)
```

             an example of strip           
    


```python
whiteRemoved = stringExample.strip()
print(whiteRemoved)
```

    an example of strip
    

---

**split** method:  

**`listVar = strVar.split(sep=None, maxsplit=-1)`**  
* Converts string to a list of words, standard delimiter is a **space**  
* **`sep`** is the delimiter, None = **default whitespaces**  
* **`maxsplit`** is the maximum number of splits to do, -1 = **default no limit**  


```python
# example of spit method

"a b c".split()
```




    ['a', 'b', 'c']



---

**join** method:  

**`string.join(iterable)`**  
* Creates **strings** from iterable objects  
* Joins each **element** of an iterable (such as lists, strings, tuples, dictionaries and sets) by a **string separator**  


```python
# example of join method
seperator = "-"
li = "ABC"
joint = seperator.join(li)
print(joint)

li2 = ["1", "2"]
print(seperator.join(li2))
print(type(joint))
```

    A-B-C
    1-2
    <class 'str'>
    

---

**user input**:  

**`var = type(input("message to user"))`**  
* Keyword **"input"** used to provide input box to user  
* **Optional message**, however better practice to provide information on what to input  
* Defining **"type"** is **optional**, however note user inputs **default to strings**  


```python
# example of user input

name = input("Enter your name: ")
print("your name is:", name)
```

    Enter your name:  j
    

    your name is: j
    


```python
# example of user input defining user input type

age = int(input("Enter your age: "))
print("your age is:", age)
```

    Enter your age:  5
    

    your age is: 5
    

---

####  **Formatting Strings**  

**Place holders**:  

**`placeHolderVar = "some string with placeholder a {}, and place holder b {}"`**  
**`placeHolderVar.format(a,b)`**


* **`{}`** can be used as place holders to insert variables later  
* Call the variable with the placeholders followed by **`.format`** to insert variables  
* Placeholders can be **positional**, or identified by a **given name**, or by **index numbers**, note this will be index **of the variables provided** and not of the placeholder position index numbers  
* Can also format using the **keys from a dictionary** and reference dictionary in format with double star **\*\*dictVar**  
* **Class members** can be used in place holders such as **{a.attribute}** and the class referenced in the formatting **.format(a=Class())**  
* Must save to a new variable to save  


```python
# example of using place holders with strings
# positional example

myTemplate = "hello, my name is {} and I am {} old."

a = "Andy"
b = 35      # note this will be changed to a String when inserted

print(myTemplate.format(a,b))
```

    hello, my name is Andy and I am 35 old.
    


```python
# placeholders by reference

print("Your {what} cost £{amount}".format(what = "laptop", amount = 500))
```

    Your laptop cost £500
    


```python
# placeholders by index of given variables

myTemplate = "My new {1} is {0}"      # note index values refer to the variables given when formatting
colour = "red"
item = "car"

print(myTemplate.format(colour, item))
```

    My new car is red
    


```python
# Formatting with a dictionary

personDictionary = {'name': 'Eric', 'age': 74}

"Hello, {name}. You are {age}.".format(**personDictionary)
```




    'Hello, Eric. You are 74.'




```python
# Formatting class members

# define Person class
class Person:
    age = 23
    name = "Adam"

# format age
print("{p.name}'s age is: {p.age}".format(p=Person()))
```

    Adam's age is: 23
    

**F-Strings**:  

**`placeHolderVar = f"some string with placeholder a {var_a}, and placeholder b {var_b}"`**  

* Good for when you have a calculation to put inside the placeholder  
* F-strings do not require the use of "format"  
* Requires **f before string**, this can be **upper or lower** case  


```python
# formatting with f-strings

name = "Bill"
age = 54

print(f"{name} is {age} years old")
```

    Bill is 54 years old
    


```python
price = 12345.12345
age = 54321.54321

print(f"{age} and {price}")
```

    54321.54321 and 12345.12345
    

**Formatting types**:  

* Formatting types can be put in placeholders after the optional index/reference  

**`:<`**  Left aligns the result (within the available space)  
**`:>`**  Right aligns the result (within the available space)  
**`:^`**  Center aligns the result (within the available space)  
**`:=`**  Places the sign to the left most position  
**`:+`**  Use a plus sign to indicate if the result is positive or negative  
**`:-`**  Use a minus sign to show negative numbers minus sign  
**`: `**  Use a space to insert an extra space before positive numbers (and a minus sign before negative numbers)  
**`:,`**  Use a comma as a thousand separator  
**`:_`**  Use a underscore as a thousand separator  
**`:b`**  Binary format  
**`:c`**  Converts the value into the corresponding unicode character  
**`:d`**  Decimal format  
**`:e`**  Scientific format, with a lower case e  
**`:E`**  Scientific format, with an upper case E  
**`:f`**  Fix point number format  
**`:F`**  Fix point number format, in uppercase format (show inf and nan as INF and NAN)  
**`:g`**  General format  
**`:G`**  General format (using a upper case E for scientific notations)  
**`:o`**  Octal format  
**`:x`**  Hex format, lower case  
**`:X`**  Hex format, upper case  
**`:n`**  Number format  
**`:%`**  Percentage format  

**Decimal places, padding and truncating strings**:  

**`f"{*index/ref : *padding(number of spaces in front).*decimal places to display or max chars from string}"`**  
* Note the **`.`** between the padding and decimal places/chars to display  
* When specifying **decimals**, must follow with **`f`** to denote number format  
* To add padding with **strings**, must specify **allignment** **OR** number of **TOTAL** characters to be displayed  
    * e.g. **`f"{*index/ref : totalNumberCharacters . decimalPlacesToDisplay f}"`**  
* Can add a **character before padding** and this will be used **instead of the default space**, when doing this, the padding number will represent the max **WIDTH including the passed variable length**    


```python
# various examples of number formatting

num = 12345.12345

print("Without 'f' after decimal places: ", f"{num : .2}")
print("With 'f' after decimal places: ", f"{num : .2f}")
print("With .format method after decimal places: ", "{:.2f}".format(num))
print("With 50 padding spaces, no limit on decimal: ", f"{num : 50}")
```

    Without 'f' after decimal places:   1.2e+04
    With 'f' after decimal places:   12345.12
    With .format method after decimal places:  12345.12
    With 50 padding spaces, no limit on decimal:                                         12345.12345
    


```python
# truncating strings and string padding

alpha = "abcdefghijklmnopqrstuvwxyz"

print(f"{alpha :>50.3}")    # padding will not work for strings without allignment

print()
print("alphabet aligned central of * characters with total width of 50:")
print(f"{alpha :*^50}")        # note the alphabet characters are INCLUDED in the 50 padding/width total
```

                                                   abc
    
    alphabet aligned central of * characters with total width of 50:
    ************abcdefghijklmnopqrstuvwxyz************
    

**zfill** method:  

**`strVar.zfill(len)`**  
* Adds zeros (0) at the beginning of the string, until it reaches the specified length  
* If the value of the len parameter is less than the length of the string, no filling is done  


```python
# zfill method example

a = "hello"
b = "welcome to the jungle"      # longer than 10, so no filling done, but complete string is still kept
c = "10.000"

print(a.zfill(10))
print(b.zfill(10))
print(c.zfill(10))
```

    00000hello
    welcome to the jungle
    000010.000
    

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>Regular Expressions (Regex);</center>

**`import re`**  

**`text_to_search = "some string"`**  
**`patternVar = re.compile(r"patternToMatch")`**  
**`matchesVar = patternVar.RegExFunction(text_to_searchVar)`**  

**`for match in matchesVar:`**  
&emsp;&emsp;**`print(match)`**  

* Allow us to search for and match specific patterns of text  
* To use, we need to first import the **`re`** module  
* Compile method allows us to seperate out our patterns into a variable and easier to reuse that variable to perform multiple searches
* Use **`r`** before pattern to ensure string is treated as raw string  
* Try to make pattern to match as specific as possible, modify it as required to match further items  


```python
import re

text_to_search = '''
abcdefghijklmnopqrstuvwxyz
ABCDEFGHIJKLMNOPQRSTUVWXYZ
1234567890

Ha HaHa

MetaCharacters (Need to be escaped):
. ^ $ * + ? { } [ ] \ | ( )

coreyms.com

321-555-4321
123.555.1234

Mr. Schafer
Mr Smith
Ms Davis
Mrs. Robinson
Mr. T
'''

sentence = 'Start a sentence and then bring it to an end'

print("\tTab - escape character for tab")
print(r"\tTab - raw string")


# compile method allows us to seperate out our patterns into a variable and easier to reuse that variable to perform multiple searches

pattern = re.compile(r"abc")    # specifies pattern to match - search for raw string "abc" 

matches = pattern.finditer(text_to_search)     # use pattern specified to search the text "text_to_search" and store matches in a variable "matches" 

for match in matches:      # for loop used to print out matches
    print(match)          # span = beginning and end of the match indexes
    
print(text_to_search[1:4])     # using indexes found to print "abc




pattern = re.compile(r"coreyms\.com")    # to search for special characters, need to escape them

matches = pattern.finditer(text_to_search)      

for match in matches:      
    print(match) 
```

    	Tab - escape character for tab
    \tTab - raw string
    <re.Match object; span=(1, 4), match='abc'>
    abc
    <re.Match object; span=(142, 153), match='coreyms.com'>
    

**Metacharacters**:  

* Characters with a special meaning  
* If searching for a **literal metacharacter** it **MUST** be **escaped**  

|**Character**|**Description**|**Example**|**Example meaning**|
|:---|:---|:---|:---|
|**[ ]**|Defines a set of characters|"[a-m]"|Find all lower case characters alphabetically between "a" and "m"|
|<b>\\<b>|Signals a special sequence (can also be used to escape special characters)|"\d"|Find all digit characters|
|**.**|Matches any character (**except** newline character)|"he..o"|Search for a sequence that starts with "he", followed by two (any(.)) characters, and an "o"|
|**^**|Starts with|"^hello"|Check if the string starts with 'hello'|
|**\$**|Ends with|"planet$"|Check if the string ends with 'planet'|
|**?**|Zero or one occurrences|"he.?o"|Search for a sequence that starts with "he", followed by 0 or 1  (any(.)) character, and an "o"|
|**\***|Zero or more occurrences|"he.*o"|Search for a sequence that starts with "he", followed by 0 or more  (any(.)) characters, and an "o"|
|**+**|One or more occurrences|"he.+o"|Search for a sequence that starts with "he", followed by 1 or more  (any (.)) characters, and an "o"|
|**{ }**|Exactly the specified number of occurrences<br>or range of number of occurences {min, max}|"he.{2}o"<br>"he.{2,5}o"|Search for a sequence that starts with "he", followed by exactly 2 (any) characters, and an "o"<br>"he" followed by between 2 and 5 (any (.)) characters, and an "o"|
|**\|**|Either or|"falls\|stays"|Check if the string contains either "falls" or "stays"|
|**( )**|Capture and group<br>A group of characters to match|"(com\|net\|gov)"|matches "com" OR "net" OR "gov"<br>**\|** means OR|
|**(?P\<name\>)**|Name a group which can then be accessed by name rather than index|"(?P\<first\>\w+) (?P\<last\>\w+)"|Matches words and groups them. Here called "first" and "last"|
|**(?P=name)**|Used within a pattern to match against a named group|"(?P\<first\>\w+) (?P=first)"|Matches a word which repeats|
|**(?=...)**|Lookahead assertion<br>Matches if ... **does matches next**, but doesn’t consume any of the string|"Isaac (?!Asimov)"|matches "Isaac " only if it **is** followed by 'Asimov'|
|**(?!...)**|Negative lookahead assertion<br>Matches if ... **doesn’t match next**|"Isaac (?!Asimov)"|Matches 'Isaac ' only if it’s **not** followed by 'Asimov'|
|**(?<=...)**|Positive lookbehind assertion<br>Matches if current position in the string **is preceded** by a match for ... that ends at the current position|"(?<=abc)def"|Matches "def" in the string "abcdef"|
|**(?<!...)**|Negative lookbehind assertion<br>Matches if current position in the string is **not preceded** by a match for ... that ends at the current position|"(?<!abc)def"|Will **not** find a match in the string "abcdef"|

**Special Sequences**:  

* A special sequence is a \\ followed by one of the characters in the list below, and has a special meaning    
* Capitals negate the function of the lowercase special sequence  

|**Character**|**Description**|**Example**|**Example meaning**|
|:---|:---|:---|:---|
|**\A**|Returns a match if the specified characters are at the beginning of the string|"\AThe"|Check if the string starts with "The"|
|**\b**|Returns a match where the specified characters are at the beginning or at the end of a word|r"\\bain"<br>r"ain\b"|Check if "ain" is present at the beginning of a WORD<br>Check if "ain" is present at the end of a WORD<br>The "r" in the beginning is making sure that the string is being treated as a "raw string"|
|**\B**|Returns a match where the specified characters are present, but NOT at the beginning (or at the end) of a word|r"\Bain"<br>r"ain\B"|Check if "ain" is present, but NOT at the beginning of a word<br>Check if "ain" is present, but NOT at the end of a word<br>The "r" in the beginning is making sure that the string is being treated as a "raw string"|
|**\d**|Returns a match where the string contains digits (numbers from 0-9)|"\d"|Check if the string contains any digits (numbers from 0-9)|
|**\D**|Returns a match where the string DOES NOT contain digits|"\D"|Return a match at every non-digit character|
|**\s**|Returns a match where the string contains a white space character|"\s"|Return a match at every white-space character (space, tab, newline)|
|**\S**|Returns a match where the string DOES NOT contain a white space character|"\S"|Return a match at every NON white-space character (NOT spaces, tabs, newlines)|
|**\w**|Returns a match where the string contains any word characters (a-z, A-Z, 0-9, and underscore _ )|"\w"|Return a match at every word character (a-z, A-Z, 0-9, and underscore _ )|
|**\W**|Returns a match where the string DOES NOT contain any word characters|"\W"|Return a match at every NON word character (characters NOT between a and Z. Like "!", "?" white-space etc.)|
|**\Z**|Returns a match if the specified characters are at the end of the string|"Spain\Z"|Check if the string ends with "Spain"|

**Sets**:  

* A set is a set of characters inside a pair of square brackets **`[]`** with a special meaning  
* Each set represents 1 character position to search for, not multiple, i.e. [1-5][a-z] means search for the numbers 1-5 which are followed by a lowercase a-z e.g. 5b    
* Note **`-`** if placed at the beginning or end of a set, then the literal **`-`** character will be searched for, however when placed between 2 characters it can denote a range e.g. **`1-9`**  

|**Set**|**Description**|
|:---|:---|
|**[arn]**|Returns a match where one of the specified characters (a, r, or n) are present|
|**[a-n]**|Returns a match for any lower case character, alphabetically between a and n|
|**[^arn]**|Returns a match for any character **EXCEPT** a, r, and n|
|**[0123]**|Returns a match where any of the specified digits (0, 1, 2, or 3) are present|
|**[0-9]**|Returns a match for any digit between 0 and 9|
|**[0-5][0-9]**|Returns a match for any two-digit numbers from 00 and 59|
|**[a-zA-Z]**|Returns a match for any character alphabetically between a and z, lower case OR upper case|
|**[+]**|In sets, **`+`** **`*`** **`.`** **`\|`** **`( )`** **`$`** **`{ }`** have no special meaning, so [+] means: return a match for any + character in the string|

#### **RegEx functions**:  

* The **`re`** module offers a set of functions that allows us to search a string for a match  

**match** function:  

**`re.match(searchFor, textToSearch)`**  
**OR**  
**`patternVar.match(textToSearch)`**  
* Checks only at the start of a string, will **NOT** find anything matching from the middle or end of the string  
* Returns a match object   
* This is **NOT** an **iterable**  

**findall** function:  

**`re.findall(searchFor, textToSearch)`**  
**OR**  
**`patternVar.findall(textToSearch)`**  
* Returns a **list of strings** containing all matches  
* Returns an **empty list** if **no match**  
* If matching groups, will only return the groups matched, not entire pattern  

**finditer** function:  

**`re.finditer(searchFor, textToSearch)`**  
**OR**  
**`patternVar.finditer(textToSearch)`**  
* Returns match objects with more information and functionality than findall  

**search** function:  

**`re.search(searchFor, textToSearch)`**  
**OR**  
**`patterVar.search(textToSearch)`**  
* Returns a **match object** if there is a match anywhere in the string  
* Only returns the **first match**, is **NOT** an **iterable**  
* If there is more than one match, only the first occurrence of the match will be returned  
* If no match, **`None`** is returned  

**split** function:  

**`re.split(splitAt, textToSearch, maxSplit)`**  
* Returns a **list** where the string has been split at each match  
* **`maxSplit`** is optional and is the number of splits to stop at **(not the number of elements in list)**  
* If no matches, returns the original string as a single element in a list  

**sub** function:  

**`re.sub(replaceThis, withThis, textToSearch, count)`**  
* Replaces one or many matches with a string  
* **`count`** is optional and is the number of replacements to stop at  
* Returns a **string**  
* If no matches, returns the original string  
* when pattern matching using **groups**, the group numbers you wish to keep can be passed and this will replace the entire matched string with the found groups:  
$\;\;\;\;$**`newStringVar = patternWithGroupsVar.sub(r'\2\3', originalStringVar)`** 
    * This example replaces the matched string with the found groups with index 2 and 3  
    * If replacing with **named groups**, use **`\g<name>`** instead of the index  

#### **Match Objects**:  

* A Match Object is an object containing information about the search and the result  
* If there is **no match**, the value **None will be returned**, instead of the Match Object  

**Match object** methods:  

**span** method:  

**`matchObj.span()`**  
* Returns a tuple containing the start and end positions of the match  

**string** function:  

**`matchObj.string`**  
* Returns the string passed into the function initially to search  

**group** method:  

**`matchObj.group()`**  
* Returns the part of the string where there was a match  
* If pattern has group matching **`( | )`** then these groups can be retrieved with **indexing** or by **name** (if named, see metacharacter table above), group(0) will return everything which was matched  
* The dictionary the groups are contained in can be retrieved using **`matchObj.groupdict()`**  

#### **Flags**  

[RegEx flags link](https://www.pythontutorial.net/python-regex/python-regex-flags/)

**ignorecase** flag:  

**`re.compile(patternToMatch, re.IGNORECASE)`**  
* Can be added in with the pattern to be matched  
* Flag will match pattern regardless of upper or lower case characters  
* Shorthand **`re.I`** can be used too  

**dotall** flag:  

**`re.compile(patternToMatch, re.DOTALL)`**  
* By default **`.`** matches any characters except a newline. The re.DOTALL makes the **`.`** match all characters **including a newline**  
* Shorthand **`re.S`** can be used too  

**multiline** flag:  

**`re.compile(patternToMatch, re.MULTILINE)`**  
* The re.MULTILINE makes the **`^`** match at the beginning of a string and at the beginning of each line and $ matches at the end of a string and at the end of each line  
* Shorthand **`re.M`** can be used too  


```python
# Try to be as specific as possible when writting RegEx patterns to match
# Start by writting to match your first case, 
# see what it doesn't match that you want it to, and modify to capture that too

emails = '''
CoreyMSchafer@gmail.com
corey.schafer@university.edu
corey-321-schafer@my-work.net
'''

"""
written to match first email, (1-many lower and upper cases, followed by literal @ symbol, 
then 1-many lower and upper case letters, followed by literal . (escaped to avoid matching any character) then literal com
"""
pattern = re.compile(r'[a-zA-Z]+@[a-zA-Z]+\.com') 

pattern2 = re.compile(r'[a-zA-Z.]+@[a-zA-Z]+\.(com|edu)') # dot added to first set to match 2nd email, and edu added to group

pattern3 = re.compile(r'[a-zA-Z0-9.-]+@[a-zA-Z-]+\.(com|edu|net)') # 0-9 and - added to first set to match 3rd email, - added to domain set and net added to group

patternDemo = re.compile(r'[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z0-9-.]+')  # Another example of a pattern which can match email addresses



matches = pattern3.finditer(emails)

for match in matches:
    print(match)
```

    <re.Match object; span=(1, 24), match='CoreyMSchafer@gmail.com'>
    <re.Match object; span=(25, 53), match='corey.schafer@university.edu'>
    <re.Match object; span=(54, 83), match='corey-321-schafer@my-work.net'>
    


```python
# Showing the different returns for "finditer" and "findall" methods

urls = '''
https://www.google.com
http://coreyms.com
https://youtube.com
https://www.nasa.gov
'''

pattern = re.compile(r'https?://(www.)?(\w+)(.\w+)')

print("finditer method:")
matches = re.finditer(pattern, urls)

for match in matches:
    print(match)

print("\nfindall method:")
matches2 = re.findall(pattern, urls)

for match in matches2:
    print(match)
```

    finditer method:
    <re.Match object; span=(1, 23), match='https://www.google.com'>
    <re.Match object; span=(24, 42), match='http://coreyms.com'>
    <re.Match object; span=(43, 62), match='https://youtube.com'>
    <re.Match object; span=(63, 83), match='https://www.nasa.gov'>
    
    findall method:
    ('www.', 'google', '.com')
    ('', 'coreyms', '.com')
    ('', 'youtube', '.com')
    ('www.', 'nasa', '.gov')
    


```python
# Showing how groups can be useful and how to use RegEx to reformat a string....could easily be used to reformat a file too

urls = '''
https://www.google.com
http://coreyms.com
https://youtube.com
https://www.nasa.gov
'''

patternNoGroups = re.compile(r'https?://w?w?w?.?\w+.\w+')
patternWithGroups = re.compile(r'https?://(www\.)?(\w+)(\.\w+)')  # grouped into sub parts, (optional www.)(domain name)(top level domain)

def printing(pattern, groupNo):
    
    matches = pattern.finditer(urls)

    for match in matches:
            print(match.group(groupNo))

            
print("No grouping in pattern, returning group 0:")
printing(patternNoGroups, 0)
print("\nFrom pattern with grouping;")
print("\n1st group, (optional www.):")
printing(patternWithGroups, 1)
print("\n2nd group, (domain name):")
printing(patternWithGroups, 2)


# Using sub method to reformat a string
# sub method used to replace all the matched strings with the found groups 2 and group 3 (domain name and top level domain)
subbed_urls = patternWithGroups.sub(r'\2\3', urls)

print("\nSubbed string:" + subbed_urls)
```

    No grouping in pattern, returning group 0:
    https://www.google.com
    http://coreyms.com
    https://youtube.com
    https://www.nasa.gov
    
    From pattern with grouping;
    
    1st group, (optional www.):
    www.
    None
    None
    www.
    
    2nd group, (domain name):
    google
    coreyms
    youtube
    nasa
    
    Subbed string:
    google.com
    coreyms.com
    youtube.com
    nasa.gov
    
    


```python
urls = '''
https://www.google.com
http://coreyms.com
https://youtube.com
https://www.nasa.gov
'''

patternWithGroups = re.compile(r'https?://(www\.)?(\w+)(\.\w+)')  # grouped into sub parts, (optional www.)(domain name)(top level domain)

# Using sub method to reformat a string
# sub method used to replace all the matched strings with the found groups 2 and group 3 (domain name and top level domain)
subbed_urls = patternWithGroups.sub(r'\2\3', urls)


print("Original string:" + urls)
print("\nSubbed string:" + subbed_urls)
```

    Original string:
    https://www.google.com
    http://coreyms.com
    https://youtube.com
    https://www.nasa.gov
    
    
    Subbed string:
    google.com
    coreyms.com
    youtube.com
    nasa.gov
    
    


```python
# naming groups and uses

nameString = "Joe Blogs"

pattern = re.compile(r"(?P<first>\w+) (?P<last>\w+)")

match = pattern.match(nameString)

print("First name: " + match.group("first"))
print("Last name: " + match.group("last"))

lastNameFirst = pattern.sub(r"\g<last> \g<first>", nameString)

print("Names swapped: " + lastNameFirst)

print("Group dictionary:", match.groupdict())
```

    First name: Joe
    Last name: Blogs
    Names swapped: Blogs Joe
    Group dictionary: {'first': 'Joe', 'last': 'Blogs'}
    


```python
# Matching repeated patterns with named groups

text = "here here is some random random text"

pattern = re.compile(r"(?P<word>\w+) (?P=word)")

matches = pattern.finditer(text)

for match in matches:
    print(match)
```

    <re.Match object; span=(0, 9), match='here here'>
    <re.Match object; span=(11, 14), match='s s'>
    <re.Match object; span=(18, 31), match='random random'>
    

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>Tuples;</center>

#### **tuples** :   

**`tupVar = (ele1, ele2, ele3)`**

* Tuples are compound data types
* They are an **ordered sequence**
* Comma separated elements within parenthesis, can contain **`str`**, **`int`** and **`float`**
* Have **round brackets**
* Tuples are **immutable**, ie cant change them. As a result, if we want to manipulate a tuple, we must assign a variable or create a new tuple


```python
# example of a tuple, note round brackets
tuple_example=(2, "a thing", 9, 5)
print(tuple_example)
```

    (2, 'a thing', 9, 5)
    


```python
# can be indexed like strings
tuple_example[0]
```




    2



**concatenate** tuples:  

**`newTupVar = tup1Var + (newEle1, newEle2)`**


```python
# can concatenate, but note a new variable HAS to be assigned
tuple2 = tuple_example + (5.6, "and this")
print(tuple2)
```

    (2, 'a thing', 9, 5, 5.6, 'and this')
    


```python
# can slice like strings: 
tuple2[2:4]
```




    (9, 5)




```python
# use len function to obtain number of elements
len(tuple2)
```




    6



**sorted** function:  

**`outListVar = sorted(tupVar, key=None, reverse=False)`**  
* Use function to sort a tuple, list or set, but note it will **output as a list**  
* **`reverse`** is **optional** and set to False if not supplied  
* **`key`** is **optional** and is usually a function when passed, this will be used on each **value in the list** to determine the resulting order, Note this can be used to access values in a list of dictionaries for sorting    
* **`key`** will be used to determine sort order, but **original values** will be **used in output**  
* A new variable must be assigned to save change  
* **`sorted`** function does not work on **`int`** and **`str`** at the same time  
* **Beware** of typecasting a sorted list back to a set as a set by definition is **unordered**   


```python
# example of `sorted` function
# note this function outputs as a list

tupleA = ("A", "Z", "F", "C")
print(tupleA)
print("tupleA Type:", type(tupleA))

a_sorted = sorted(tupleA)
print(a_sorted)
print("a_sorted Type:", type(a_sorted))
```

    ('A', 'Z', 'F', 'C')
    tupleA Type: <class 'tuple'>
    ['A', 'C', 'F', 'Z']
    a_sorted Type: <class 'list'>
    


```python
# example of using `sorted` function when both `int` and `str` are in a tuple
print(tuple2)
tuple2_Sorted = sorted(tuple2)
```

    (2, 'a thing', 9, 5, 5.6, 'and this')
    


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_6032/2710235088.py in <module>
          1 # example of using `sorted` function when both `int` and `str` are in a tuple
          2 print(tuple2)
    ----> 3 tuple2_Sorted = sorted(tuple2)
    

    TypeError: '<' not supported between instances of 'str' and 'int'



```python
# sorted function

list1 = [1,5,3,2]

sorted(list1)
print(list1)   # must assign variable to save change
```

    [1, 5, 3, 2]
    


```python
# sorted function being assigned to a new variable to save change and showing reverse parameter

list1 = [1,5,3,2]

a = sorted(list1,reverse=True)
print(a)
```

    [5, 3, 2, 1]
    

**sort** method:  

**`tupVar.sort(reverse=False)`**  
* Similar to sorted function, however this **will affect original variable**
* Use method to sort a tuple or list but note it will **output as a list**  
* **"reverse"** is **optional** and set to False if not supplied  
* **`sort`** method does not work on **`int`** and **`str`** at the same time  
* **Beware** of typecasting a sorted list back to a set as a set by definition is **unordered**   


```python
# sort method

tup1 = [5,3,10,13]

tup1.sort()
print(tup1) # changes original variable, note its converted to a list
```

    [3, 5, 10, 13]
    

**nest** tuples:  

**`tupVar = (ele1, (nesTupVar), ele3)`**  
* Other tuples can be **nested** in a tuple


```python
# showing nesting of a Tuple
t1=(3,"Hello",1)
t2=(8,(t1),4)
print(t2)
```

    (8, (3, 'Hello', 1), 4)
    

**indexing** nested tuples:  

**`var[outIndex][nextLayerIndex][...][lastLayerIndex]`**


```python
# indexing of nested tuples
print("t1:",t1)
print("t2:",t2)
print("number of elements in t2:", len(t2))
# t1 elements can be accessed as follows:
t2[1][1][4]  # accessing 5th element of 2nd element of nested t1
```

    t1: (3, 'Hello', 1)
    t2: (8, (3, 'Hello', 1), 4)
    number of elements in t2: 3
    




    'o'



**unpacking** tuples:  

**`var1, var2 = tupVar`**  
* Allows elements of a tuple to be assigned to variables in one line of code  
* Note there will need to be as many variables as elements or an error will occur  
* See lists for unpacking more elements than variables  
* Dictionary key-value pairs can be unpacked to tuples using the **`.items()`** method  


```python
# Showing elements of a tuple being unpacked
x, y = ("a", 2)

print(x, y)
```

    a 2
    


```python
# Dictionary key-value pairs being unpacked as tuples
my_dict = {'one': 1, 'two':2, 'three': 3}
a, b, c = my_dict.items()  # Unpacking key-value pairs

print(a, b)
```

    ('one', 1) ('two', 2)
    

**packing** tuples:  

**`tupVar = ele1, ele2......`**  
* Packs elements into a tuple  
* See lists for packing leading/trailing elements into a single list  


```python
# Showing 3 elements being packed into a tuple
a = 1,2,3

print(a)
```

    (1, 2, 3)
    

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>Lists;</center>

#### **lists**:   

**`listVar = [ele1, ele2, ele3]`**

* Lists are also compound data types
* Also an ordered sequence
* Lists are represented with **square brackets**
* Lists are **mutable**, meaning we can change them
* They can contain **`str`**, **`float`**, **`int`**, can also **nest** other **lists**, **tuples** and **other data structures**

**concatenate** lists:  

**`newListVar = list1Var + [newEle1, newEle2]`**


```python
# example of concatinating a list by adding
l1 = ["MJ", 10.1, 1982]
print("l1:", l1)
l2 = l1 + ["pop", 10]
print("l2:", l2)
```

    l1: ['MJ', 10.1, 1982]
    l2: ['MJ', 10.1, 1982, 'pop', 10]
    

**sorted** function:  

**`outListVar = sorted(listVar,key=None, reverse=False)`**  
* Use function to sort a tuple, list or set, but note it will **output as a list**  
* **`reverse`** is **optional** and set to False if not supplied  
* **`key`** is **optional** and is usually a function when passed, this will be used on each **value in the list** to determine the resulting order, Note this can be used to access values in a list of dictionaries for sorting    
* **`key`** will be used to determine sort order, but **original values** will be **used in output**  
* A new variable must be assigned to save change  
* **`sorted`** function does not work on **`int`** and **`str`** at the same time  
* **Beware** of typecasting a sorted list back to a set as a set by definition is **unordered**   


```python
# example of `sorted` function
# note this function outputs as a list even when used to sort a tuple or set

listA = ["A", "Z", "F", "C"]
print(listA)
print("listA Type:", type(listA))

a_sorted = sorted(listA)
print(a_sorted)
print("a_sorted Type:", type(a_sorted))
```

    ['A', 'Z', 'F', 'C']
    listA Type: <class 'list'>
    ['A', 'C', 'F', 'Z']
    a_sorted Type: <class 'list'>
    


```python
# sorted function

list1 = [1,5,3,2]

sorted(list1)
print(list1)   # must assign variable to save change
```

    [1, 5, 3, 2]
    


```python
# sorted function being assigned to a new variable to save change and showing reverse parameter

list1 = [1,5,3,2]

a = sorted(list1,reverse=True)
print(a)
```

    [5, 3, 2, 1]
    


```python
# Using len function as key to sort
words = ['banana', 'pie', 'Washington', 'book']
sorted(words, key=len)
```




    ['pie', 'book', 'banana', 'Washington']




```python
# Function passed to key will be used to determine sort order, but original values will be used in output
names_with_case = ['harry', 'Suzy', 'al', 'Mark']

print(sorted(names_with_case))
print(sorted(names_with_case, key=str.lower))
```

    ['Mark', 'Suzy', 'al', 'harry']
    ['al', 'harry', 'Mark', 'Suzy']
    

**sort** method:  

**`listVar.sort(reverse=False)`**  
* Similar to sorted function, however this **will affect original variable**
* Use method to sort a tuple or list but note it will **output as a list**  
* **"reverse"** is **optional** and set to False if not supplied  
* **`sort`** method does not work on **`int`** and **`str`** at the same time  
* **Beware** of typecasting a sorted list back to a set as a set by definition is **unordered**   


```python
# sort method

list1 = [5,3,10,13]

list1.sort()
print(list1) # changes original variable
```

    [3, 5, 10, 13]
    

**extend** method:  

**`listVar.extend([newEle1, newEle2])`**  
* This will add each element as individual elements


```python
# example of `extend` method
l1.extend(["pop", 10,])
print("l1:", l1)
```

    l1: ['MJ', 10.1, 1982, 'pop', 10]
    

**append** method:  

**`listVar.append([newEle1, newEle2])`**  
* This will add all the new elements as only one new element (nested list)


```python
# showing append method and comparing number of elements
print("l1 before append:", l1)
print("l1 number of elements before append:", len(l1))
l1.append(["pop", 10])
print("l1 after append:", l1)
print("l1 number of elements after append", len(l1))
```

    l1 before append: ['MJ', 10.1, 1982, 'pop', 10]
    l1 number of elements before append: 5
    l1 after append: ['MJ', 10.1, 1982, 'pop', 10, ['pop', 10]]
    l1 number of elements after append 6
    

>With lists, **every time a method is applied**, the list changes unless assigned to a new variable

**insert** method:  

**`listVar.insert(index, newEle)`**  
* Inserts a element provided at index given  


```python
# example of insert method 

list1 = ["apple", "orange", "lemon"]
print("before insert: ", list1)

list1.insert(1, "pear")
print("after insert: ", list1)
```

    before insert:  ['apple', 'orange', 'lemon']
    after insert:  ['apple', 'pear', 'orange', 'lemon']
    

**change** a list element:  

**`listVar[indexOrSlice] = newEle`**  
* This will replace the indexed or sliced element with the new element


```python
# example of changing an element in a list, note difference when slicing if not using brackets
print("l1 before change:", l1)
l1[0] = "New1"
print("l1 after single element [0] change:", l1)
l1[1:5] = "New2"
print("l1 after slicing [1:5] change, no brackets:", l1)
l1[2:4] = ["New3"]
print("l1 after slicing [2:4] change, with brackets:", l1)
```

    l1 before change: ['MJ', 10.1, 1982, 'pop', 10, ['pop', 10]]
    l1 after single element [0] change: ['New1', 10.1, 1982, 'pop', 10, ['pop', 10]]
    l1 after slicing [1:5] change, no brackets: ['New1', 'N', 'e', 'w', '2', ['pop', 10]]
    l1 after slicing [2:4] change, with brackets: ['New1', 'N', 'New3', '2', ['pop', 10]]
    

**delete** a list element:  

**`del(listVar[indexOrSlice])`**   
      
**delete** list:  

**`del(listVar)`**


```python
# example of deleting an element with `del`
print("l1 before del:",l1)
# deletes first element of list
del(l1[0])
print("l1 after del:",l1)
# can even delete variable completely...
del(l1)
print("After list has been deleted")
print(l1)
```

    l1 before del: ['New1', 'N', 'New3', '2', ['pop', 10]]
    l1 after del: ['N', 'New3', '2', ['pop', 10]]
    After list has been deleted
    


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_6032/784032891.py in <module>
          7 del(l1)
          8 print("After list has been deleted")
    ----> 9 print(l1)
    

    NameError: name 'l1' is not defined


**split** method:  

**`listVar = strVar.split(sep=None, maxsplit=-1)`**  
* Converts string to a list of words, standard delimiter is a **space**  
* **`sep`** is the delimiter, None = **default whitespaces**  
* **`maxsplit`** is the maximum number of splits to do, -1 = **default no limit**  


```python
# example of converting string to a list
l = "Hard rock"
print("l:",l)
print("l type:",type(l))
l = l.split()
print("l after split:",l)
print("l type after split:",type(l))
```

    l: Hard rock
    l type: <class 'str'>
    l after split: ['Hard', 'rock']
    l type after split: <class 'list'>
    

Split on a specific **delimiter** by putting argument in the brackets:  

**`listVar = strVar.split("delimiter")`**


```python
# example of splitting on commas
li = "A, B, C, D"
li = li.split(",")
print(li)
print(type(li))
```

    ['A', ' B', ' C', ' D']
    <class 'list'>
    

**join** method:  

**`string.join(iterable)`**  
* Creates **strings** from iterable objects  
* Joins each **element** of an iterable (such as lists, strings, tuples, dictionaries and sets) by a **string separator**  


```python
# example of join method
seperator = " -"
joint = seperator.join(li)
print(joint)
print(type(joint))
```

    A - B - C - D
    <class 'str'>
    

**copy list**:  

**`listVar1 = listVar2`**  
* **Beware** copying by reference, when one variable is set to another changing one element in a list on one variable will affect the other


```python
# example of copying a list by reference and changing one element in a list which affects the other:
a=[1,2]
b=a
print("a before element changed:",a)
print("b before element changed:",b)
a[0]="a" # just 1st element in a is changed, but affects both "a", and "b"
print("a after change:",a)
print("b after change:",b)
```

    a before element changed: [1, 2]
    b before element changed: [1, 2]
    a after change: ['a', 2]
    b after change: ['a', 2]
    

**cloning list**:  

**`listVar1 = listVar2[:]`**  
* This protects against changes in one list affecting the other


```python
# example of cloning
a = [1, 2]
b = a[:]
print("a before any change:", a)
print("b before any change:", b)
a[-2] = [2, 2] # just a changed, also example of negative indexing
print("a after change:", a)
print("b after change:", b)
```

    a before any change: [1, 2]
    b before any change: [1, 2]
    a after change: [[2, 2], 2]
    b after change: [1, 2]
    

**unpacking** lists:  

**`var1, var2 = listVar`**  
* Allows elements of a list to be assigned to variables in one line of code  
* Note there will need to be as many variables as elements or an error will occur  
* Variables proceeded with **`*`** will be an empty list unless there are remaining elements after the manditory variables (those without **`*`** ) in which case all remaining elements will be put in this list  


```python
# Showing elements of a list being unpacked
x, y = ["a", 2]

print(x, y)
```

    a 2
    


```python
# Leading elements unpacked to a list
*a,b = [1,2,3,4,5]

print("a: ", a, "\n" + "b: ", b)
```

    a:  [1, 2, 3, 4] 
    b:  5
    


```python
# Trailing elements unpacked to a list
a, *b = [1,2,3,4]

print("a: ", a, "\n" + "b: ", b)
```

    a:  1 
    b:  [2, 3, 4]
    


```python
# Starred variables will be filled after manditory variables, if not enough, the starred variable will be an empty list
a, b, *c, d, e = [1,2,3,4]

print(a,b,c,d,e)
```

    1 2 [] 3 4
    

**packing** lists:  

**`*listVar, = ele1, ele2......`**  
* With exactly the same number of variables as elements will produce a **tuple** not a list  
* To pack elements into a list, proceed variable name with a **`*`** and follow it with **`,`**  
* Other vaiables can be added to assign other elements to variables at the same time  


```python
# Showing 3 elements being packed into a list
*a, = 1,2,3

print(a)
```

    [1, 2, 3]
    


```python
# Showing first element being assigned to a, and the rest being packed to a list
a, *b, = 1,2,3,4

print(a,b)
```

    1 [2, 3, 4]
    

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>Dictionairies;</center>

#### **dictionaries**:   

**`dictVar = {"key1" : val1, "key2" : [listVal1, listVal2], "key3" : (tupVal1, tupVal2)}`**  

* Dictionaries are a type of collection
* Uses **curley brackets**
* Dictionaries have keys and values as lists have indexes and elements, but the keys do not need to be integers, they are usually characters 
* **"keys"** must be **mutable and unique**
* **"keys"** can **only** be **strings, numbers or tuples**
* **"values"** can be **any data type**
* **"values"** can be **immutable, mutable and duplicates** 
* **"keys"** and values separated with a **colon**
* "key"/"value" pairs are separated with a comma

**lookup dictionary value** using key:  

**`dictVar[key]`**  
* This is essentially the same as indexing
* Note this **will raise an error** if key is not present


```python
# example showing looking up a value using the key 
dict = {"Thriller":"1982","Back in Black":"1980","The Dark Side of the Moon":"1973","The Bodyguard":"1992","Bat Out of Hell":"1977","Their Greatest...":"1976","Saturday Night Fever":"1977","Rumours":"1977"}
dict["Back in Black"]
```




    '1980'




```python
# showing dictionary lookup when key is not present  

dict["a"]
```


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_6032/256721380.py in <module>
          1 # showing dictionary lookup when key is not present
          2 
    ----> 3 dict["a"]
    

    KeyError: 'a'


**get** method:  

**`dictVar.get(key)`**  
* This will return the value of the key given  
* Note this will **not raise an error** if key is not present  


```python
# example of get method

myDict = {"val1":1, "val2":2}

myDict.get("val2")
```




    2




```python
# example showing no error generated if key not present with get method

myDict = {"val1":"a", "val2":"b"}

myDict.get("val3")

print("Note no error when key not present with get method")
```

    Note no error when key not present with get method
    

**add dictionary value**:  

**`dictVar[newKey] = "newVal"`**


```python
# example showing adding a value to a dictionary 
dict["Graduation"] = "2007"
print(dict)
```

    {'Thriller': '1982', 'Back in Black': '1980', 'The Dark Side of the Moon': '1973', 'The Bodyguard': '1992', 'Bat Out of Hell': '1977', 'Their Greatest...': '1976', 'Saturday Night Fever': '1977', 'Rumours': '1977', 'Graduation': '2007'}
    

**delete dictionary entry**:  

**`del(dictVar[key])`**  
* This will delete the entered key and its associated values 
* Can also delete entire dictionary by just providing dictVar with no key  


```python
# example showing deleting a dictionary key and associated value 

dict = {1:"a", 2:"b", 3:"c"}

del(dict[2])
```


```python
print(dict)
```

    {1: 'a', 3: 'c'}
    


```python
# example showing del can delete entire dictionary

del(dict)

print(type(dict))
```

    <class 'type'>
    

**clear** method:  

**`dictVar.clear()`**  
* Removes all elements from a dictionary but **does not** delete dictionary itself  


```python
# clearing a dictionary 

dict = {1:"a", 2:"b", 3:"c"}

dict.clear()
print(dict)
```

    {}
    

**pop** method:  

**`dictVar.pop(keyOfValueToBeRemoved)`**  
* Will remove key and value from dictionary  
* At the same time, it will **"pop" and return** the **value**  


```python
#showing a value being "popped" from a dictionary

dict = {1:"a", 2:"b", 3:"c"}

dict.pop(2)
```




    'b'




```python
print(dict)
```

    {1: 'a', 3: 'c'}
    

**popitem** method:  

**`dictVar.popitem()`**  
* Removes **last** key and value from dictionary  
* **Pops and returns** the key-value **pair**  


```python
dict = {1:"a", 2:"b", 3:"c"}

dict.popitem()
```




    (3, 'c')




```python
print(dict)
```

    {1: 'a', 2: 'b'}
    

**change value**:  

**`dictVar[keyOfValueToBeChanged] = newVal`**  
* This will replace the old value with the new value  


```python
# example changing a dictionary value

dict = {1:"a", 2:"b", 3:"c"}

print("Before change: ", dict)

dict[2] = "z"
print("After change: ", dict)
```

    Before change:  {1: 'a', 2: 'b', 3: 'c'}
    After change:  {1: 'a', 2: 'z', 3: 'c'}
    

**in** command:  

**`keyToSearch in dictVar`**  
* This can be used to search a dictionary if a **"key"** is present or not  
* Note this is **case sensitive**   
* If present, it'll return True, else it'll return False  
* Can also be used on Sets to check if element is present


```python
# example using the "in" command searching to see if "The Bodyguard" is present
"The Bodyguard" in dict
```




    False



**view all keys** method:  

**`dictVar.keys()`**  
* This will return all "keys" in a dictionary as a list-like object (<class 'dict_keys'>)


```python
# example showing all keys in dictionary 
dict.keys()
```




    dict_keys([1, 2, 3])



**view all values** method:  

**`dictVar.values()`**  
* This will return all "values" in a dictionary as a list-like object (<class 'dict_values'>)


```python
# example showing values method to lookup all values in a dictionary
dict.values()
```




    dict_values(['a', 'z', 'c'])



**items()** method:  

**`dictVar.items()`**  
* Returns a **view object** containing the **key-value pairs as tuples in a list**  
* Note this **will change as the object it references does** even when saved to a variable previously  
* Can be used in loops and dictionary comprehension  


```python
# Demonstrating items() method and that it reflexs the object it references

car = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}

x = car.items()

car["year"] = 2018

print(x)
```

    dict_items([('brand', 'Ford'), ('model', 'Mustang'), ('year', 2018)])
    


```python
# Using items() method in a for loop

month_days={
    "Jan": 31,
    "Feb": 28,
    "Mar": 31,
    "Apr": 30,
    "May": 31,
    "Jun": 30,
    "Jul": 31,
    "Aug": 31,
    "Sep": 30,
    "Oct": 31,
    "Nov": 30,
    "Dec": 31
    
}

print(month_days.items())
print()

#items retuns a list of pairs (key/value), similar to enumerate
for mth,days in month_days.items(): 
    print (mth,"has",days,"days")
```

    dict_items([('Jan', 31), ('Feb', 28), ('Mar', 31), ('Apr', 30), ('May', 31), ('Jun', 30), ('Jul', 31), ('Aug', 31), ('Sep', 30), ('Oct', 31), ('Nov', 30), ('Dec', 31)])
    
    Jan has 31 days
    Feb has 28 days
    Mar has 31 days
    Apr has 30 days
    May has 31 days
    Jun has 30 days
    Jul has 31 days
    Aug has 31 days
    Sep has 30 days
    Oct has 31 days
    Nov has 30 days
    Dec has 31 days
    


```python
# example using dictionary comprehension

only_31_days = { key.upper():value for key,value in month_days.items() if value==31}

print(only_31_days)
```

    {'JAN': 31, 'MAR': 31, 'MAY': 31, 'JUL': 31, 'AUG': 31, 'OCT': 31, 'DEC': 31}
    

**unpacking** dictionaries:  

**`var1, var2 = dictVar`**  
* Allows **keys** of a dictionary to be assigned to variables in one line of code  
* To unpack **values** use **`dictVar.values()`**  
* To unpack **key-value pairs as tuples** use **`dictVar.items()`**  
* Note there will need to be as many variables as keys or an error will occur  
* Variables proceeded with **`*`** will be an empty list unless there are remaining keys after the manditory variables (those without **`*`** ) in which case all remaining keys will be put in this list  


```python
# Showing keys of a dictionary being unpacked
my_dict = {'one': 1, 'two':2, 'three': 3}
a, b, c = my_dict  # Unpack keys

print(a, b)
```

    one two
    


```python
# Showing keys of a dictionary being unpacked with multiple keys added to a list variable
my_dict = {'one': 1, 'two':2, 'three': 3}
a, *b = my_dict  # Unpack keys

print(a, b)
```

    one ['two', 'three']
    


```python
# Values of a dictionary being unpacked
my_dict = {'one': 1, 'two':2, 'three': 3}
a, b, c = my_dict.values()  # Unpack values

print(a, b)
```

    1 2
    


```python
# Key-value pairs being unpacked as tuples
my_dict = {'one': 1, 'two':2, 'three': 3}
a, b, c = my_dict.items()  # Unpacking key-value pairs

print(a, b)
```

    ('one', 1) ('two', 2)
    

**sorting** dictionaries in a list:  

**`outListVar = sorted(listOfDictVar, key=lambda itm: itm["dictKeyToSortBy"])`**  
* Usually used to sort a tuple, list or set, but note it will **output as a list**  
* **`Reverse`** is **optional** and set to False if not supplied  
* **`key`** is **optional** and is usually a function when passed, this will be used on each **value in the list** to determine the resulting order, Note this can be used to access values in a list of dictionaries for sorting    
* **`key`** will be used to determine sort order, but **original values** will be **used in output**  
* A new variable must be assigned to save change  
* **`sorted`** function does not work on **`int`** and **`str`** at the same time  
* **Beware** of typecasting a sorted list back to a set as a set by definition is **unordered**   


```python
# Sorting a list of dictionaries by value using sorted and a lambda function
dictList = [{"num" : 3, "let" : "d"},
            {"num" : 2, "let" : "z"},
            {"num" : 5, "let" : "a"}]

sortBy = "let"
sorted(dictList, key=lambda itm: itm[sortBy])
```




    [{'num': 5, 'let': 'a'}, {'num': 3, 'let': 'd'}, {'num': 2, 'let': 'z'}]



[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

--- 

## <center>Sets;</center>

**sets**:  

**`setVar = {"ele1", "ele2", "ele3"}`**  

* Type of collection  
* Uses **curley brackets**  
* Sets are **unordered** meaning element positions are not recorded   
* Sets only have **unique elements**  
* Duplicates can be present in the creation of a set, but there will only be one unique element once the set is created

**set** function:  

**`set(listVar)`**  
* This will convert a list to a set (typecasting)


```python
# example showing a list being converted to a set 
album_list = ["Micheal Jackson", "Thriller", "Thriller", "1982"]
print("album_list:", album_list)
print("album_list type:", type(album_list))
album_set = set(album_list)
print("album_set:", album_set) # notice no duplicate elements
print("album_set type:", type(album_set))
```

    album_list: ['Micheal Jackson', 'Thriller', 'Thriller', '1982']
    album_list type: <class 'list'>
    album_set: {'1982', 'Thriller', 'Micheal Jackson'}
    album_set type: <class 'set'>
    

**sorted** function:  

**`outListVar = sorted(setVar, key=None, reverse=False)`**  
* Use function to sort a tuple, list or set, but note it will **output as a list**  
* **`reverse`** is **optional** and set to False if not supplied  
* **`key`** is **optional** and is usually a function when passed, this will be used on each **value in the list** to determine the resulting order, Note this can be used to access values in a list of dictionaries for sorting    
* **`key`** will be used to determine sort order, but **original values** will be **used in output**  
* A new variable must be assigned to save change  
* **`sorted`** function does not work on **`int`** and **`str`** at the same time  
* **Beware** of typecasting a sorted list back to a set as a set by definition is **unordered**  



```python
# sorted function
set1 = {5,5,10,1,0}

sorted(set1)
print(set1)   # must assign variable to save change
```

    {0, 1, 10, 5}
    


```python
# example of `sorted` function
# note this function outputs as a list

setA = {"A", "Z", "F", "C"}
print(setA)
print("setA type:", type(setA))

a_sorted = sorted(setA)
print(a_sorted)
print("a_sorted type:", type(a_sorted))
```

    {'C', 'A', 'F', 'Z'}
    setA type: <class 'set'>
    ['A', 'C', 'F', 'Z']
    a_sorted type: <class 'list'>
    


```python
# sorted function being assigned to a new variable to save change and showing reverse parameter
set2 = {5,5,10,1,0}

a = sorted(set2,reverse=True)
print(a)         # note outputs as a list

# beware of typecasting a sorted list back to a set as a set is unordered by definition 
print(set(a))
```

    [10, 5, 1, 0]
    {0, 1, 10, 5}
    

**update** method:  

**`setToBeUpdated.update(setToGetElementsFrom)`**  
* Updates a set by **adding** items from another set  


```python
setForUpdate = {9,9,11,15}
setToAdd = {1,1,5,6}

print("before update -")
print("setForUpdate: ", setForUpdate)
print("setToAdd: ", setToAdd)

setForUpdate.update(setToAdd)
print("after update -")
print("setForUpdate: ", setForUpdate)
```

    before update -
    setForUpdate:  {9, 11, 15}
    setToAdd:  {1, 5, 6}
    after update -
    setForUpdate:  {1, 5, 6, 9, 11, 15}
    

**add** method:  

**`setVar.add(newEle)`**  
* This will add a new element to a set  
* If same element is added twice, nothing will happen as cannont have duplicates


```python
# example showing adding an element to a set
a = {"Thriller", "Back in Black", "AC/DC"} # set creation
print(a)
a.add("NSYNC") # adding element to set
print("After adding element:", a)
a.add("NSYNC") # showing adding a second time doesn't affect set
print("After adding element again:", a)
```

    {'AC/DC', 'Thriller', 'Back in Black'}
    After adding element: {'AC/DC', 'Thriller', 'Back in Black', 'NSYNC'}
    After adding element again: {'AC/DC', 'Thriller', 'Back in Black', 'NSYNC'}
    

**remove** method:  

**`setVar.remove(ele)`**  
* This will remove element from a set
* Note this **will raise an error** if element to be removed is not present


```python
# example showing removal of an element from a set
print("Set before element removal", a)
a.remove("NSYNC") # removing element from set
print("Set after removal", a)
```

    Set before element removal {'AC/DC', 'Thriller', 'Back in Black', 'NSYNC'}
    Set after removal {'AC/DC', 'Thriller', 'Back in Black'}
    


```python
# example showing error when trying to remove item that is not present in a set

errorSet = {1,2,3}

errorSet.remove(5)
```


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_6032/4056804799.py in <module>
          3 errorSet = {1,2,3}
          4 
    ----> 5 errorSet.remove(5)
    

    KeyError: 5


**discard** method:  

**`setVar.discard(ele)`**  
* This will remove element from a set  
* Note this will **not raise an error** if element to be removed is not present  


```python
# demonstrating discard method

discardSet = {1,2,3,4}
print("Before discard: ", discardSet)

discardSet.discard(2)
print("After discard: ", discardSet)
```

    Before discard:  {1, 2, 3, 4}
    After discard:  {1, 3, 4}
    


```python
# showing discard method when element not present

discardSet2 = {1,2,3,4}

discardSet2.discard(5)

print("Note no error when discarding an element not present in set")
```

    Note no error when discarding an element not present in set
    

**in** command:  

**`eleToSearch in setVar`**  
* This can be used to search a set if an **element** is present or not  
* Note this is **case sensitive**   
* If present, it'll return True, else it'll return False
* Can also be used on Dictionaires to check if a key is present


```python
# example using the "in" command searching to see if "AC/DC" is present
"AC/DC" in a
```




    True



1. **Union:** $C=A\cup B$. $C$ is the set obtained by merging $A$ and $B$: $a,b \in C$
1. **Intersection:** $D=A\cap B$. $D$ is the set obtained by taking the common elements from A and B. This means that if $a\in A, b\in B$, then $a \in D$ if and only if $a=b$

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/86/A_union_B.svg/1280px-A_union_B.svg.png" width="20%" style="background-color:white">

If $A$ and $B$ do not have elements in common, then they are said _disjoint_: $A\cap B = \emptyset$, where $\emptyset$ denotes the empty set (the set with no elements).

If $A\cap B = A$, this means that all the elements in $A$ are contained in $B$. Therefore, if $B$ contains $A$, then it is denoted as $A\subset B$ (or $A\subseteq B$ depending on the case).

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b0/Venn_A_subset_B.svg/1024px-Venn_A_subset_B.svg.png" width="20%" style="background-color:white">

**intersection** method:  

**`intersection_SetVar = set1_Var & set2_Var`**  
* Uses ampersand operator **`&`**  
* This would compare set1 and set2 elements, returning the common elements in the new variable


```python
# example using the intersection method (ampersand)
set1 = {"AC/DC", "Back in Black", "Thriller"} # define set1
set2 = {"AC/DC", "Back in Black", "The Dark Side of the Moon"} # define set2, note similar elements to set1
print("set1:", set1)
print("set2:", set2)
intersection_Set = set1 & set2 # combining common elements from set1 and set2 into new set variable
print("intersection set:", intersection_Set)
```

    set1: {'AC/DC', 'Thriller', 'Back in Black'}
    set2: {'AC/DC', 'Back in Black', 'The Dark Side of the Moon'}
    intersection set: {'AC/DC', 'Back in Black'}
    

**union** method:  

**`union_setVar = set1_Var.union(set2_Var)`**  
* This combines all of set1 and all of set2 elements into a new set variable


```python
# example showing union of two sets
set3 = set1.union(set2)
print(set1)
print(set2)
print(set3)
```

    {'AC/DC', 'Thriller', 'Back in Black'}
    {'AC/DC', 'Back in Black', 'The Dark Side of the Moon'}
    {'Thriller', 'The Dark Side of the Moon', 'AC/DC', 'Back in Black'}
    

**difference** method:  

**`difference_setVar = set1_Var.difference(set2_Var)`**  
* Elements that are **only in set1** are returned in a new set variable


```python
# example showing difference of two sets
difference_set = set1.difference(set2)
print("set1:", set1)
print("set2:", set2)
print("difference_set:", difference_set)
```

    set1: {'AC/DC', 'Thriller', 'Back in Black'}
    set2: {'AC/DC', 'Back in Black', 'The Dark Side of the Moon'}
    difference_set: {'Thriller'}
    

**symmetric difference** method:  

**`symmetric_differenceSetVar = set1.symmetric_difference(set2)`**  
* Returns **all** elements that **only** appear in one or other of the sets


```python
# example showing symmetric difference of two sets  
a = {'a', 'b', 'c', 'd'} # generate set "a"
b = {'c', 'd', 'e' } # generate set "b"
c = {} # generate set "c"

print("set a:", a) # print sets to view
print("set b:", b)
print("set c:", c)
print() # print blank line for ease of viewing
print("sets a/b symmetric difference:", a.symmetric_difference(b)) # print symmetric differences
print("sets b/a symmetric difference:", b.symmetric_difference(a))
print("sets a/c symmetric difference:", a.symmetric_difference(c))
print("sets b/c symmetric difference:", b.symmetric_difference(c))
```

    set a: {'b', 'a', 'c', 'd'}
    set b: {'d', 'c', 'e'}
    set c: {}
    
    sets a/b symmetric difference: {'b', 'a', 'e'}
    sets b/a symmetric difference: {'b', 'a', 'e'}
    sets a/c symmetric difference: {'b', 'd', 'c', 'a'}
    sets b/c symmetric difference: {'e', 'c', 'd'}
    

**issubset** method:  

**`set_to_check.issubset(against_this_set)`**  
* Checks if a set is a subset and all of its elements are contained in another set  
* Returns True or False


```python
# example checking if "set1" `issubset` of "set3"
print("set1:", set1)
print("set3:", set3)
print("issubset:", set1.issubset(set3))
```

    set1: {'AC/DC', 'Thriller', 'Back in Black'}
    set3: {'Thriller', 'The Dark Side of the Moon', 'AC/DC', 'Back in Black'}
    issubset: True
    

**issuperset** method:  

**`set_to_check.issuperset(against_this_set)`**  
* Checks if a set is a superset and contains a minimum of all elements of another set   
* Returns True or False


```python
# example checking if "set3" `issuperset` of "set1"
print("set3:", set3)
print("set1:", set1)
print("issuperset:", set3.issuperset(set1))
```

    set3: {'Thriller', 'The Dark Side of the Moon', 'AC/DC', 'Back in Black'}
    set1: {'AC/DC', 'Thriller', 'Back in Black'}
    issuperset: True
    

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>Branching;</center>

* Has <ins>**OPTIONAL**</ins> **round brackets** followed by <ins>**COMPULSARY**</ins> **colon**  
* Must use comparison operator in test argument, **Not** just regular operator e.g., **`=`**  
* Variable to be tested must be defined **prior** to "if statement"  

**if** statement:  

**`if(test_argument):`**  
    **`    when_true_do_this_and_continue (note indent)`**  
**`when_false_continue_from_here (note no indent)`**  
* When "True", **both** true and false branches will be actioned  
* When "False", **only false** branch will be actioned  
* **Must Not** indent false branch or it will be deemed part of true branch



```python
# example of if statement when false
age=18
if(age>18):
    print("you can enter")    # argument false, so this line is skipped
print("move on")              # continues from here
```

    move on
    


```python
# example of if statement when true
age=19
if(age>18):
    print("you can enter")    # argument true, so continues from here
print("move on")
```

    you can enter
    move on
    


```python
# example showing that when "False" branch not indented, it is deemed part of "True" branch
age=17
if(age>18):
    print("you can enter")     # argument false, so this line is skipped
    print("move on")           # line indented, so this line is skipped also
```

**else** statement:  

**`if(test_argument):`**  
    **`    when_true_do_this_and_continue (note indent)`**   
**`else:`**  
    **`    when_false_do_this_and_continue (note indent)`**  
**`then_continue_from_here (note no indent)`**  
* Similar to "if statement" with the addition of the "else" branch  
* "Else" branch will **only** be done when "if" argument is "False"  
* Program will continue from line after "else" branch that is **Not** indented after completing relevant branch


```python
# example of else statement
age=18
if(age>18):
    print("you can enter")    # argument false, so this line is skipped
else:
    print("go see Meat Loaf")  # argument false, so continues from here, this line would be skipped if true
print("move on")
```

    go see Meat Loaf
    move on
    

**elif** statement:  

**`if(test_argument):`**  
    **`    when_true_do_this_and_continue (note indent)`**  
**`elif(test_argument_when_false):`**  
    **`    when_true_for_second_argument_do_this_and_continue (note indent)`**  
**`else:`**  
    **`    when_false_do_this_and_continue (note indent)`**  
* Similar to "else statement" with the addition of the "elif" branch  
* Continues "if" statement without ending code block as would happen with a further "if" statement
* "Elif" branch will **only** be done when previous "if" argument and previous "elif" arguments in block are "false"   
* Program will continue from line after "else" branch that is **Not** indented after completing relevant branch


```python
#  example of elif statement
age=18
if(age>18):
    print("you can enter")       # argument false, so this line is skipped
elif(age==18):
    print("go see Pink Floyd")   # 2nd argument true, so continues from here
else:
    print("go see Meat Loaf")    # 2nd argument true, so this line is skipped
print("move on")                 # continues from here
```

    go see Pink Floyd
    move on
    

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>Logic Operators;</center>

* Takes boolean values and produces different boolean values  
* Can be combined with branching

**not** operator:  

**`not(test_argument)`**   
* Returns opposite boolean value to test argument


```python
# example of "not" operator
x=1
not(x==1)
```




    False




```python
# example of not operator combined with "if" statement
album_year = 1983 # define album year

if not(album_year == 1984):
    print ("Album year is not 1984")
```

    Album year is not 1984
    

**or** operator:  

**`(test_argument_1) or (test_argument_2)`**  
* Returns "True" when **either or both** arguments are **"True"**  
* **Inclusive** or  


```python
# example of "or" operator  
x=3
(x<0)or(x>2)
```




    True




```python
# example of "or" operator combined with "if" statement
album_year = 1980 # define album year

if(album_year < 1980) or (album_year > 1989):
    print ("Album was not made in the 1980's")
else:
    print("The Album was made in the 1980's ")
```

    The Album was made in the 1980's 
    

**and** operator:  

**`(test_argument_1) and (test_argument_2)`**  
* Returns "True" when both arguments are "True"  


```python
# example of "and" operator
x=1
(x>0)and(x<2)
```




    True




```python
# example of "and" operator combined with "if" statement
album_year = 1983 # define album year

if(album_year>1979)and(album_year<1990):
    print("This album was made in the 80's")
```

    This album was made in the 80's
    

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>Loops;</center>

* Must include **colon**  
* Must **indent** loop "block" ("do_this") section 

**for** loop:  

**`for var in sequence :`**  
   **`    do_this_with_var`**  
* Used when number of times loop is to be executed is **known** or **fixed** 
* "Var" is a variable that is used for iterating over a "sequence", on every iteration it takes the next value from "sequence"  until the end of "sequence" is reached  
* "Var" is **not required** to be defined prior to loop as loop will automatically increase incrementally as per sequence given  


```python
# example of for loop used to print out a sequence of numbers from 0 to 7

for i in range(0, 8):
    print(i)
```

    0
    1
    2
    3
    4
    5
    6
    7
    


```python
# write a "for" loop that prints out the elements from the following list: squares=['red', 'yellow', 'green', 'purple', 'blue']

squares = ["red", "yellow", "green", "purple", "blue"]

for colour in squares:
    print(colour)
```

    red
    yellow
    green
    purple
    blue
    


```python
# write a program to print squares of all numbers present in a list

# list of integer numbers
numbers = [1, 2, 4, 6, 11, 20]

# variable to store the square of each num temporarily
sq = 0

# iterating over the given list
for val in numbers:
    # calculating square of each number
    sq = val * val
    # displaying the squares
    print(sq)
```

    1
    4
    16
    36
    121
    400
    


```python
# Loop through the list and iterate on both index and element value

colours=['red', 'yellow', 'green', 'purple', 'blue']

for i, colour in enumerate(colours):
    print(i, colour)
```

    0 red
    1 yellow
    2 green
    3 purple
    4 blue
    


```python
# from any given "list" of numbers, create a "for" loop to print 2 seperate tuples
# one of all the odd numbers 
# and one of all the even numbers
# do NOT print any repeats of any number
# sort each tuple


list1 = [3,8,15,22,15,1,10,109,3]

even = []
odd = []

for i in range(0,len(list1)):
    if list1[i] % 2 == 0:
        even.append(list1[i])
    else:
        odd.append(list1[i])

even = set(even)
even = tuple(sorted(even))

odd = set(odd)
odd = tuple(sorted(odd))

if even != ():
    print("even:", even)
if odd != ():
    print("odd:", odd)
    
print(type(even))
print(type(odd))
```

    even: (8, 10, 22)
    odd: (1, 3, 15, 109)
    <class 'tuple'>
    <class 'tuple'>
    


```python
# For loops with dictionaries

month_days={
    "Jan": 31,
    "Feb": 28,
    "Mar": 31,
    "Apr": 30,
    "May": 31,
    "Jun": 30,
    "Jul": 31,
    "Aug": 31,
    "Sep": 30,
    "Oct": 31,
    "Nov": 30,
    "Dec": 31
    
}

print(month_days.items())
print()

#items retuns a list of pairs (key/value), similar to enumerate
for mth,days in month_days.items(): 
    print (mth,"has",days,"days")
```

    dict_items([('Jan', 31), ('Feb', 28), ('Mar', 31), ('Apr', 30), ('May', 31), ('Jun', 30), ('Jul', 31), ('Aug', 31), ('Sep', 30), ('Oct', 31), ('Nov', 30), ('Dec', 31)])
    
    Jan has 31 days
    Feb has 28 days
    Mar has 31 days
    Apr has 30 days
    May has 31 days
    Jun has 30 days
    Jul has 31 days
    Aug has 31 days
    Sep has 30 days
    Oct has 31 days
    Nov has 30 days
    Dec has 31 days
    

**Parallel iteration**:  

**`for a,b..... in zip(iterableA, iterableB.....):`**  
    **`    do something with a, b etc.`**  
* **zip** can be used to **iterate** over **multiple iterables in parallel** when used with **for loop**  


```python
# Using zip to iterate in parallel 

letters = ['a', 'b', 'c']
numbers = [0, 1, 2]

for l, n in zip(letters, numbers):
    print(f'Letter: {l}')
    print(f'Number: {n}')
```

    Letter: a
    Number: 0
    Letter: b
    Number: 1
    Letter: c
    Number: 2
    

**List comprehension**:  

**`[eleToReturn for var in sequence condition]`**  
* Keywords **for** and **in** are compulsary  
* List comprehensions are given in **square brackets**  
* Must assign to a new variable to save changes  
* `sequence` is the **sequence** to **extract each variable** from, can be a range or a list etc  
* `var` is the **variable** to test against the condition given from the sequence
* `eleToReturn` will usually be the same as `var`....this is what will be **entered in the return list if condition is met**  


```python
# some examples demonstrating list comprehension

fruits = ["apple", "orange", "lemon", "cherry", "mango"]

fruitsWithA = [ele for ele in fruits if "a" in ele]
fruitsIndexWithA = [ind for ind, ele in enumerate(fruits) if "a" in ele]

print(fruitsWithA)
print(fruitsIndexWithA)
```

    ['apple', 'orange', 'mango']
    [0, 1, 4]
    

**Dictionary comprehension**:  

**`{elementToReturn for key,value in dictVar.items() condition}`**  
* Similar to list comprehension, but contained in **`{}`** brackets  
* **elementToReturn** will usually be **key:value**, or maybe just **key**  
* **.items()** method is used to **obtain key:value pair** to carry out condition check on  
* **value** can be used in the **condition** statement  


```python
month_days={"Jan": 31,"Feb": 28,"Mar": 31,"Apr": 30,"May": 31,"Jun": 30,"Jul": 31,"Aug": 31,"Sep": 30,"Oct": 31,"Nov": 30,"Dec": 31}

only_31_days = { key.upper():value for key,value in month_days.items() if value==31}

print(only_31_days)
```

    {'JAN': 31, 'MAR': 31, 'MAY': 31, 'JUL': 31, 'AUG': 31, 'OCT': 31, 'DEC': 31}
    


```python
only_31_days = { key for key,value in month_days.items() if value==31}

print(only_31_days)
```

    {'May', 'Jan', 'Jul', 'Oct', 'Dec', 'Aug', 'Mar'}
    

**while** loop:  

**`while condition_statement :`**  
    **`    do_this`**  
* Used when number of times loop will need to be executed is **unknown**  
* "While" loop will continue whilst condition_statement remains "True"  
* Ensure to **define** any variable used in "condition_statement" **prior** to loop to "get into loop"  
* Ensure to **adjust the value** of any variable used in "condition_statement" **within** loop, otherwise may create an infinite loop  


```python
# example of "while" loop  

num = 1
# loop will repeat itself as long as num < 10 remains true  

while num < 10:  
    print(num)  
    
    # incrementing the value of num  
    num = num + 3  
```

    1
    4
    7
    


```python
# Write a while loop to copy the strings 'orange' of the list "squares" to the list "new_squares"  
# Stop and exit the loop if the value on the list is NOT 'orange'

squares = ['orange', 'orange', 'purple', 'blue ', 'orange']

new_squares = []
i = 0
colour = squares[i]

while colour == "orange":
    new_squares.append(colour)
    i = i + 1
    colour = squares[i]
    
    
print("new_squares = ", new_squares)
```

    new_squares =  ['orange', 'orange']
    


```python
# for any given number, create a "while" loop to print out every number from "0" upto and including the given number 
# where the number is divisible by "3", print "fizz"
# where the number is divisible by "5", print "buzz"
# where the number is divisible by both "3" AND "5", print "fizzbuzz"

user = 30
i = 0

while i <= user:
    result = ""
    
    if i % 3 == 0:
        result = "fizz"
    if i % 5 == 0:
        result = (result + "buzz")
    if i == 0:
        print(i)
    elif len(result) >1:
        print(result)
    else:
        print(i)
    i += 1
```

    0
    1
    2
    fizz
    4
    buzz
    fizz
    7
    8
    fizz
    buzz
    11
    fizz
    13
    14
    fizzbuzz
    16
    17
    fizz
    19
    buzz
    fizz
    22
    23
    fizz
    buzz
    26
    fizz
    28
    29
    fizzbuzz
    


```python
# from any given "list" of numbers, create a "while" loop to print 2 seperate tuples
# one of all the odd numbers 
# and one of all the even numbers
# do NOT print any repeats of any number
# sort each tuple

list1 = [1,3,5,7,9, 88, 64, 10, 10]
i=0
even = []
odd = []

while i < (len(list1)):
    if list1[i] % 2 == 0:
        even.append(list1[i])
    else:
        odd.append(list1[i])
    i += 1
    
even = set(even)
even = tuple(sorted(even))

odd = set(odd)
odd = tuple(sorted(odd))

if even != ():
    print("even:", sorted(even))
if odd != ():
    print("odd:", sorted(odd))
    
print(type(even))
print(type(odd))
```

    even: [10, 64, 88]
    odd: [1, 3, 5, 7, 9]
    <class 'tuple'>
    <class 'tuple'>
    

**break** statement:

**`for var in sequence:`**  
    **`    if (test argument):`**  
    **`        break  (exit loop when condition is True)`**  
    **`    else:`**  
    **`        do_this`**  
* Break statement in Python is used to **bring the control out of the loop** when some external condition is triggered  
* Statement is put inside the loop body (generally after if condition)


```python
# example of break statement where "print" line is after break

number = 0

for number in range(10):
    if number == 5:
        break    # breaks here before integer 5 is printed

    print('Number is ' + str(number))

print('Out of loop')
```

    Number is 0
    Number is 1
    Number is 2
    Number is 3
    Number is 4
    Out of loop
    


```python
# example of break statement where "print" line is before break

s = 'Hello World'

for letter in s: 
  
    print(letter) 
    
    if letter == 'o' or letter == 'r': 
        break   # break the loop as soon it sees 'o' or 'r' but after it has printed that string
  
print("Out of for loop") 
print() 
```

    H
    e
    l
    l
    o
    Out of for loop
    
    

**continue** statement:  

**`for var in sequence:`**  
    **`    if (test argument):`**  
    **`        continue (do next iteration when condition is True)`**  
    **`    else:`**  
    **`        do_this`**  
* Continue statement is opposite to that of break statement, instead of terminating the loop, it forces the program to execute the next iteration of the loop  
* Statement is put inside the loop body (generally after if condition)  


```python
# write a program which prints the numbers from 1 to 10, but not 6
# do this using loop and only one loop is allowed to be used

for i in range(1, 11): 
  # If i is equals to 6, continue to next iteration without printing  
    
    if i == 6: 
        continue
    else: 
        # otherwise print the value of i 
        
        print(i, end = " ") 
```

    1 2 3 4 5 7 8 9 10 

**pass** statement:

**`for var in sequence:`**  
    **`    pass (do nothing and continue program)`**  
* Generally used as a **placeholder for future code**  
* When the pass statement is executed, nothing happens, but you avoid getting an error when empty code is not allowed  
* Difference between pass and comment is that comment is ignored by the interpreter whereas pass is not ignored  
* Empty code is not allowed in **loops, function definitions, class definitions, or in if statements**   


```python
# example where pass can be used as a placeholder and code can be added later

n = 10
for i in range(n): 
    
    pass     # program sees pass statement and does nothing
```


```python
# example where pass statement gets executed when the condition is true 

li =['a', 'b', 'c', 'd'] 
  
for i in li: 
    if(i =='a'): 
        pass 
    else: 
        print(i)
```

    b
    c
    d
    

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>Exception Handling;</center>

**exceptions:**  
* Exceptions are a Python object that represents an **error**  
* When a Python script raises an exception, it must either **handle the exception immediately otherwise it terminates and quits**  


```python
# example of a "ZeroDivisionError" exception

1/0
```


    ---------------------------------------------------------------------------

    ZeroDivisionError                         Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_6032/3703746326.py in <module>
          1 # example of a "ZeroDivisionError" exception
          2 
    ----> 3 1/0
    

    ZeroDivisionError: division by zero



```python
# example of a "NameError" exception

y = a + 1
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_6032/734013698.py in <module>
          1 # example of a "NameError" exception
          2 
    ----> 3 y = a + 1
    

    TypeError: unsupported operand type(s) for +: 'set' and 'int'


[**List of Built-in Exceptions**](https://docs.python.org/3/library/exceptions)

**try except (else finally)** statement:  

**`# potential code before try catch`**

**`try:`**  
    **`    try_this`**  
**`except exception_name:`**  
    **`    run_this_if_named_exception_occurs`**  
**`except (another_exception_name, a_further_exception_name):`**  
    **`    run_this_if_any_named_exception_occurs`**  
**`except:`**  
    **`    run_this_if_any_other_exception_occurs`**  
**`else:`**  
    **`    run_this_if_no_exceptions`**  
**`finally:`**  
    **`    run_this_regardless_of_exceptions`**  
* All **colons** are **manditory**  
* Using **"except"** statement **without specifying exceptions** can be **bad practice** as will catch all error without notifying programmer of root cause of problems that may occur  
* **Multiple exception names** can be entered into one except branch in **round brackets seperated by comma**
* **Else** branch will run **if no errors** are encountered   
* **Finally** branch will run **regardless of errors** encountered  
* Can have 1 or many except branchs, if including except branch without specifying exceptions, this must be **last of the except branchs**  
* **else** branch is **optional**  
* **finally** branch is **optional**  
* Can use further indented "try" branches instead of "else" branch, **however is not good practice**


```python
# example of try except statement

# using "except" without naming specific errors can be bad practice as will catch 
# all errors without notifying programmer of root cause of problems that may occur

try:      # getting input from user
    a=int(input("y = 5 / a\nInput value for 'a'\n\nTry running using:\n 1. A letter\n 2. Zero\n 3. Another number\n\n"))
    y = 5/a
except ValueError:       # will run this block if anything except a number was input
    print("A number was not entered")
except:                  # will run this block if an error occurs that is not a ValueError, can be bad practice!!
    print("Cannot devide by zero")
else:                    # will run this block if no error was encountered
    print("y =",y)
finally:                 # will run this block regardless of errors encountered
    print("Program complete")
```

    y = 5 / a
    Input value for 'a'
    
    Try running using:
     1. A letter
     2. Zero
     3. Another number
    
     4
    

    y = 1.25
    Program complete
    


```python
# same example as above of try except statement
# but now catching ONLY specified errors

try:      # getting input from user
    a=int(input("y = 5 / a\nInput value for 'a'\n\nTry running using:\n 1. A letter\n 2. Zero\n 3. Another number\n\n"))
    y = 5/a
except (ValueError,ZeroDivisionError):       # will run this block if specified errors occur
    print("A valid number was not entered")
else:                    # will run this block if no error was encountered
    print("y =",y)
finally:                 # will run this block regardless of errors encountered
    print("Program complete")
```

    y = 5 / a
    Input value for 'a'
    
    Try running using:
     1. A letter
     2. Zero
     3. Another number
    
     5
    

    y = 1.0
    Program complete
    


```python
# same example as above
# but now with 2nd "try" branch instead of "else" branch
# NOTE this is not best practice due to errors potentially not being caught in 2nd branch
# or multiple finally branches

try:      # getting input from user
    a=int(input("y = 5 / a\nInput value for 'a'\n\nTry running using:\n 1. A letter\n 2. Zero\n 3. Another number\n\n"))
    y = 5/a
    try:                    # will run this block if no error was encountered
        print("y =",y)
    finally:                 # will run this block regardless of errors encountered in 2nd try branch
        print("Program complete")
except (ValueError,ZeroDivisionError):       # will run this block if specified errors occur
    print("A valid number was not entered")
finally:
    print("This is to demonstrate multiple finally branches")
```

    y = 5 / a
    Input value for 'a'
    
    Try running using:
     1. A letter
     2. Zero
     3. Another number
    
     5
    

    y = 1.0
    Program complete
    This is to demonstrate multiple finally branches
    

**raise** exception:  

**`raise Exception_Name ("info on why exception raised")`**  
* **Bad practice** to handle all Exceptions with a **single statement, better to be specific**  
* Can manually raise or cause an exception to be thrown with keyword **"raise"**  
* "exception_name" should be a built in exception  
* **Optional** information can be provided in **round brackets** but ideally should provide more information on why exception was raised  
* **Different errors** can be raised, note has **capital letter** at beginning. These include (but not limited to):  
    * **ValueError** 
    * **TypeError**  
    * **Exception**  


```python
# example of raising an exception

x = 9

if x < 10:               # condition to raise exception
    raise ValueError("X should not be less than 10")         
```


    ---------------------------------------------------------------------------

    ValueError                                Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_6032/3744701145.py in <module>
          4 
          5 if x < 10:               # condition to raise exception
    ----> 6     raise ValueError("X should not be less than 10")
    

    ValueError: X should not be less than 10



```python
raise TypeError("This is a type error")
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_6032/2932973553.py in <module>
    ----> 1 raise TypeError("This is a type error")
    

    TypeError: This is a type error



```python
# should be used as the last case if not wanting any errors, but still bad practice to use
# Catches all Exceptions

raise Exception("This is an exception")
```


    ---------------------------------------------------------------------------

    Exception                                 Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_6032/1502614021.py in <module>
          2 # Catches all Exceptions
          3 
    ----> 4 raise Exception("This is an exception")
    

    Exception: This is an exception


**Create custom exception**:  

**`class ExceptionName(Exception):`**       # inherits from Exception  
$\;\;\;\;$**`def __init__(self,*args,**kwargs):`**  
$\;\;\;\;\;\;\;\;$**`super().__init__(*args,**kwargs)`**  
* Creates custom Exception that can be raised the same as any other  
* Only benefits of having your own exception is to make code more readable and to write for aimed error handling  


```python
# Creating custom Exception

import numpy as np

class MyRandomException(Exception):
    def __init__(self,*args,**kwargs):
        super().__init__(*args,**kwargs)
        
while(True):
    r = np.random.randint(0,10)
    print(r)
    if (r==5):
        raise MyRandomException('A weird number has been generated randomly')
```

    5
    


    ---------------------------------------------------------------------------

    MyRandomException                         Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_6032/3706247615.py in <module>
         11     print(r)
         12     if (r==5):
    ---> 13         raise MyRandomException('A weird number has been generated randomly')
    

    MyRandomException: A weird number has been generated randomly


**Traceback**:  

A python module that provides a standard interface to extract, format and print stack traces of a python program  
When it prints the stack trace it exactly mimics the behaviour of a python interpreter  
Useful when you want to print the stack trace at any step, usually seen when an exception occurs  
Since a traceback gives all the information regarding the exception it becomes easier to track one and fix it  

**`import traceback`**  

**`try:`**  
$\;\;\;\;$**`some code`**  
**`except:`**  
$\;\;\;\;$**` traceback.print_exc()`**  


```python
import traceback
  
# declaring array
A = [1, 2, 3, 4]
  
try:
    value = A[5]
      
except:
    # printing stack trace
    traceback.print_exc()
```

    Traceback (most recent call last):
      File "C:\Users\ajdpi\AppData\Local\Temp/ipykernel_6032/126516669.py", line 7, in <module>
        value = A[5]
    IndexError: list index out of range
    


```python
import traceback

try:
    while(True):
        r = np.random.randint(0,10)
        print(r)
        if (r==5):
            raise RandomException('A weird number has been generated randomly')
except RandomException as e:
    print(e)
    print('The error was somewhere here:')
    traceback.print_exc()
```

    9
    4
    8
    8
    9
    5
    


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_6032/3219596871.py in <module>
          7         if (r==5):
    ----> 8             raise RandomException('A weird number has been generated randomly')
          9 except RandomException as e:
    

    NameError: name 'RandomException' is not defined

    
    During handling of the above exception, another exception occurred:
    

    NameError                                 Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_6032/3219596871.py in <module>
          7         if (r==5):
          8             raise RandomException('A weird number has been generated randomly')
    ----> 9 except RandomException as e:
         10     print(e)
         11     print('The error was somewhere here:')
    

    NameError: name 'RandomException' is not defined


**assert**:  

**`try:`**  
$\;\;\;\;$**`assert condition, errorMessage`**  
**`except AssertionError as ae:`**  
$\;\;\;\;$**`other code`**  
$\;\;\;\;$**`raise ae`**  
* **Keyword** **`assert`** lets you test if a condition in your code returns True, if not, the program will raise an AssertionError  
* assert **does nothing when** condition returns **True**  
* assert can be done outside of a try, except, but shown here to show calling AssertionError created  


```python
try:
    assert False, "my error message"
except AssertionError as ae:
    print("some other code")
    raise ae
```

    some other code
    


    ---------------------------------------------------------------------------

    AssertionError                            Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_6032/2600895788.py in <module>
          3 except AssertionError as ae:
          4     print("some other code")
    ----> 5     raise ae
    

    ~\AppData\Local\Temp/ipykernel_6032/2600895788.py in <module>
          1 try:
    ----> 2     assert False, "my error message"
          3 except AssertionError as ae:
          4     print("some other code")
          5     raise ae
    

    AssertionError: my error message


[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center> Useful Built-in Functions;</center>

**range** function:  

**`range(start,stop,step)`**  
* Represents a range of immutable sequence of numbers  
* "stop" is **required**, will stop at and **NOT** include that value   
* "start" is **NOT required**, set to "0" if not given  
* "step" is **NOT required**, set to "1" if not given  
* Will print as a **"range"** unless typecasted  


```python
# example showning how a range prints a range unless typecasted

range(6)
```




    range(0, 6)




```python
# example showing how a range does not include the "stop" value
list(range(0,6))
```




    [0, 1, 2, 3, 4, 5]




```python
# example showing start and step values
print(list(range(10,20,2)))
```

    [10, 12, 14, 16, 18]
    


```python
# another example showing start and step values with negative numbers
print(list(range(-20,-30,-2)))
```

    [-20, -22, -24, -26, -28]
    

**enumerate** function: 

**`enumerate(iterable, start=0)`**  
* Outputs **(index value + start value)** with each element stored as a tuple, whilst the entire object is stored as an **enumerate** list  
* "iterable" can be any object that supports iteration  
* "start" is **NOT** required, it is the value from which the counter is to be started, by default it is "0"   


```python
list1 = ["eat","sleep","repeat"] 
string1 = "geek"

# creating enumerate objects 
obj1 = enumerate(list1) 
obj2 = enumerate(string1) 

print("Return type:",type(obj1)) 
print(list(enumerate(list1)))
  
# changing start index to 2 from 0 
print(list(enumerate(string1,2)))
```

    Return type: <class 'enumerate'>
    [(0, 'eat'), (1, 'sleep'), (2, 'repeat')]
    [(2, 'g'), (3, 'e'), (4, 'e'), (5, 'k')]
    


```python
# Python program to illustrate 
# enumerate function in loops 
list1 = ["eat","sleep","repeat"] 
print("list1 type:", type(list1)) 

print("")

# printing the tuples in object directly 
for ele in enumerate(list1): 
    print(ele)
    print("enumerate ele type:", type(ele))

print("")
    
# changing index and printing separately 
for count,ele in enumerate(list1,100): 
    print(count,ele)
    print("count type:", type(count))
    print("ele type:", type(ele))
```

    list1 type: <class 'list'>
    
    (0, 'eat')
    enumerate ele type: <class 'tuple'>
    (1, 'sleep')
    enumerate ele type: <class 'tuple'>
    (2, 'repeat')
    enumerate ele type: <class 'tuple'>
    
    100 eat
    count type: <class 'int'>
    ele type: <class 'str'>
    101 sleep
    count type: <class 'int'>
    ele type: <class 'str'>
    102 repeat
    count type: <class 'int'>
    ele type: <class 'str'>
    

**count** method:  

**`var.count(object)`**  
* Counts number of times "object" occurs in "var"  


```python
# count number of times "1" occurs in tuple

tup1=(1,2,1,4,6,1)

print(tup1.count(1))
```

    3
    

**sum** function:  

**`sum(iterable, start=0)`**  
* Sum of elements in "iterable"  
* Starts at **value** given for start, if no value given, defaults to "0"  


```python
list1 = [1,2,3,4,5]

print("sum(list1):", sum(list1)) # sum of list1
print("sum(list1[1:3]):", sum(list1[1:3])) # sum of list1 elements 1:3
print("sum(list1,2):", sum(list1,2)) # sum of list1, starting at value 2
print("sum(list1,list1[3]):", sum(list1,list1[3])) # sum of list1, starting at value of element index 3 (4)
```

    sum(list1): 15
    sum(list1[1:3]): 5
    sum(list1,2): 17
    sum(list1,list1[3]): 19
    

**isnumeric( )** function:  

**`var.isnumeric()`**  
* Checks variable to see if it is a number and returns a boolean  
* Useful for checking input before converting to an int  


```python
# example of isnumeric() function

"6".isnumeric()
```




    True




```python
# isnumeric() function on a variable

var = "hello"

var.isnumeric()
```




    False



**isinstance( )** function:  

**`isinstance(var, typeToCheckFor)`**  
* Checks given variable if it is of type given, returns **boolean**  
* Considers **subclasses** too unlike type(x) == .....  


```python
isinstance(54, int)
```




    True




```python
isinstance("hello!", bool)
```




    False



**zip** function:  

**`zip(iterable1, iterable2)`**  
* **Combines** items one at a time taking **first from iterable1, then from iterable2**  
* **Iterable with** the **least** items **defines** the **length of output** zip object  
* If iterables are **tuples** and **one** has **exactly 1 object** whilst the other has multiple, it will be **elements** from that object which will be used  
* **NOTE** zip objects can **ONLY** be **iterated** over **ONCE before it is exhaused** and the zipped object will be **empty**   
* Can **avoid exhausting** the zipped object by **typecasting** to a list for example **when assigning to a variable** rather than when using the zipped object.  

**Create tuples from zip object**:  

**`tupVar1, tupVar2, tupVar3... = zip(*zippedObject)`**  
* The **`*`** defines splitting function  
* As long as the zippedObject has not been iterated over already, this will **split each zipped elements into defined tuples**  
* Must define same number of **tuples as components in each zippedObject elements**  


```python
# zip example, shows they can only be iterated ONCE before being exhausted

numbers = [1, 2, 3, 4, 5]
letters = ['a', 'b', 'c', 'd', 'e']
otherLet = ["aa","bb","cc"]                  # note shortest iterable defines length of zipped object
zipped = zip(numbers, letters, otherLet)

print("first print of zipped: ", list(zipped))
print("second print of zipped: ", list(zipped))
```

    first print of zipped:  [(1, 'a', 'aa'), (2, 'b', 'bb'), (3, 'c', 'cc')]
    second print of zipped:  []
    


```python
# zip example, avoiding exhausting the zipped object by typcasting when assigning to a variable

numbers = [1, 2, 3, 4, 5]
letters = ['a', 'b', 'c', 'd', 'e']
otherLet = ["aa","bb","cc"]                  # note shortest iterable defines length of zipped object
zipped = list(zip(numbers, letters, otherLet))

print("This is the same example as above, with the exception of being typecasted when assigning to a variable")
print("first print of zipped: ", zipped)
print("second print of zipped: ", zipped)
```

    This is the same example as above, with the exception of being typecasted when assigning to a variable
    first print of zipped:  [(1, 'a', 'aa'), (2, 'b', 'bb'), (3, 'c', 'cc')]
    second print of zipped:  [(1, 'a', 'aa'), (2, 'b', 'bb'), (3, 'c', 'cc')]
    


```python
# Taking a zipped object and putting elements into new tuples

numbers = [1, 2, 3]
letters = ['a', 'b', 'c']
zipped = zip(numbers, letters)

newLetters, newNumbers = zip(*zipped)
print(newNumbers)
```

    ('a', 'b', 'c')
    


```python
# example showing zipping lists and tuples can be very different

numbersList = ["1234"]
nameList = ["Andy", "Bill"]
print("Zipped lists: ", list(zip(numbersList,nameList)))

numbersTup = ("1234")
nameTup = ("Andy", "Bill")
print("Zipped tuples: ", list(zip(numbersTup,nameTup)))
```

    Zipped lists:  [('1234', 'Andy')]
    Zipped tuples:  [('1', 'Andy'), ('2', 'Bill')]
    

**map** function:  

**`map(function, iterables)`**  
* Executes a specified function for each item in an iterable  
* **`iterables`** are a sequence, collection or an iterator object  
* Can send as many iterables as you like, just make sure the function has one parameter for each iterable  
* Outputs as a **map object**  


```python
# Using map with a lambda function on a list
listOfWords = ["hello", "goodbye", "words"]
list(map(lambda w:w[0].upper()+w[1:],listOfWords))
```




    ['Hello', 'Goodbye', 'Words']




```python
# Using map function with a custom function which takes 2 parameters on 2 tuples
def myfunc(a, b):
  return a + " " + b

x = map(myfunc, ('apple', 'banana', 'cherry'), ('orange', 'lemon', 'pineapple'))

print(x)

#convert the map into a list, for readability:
print(list(x))
```

    <map object at 0x0000018A1D3D73D0>
    ['apple orange', 'banana lemon', 'cherry pineapple']
    

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center> Building Functions;</center>

Build functions to replace **repeating lines of code**  

**functions**:  

* Functions are a block of code that is also called by its name (**independent**)
* The function can have different parameters or may not have any at all. If any data is passed, they are **passed explicitly**  
* It **may or may not** return any data  
* Function does not deal with class and its instance concept  

**difference between methods and functions**:  

* Functions and Methods both look similar as they perform in almost similar ways, but the key difference is the concept of ‘Class and its Object‘  
* Functions can be called only by its name, as it is defined independently  
* Methods can’t be called by its name only, we need to invoke the class by a reference of that class in which it is defined, i.e., method is defined within a class and hence they are dependent on that class and so methods need to be called on an object    
* A method may alter an object’s state, but Python function usually only operates on it, and then prints something or returns a value  

**typical function**:  
**`func_name(arguments)`**  
  
**typical method**:  
**`obj.meth_name(arguments)`**  

**define** a function:  

**`def funcName(para1, para2, *args, keywordArg=value, **kwargs):`**  
$\;\;\;\;$**`"""description of func for help()"""`**  
$\;\;\;\;$**`code block`**  
$\;\;\;\;$**`return "this"`**  
* Function name should be descriptive and begin with a lower case letter with words separated by underscores    
* Parameters ("para") is what will be taken from program and applied in code block, these are **optional**   
* Must include **colon**  
* **Optional** help description is in **triple quotes**  
* Code block is **indented**  
* Can have **single or multiple "positional" parameters** seperated with a **comma**  
* Positional arguments are defined by **name only**  
* **Positional** arguments can be passed in a **different order** by **assigning to parameter name when calling function**  
* **Positional arguments** can have **multiple argument entries** when parameter is preceded with a **`*`** allowing unlimited number of arguments, this is defined in description as **`*args`**  
* **Positional arguments** are implemented as a **tuple**  
* Keyword arguments are defined by **name and default value** (after the assignment operator). These must be **after** any **positional arguments**  
* **Keyword arguments** can take **unlimited keyword arguments** when parameter is preceded with **`**`**. These must be **after** any **positional arguments**. This is defined in description as **`**kwargs`**
* **Keyword arguments** are implemented as **dictionaries**  
* **Beware** of functions where code contains **multiplication** **`*`**, if a string is passed to function, could cause unexpected errors  
* **Return** statement exits a function, optionally passing back a value. It is not required in some circumstances, however without it can cause errors in passing data back to the main program  
* Functions that perform no task will return "none"  


```python
# example defineing a function

# must include "def" to define the function, name should be descriptive of what it does
# colon is required

def add1(a):         # name of function here is "add1", the function formal parameters "a" in parentheses
    """adds 1 to a""" # documentaion string, contained in triple quotes to describe function, displays in "help()"
    b = a + 1        # function code block, indented
    return b

    
```


```python
# example showing positional arguments can be passed in a different order by assigning to parameter name when calling function

# NOTE - even when you do this, if you do not assign by keyword, any remaining positional parameters MUST be in front

def con(a,b, c=5):
    return a + b + c

print(con("a","b",c="c"))
print(con(b="a",a="b", c= "c"))
```

    abc
    bac
    


```python
# Position of "b" is still correct, but a has been assigned to keyword which changes it from positional to keyword. 
# Because of this, "b" should now be defined first

print(con(a="a","b",c="c"))
```


      File "C:\Users\ajdpi\AppData\Local\Temp/ipykernel_6032/196375150.py", line 4
        print(con(a="a","b",c="c"))
                                 ^
    SyntaxError: positional argument follows keyword argument
    


**calling** a function:    

**`funcName(argument)`**  
* Argument value is sent to function parameter  
* Function result can be assigned to a variable or printed in usual way  
* **Without parentheses** will return function **parameter format**  


```python
# after function has been defined, we can call it

c=add1(7)
print(c)
```

    8
    


```python
# Without parentheses will return function parameter format 
# example using "len" function without parentheses

len
```




    <function len(obj, /)>




```python
# example without parentheses on "add1" function

add1
```




    <function __main__.add1(a)>



**help** on a function:   

**`help(funcName)`**  
* Will return "help description" part of function and module function is in  


```python
# calling the documentation string using help()

help(add1)
```

    Help on function add1 in module __main__:
    
    add1(a)
        adds 1 to a
    
    


```python
# a function can have multiple defined parameters

def mult(a,b):    # function defined with 2 positional arguments
    c = a * b
    return c
```


```python
# calling function with multiple parameters with integers 

mult(2,3)
```




    6



**global and local scope** variables:  

* Variables can be **local** to the function, requires no defining as such, these will **not have name conflicts** with variables already defined in main program, they will be seperate allowing them to have same variable names with different stored values which are deleted after function is executed  
* Variables can be **global**, define variable name preceded by **"global"** in the function, in this case they will not be deleted after function is executed, **alternatively** do not define variable inside function requiring it to be defined prior to function being run in the main program  


```python
# Scope of program is part of program where that variable is accessable
# A variable accessible anywhere in program is called a global variable

# Variable "c" is a local variable only accessible within the function
# This is the "scope of the function"
# After the function has returned the variable, the scope of the function is deleted

# This means that variables within the local scope can have the same name as variables in the global scope
# without conflict

# If a variable is not defined within a function, it will check the global scope

print(c)          # global scope of "c" has already been defined above ("calling a function") with the value of 8
                  # local scope of "c" defined in the "mult" function above had a value of 6
```

    8
    


```python
# calling function with an integer and a string
# beware of * being able to be used with both integers and strings, 
# could cause an error further down program where expecting an integer

mult(2, "Micheal Jackson ")
```




    'Micheal Jackson Micheal Jackson '




```python
# function showing variable "rating" is local and unaffected by global variable

def ACDC(y):
    rating = 1         # local scope "rating" set to 1
    y = 2
    return(rating+y)
```


```python
rating=9           # global scope "rating" set to 9

z=ACDC(1)          # calling function with local scope "rating" set to 1

print("z =", z)     # printing local scope (1) + y(2) = 3
print(rating)       # global scope printed showing different value
```

    z = 3
    9
    


```python
# global scope example

def pinkFloyd():
    
    # variable "claimedSales" is defined as being part of the global scope,
    # i.e., the variable as definded in the function is set to the same for the rest of the program outside 
    # of the function
    
    global claimedSales 
    claimedSales = "45 million"
    return claimedSales
```


```python
pinkFloyd()
print(claimedSales)
```

    45 million
    


```python
# defining function which performs no task

def noWork():
    pass      # Python does not allow function to contain no body,
              # hense "pass" allows function to progress but does nothing
```


```python
# calling function with no return statement produces a "None"

print(noWork())
```

    None
    


```python
# Variadic parameters allows an argument to contain multiple entries, defined with an asterisk

def artistNames(a,b,*names):
    for name in names:
        print(a,b,name)
```


```python
artistNames("Micheal Jackson", "AC/DC", "something", "something else", "another")
```

    Micheal Jackson AC/DC something
    Micheal Jackson AC/DC something else
    Micheal Jackson AC/DC another
    


```python
help(artistNames)
```

    Help on function artistNames in module __main__:
    
    artistNames(a, b, *names)
    
    


```python
# return statement exits a function, optionally passing back a value. In some circumstances it isnt always required 
# in this example the return statement is missing and the function doesn't know whether to return the 
# "squared" variable or the "complication" variable, hense this returns "none"

def more_complicated(n):
  """Returns the square of a number and adds 2 to that number."""
  squared = n ** 2
  complication = squared + 2
```


```python
print(more_complicated(10))
```

    None
    

**lambda functions**:  

**`functionName = lambda arguments : expression`**  
* Lambda functions are small anonymous functions.  
* Can take **any** number of **arguments**  
* Can **only** have **one expression**  
* Can be used inside another function  
* If, else in expression **does not** contain colon **`:`**  


```python
# example of a lambda function

x = lambda a,b : a * b

print(x(3,5))
```

    15
    


```python
# example of a lambda function being used within another function

def myfunc(n):
  return lambda a : a * n

mydoubler = myfunc(2)
mytripler = myfunc(3)

print(mydoubler(11))
print(mytripler(11))
```

    22
    33
    


```python
# Lambda function with if, else
div = lambda a,b : a/b if b!=0 else None

div(10,2)
```




    5.0



[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>Classes, Objects and Methods;</center>

**classes**:  

* Classes are **user-defined types** or blueprint from which objects are created  
* They provide a means of bundling data and functionality together  
* Creating a new class creates a **new type of object**, allowing new instances (objects) of that type to be made  
* Each class instance can have **attributes** attached to it for **maintaining its state**  
* Class instances can also have **methods (defined by its class) for modifying its state**

**define class**:  

**`class ClassName(object):`**  
$\;\;\;\;$**`"""help() description in triple quotes"""`**  

$\;\;\;\;$**`attribbute1 = None`**  ---- Good practice to add attributes at top and assign them None for better readability   
$\;\;\;\;$**`attribute2 = None`**  

$\;\;\;\;$**`# constructor to initialize the object`**  
$\;\;\;\;$**`def __init__(self,attribute1,attribute2 = optionalDefautValue):`**  
$\;\;\;\;\;\;\;\;$**`self.attribute1 = attribute1`**  
$\;\;\;\;\;\;\;\;$**`self.attribute2 = attribute2`**  
        
$\;\;\;\;$**`# method(s) to access and modify the objects argument state values`**  
$\;\;\;\;$**`def meth_Name(self, parameter):`**  
$\;\;\;\;\;\;\;\;$**`self.attribute1 = code_to_modify_attribute1 (e.g.; self.attribute1 = self.attribute1 + parameter)`**  
$\;\;\;\;\;\;\;\;$**`return(self.attribute1)`**   
* Created by keyword **class**  
* Class names should be **Capitalised**  
* Must include **colon**  
* Must include the term **object**  
* **`__init__`** is a special method which is called as a constructor when an object is created from a class and it allows the class to **initialize the attributes** of the class, has **double underscores** either side  
* **`self`** is a parameter in function and the user can use another parameter name in place of it, however it is advisable to use self because it increases the readability of code  
* **`self`** represents the instance of the class. By using the **`self`** keyword we can access the attributes and methods of the class in Python. It binds the attributes with the given arguments  
* Can include **default values** for attributes by setting them with **`=`** in the constructor  
* **Attribute** = variable of any type that belongs to or is declared directly in a class  
* Attributes are always public and accessed by using dot (.) operator e.g.; className.attribute1  
* **Parameter** = temporary variable names within functions, placeholders for the argument it is passed  
* **Argument** = value that is assigned to that temporary variable


```python
# example instantiating a class 
# note American spelling of colour / color is so the drawCircle method works with imported library (see below)
  
class Circle(object):           # defining a class using keyword "class" followed by name (in this case "circle")
                                # class name should be Captalised  
                                # must include colon
                                # "object" is the class parent
        
    # help() description is enclosed in triple quotes    
    """Creates a circle object with parameters 'radius', and 'color'
    default values are radius = 3, and color = 'blue'"""
        
    # special method __init__ is a constructor which allows the class to initialize the 
    # attributes of the class when an object is created
    def __init__(self, radius=3, color="blue"):        # __init__ must have double underscores either side
        self.radius = radius                            # attributes here are "radius", and "color"
        self.color = color                            # optional defaults set with "="
                                                # the keyword "self" binds the attributes with the given argument
            
    
    # define a method within the class
    def add_radius(self, r):            # name of the method "add_radius", along with self, and any parameters
        self.radius = self.radius + r   # defining what is to be done when the method is called
        return(self.radius)             # defining what is to be returned after method is called
        
        
    # method for displaying the created circle objects 
    def drawCircle(self):
        plt.gca().add_patch(plt.Circle((0, 0), radius=self.radius, fc=self.color))
        plt.axis('scaled')
        plt.show() 
```


```python
help(Circle)
```

    Help on class Circle in module __main__:
    
    class Circle(builtins.object)
     |  Circle(radius=3, color='blue')
     |  
     |  Creates a circle object with parameters 'radius', and 'color'
     |  default values are radius = 3, and color = 'blue'
     |  
     |  Methods defined here:
     |  
     |  __init__(self, radius=3, color='blue')
     |      Initialize self.  See help(type(self)) for accurate signature.
     |  
     |  add_radius(self, r)
     |      # define a method within the class
     |  
     |  drawCircle(self)
     |      # method for displaying the created circle objects
     |  
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |  
     |  __dict__
     |      dictionary for instance variables (if defined)
     |  
     |  __weakref__
     |      list of weak references to the object (if defined)
    
    


```python
# importing the library to be able to draw the objects
# only works when attribute colour / color is defined using American spelling "color"

import matplotlib.pyplot as plt
%matplotlib inline  
```

**objects**:  

* An object is an instance of a class. A class is like a blueprint while an instance is a copy of the class with actual values. It’s not an idea anymore  
* An object consists of :  
    **Identity** : It gives a **unique name** to an object and enables one object to interact with other objects  
    **State** : It is represented by **attributes** of an object. It also reflects the properties of an object  
    **Behavior** : It is represented by **methods** of an object. It also reflects the response of an object with other objects  

**creating** an object:  

**`objVar_Name = ClassName(attribute1_value, attribute2_value)`**  
* Object constructor consists of the name of the class as well as the parameters to be passed  


```python
#example of creating an object redCircle

redCircle = Circle(10, "red")
```

**Inheritance**:  

* Unlike other languages, Python can inherit from **multiple classes**  
* Python **does not** have **method overloading** (several methods with same name but different signature)  

**`class ChildClassName(ParentClassName1, ParentClassName2):`**  
$\;\;\;\;$**`pass`**  
* Inheriting from multiple classes is defined after class name in parentheses  
* Keyword pass will allow child class to inherit all parent classes properties and methods when you do not want to add any new ones  


```python
# creating a class "Person" for examples

class Person:
    def __init__(self, fname, lname):
        self.firstname = fname
        self.lastname = lname
    def printname(self):
        print(self.firstname, self.lastname)

#Use the Person class to create an object, and then execute the printname method:

x = Person("John", "Doe")
x.printname()
```

    John Doe
    


```python
# creating a child class

class Student(Person):
    pass

# creating an object of class Student and calling printname() method from parent class

x = Student("Mike", "Olsen")
x.printname()
```

    Mike Olsen
    

**`class ChildClassName(ParentClassName):`**  
$\;\;\;\;$**`def __init__(self, attribute1, attribute2):`**  
$\;\;\;\;\;\;\;\;$**`# add properties etc.`**  
* When the \_\_init\_\_ function is used, it will automatically **override the parents \_\_init\_\_ function**  

**`class ChildClassName(ParentClassName):`**  
$\;\;\;\;$**`def __init__(self, attribute1, attribute2):`**  
$\;\;\;\;\;\;\;\;$**`ParentClassName.__init__(self, attribute1, attribute2)`** 
* A call to the parents \_\_init\_\_ function will allow the child class to **inherit the \_\_init\_\_ function**  
* Note the **.** before the \_\_init\_\_ call  
* Note **no parentheses** after ParentClassName  

**`class ChildClassName(ParentClassName):`**  

$\;\;\;\;$**`def __init__(self, attribute1, attribute2):`**  
$\;\;\;\;\;\;\;\;$**`super().__init__(attribute1, attribute2)`**  
* The super() function will allow the child class to **inherit all the properties and methods** of the parent class  
* When wanting to **modify the output** of a parent method when **overriding a method**, use super() call in the method  
* Further attributes for the child class can be passed in its own \_\_init\_\_ and set in the normal way (along with further methods) after and below the super call  
* Note Python 2.x and earlier requires calls to the super class be defined as  
    **`super(Derived_Class_Name, self).__init__(Parameters_of_Super_Class_Constructor)`**  


```python
# Class B inherits from class A
class A:
    def __init__(self):
        self.property_a = 'Hello'
    
    def do_something(self,smth):
        return self.property_a+str(smth)

    
class B(A):
    def __init__(self):
        super().__init__()      # Inherits methods and properties of class A
    
    #overridden method!!!
    def do_something(self,smth):
        return super().do_something(' --THIS IS B--') + (str(smth)*2)      # Uses output of parent method when overriding
    
    
    
objA = A()
objB = B()

print (objA.do_something(' World'))
print (objB.do_something(' World'))
```

    Hello World
    Hello --THIS IS B-- World World
    

**Method Resolution Order (MRO)**:  

**`ClassName.mro()`**  
**OR**  
**`ClassName.__mro__`**  
* Defines the order in which the base classes are searched when executing a method  
* Old style (Python 2.x and older) classes use DLR or depth-first left to right algorithm (depth first, then left to right) whereas new style classes use Linearization. Child classes are preceeded before their parents, and left to right is searched for each depth level before proceeding to the next parent  

A  &emsp;&emsp;&emsp;&emsp;&ensp;&nbsp;&nbsp; **5th:** Base class is searched last  
|&ensp;\  
|&emsp;B  &emsp;&emsp;&emsp;&emsp; **4th:** Next level up parent is searched (again left to right if more than one)  
|&emsp;&ensp;&nbsp;\  
C&emsp;&emsp;D  &emsp;&emsp;&ensp; **2nd & 3rd:** Immediate parent classes are searched left to right after child class    
|&emsp;&ensp;&nbsp;/  
|&emsp;/  
&nbsp;E  &emsp;&emsp;&emsp;&emsp;&emsp; **1st:** Child class is searched first  


```python
# Showing MRO with multiple class inheritance 
class A:
    def myMethod(self):
        print("In class A")

class B(A):
    def myMethod(self):
        print("In class B")

class C(A):
    pass

class D(B):
    pass

class E(C, D):      # C is prioritised for searching over D
    pass

myObj = E()
myObj.myMethod()

print(E.mro())
print(E.__mro__)
```

    In class B
    [<class '__main__.E'>, <class '__main__.C'>, <class '__main__.D'>, <class '__main__.B'>, <class '__main__.A'>, <class 'object'>]
    (<class '__main__.E'>, <class '__main__.C'>, <class '__main__.D'>, <class '__main__.B'>, <class '__main__.A'>, <class 'object'>)
    

**accessing attribute** values:  

**`objVar_Name.attributeName`**  
* This will display the current value of the attribute stored for the object  


```python
# example obtaining the object attribute radius

redCircle.radius
```




    10



**changing data attributes** directly:  

**`objVar_Name.attributeName = new_AttributeValue`**  
* This will set a new value of the attribute for the object  


```python
# Set the object attribute radius

redCircle.radius = 1
redCircle.radius
```




    1



**methods**:  

* Methods are called by its name, but it's associated to an object (**dependent**)  
* A method is **implicitly passed to the object** on which it is invoked  
* It **may or may not** return any data  
* Methods can operate on the data (instance variables) that is contained by the corresponding class

**difference between methods and functions**:  

* Functions and Methods both look similar as they perform in almost similar ways, but the key difference is the concept of ‘Class and its Object‘  
* Functions can be called only by its name, as it is defined independently  
* Methods can’t be called by its name only, we need to invoke the class by a reference of that class in which it is defined, i.e., method is defined within a class and hence they are dependent on that class and so methods need to be called on an object    
* A method may alter an object’s state, but Python function usually only operates on it, and then prints something or returns a value  

**typical function**:  
**`func_name(arguments)`**  
  
**typical method**:  
**`obj.meth_name(arguments)`**  

**calling** a method:  

**`objVar_Name.meth_Name(argument)`**  
* This will call the method named and change or interact with the data attributes stored for the object as denoted by the method code block  
* **Without parentheses** will return method **parameter format**  


```python
# example using a method to change the object attributes

# print original attribute "radius" value
print("Radius of object:", redCircle.radius)

# use method to add 2 to value
redCircle.add_radius(2)

# print new attribute value
print("Radius of object of after applying the method add_radius(2):", redCircle.radius)

# use method to add 5 to value
redCircle.add_radius(5)

# print new attribute value
print("Radius of object of after applying the method add_radius(5):", redCircle.radius)
```

    Radius of object: 1
    Radius of object of after applying the method add_radius(2): 3
    Radius of object of after applying the method add_radius(5): 8
    


```python
# call method drawCircle to display object

redCircle.drawCircle()
```


    
![png](%23%20%21%20Python_basics%2001.10.23_files/%23%20%21%20Python_basics%2001.10.23_501_0.png)
    


**Method and attribute types (access modifiers)**:  

* Python **does not** implement access modifiers as such, **everything is visible to everyone always**  
* Access to variables or functions can be limited in python, but note **above**  

**Public**:  
Attribues and methods defined without any underscores, these are accessible from outside the Class through an object of the class.  

**Protected**:  
Attributes and methods defined with **1 leading underscore**  
The members declared as Protected are accessible from outside the class but only in a class derived from it that is in the child or subclass.  

**Private**:  
Attributes and methods defined with **2 leading underscores**  
These members are only accessible from within the class. No outside Access is allowed.  


Though note **Python internally renames** the property's and method's names starting with **`__`** with   
**`_CLASSNAME__PROPERTYNAME/METHODNAME`**  
This means they **can actually be accessed** (see above)  

**Special Methods aka Dunder Methods**:  
Methods defined with **2 leading AND 2 trailing underscores**  
These are typically reserved for Python built in and predefined methods and it is **discouraged to create your own** to avoid clashes  

**Special methods**:  

**<center>Arithmetic:<center>**  

|**Operator**|**Description**|**Special Method**|
|:---:|:---|:---|
|+|Addition|\_ \_add_ _(self,other)|
|-|Subtraction|\_ \_sub_ _(self,other)|
|\*|Multiplication|\_ \_mul_ _(self,other)|
|/|Division|\_ \_div_ _(self,other)|
|%|Modulus|\_ \_mod_ _(self,other)|
|\*\*|Exponentiation|\_ \_pow_ _(self,other)|
|+=|In-place addition|\_ \_iadd_ _(self,other)|
|-=|In-place subtraction|\_ \_isub_ _(self,other)|
|\*=|In-place multiplication|\_ \_imul_ _(self,other)|
|/=|In-place division|\_ \_idiv_ _(self,other)|
|%=|In-place modulus|\_ \_imod_ _(self,other)|
|\*\*=|In-place exponentiation|\_ \_ipow_ _(self,other)|  

**<center>Comparison Operators:<center>**  

|**Operator**|**Description**|**Special Method**|
|:---:|:---|:---|
|==|Equal|\_ \_eq_ _(self,other)|
|!=|Not Equal|\_ \_ne_ _(self,other)|
|>|Greater than|\_ \_gt_ _(self,other)|
|>=|Greater or equal than|\_ \_ge_ _(self,other)|
|<|Less than|\_ \_lt_ _(self,other)|
|<=|Less or equal than|\_ \_le_ _(self,other)|

**<center>Type Conversion Operators:<center>**  

|**Operator**|**Description**|**Special Method**|
|:---:|:---|:---|
|str( )|String representation|\_ \_str_ _(self)|
|repr( )|Printable representation (very similar to str())|\_ \_repr_ _(self)|
|int( )|Integer representation|\_ \_int_ _(self)|
|float( )|Float representation|\_ \_float_ _(self)|

**<center>Sequence Operators<center>**  
    
|**Operator**|**Usage**|**Description**|**Special Method**|
|:---:|:---|:---|:---|
|[ ]|myObj [ key ]|Get an item from myObj|\_ \_getitem_ _(self, key)|
|[ ]=|[ key ] = value|Set an item in myObj|\_ \_setitem_ _(self, key, value)|
|del|del myObj[ key ]|Deletes an item in myObj|\_ \_delitem_ _(self, key)|
|[ : ]|myObj[ i : j ]|Get a slice from myObj|\_ \_getslice_ _(self, i, j)|
|[ : ]=|myObj[ i : j ]=values|Set a slice in myObj|\_ \_setslice_ _(self, i, j, values)|
|in|value in myObj|Returns True if value is in myObj|\_ \_contains_ _(self, value)|
|len|len(myObj)|Returns the length of myObj|\_ \_len_ _(self)|

**Getters and Setters**:  

**Getter:**  
**`@property`**  
**`def attributeName(self):`**  
$\;\;\;\;$**`return self.__privateAttribute`**  

**Call with:**  
**`obj.attributeName`**  

**Setter:**  
**`@attributeName.setter`**  
**`def attributeName(self, newVal):`**  
$\;\;\;\;$**`validataion checks prior to setting...`**  
$\;\;\;\;$**`self.__privateAttribute = newVal`**  

**Set with:**  
**`obj.attributeName = newVal`**  

* **`attributeName`** is the name of the method or attribute to set using the decorator and should not be private here, however ensure to call the private attribute and set accordingly within the method  
* Can be done in a similar way to Java with seperate methods for getting and setting attributes, however this means methods will need to be explicitly called otherwise relevant validation checks will not be carried out, or even the wrong attribute may be changed  
* In Python, we can use the **@property** decorator as the getter, and **@attributeName.setter**  


```python
# Java style getters and setters
class Exam:
    def __init__(self, name):
        self.name = name
        self.__mark = None
        
    def set_mark(self, mark):
        if ((mark is None) or (0<=mark<=100)):
            self.__mark = mark
        else:
            raise Exception("Invalid mark.")
    
    def get_mark(self):
        return self.__mark
```


```python
# need to explicitly call the corresponding method, because we cannot change the value of the property (its private)
myExam = Exam("Scripting_for_Data_Science")
myExam.set_mark(90)
print(myExam.get_mark())
```

    90
    


```python
# Showing private attributes can still be set and retrieved without use of the methods, and hence the validation checks are not carried out
# Note this can also be done when using the @property decorator
myExam._Exam__mark = 120
print("Private attribute set explicitly;")
print("Private attribute retrieved explicitly: ", myExam._Exam__mark)
print("Private attribute retrieved with getter method: ", myExam.get_mark())
```

    Private attribute set explicitly;
    Private attribute retrieved explicitly:  120
    Private attribute retrieved with getter method:  120
    


```python
# If attribute is set (without using the private underscores) with Java style getters and setters, 
# a new attribute will be created and no validation checks done
myExam.mark = 150
print("Attribute set with non-private attribute name;")
print("Different non-private attribute has been set: ", myExam.mark)
print("Private attribute retrieved with getter method: ", myExam.get_mark())
```

    Attribute set with non-private attribute name;
    Different non-private attribute has been set:  150
    Private attribute retrieved with getter method:  120
    


```python
# Using @property decorator to get and set private attribute
class Exam:
    def __init__(self, name):
        self.name = name
        self.__mark = None
    
    # getter for property (attribute) "mark" ("__mark")
    @property
    def mark(self):
        return self.__mark
    
    # setter for property (attribute) "mark" ("__mark")
    @mark.setter
    def mark(self, mark):
        if ((mark is None) or (0<=mark<=100)):
            self.__mark = mark
        else:
            raise Exception("Invalid mark.") 
```


```python
# Setting private attribute without having to call methods explicitly
# Note validation checks are still carried out and it is in fact the private attribute which is set
myExam = Exam("Scripting_for_Data_Science")
myExam.mark = 90
print("Attribute set with non-private attribute name;")
print("Mark retrieved using @property decorator: ", myExam.mark)
print("Private mark retrieved explicitly: ", myExam._Exam__mark)
```

    Attribute set with non-private attribute name;
    Mark retrieved using @property decorator:  90
    Private mark retrieved explicitly:  90
    

**dir** function:  

**`dir(objVar_Name)`**  
* This returns a list of the attributes and methods of the named object  


```python
# example of finding which methods can be used on the object redCircle

dir(redCircle)
```




    ['__class__',
     '__delattr__',
     '__dict__',
     '__dir__',
     '__doc__',
     '__eq__',
     '__format__',
     '__ge__',
     '__getattribute__',
     '__gt__',
     '__hash__',
     '__init__',
     '__init_subclass__',
     '__le__',
     '__lt__',
     '__module__',
     '__ne__',
     '__new__',
     '__reduce__',
     '__reduce_ex__',
     '__repr__',
     '__setattr__',
     '__sizeof__',
     '__str__',
     '__subclasshook__',
     '__weakref__',
     'add_radius',
     'color',
     'drawCircle',
     'radius']



**Duck typing**:  

* In Python, an object or classes type is of lesser importance than the methods or attributes it defines  
* If two or more classes contains a certain attribute or method, they can all be passed to the same function which makes use of that attribute or method without issue  


```python
# Python program to demonstrate
# duck typing
  
class Bird:
    def fly(self):
        print("fly with wings")
        
class Airplane:
    def fly(self):
        print("fly with fuel")
        
class Fish:
    def swim(self):
        print("fish swim in sea")
        
# Attributes having same name are
# considered as duck typing
for obj in Bird(), Airplane(), Fish():
    obj.fly()
```

    fly with wings
    fly with fuel
    


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_6032/32223823.py in <module>
         17 # considered as duck typing
         18 for obj in Bird(), Airplane(), Fish():
    ---> 19     obj.fly()
    

    AttributeError: 'Fish' object has no attribute 'fly'


[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>Command line arguments;</center>

**Using sys**:  

**`import sys`**  
**`for i,v in enumerate(sys.argv):`**  
$\;\;\;\;$**`print("Parameter #{}: {}".format(i,v))`**  
* Iterates over command line parameters  
* **`argv[0]`** is the **script name** (it is operating system dependent whether this is a full pathname or not)  


```python
import sys

for i,v in enumerate(sys.argv):
    print("Parameter #{}: {}".format(i,v))
```

    Parameter #0: C:\Users\ajdpi\anaconda3\lib\site-packages\ipykernel_launcher.py
    Parameter #1: -f
    Parameter #2: C:\Users\ajdpi\AppData\Roaming\jupyter\runtime\kernel-4e40d79a-99de-41b0-a21d-15ece96748bb.json
    

**argparse**:  

**`import argparse`**  


**`parser = argparse.ArgumentParser(prog=None, description=None)`**  
* **`prog`** = name of program (default: sys.argv[0])  
* **`description`** = Description of what the program does  


**`parser.add_argument('--parameterFullName', '-p', dest='var', type=str, help='Some help info', required=False, default='defaultValue', choices
=['ele1','ele2'], nargs=intNumberOfArgs, metavar='nameOfExpectedValue', action='append')`**  
* **`-p`** is an abreviation (leading with a single **`-`** ) of **`parametersFullName`** ( leading with double **`--`** ) and either can be used to provide the input  
* **`dest`** is the variable name you want to save the parameter to (accessed: args.var), if none given, name is inferred from the option  
* **`choices`** option limits arguments to the given list  
* **`nargs`** specifies the exact number of command-line arguments that should be provided, **`'*'`** specifies variable  
* **`metavar`** option gives a name to the expected value in error and help outputs  
* **`action`** allows grouping of repeating inputs  



**`args = parser.parse_args()`**  
* Adds arguments to a variable  

**`argVar = args.dest`**  
* Access variable 'dest' and saves to variable, other parameters can be accessed in a similar way  


```python
import argparse

help(argparse.ArgumentParser.add_argument)
```

    Help on function add_argument in module argparse:
    
    add_argument(self, *args, **kwargs)
        add_argument(dest, ..., name=value, ...)
        add_argument(option_string, option_string, ..., name=value, ...)
    
    

**exit codes**:  

**`import sys`**  

**`{code}`**  

**`sys.exit(intExitCode)`**  
* Usually used after an if statement  
* If no exit code provided, then system exit code **`0`** is used which is considered **successful termination**  
* A string can also be passed as an exit code message, and will have the exit code **`1`**  
* In Windows, the exit code from the last program run can be obtained in PowerShell using command **`echo $lastexitcode`**  

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>PIP;</center>

* PIP is a package manager for Python that allows you to install and manage additional libraries and dependencies that are not distributed as part of the standard library  
* A package is a unit of distribution that can contain a library or an executable or both  
* a library is a set of modules which makes sense to be together and that can be used in a program or another library  


```python
# get pip version

!pip --version
```

    pip 21.2.4 from C:\Users\ajdpi\anaconda3\lib\site-packages\pip (python 3.9)
    
    


```python
# get list of installed packages

!pip list
```

    Package                            Version
    ---------------------------------- --------------------
    alabaster                          0.7.12
    anaconda-client                    1.9.0
    anaconda-navigator                 2.1.4
    anaconda-project                   0.10.1
    anyio                              2.2.0
    appdirs                            1.4.4
    argh                               0.26.2
    argon2-cffi                        20.1.0
    arrow                              0.13.1
    asn1crypto                         1.4.0
    astroid                            2.6.6
    astropy                            4.3.1
    async-generator                    1.10
    atomicwrites                       1.4.0
    attrs                              21.2.0
    autopep8                           1.5.7
    Babel                              2.9.1
    backcall                           0.2.0
    backports.functools-lru-cache      1.6.4
    backports.shutil-get-terminal-size 1.0.0
    backports.tempfile                 1.0
    backports.weakref                  1.0.post1
    bcrypt                             3.2.0
    beautifulsoup4                     4.10.0
    binaryornot                        0.4.4
    bitarray                           2.3.0
    bkcharts                           0.2
    black                              19.10b0
    bleach                             4.0.0
    bokeh                              2.4.1
    boto                               2.49.0
    Bottleneck                         1.3.2
    brotlipy                           0.7.0
    cached-property                    1.5.2
    certifi                            2021.10.8
    cffi                               1.14.6
    chardet                            4.0.0
    charset-normalizer                 2.0.4
    click                              8.0.3
    cloudpickle                        2.0.0
    clyent                             1.2.2
    colorama                           0.4.4
    comtypes                           1.1.10
    conda                              22.9.0
    conda-build                        3.21.6
    conda-content-trust                0+unknown
    conda-pack                         0.6.0
    conda-package-handling             1.7.3
    conda-repo-cli                     1.0.4
    conda-token                        0.3.0
    conda-verify                       3.4.2
    contextlib2                        0.6.0.post1
    cookiecutter                       1.7.2
    cryptography                       3.4.8
    cycler                             0.10.0
    Cython                             0.29.24
    cytoolz                            0.11.0
    daal4py                            2021.3.0
    dask                               2021.10.0
    debugpy                            1.4.1
    decorator                          5.1.0
    defusedxml                         0.7.1
    diff-match-patch                   20200713
    distributed                        2021.10.0
    docutils                           0.17.1
    entrypoints                        0.3
    et-xmlfile                         1.1.0
    fastcache                          1.1.0
    filelock                           3.3.1
    flake8                             3.9.2
    Flask                              1.1.2
    fonttools                          4.25.0
    fsspec                             2021.10.1
    future                             0.18.2
    gevent                             21.8.0
    glob2                              0.7
    greenlet                           1.1.1
    h5py                               3.2.1
    HeapDict                           1.0.1
    html5lib                           1.1
    ibm-cloud-sdk-core                 1.7.3
    ibm-watson                         5.0.2
    idna                               3.2
    imagecodecs                        2021.8.26
    imageio                            2.9.0
    imagesize                          1.2.0
    importlib-metadata                 4.8.1
    inflection                         0.5.1
    iniconfig                          1.1.1
    intervaltree                       3.1.0
    ipykernel                          6.4.1
    ipython                            7.29.0
    ipython-genutils                   0.2.0
    ipywidgets                         7.6.5
    isort                              5.9.3
    itsdangerous                       2.0.1
    jdcal                              1.4.1
    jedi                               0.18.0
    Jinja2                             2.11.3
    jinja2-time                        0.2.0
    joblib                             1.1.0
    json5                              0.9.6
    jsonschema                         3.2.0
    jupyter                            1.0.0
    jupyter-client                     6.1.12
    jupyter-console                    6.4.0
    jupyter-core                       4.8.1
    jupyter-server                     1.4.1
    jupyterlab                         3.2.1
    jupyterlab-pygments                0.1.2
    jupyterlab-server                  2.8.2
    jupyterlab-widgets                 1.0.0
    keyring                            23.1.0
    kiwisolver                         1.3.1
    lazy-object-proxy                  1.6.0
    libarchive-c                       2.9
    llvmlite                           0.37.0
    locket                             0.2.1
    lxml                               4.6.3
    MarkupSafe                         1.1.1
    matplotlib                         3.4.3
    matplotlib-inline                  0.1.2
    mccabe                             0.6.1
    menuinst                           1.4.18
    mistune                            0.8.4
    mkl-fft                            1.3.1
    mkl-random                         1.2.2
    mkl-service                        2.4.0
    mlxtend                            0.21.0
    mock                               4.0.3
    more-itertools                     8.10.0
    mpmath                             1.2.1
    msgpack                            1.0.2
    multipledispatch                   0.6.0
    munkres                            1.1.4
    mypy                               0.942
    mypy-extensions                    0.4.3
    navigator-updater                  0.2.1
    nbclassic                          0.2.6
    nbclient                           0.5.3
    nbconvert                          6.1.0
    nbformat                           5.1.3
    nest-asyncio                       1.5.1
    networkx                           2.6.3
    nltk                               3.6.5
    nose                               1.3.7
    notebook                           6.4.5
    numba                              0.54.1
    numexpr                            2.7.3
    numpy                              1.20.3
    numpydoc                           1.1.0
    olefile                            0.46
    opencv-python                      4.5.5.62
    openpyxl                           3.0.9
    packaging                          21.0
    pandas                             1.3.4
    pandocfilters                      1.4.3
    paramiko                           2.7.2
    parso                              0.8.2
    partd                              1.2.0
    path                               16.0.0
    pathlib2                           2.3.6
    pathspec                           0.7.0
    patsy                              0.5.2
    pep8                               1.7.1
    pexpect                            4.8.0
    pickleshare                        0.7.5
    Pillow                             8.4.0
    pip                                21.2.4
    pkginfo                            1.7.1
    plotly                             4.14.3
    pluggy                             0.13.1
    ply                                3.11
    poyo                               0.5.0
    prometheus-client                  0.11.0
    prompt-toolkit                     3.0.20
    psutil                             5.8.0
    ptyprocess                         0.7.0
    py                                 1.10.0
    pycodestyle                        2.7.0
    pycoingecko                        2.2.0
    pycosat                            0.6.3
    pycparser                          2.20
    pycurl                             7.44.1
    pydocstyle                         6.1.1
    pyerfa                             2.0.0
    pyflakes                           2.3.1
    Pygments                           2.10.0
    PyJWT                              2.1.0
    pylint                             2.9.6
    pyls-spyder                        0.4.0
    PyNaCl                             1.4.0
    pyodbc                             4.0.0-unsupported
    pyOpenSSL                          21.0.0
    pyparsing                          3.0.4
    pyreadline                         2.1
    pyrsistent                         0.18.0
    PySocks                            1.7.1
    pytest                             6.2.4
    python-dateutil                    2.8.2
    python-lsp-black                   1.0.0
    python-lsp-jsonrpc                 1.0.0
    python-lsp-server                  1.2.4
    python-slugify                     5.0.2
    pytz                               2021.3
    PyWavelets                         1.1.1
    pywin32                            228
    pywin32-ctypes                     0.2.0
    pywinpty                           0.5.7
    PyYAML                             6.0
    pyzmq                              22.2.1
    QDarkStyle                         3.0.2
    qstylizer                          0.1.10
    QtAwesome                          1.0.2
    qtconsole                          5.1.1
    QtPy                               1.10.0
    regex                              2021.8.3
    requests                           2.26.0
    retrying                           1.3.3
    rope                               0.19.0
    Rtree                              0.9.7
    ruamel-yaml-conda                  0.15.100
    scikit-image                       0.18.3
    scikit-learn                       1.1.3
    scikit-learn-intelex               2021.20210714.120553
    scipy                              1.7.1
    seaborn                            0.11.2
    Send2Trash                         1.8.0
    setuptools                         58.0.4
    simplegeneric                      0.8.1
    singledispatch                     3.7.0
    sip                                4.19.13
    six                                1.16.0
    sniffio                            1.2.0
    snowballstemmer                    2.1.0
    sortedcollections                  2.1.0
    sortedcontainers                   2.4.0
    soupsieve                          2.2.1
    Sphinx                             4.2.0
    sphinxcontrib-applehelp            1.0.2
    sphinxcontrib-devhelp              1.0.2
    sphinxcontrib-htmlhelp             2.0.0
    sphinxcontrib-jsmath               1.0.1
    sphinxcontrib-qthelp               1.0.3
    sphinxcontrib-serializinghtml      1.1.5
    sphinxcontrib-websupport           1.2.4
    spyder                             5.1.5
    spyder-kernels                     2.1.3
    SQLAlchemy                         1.4.22
    statsmodels                        0.12.2
    sympy                              1.9
    tables                             3.6.1
    TBB                                0.2
    

**install PIP package**:  

**`!pip install package_name`**  
* Will install package named  
* Once installed, packages / modules can be imported  

**uninstall PIP packages**:  

**`!pip uninstall package_name`**  
* Will uninstall package named  

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>Working with Files

### <center>Opening and Reading Files;</center>

**open** function:  

**`open("file", "mode")`**  
* Built in function  
* Opens a file and returns a corresponding file object  
* Both **"file" and "mode"** must be entered as a **string within parentheses**  
* "file" is a path-like object made up of **file name and directory**  
* "mode" is an **optional** string which specifies which mode file is to be opened in, common modes include:<br>
**`r`* = **reading (default mode)**, will **fail** if file does **not exist**<br>
**`a`* = **appending**, stream is positioned at **end of file**, **creates new file** if file does **not exist**<br>
**`w`* = **writing**, will **truncate file first** (empty contents), or **create new file** if file does **not exist**  
**`+`* = **updating**, add **`+`** after any usual mode e.g. `w+` to allow **reading and writing**, note `w+` mode will still truncate file first, `r+` will overwrite what is in streams way  

**file object**

**`varFile_Obj = open(file, mode)`**  
* **Information** about the file can be obtained by setting the open function to a **file object variable**  
* "mode" is again **optional**  
* Once a file is opened and data saved as a file object, then the following methods can be used on it  
* **MUST close** file object once finished using file unless using with statement (see below)


```python
# setting file name to save retyping each time

file_name = "data/reading files test.txt"
```


```python
# example opening a .txt file and assigning the data to a file object variable

file_obj = open(file_name, "w")
```


```python
# the file object just stores the access data for the file, this is what NEEDS closing when finished

print(file_obj)
```

    <_io.TextIOWrapper name='data/reading files test.txt' mode='w' encoding='cp1252'>
    

**name** method:

**`varFile_Obj.name`**
* Returns **name** of the file 


```python
# method used to obtain name of file

file_obj.name
```




    'data/reading files test.txt'



**mode** method:  

**`varFile_Obj.mode`**  
* Returns **mode** of file object  


```python
# method used to see what mode file is opened in

file_obj.mode      # 'r' is for reading
```




    'w'



**closed** method:  

**`varFile_Obj.closed`**  
* Checks if a file is **closed** and returns **True** if is


```python
# note file is still open after executing the open function as above

file_obj.closed
```




    False



**close** method:  

**`varFile_Obj.close()`**  
* **Closes** a file  
* **ALWAYS** close a file after opening with the above function 
* Note it is the **"file object variable"** that gets **closed**
* Must include **parenthesis**  


```python
# always close file (file object variable) after opening as above with following method

file_obj.close()
```


```python
# checking file is closed

file_obj.closed
```




    True



**with** statment:  

**`with open(file, mode) as varFile_Obj:`**  
    **`    var = varFile_Obj.read()`**  
* **Better practice** to use **"with" statment** to open files as it **automatically closes** them 
* Code will **run everything indented, then close file**  
* Can check file is closed as well as print file content, but **cannot read from file** outside of code block  
* Must include **colon**

**read** method:  

**`.read()`**  
* File read as a **whole** and stores values in the variable "var" as a **string**  
* Stream positioned at the end of the file after running   
* **Optional argument** determines **number of characters read** each time method is run moving stream position accordingly, note new line characters "\n" count as a single character  
* Stream position reset if the file is reopened 


```python
# example using read method to save data from a file

file_obj = open(file_name)       # openeing file and storing access data as a file object

file_data = file_obj.read()      # reading data from file and saving to a variable
file_data                        # examining the raw data, we can see that "\n" is 
                                 # included which signals Python to start a new line
```




    ''




```python
# if we print the data, the "\n" is not visable as the new line operation has been executed

print(file_data)

file_obj.close()      # closing file
```

    
    


```python
file_obj.closed
```




    True




```python
# opening file using "with" statement
# better practice as it automatically closes file after runing indented block

# "read" method saves the values of the file to the variable "file_data" as a string

with open(file_name, "r") as file_obj2:
    file_data = file_obj2.read()
    file_data
    print(file_obj2.closed)    # shows file is still open during running of indented block
```

    False
    


```python
# file is now closed after "with" statement has been completed

file_obj2.closed
```




    True




```python
# can print the values of the file that are stored in the "file_data" variable

print(file_data)
```

    
    


```python
# stream moves position each time the code is run until  
# file is closed and reopened which will reset its position

# note with "read" method, file is read as a whole, so stream is  
# positioned at end of file after initial running
# data is stored as a string  
# subsiquent runs of the code without reopening file will return 
# blank due to stream being at end of file

with open(file_name, "r") as file_obj3:
    file_data2 = file_obj3.read()                  # 1st pass of code
    print("first running of code:", file_data2)
    print("")
    file_data2 = file_obj3.read()                  # 2nd pass of code
    print("second running of code:", file_data2)
```

    first running of code: 
    
    second running of code: 
    


```python
file_obj3.closed
```




    True



**readline** method:  

**`.readline()`**  
* Reads **each line** of file each time code is run and stream is updated accordingly  
* Stores values as a **string**  
* **Optional argument** determines **number of characters read** each time method is run up to **max end of line**  
* If line has **NOT** been completely read, stream will **stay in position** and continue from there next time code is run  
* Stream position reset if the file is reopened  
* Must include **colon**


```python
# method "readline" reads each line of the file, data is also stored as a string
# each subsiquent pass reads the next line and updates the streams position accordingly
# if file is closed and reopened, the stream will reset to the beginning of the file

with open(file_name, "r") as file_obj4:
    file_data3 = file_obj4.readline()               # 1st pass of code
    print("first running of code:", file_data3)
    file_data3 = file_obj4.readline()               # 2ns pass of code
    print("second running of code:", file_data3)
```

    first running of code: 
    second running of code: 
    


```python
file_obj4.closed
```




    True



**readlines** method:  

**`.readlines()`**  
* Outputs **each line** as an **element** in a **list**  
* **Optional argument** will read **complete lines up to the end of the line** which equals the number of Characters entered, note new line characters **"\n" count as the beginning of a line**  
* Must include **colon**


```python
# method "readlines" outputs each line of the file as an element in a list
# note "new line" escape character is also stored in the list

with open(file_name, "r") as file_obj5:
    file_data4 = file_obj5.readlines()
    
    print(file_data4)
```

    []
    

using a **loop** to print **each line** individually  

**`with open(file_name, "r") as file_obj5:`**  
$\;\;\;\;$**`i = 1      # Used as an iterator`**  
$\;\;\;\;$**`for line in file_obj5:`**  
$\;\;\;\;\;\;\;\;$**`print("Line ", i, ": ", line)`**  
$\;\;\;\;\;\;\;\;$**`i+=1`**  
* Two methods to read file line by line:  
    * Either read the file as before and break the rows manually, this can be troublesome as different systems use differnt **end-of-line** characters 
    * Or read them line by line as shown here delegating this task to the underlying library allowing code to be **cross-platform**  


```python
# a loop can be used to print out each line individually as a string

with open(file_name, "r") as file_obj5:
    i = 1      # Used as an iterator 
    for line in file_obj5:
        print("Line ", i, ": ", line)
        i+=1
```


```python
file_obj5.closed
```




    True




```python
# argument in "read" method determines how many characters are read each time code is run, 
# the stream is updated at each pass continuing on the next and resetting when file is reopened

# note the \n for new line is read as a single character
# each line is 14 characters long NOT including escape characters for new line

with open (file_name, "r") as file_obj6:
    
    file_data5 = file_obj6.read(16)
    print("1st pass of read method, 16 characters:", file_data5)
    
    file_data5 = file_obj6.read(16)
    print("2nd pass of read method, 16 characters:", file_data5)
```

    1st pass of read method, 16 characters: 
    2nd pass of read method, 16 characters: 
    


```python
# using readline method the argument determines how many characters are read up to MAX end of line
# if line has NOT been completely read, stream will NOT go to end of line but stay in position
# continuing on next pass

# each line is 14 characters long NOT including escape characters for new line

with open (file_name, "r") as file_obj6:
    
    file_data6 = file_obj6.readline(8)
    print("1st pass of readline method, 8 characters:", file_data6)
    
    file_data6 = file_obj6.readline(12)
    print("2nd pass of readline method, 12 characters:", file_data6)
    
    file_data6 = file_obj6.readline(16)
    print("2nd pass of readline method, 16 characters:", file_data6)
```

    1st pass of readline method, 8 characters: 
    2nd pass of readline method, 12 characters: 
    2nd pass of readline method, 16 characters: 
    


```python
# method readlines argument will read the entire line regardless of characters entered 
# and forward the stream position, if enough characters are passed to the argument, it 
# will read the next line entirely too
# note that the new line character counts towards the next line

# each line is 14 characters long NOT including escape characters for new line

with open (file_name, "r") as file_obj6:
        
    file_data7 = file_obj6.readlines(15)
    print("1st pass of readlines method, 15 characters:", file_data7)
            
    file_data7 = file_obj6.readlines(5)
    print("2nd pass of readlines method, 5 characters:", file_data7)
              
    file_data7 = file_obj6.readlines(5)
    print("2nd pass of readlines method, 5 characters:", file_data7)
```

    1st pass of readlines method, 15 characters: []
    2nd pass of readlines method, 5 characters: []
    2nd pass of readlines method, 5 characters: []
    

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <Center>Working with Files

### <center>Writing to Files;</center>

**write** method:  

**`file_obj.write("text_to_be_written_to_file")`**  
* This will write string in argument as text in file  
* If wanting to start a new line, **add "\n"** escape character to **end of string**  


```python
# setting file name to save retyping for each example 

file_name = "data/writing to files test.txt"
```


```python
# see "open function" above for more info on opening files

# opening in write mode will overwrite file if it exists, or creates a new file

file_object = open(file_name, "w")
```


```python
# example using write method to write to file
# this will not write "\n" in the file, but start a new line
# note number of characters added to file are printed

file_object.write("This is line 1\n")    # 14 characters plus "\n", seen as 15 characters
```




    15




```python
# as before, if opening a file this way, ALWAYS close it when finished

file_object.close()
```


```python
# checking to see if file is closed

file_object.closed
```




    True




```python
# reading and printing contents of file

with open(file_name, "r") as file_object:
    file_data = file_object.read()
    
    print(file_data)
```

    This is line 1
    
    


```python
# using "with" statement is better practice as it closes file automatically after running indented block

# example using with statement to write 2 separate lines to file before closing it

with open(file_name, "w") as file_object:
    file_object.write("This is now line 1\n")
    file_object.write("This is line 2\n")
```


```python
# reading and printing contents of file

with open(file_name, "r") as file_object:
    file_data = file_object.read()
    
    print(file_data)
```

    This is now line 1
    This is line 2
    
    

**seek** method:  

**`file_obj.seek(offset, whence=0)`**  
* Used to **set** the **streams position** within a file 
* **"offset"** is **required**, determines number of characters to skip over  
* **"whence"** is **optional** and **defaults to 0**  
* whence can be set to 0 = absolute file positioning (from beginning), 1 = seek relative to current position, 2 = set stream at end of file...in Python 3 CANNOT seek backwards  
* Theres **no return value**  


```python
# setting file name to save retyping for each example 

test_file_name = "data/stream test.txt"
```


```python
# without resetting stream position, stream will be at end of file after writing to it 
# and would need to be closed and reopened to read the contents

with open(test_file_name, "w+") as file_object:        # open file
    file_object.write("This is now line 1\n")          # write text to file
    file_object.write("This is now line 2\n")
    
    file_data = file_object.read()                     # read file and assign to variable
    
    print(file_data)                                   # Will print nothing as stream was at end of file when read
```

    
    


```python
# combining write and read in the same "with" statement
# using "seek" method to reset stream position to be able to read and print contents
# this works in both "r+" and "w+" modes ("+" mode = for updating)

with open(test_file_name, "w+") as file_object:        # open file
    file_object.write("This is now line 3\n")          # write text to file
    file_object.write("This is now line 4\n")
    
    file_object.seek(0)                                # reset stream position
    
    file_data = file_object.read()                     # read file and assign to variable
    
    print(file_data)  
```

    This is now line 3
    This is now line 4
    
    


```python
# using seek method to position stream to write to file using absolute positioning

with open(test_file_name, "r+") as file_object:        # open file
    file_object.seek(38)                               # setting stream to end of file using absolute positioning
    file_object.write("This is now line 5\n")          # write text to file
    file_object.write("This is now line 6\n")
    
    file_object.seek(0)                                # reset stream position to beginning of file
    
    file_data = file_object.read()                     # read file and assign to variable
    
    print(file_data)  
```

    This is now line 3
    This is now line 4This is now line 5
    This is now line 6
    
    


```python
# using seek method to position stream to write to file using end of file seek positioning

with open(test_file_name, "r+") as file_object:     # open file
    file_object.seek(0,2)                           # setting stream to end of file using end of file positioning
    file_object.write("This is now line 7\n")       # write text to file
    file_object.write("This is now line 8\n")
    
    file_object.seek(0)                             # reset stream position to beginning of file
    
    file_data = file_object.read()                  # read file and assign to variable
    
    print(file_data)  
```

    This is now line 3
    This is now line 4This is now line 5
    This is now line 6
    This is now line 7
    This is now line 8
    
    

**tell** method:  

**`file_obj.tell()`**  
* Will return **current stream position**, when file is opened stream will be at 0 (beginning of file) unless opened in append mode  


```python
# example using .tell() method to return stream position

with open(test_file_name, "w+") as file_object:        # open file
    file_object.write("This is now line 9\n")          # write text to file
    file_object.write("This is now line 10\n")
    
    file_object.seek(0)                                # reset stream position to beginning of file
    
    print("Stream position: ", file_object.tell())     # print stream position using .tell() method
    
    file_data = file_object.read(5)                    # read first 5 characters of file and assign to variable
    
    print(file_data)                                   # print read characters
    print("Updated stream position: ", file_object.tell())   # print updated stream position
```

    Stream position:  0
    This 
    Updated stream position:  5
    


```python
# checking file is closed

file_object.closed
```




    True



**writing from a list**:  

**`list_var = ["line1", "line2",....]`**  

**`with open("file", "mode") as file_obj:`**  
**`      for each_line in list_var:`**  
**`           file_obj.write(each_line)`**  
* **Must** use **loop** to iterate over each element to write, **cannot write list direct** to file (writing to file needs to be a string)  



```python
# can write to a file from a list using a for loop

list1 = ["Line A\n", "Line B\n", "Line C\n"]      # populating list

with open(file_name, "w+") as file_object:  # opening file
                                            # if we tried to write to file here, would cause error 
                                            # as cannot write direct from a list, only a string
    
    for each_line in list1:                 # using for loop to write each element of list to file
        file_object.write(each_line)  
    
    file_object.seek(0)                     # reset stream position
    
    file_data = file_object.read()          # read file contents
    print(file_data)                        # print file contents
```

    Line A
    Line B
    Line C
    
    

**copying files**:  
  
**`with open("file", "readable_mode") as readfile_obj:`**  
    **`    with open("file2", "writable_mode") as writefile_obj:`**  
    **`        for each_line in readfile_obj:`**  
    **`            writefile_obj.write(each_line)`**  
* **Must** open file to be copied in a **readable mode** e.g. `r` or `r+`  
* **Must** open file to be written to in a **writable / appendable mode** e.g. `w` or `a`  
* Use **loop** to iterate over each line from file to be copied  


```python
# a file can be copied as follows

with open(file_name, "r") as readfile_obj:                      # open file to be copied in readable mode
    
    with open(file_name + " copy", "w+") as writefile_obj:      # open/create file to copy to in writable mode
        
        for each_line in readfile_obj:                  # for loop to iterate over each line in file to be copied
            
            writefile_obj.write(each_line)              # write each line to new file
            
        readfile_obj.seek(0)                            # reset stream position on read file
        writefile_obj.seek(0)                           # reset stream position on write file

        readfile_data = readfile_obj.read()             # read file content and save to variable
        writefile_data = writefile_obj.read()           
        
print("readfile:\n", readfile_data)                       # print file content
print("copied file:\n", writefile_data)
```

    readfile:
     Line A
    Line B
    Line C
    
    copied file:
     Line A
    Line B
    Line C
    
    

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>CSV Files;</center>

**CSV files**:  

* csv files are "comma-separated values" and is a structured text file  
* Each line contains an entry in the dataset  
* Each attribute is separated by a **delimiter** (typically a comma or semi-colon)  
* **Usually** the first line is the **column headers**  
* CSV files are normally created by programs that handle large amounts of data. They are a convenient way to export data from spreadsheets and databases as well as import or use it in other programs  
* Can **read** and **write** to **csv files** with **pandas**, see pandas section for more info  

**Reading csv files**  

csv files can be opened in the normal way (though better to use **csv** or **pandas** libraries:  
**`with open(filePath,mode) as file_objVar:`**  
$\;\;\;\;$**`text = file_objVar.read()`**  
$\;\;\;\;$**`print(text)`**  
* Note **end of line characters** are still **present**  


```python
# example reading in a csv file without use of a library

print("1st line is a header (though not always present):\n")

with open('data/iris.csv','r') as fs:
    text = fs.read()
    print(text[:101])    # Only printing first 3 lines for clarity
```

    1st line is a header (though not always present):
    
    sepal_length,sepal_width,petal_length,petal_width,species
    5.1,3.5,1.4,0.2,setosa
    4.9,3,1.4,0.2,setosa
    

**Reading csv to a dataset list**  

csv files can also be read in splitting each line element by its delimiter and adding each line as an entry to a list  
This is **easier** to do **using the csv library** (see below)  
**`datasetVar = [ ]`**  
**`with open(filePath) as file_objVar:`**  
$\;\;\;\;$**`headerVar = file_objVar.readline()`**  
$\;\;\;\;$**`for line in file_objVar:`**  
$\;\;\;\;\;\;\;\;$**`datasetVar.append( line.split(delimeter))`**  
* **Header** can be read off as the first line outside of the for loop to its own variable  
* Each line is read one at a time before spliting each element by the given delimeter and appending the entry as an element in the dataset  
* Note **end of line characters** are still **present**  


```python
# example of manually reading a csv file to a dataset

dataset = []

with open('data/iris.csv') as fs:
    header = fs.readline()
    print (header)
    for line in fs:
        dataset.append( line.split(',') )
        
print(dataset[:2])
```

    sepal_length,sepal_width,petal_length,petal_width,species
    
    [['5.1', '3.5', '1.4', '0.2', 'setosa\n'], ['4.9', '3', '1.4', '0.2', 'setosa\n']]
    

**Using csv library**:  

**`import csv`**  

**`datasetVar = [ ]`**  
**`with open(filePath) as file_objVar:`**  
$\;\;\;\;$**`csvReaderObj = csv.reader(file_objVar, delimiter= delimeter)`**  
$\;\;\;\;$**`for listEntryRead/rowVar in csvReaderObj:`**  
$\;\;\;\;\;\;\;\;$**`datasetVar.append(listEntryRead/rowVar)`**  
* **`delimiter`** defaults to **`","`**  
* This method will read in the **header row** as the first element in the dataset (**index [0]**)  
* Library will **remove end of line characters**  
* **Faster than Pandas** for **small datasets (<1k rows)**  
* Though **Pandas** is **faster** for **large datasets**  


```python
# Using csv library to read csv file to a dataset

import csv

dataset =[]

with open('data/iris.csv') as fs:
    csv_reader = csv.reader(fs,delimiter=',') #if it is a comma, it can be omitted
    for row in csv_reader:
        dataset.append(row)
        
print(dataset[:3])
```

    [['sepal_length', 'sepal_width', 'petal_length', 'petal_width', 'species'], ['5.1', '3.5', '1.4', '0.2', 'setosa'], ['4.9', '3', '1.4', '0.2', 'setosa']]
    

**Using pandas to read csv to dataframe:**  

**`import pandas as pd`**  

**`df = pd.read_csv('filePath',header=None)`**  
* Reads csv file to dataframe  
* **`header`** is optional, defaults to using column names, set to none (as above) if none present in file  


```python
import pandas as pd

df = pd.read_csv('data/iris.csv')
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>sepal_length</th>
      <th>sepal_width</th>
      <th>petal_length</th>
      <th>petal_width</th>
      <th>species</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>5.1</td>
      <td>3.5</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4.9</td>
      <td>3.0</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4.7</td>
      <td>3.2</td>
      <td>1.3</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4.6</td>
      <td>3.1</td>
      <td>1.5</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5.0</td>
      <td>3.6</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>145</th>
      <td>6.7</td>
      <td>3.0</td>
      <td>5.2</td>
      <td>2.3</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>146</th>
      <td>6.3</td>
      <td>2.5</td>
      <td>5.0</td>
      <td>1.9</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>147</th>
      <td>6.5</td>
      <td>3.0</td>
      <td>5.2</td>
      <td>2.0</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>148</th>
      <td>6.2</td>
      <td>3.4</td>
      <td>5.4</td>
      <td>2.3</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>149</th>
      <td>5.9</td>
      <td>3.0</td>
      <td>5.1</td>
      <td>1.8</td>
      <td>virginica</td>
    </tr>
  </tbody>
</table>
<p>150 rows × 5 columns</p>
</div>



**Writing to csv file**:  

**Better to use csv library** (see below)  
**`populatedDataset = [[entry1_ele1, entry1_ele2],[entry2_ele1, entry2_ele2]...]`**  
**`with open(filePath, 'w') as file_objVar:`**  
$\;\;\;\;$**`for line in populatedDataset:`**  
$\;\;\;\;\;\;\;\;$**`file_objVar.write(delimeterToUse.join(line)+"\n")`**  
* Writes to a csv file from a dataset (list of lists)  
* **join** method used to set delimeter between each element of an entry  
* **`\n`** used to start a new line after each entry added to file  


```python
# example of manually writting to a csv file from a dataset

with open('data/my_iris.csv','w') as fs:
    for line in dataset:
        fs.write(",".join(line)+"\n")
```

**Using csv library**:  

**`populatedDataset = [[entry1_ele1, entry1_ele2],[entry2_ele1, entry2_ele2]...]`**  
**`with open(filePath, 'w') as file_objVar:`**  
$\;\;\;\;$**`csv_writerObj = csv.writer(file_objVar, delimiter= delimiter)`**  
$\;\;\;\;$**`for line in populatedDataset:`**  
$\;\;\;\;\;\;\;\;$**`csv_writerObj.writerow(line)`**  
* Writes to a csv file from a dataset (list of lists)  
* **`delimeter`** is defaulted to **`","`**   


```python
# example writting to a csv file using csv library and setting ; as the delimiter

with open('data/my_iris2.csv','w') as fs:
    csv_writer = csv.writer(fs, delimiter=";")
    for line in dataset:
        csv_writer.writerow(line)
```

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>Excel Files;<center>

[How to Work with Excel files in Pandas (see if getting errors)](https://towardsdatascience.com/how-to-work-with-excel-files-in-pandas-c584abb67bfb)

**Read Excel files**:  

**`import pandas as pd`**  
* Must first **import pandas**  


```python
import pandas as pd
```

**`dataframe_varObj = pd.read_excel(path_var_and_extension, sheet_name=’…’, header=0, skipfooter=0)`**  
* Function will read excel file to a **dataframe**  
* **Not the best way** to read excel files as excel files can be messy containing comments/explanations in the first and/or last couple of rows, better to use **ExcelFile** (see below)    
* For **`sheet_name`**:  
    * **not** provided, then the **first sheet** will be read in **as pandas dataframe** 
    * If **Sheet name** is provided, that **specific sheet** will be read in **as pandas dataframe**  
    * **None** specified, then **all sheets** will be read in **as dictionary of dataframes** where the **keys** will be **sheet names**  
    * Read in **Multiple specific sheets** by providing names of sheets wanted as a **list**  
* **`header`** defaults to 0, and is the index of the row to start reading, the **first row** is used for the **names** of the **dataframe columns**  
* **`skipfooter`** defaults to 0 and specifies the **number of rows** at the **bottom of** the **file** to **NOT read**  


```python
# Reading the 1st sheet in the excel file setting the reading to start from the 3rd row and using that as the names of the columns
df1 = pd.read_excel("data/iris.xlsx", header=2)
df1
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>4.9</th>
      <th>3</th>
      <th>1.4</th>
      <th>0.2</th>
      <th>setosa</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>4.7</td>
      <td>3.2</td>
      <td>1.3</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4.6</td>
      <td>3.1</td>
      <td>1.5</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>2</th>
      <td>5.0</td>
      <td>3.6</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>3</th>
      <td>5.4</td>
      <td>3.9</td>
      <td>1.7</td>
      <td>0.4</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>4</th>
      <td>4.6</td>
      <td>3.4</td>
      <td>1.4</td>
      <td>0.3</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>143</th>
      <td>6.7</td>
      <td>3.0</td>
      <td>5.2</td>
      <td>2.3</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>144</th>
      <td>6.3</td>
      <td>2.5</td>
      <td>5.0</td>
      <td>1.9</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>145</th>
      <td>6.5</td>
      <td>3.0</td>
      <td>5.2</td>
      <td>2.0</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>146</th>
      <td>6.2</td>
      <td>3.4</td>
      <td>5.4</td>
      <td>2.3</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>147</th>
      <td>5.9</td>
      <td>3.0</td>
      <td>5.1</td>
      <td>1.8</td>
      <td>virginica</td>
    </tr>
  </tbody>
</table>
<p>148 rows × 5 columns</p>
</div>




```python
# Reading the 2nd sheet in the excel file named "stats"
df2 = pd.read_excel("data/iris.xlsx", sheet_name="stats")
df2
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>sepal_length</th>
      <th>sepal_width</th>
      <th>petal_length</th>
      <th>petal_width</th>
      <th>species</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>5.006</td>
      <td>3.418</td>
      <td>1.464</td>
      <td>0.244</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>1</th>
      <td>5.936</td>
      <td>2.770</td>
      <td>4.260</td>
      <td>1.326</td>
      <td>versicolor</td>
    </tr>
    <tr>
      <th>2</th>
      <td>6.588</td>
      <td>2.974</td>
      <td>5.552</td>
      <td>2.026</td>
      <td>virginica</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Reading all sheets in to a dictionary

df3 = pd.read_excel("data/iris.xlsx", sheet_name=None)
df3
```




    {'iris':      sepal_length  sepal_width  petal_length  petal_width    species
     0             5.1          3.5           1.4          0.2     setosa
     1             4.9          3.0           1.4          0.2     setosa
     2             4.7          3.2           1.3          0.2     setosa
     3             4.6          3.1           1.5          0.2     setosa
     4             5.0          3.6           1.4          0.2     setosa
     ..            ...          ...           ...          ...        ...
     145           6.7          3.0           5.2          2.3  virginica
     146           6.3          2.5           5.0          1.9  virginica
     147           6.5          3.0           5.2          2.0  virginica
     148           6.2          3.4           5.4          2.3  virginica
     149           5.9          3.0           5.1          1.8  virginica
     
     [150 rows x 5 columns],
     'stats':    sepal_length  sepal_width  petal_length  petal_width     species
     0         5.006        3.418         1.464        0.244      setosa
     1         5.936        2.770         4.260        1.326  versicolor
     2         6.588        2.974         5.552        2.026   virginica}




```python
# Reading in specific sheets to a dictionary, and accessing specific sheet

iris_dataframes = pd.read_excel('data/iris.xlsx',sheet_name=['iris','stats'])
iris_dataframes['stats']
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>sepal_length</th>
      <th>sepal_width</th>
      <th>petal_length</th>
      <th>petal_width</th>
      <th>species</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>5.006</td>
      <td>3.418</td>
      <td>1.464</td>
      <td>0.244</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>1</th>
      <td>5.936</td>
      <td>2.770</td>
      <td>4.260</td>
      <td>1.326</td>
      <td>versicolor</td>
    </tr>
    <tr>
      <th>2</th>
      <td>6.588</td>
      <td>2.974</td>
      <td>5.552</td>
      <td>2.026</td>
      <td>virginica</td>
    </tr>
  </tbody>
</table>
</div>



**ExcelFile**:  

**`pdExcelFileObj = pd.ExcelFile(filePathAndExtension)`**  
* Reads an excel file into a **pandas ExcelFile object**  
* Has **built-in methods** to make it easy to retrieve and manipulate data  


```python
# Reading iris excel file to a pandas ExcelFile object

xlsx = pd.ExcelFile("data/iris.xlsx")
```

**sheets** method:  

**`xlsxFIleObj.sheet_names`**  
* Returns a list of all the **sheet names** in the file  


```python
xlsx.sheet_names
```




    ['iris', 'stats']



**parse** method:  

**`xlsxFileObj.parse(self, sheet_name=0, header=0, skipfooter=0)`**  
* If no arguments passed, the **first excel sheet** will be returned as a **pandas dataframe**  
* **Each sheet** can be accessed by passing the **index OR sheet name as a string**  
* The other arguments are similar to **`pd.read_excel()`** method above  


```python
# Returning the 2nd sheet (index 1) as a dataframe

xlsx.parse(1)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>sepal_length</th>
      <th>sepal_width</th>
      <th>petal_length</th>
      <th>petal_width</th>
      <th>species</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>5.006</td>
      <td>3.418</td>
      <td>1.464</td>
      <td>0.244</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>1</th>
      <td>5.936</td>
      <td>2.770</td>
      <td>4.260</td>
      <td>1.326</td>
      <td>versicolor</td>
    </tr>
    <tr>
      <th>2</th>
      <td>6.588</td>
      <td>2.974</td>
      <td>5.552</td>
      <td>2.026</td>
      <td>virginica</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Returning sheet as a dataframe by sheet name
# Note this particular sheet could have been accessed without passing any arguments as it is the first sheet

xlsx.parse("iris")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>sepal_length</th>
      <th>sepal_width</th>
      <th>petal_length</th>
      <th>petal_width</th>
      <th>species</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>5.1</td>
      <td>3.5</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4.9</td>
      <td>3.0</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4.7</td>
      <td>3.2</td>
      <td>1.3</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4.6</td>
      <td>3.1</td>
      <td>1.5</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5.0</td>
      <td>3.6</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>setosa</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>145</th>
      <td>6.7</td>
      <td>3.0</td>
      <td>5.2</td>
      <td>2.3</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>146</th>
      <td>6.3</td>
      <td>2.5</td>
      <td>5.0</td>
      <td>1.9</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>147</th>
      <td>6.5</td>
      <td>3.0</td>
      <td>5.2</td>
      <td>2.0</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>148</th>
      <td>6.2</td>
      <td>3.4</td>
      <td>5.4</td>
      <td>2.3</td>
      <td>virginica</td>
    </tr>
    <tr>
      <th>149</th>
      <td>5.9</td>
      <td>3.0</td>
      <td>5.1</td>
      <td>1.8</td>
      <td>virginica</td>
    </tr>
  </tbody>
</table>
<p>150 rows × 5 columns</p>
</div>




```python
# Creating a dataframe to write to excel file

data_to_write = [
    [1,2,3,4],
    [5,6,7,8],
    [9,10,11,12]
]
df = pd.DataFrame(data_to_write, columns=['A','B','C','D'])
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>A</th>
      <th>B</th>
      <th>C</th>
      <th>D</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>2</td>
      <td>3</td>
      <td>4</td>
    </tr>
    <tr>
      <th>1</th>
      <td>5</td>
      <td>6</td>
      <td>7</td>
      <td>8</td>
    </tr>
    <tr>
      <th>2</th>
      <td>9</td>
      <td>10</td>
      <td>11</td>
      <td>12</td>
    </tr>
  </tbody>
</table>
</div>



**Writing to excel**:  

**`dataFrameObj.to_excel(filePathWithExtension, sheet_name='Sheet1', index=True)`**  
* **`sheet_name`** is **optional, defaulting to `Sheet1`** or equivalent number  
* By default **`index=` True**, this will **write** the **index column to the excel file**, set to **False** to **turn off**  
* Note if trying to write a different sheet to the same file, it will **overwrite** the previous with just 1 sheet  
* To write **multiple sheets to file** use **`ExcelWriter`** method (see below)  


```python
# Writes dataframe to excel sheet with the sheet name "Number Matrix"

df.to_excel("data/writing to excel.xlsx", sheet_name="Number Matrix")
```


```python
# Check the excel file before and after running this line (and after running above)
# The previous sheet will have been overwritten
# This line also turns off the index parameter

df.to_excel("data/writing to excel.xlsx", sheet_name="New Number Matrix", index=False)
```

**ExcelWriter** method:  

**`with pd.ExcelWriter(filePathWithExtension, mode='w') as writerObj:`**  
$\;\;\;\;$**`dataFrameObj.to_excel(writerObj, sheet_name='Sheet1', index=True)`**  
$\;\;\;\;$**`dataFrameObj.to_excel(writerObj, sheet_name='Sheet1', index=True)`**  
* This will add multiple sheets to an excel file  
* If no **`sheet_name`** provided to **any**, **only 1 sheet** will get **written**, providing the **1st but not the 2nd**, and the **2nd sheet** will default to **`Sheet1`**  
* If wanting to **add sheets** to an **existing excel file**, set **`mode`** to **`'a'` (append)**  


```python
# Writing multiple sheets to an Excel file

with pd.ExcelWriter("data/writing to excel.xlsx") as writer:
    df.to_excel(writer, sheet_name="Numbers", index=False)
    df.to_excel(writer)    # This sheet will be named "Sheet1"
```

**Writing formula to an Excel file**:  

* Formula can be written directly into the dataset as a string, this will then be interpreted by Excel as formulas  


```python
# Creating a dataframe containing string formulas

df = pd.DataFrame(data=[[1, 2, '=SUM(A2:B2)'], [3,4, '=SUM(A3:B3)'], [5,6, '=SUM(A4:B4)']], columns=['A','B','SUM'])
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>A</th>
      <th>B</th>
      <th>SUM</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>2</td>
      <td>=SUM(A2:B2)</td>
    </tr>
    <tr>
      <th>1</th>
      <td>3</td>
      <td>4</td>
      <td>=SUM(A3:B3)</td>
    </tr>
    <tr>
      <th>2</th>
      <td>5</td>
      <td>6</td>
      <td>=SUM(A4:B4)</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Writing dataframe with formulas to excel file

df.to_excel("data/formula writing.xlsx", sheet_name="formula", index=False)
```

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

## <center>Simple APIs;</center>

**API's - Application Program Interface**:

* Allows two programs to talk to each other via inputs and outputs  
* An API is a simple interface that defines the types of requests (demands/questions, etc.) that can be made, how they are made, and how they are processed  
* Pandas is a type of API  
* Any time the API is called on some data, you are creating an **instance**

**rest API's**:  

* A popular type of API which allows you to communicate through the internet to take advantage of resources like storage, access more data, AI algorithms, and much more  
* **REST** stands for **RE**presentational **S**tate **T**ransfer  
* Your program is called the **Client** which the API communicates with to a **Web Server** referred to as a **Resource** which you call through the internet  
* **Client** finds service via an **endpoint**  
* HTTP methods are a way of transmitting data over the internet  
* **Requests** are sent from the **client** to the **resource** usually communicated via a **HTTP message usually containing a JSON file** containing instructions on what operation we would like the service to perform. Service performs the operation and the **Response** is sent from the **resource** to the **client** usually via a **JSON file**  
* Set of rules regarding:  
  1. Communication  
  2. Input or Request  
  3. Output or Response  


![](https://res.cloudinary.com/practicaldev/image/fetch/s--YTDTEgpk--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/ekawmj3rafdtn06hzj79.png "REST API process")

**wrappers**:  

*  An API wrapper is a language-specific package or kit that encapsulates multiple API calls to make complicated functions easy to use  
* They help developers call various APIs without the need for their real-time interaction. As such, wrappers can be used to automate API-reliant processes  
* Wrappers are used to add functions that the API might not have itself  

**example of using API to get live Bitcoin data and plot to a candlestick diagram**:


```python
# install pycoingecko wrapper for CoinGeckoAPI using pip
# and import CoinGeckoAPI
# pycoingecko will deal with endpoint targeting

!pip install pycoingecko

from pycoingecko import CoinGeckoAPI
```

    Requirement already satisfied: pycoingecko in c:\users\ajdpi\anaconda3\lib\site-packages (2.2.0)
    Requirement already satisfied: requests in c:\users\ajdpi\anaconda3\lib\site-packages (from pycoingecko) (2.26.0)
    Requirement already satisfied: certifi>=2017.4.17 in c:\users\ajdpi\anaconda3\lib\site-packages (from requests->pycoingecko) (2021.10.8)
    Requirement already satisfied: charset-normalizer~=2.0.0 in c:\users\ajdpi\anaconda3\lib\site-packages (from requests->pycoingecko) (2.0.4)
    Requirement already satisfied: idna<4,>=2.5 in c:\users\ajdpi\anaconda3\lib\site-packages (from requests->pycoingecko) (3.2)
    Requirement already satisfied: urllib3<1.27,>=1.21.1 in c:\users\ajdpi\anaconda3\lib\site-packages (from requests->pycoingecko) (1.26.7)
    


```python
# abbreviate CoinGeckoAPI() to "cg" for ease
# use help function to see functions of API

cg = CoinGeckoAPI()
help(cg)
```

    Help on CoinGeckoAPI in module pycoingecko.api object:
    
    class CoinGeckoAPI(builtins.object)
     |  CoinGeckoAPI(api_base_url='https://api.coingecko.com/api/v3/')
     |  
     |  Methods defined here:
     |  
     |  __init__(self, api_base_url='https://api.coingecko.com/api/v3/')
     |      Initialize self.  See help(type(self)) for accurate signature.
     |  
     |  get_asset_platforms = input_args(*args, **kwargs)
     |  
     |  get_coin_by_id = input_args(*args, **kwargs)
     |  
     |  get_coin_history_by_id = input_args(*args, **kwargs)
     |  
     |  get_coin_info_from_contract_address_by_id = input_args(*args, **kwargs)
     |  
     |  get_coin_market_chart_by_id = input_args(*args, **kwargs)
     |  
     |  get_coin_market_chart_from_contract_address_by_id = input_args(*args, **kwargs)
     |  
     |  get_coin_market_chart_range_by_id = input_args(*args, **kwargs)
     |  
     |  get_coin_market_chart_range_from_contract_address_by_id = input_args(*args, **kwargs)
     |  
     |  get_coin_ohlc_by_id = input_args(*args, **kwargs)
     |  
     |  get_coin_status_updates_by_id = input_args(*args, **kwargs)
     |  
     |  get_coin_ticker_by_id = input_args(*args, **kwargs)
     |  
     |  get_coins = input_args(*args, **kwargs)
     |  
     |  get_coins_categories = input_args(*args, **kwargs)
     |  
     |  get_coins_categories_list = input_args(*args, **kwargs)
     |  
     |  get_coins_list = input_args(*args, **kwargs)
     |  
     |  get_coins_markets = input_args(*args, **kwargs)
     |  
     |  get_companies_public_treasury_by_coin_id = input_args(*args, **kwargs)
     |  
     |  get_derivatives = input_args(*args, **kwargs)
     |  
     |  get_derivatives_exchanges = input_args(*args, **kwargs)
     |  
     |  get_derivatives_exchanges_by_id = input_args(*args, **kwargs)
     |  
     |  get_derivatives_exchanges_list = input_args(*args, **kwargs)
     |  
     |  get_events = input_args(*args, **kwargs)
     |  
     |  get_events_countries = input_args(*args, **kwargs)
     |  
     |  get_events_types = input_args(*args, **kwargs)
     |  
     |  get_exchange_rates = input_args(*args, **kwargs)
     |  
     |  get_exchanges_by_id = input_args(*args, **kwargs)
     |  
     |  get_exchanges_id_name_list = input_args(*args, **kwargs)
     |  
     |  get_exchanges_list = input_args(*args, **kwargs)
     |  
     |  get_exchanges_status_updates_by_id = input_args(*args, **kwargs)
     |  
     |  get_exchanges_tickers_by_id = input_args(*args, **kwargs)
     |  
     |  get_exchanges_volume_chart_by_id = input_args(*args, **kwargs)
     |  
     |  get_finance_platforms = input_args(*args, **kwargs)
     |  
     |  get_finance_products = input_args(*args, **kwargs)
     |  
     |  get_global = input_args(*args, **kwargs)
     |  
     |  get_global_decentralized_finance_defi = input_args(*args, **kwargs)
     |  
     |  get_indexes = input_args(*args, **kwargs)
     |  
     |  get_indexes_by_market_id_and_index_id = input_args(*args, **kwargs)
     |  
     |  get_indexes_list = input_args(*args, **kwargs)
     |  
     |  get_price = input_args(*args, **kwargs)
     |  
     |  get_search_trending = input_args(*args, **kwargs)
     |  
     |  get_status_updates = input_args(*args, **kwargs)
     |  
     |  get_supported_vs_currencies = input_args(*args, **kwargs)
     |  
     |  get_token_price = input_args(*args, **kwargs)
     |  
     |  ping(self)
     |      Check API server status
     |  
     |  ----------------------------------------------------------------------
     |  Data descriptors defined here:
     |  
     |  __dict__
     |      dictionary for instance variables (if defined)
     |  
     |  __weakref__
     |      list of weak references to the object (if defined)
    
    


```python
# getting list of all supported coins id's, name's and symbol's from CoinGeckoAPI

cg.get_coins_list()
```




    [{'id': '01coin', 'symbol': 'zoc', 'name': '01coin'},
     {'id': '0chain', 'symbol': 'zcn', 'name': 'Zus'},
     {'id': '0-knowledge-network', 'symbol': '0kn', 'name': '0 Knowledge Network'},
     {'id': '0-mee', 'symbol': 'ome', 'name': 'O-MEE'},
     {'id': '0vix-protocol', 'symbol': 'vix', 'name': '0VIX Protocol'},
     {'id': '0x', 'symbol': 'zrx', 'name': '0x Protocol'},
     {'id': '0x0-ai-ai-smart-contract',
      'symbol': '0x0',
      'name': '0x0.ai: AI Smart Contract'},
     {'id': '0x1-tools-ai-multi-tool',
      'symbol': '0x1',
      'name': '0x1.tools: AI Multi-tool'},
     {'id': '0xauto-io-contract-auto-deployer',
      'symbol': '0xa',
      'name': '0xAuto.io : Contract Auto Deployer'},
     {'id': '0xcoco', 'symbol': 'coco', 'name': '0xCoco'},
     {'id': '0xdao', 'symbol': 'oxd', 'name': '0xDAO'},
     {'id': '0xdefcafe', 'symbol': 'cafe', 'name': '0xDEFCAFE'},
     {'id': '0xfriend', 'symbol': '0xf', 'name': '0xFriend'},
     {'id': '0xgasless', 'symbol': '0xgas', 'name': '0xGasless'},
     {'id': '0x-leverage', 'symbol': 'oxl', 'name': '0x Leverage'},
     {'id': '0xmonero', 'symbol': '0xmr', 'name': '0xMonero'},
     {'id': '0xs', 'symbol': '$0xs', 'name': '0xS'},
     {'id': '0xshield', 'symbol': 'shield', 'name': '0xShield'},
     {'id': '0xsniper', 'symbol': '0xs', 'name': '0xSniper'},
     {'id': '12ships', 'symbol': 'tshp', 'name': '12Ships'},
     {'id': '1art', 'symbol': '1art', 'name': 'OneArt'},
     {'id': '1eco', 'symbol': '1eco', 'name': '1eco'},
     {'id': '1hive-water', 'symbol': 'water', 'name': '1Hive Water'},
     {'id': '1inch', 'symbol': '1inch', 'name': '1inch'},
     {'id': '1inch-yvault', 'symbol': 'yv1inch', 'name': '1INCH yVault'},
     {'id': '1million-nfts', 'symbol': '1mil', 'name': '1MillionNFTs'},
     {'id': '1minbet', 'symbol': '1mb', 'name': '1minBET'},
     {'id': '1move token', 'symbol': '1mt', 'name': '1Move Token'},
     {'id': '1peco', 'symbol': '1peco', 'name': '1peco'},
     {'id': '1reward-token', 'symbol': '1rt', 'name': '1Reward Token'},
     {'id': '1safu', 'symbol': 'safu', 'name': '1SAFU'},
     {'id': '1sol', 'symbol': '1sol', 'name': '1Sol'},
     {'id': '1sol-io-wormhole', 'symbol': '1sol', 'name': '1sol.io (Wormhole)'},
     {'id': '-2', 'symbol': '₿', 'name': '₿'},
     {'id': '2049', 'symbol': '2049', 'name': '2049'},
     {'id': '2080', 'symbol': '2080', 'name': '2080'},
     {'id': '20weth-80bal', 'symbol': '20weth-80bal', 'name': '20WETH-80BAL'},
     {'id': '28vck', 'symbol': 'vck', 'name': '28VCK'},
     {'id': '2acoin', 'symbol': 'arms', 'name': '2ACoin'},
     {'id': '2crazynft', 'symbol': '2crz', 'name': '2crazyNFT'},
     {'id': '2dai-io', 'symbol': '2dai', 'name': '2DAI.io'},
     {'id': '2g-carbon-coin', 'symbol': '2gcc', 'name': '2G Carbon Coin'},
     {'id': '2omb-finance', 'symbol': '2omb', 'name': '2omb'},
     {'id': '2share', 'symbol': '2shares', 'name': '2SHARE'},
     {'id': '300fit', 'symbol': 'fit', 'name': '300FIT'},
     {'id': '3d3d', 'symbol': '3d3d', 'name': '3d3d'},
     {'id': '3-kingdoms-multiverse',
      'symbol': '3km',
      'name': '3 Kingdoms Multiverse'},
     {'id': '3shares', 'symbol': '3share', 'name': '3Share'},
     {'id': '3xcalibur', 'symbol': 'xcal', 'name': '3xcalibur Ecosystem Token'},
     {'id': '42-coin', 'symbol': '42', 'name': '42-coin'},
     {'id': '4artechnologies', 'symbol': '4art', 'name': '4ART Coin'},
     {'id': '4chan', 'symbol': '4chan', 'name': '4Chan'},
     {'id': '4d-twin-maps', 'symbol': 'map', 'name': '4D Twin Maps (OLD)'},
     {'id': '4d-twin-maps-2', 'symbol': '4dmaps', 'name': '4D Twin Maps'},
     {'id': '4int', 'symbol': '4int', 'name': '4INT'},
     {'id': '4jnet', 'symbol': '4jnet', 'name': '4JNET'},
     {'id': '50cent', 'symbol': '50c', 'name': '50Cent'},
     {'id': '5g-cash', 'symbol': 'vgc', 'name': '5G-CASH'},
     {'id': '5km-run', 'symbol': 'run', 'name': '5KM RUN'},
     {'id': '7pixels', 'symbol': '7pxs', 'name': '7Pixels'},
     {'id': '888tron', 'symbol': '888', 'name': '888tron'},
     {'id': '88mph', 'symbol': 'mph', 'name': '88mph'},
     {'id': '8bitearn', 'symbol': '8bit', 'name': '8BITEARN'},
     {'id': '8pay', 'symbol': '8pay', 'name': '8Pay'},
     {'id': '99starz', 'symbol': 'stz', 'name': '99Starz'},
     {'id': '9-lives-network', 'symbol': 'ninefi', 'name': '9 Lives Network'},
     {'id': 'a4-finance', 'symbol': 'a4', 'name': 'A4 Finance'},
     {'id': 'aada-finance', 'symbol': 'aada', 'name': 'Aada Finance'},
     {'id': 'aag-ventures', 'symbol': 'aag', 'name': 'AAG'},
     {'id': 'aardvark', 'symbol': 'ardvrk', 'name': 'Aardvark'},
     {'id': 'aave', 'symbol': 'aave', 'name': 'Aave'},
     {'id': 'aave-aave', 'symbol': 'aaave', 'name': 'Aave AAVE'},
     {'id': 'aave-amm-bptbalweth',
      'symbol': 'aammbptbalweth',
      'name': 'Aave AMM BptBALWETH'},
     {'id': 'aave-amm-bptwbtcweth',
      'symbol': 'aammbptwbtcweth',
      'name': 'Aave AMM BptWBTCWETH'},
     {'id': 'aave-amm-dai', 'symbol': 'aammdai', 'name': 'Aave AMM DAI'},
     {'id': 'aave-amm-uniaaveweth',
      'symbol': 'aammuniaaveweth',
      'name': 'Aave AMM UniAAVEWETH'},
     {'id': 'aave-amm-unibatweth',
      'symbol': 'aammunibatweth',
      'name': 'Aave AMM UniBATWETH'},
     {'id': 'aave-amm-unicrvweth',
      'symbol': 'aammunicrvweth',
      'name': 'Aave AMM UniCRVWETH'},
     {'id': 'aave-amm-unidaiusdc',
      'symbol': 'aammunidaiusdc',
      'name': 'Aave AMM UniDAIUSDC'},
     {'id': 'aave-amm-unidaiweth',
      'symbol': 'aammunidaiweth',
      'name': 'Aave AMM UniDAIWETH'},
     {'id': 'aave-amm-unilinkweth',
      'symbol': 'aammunilinkweth',
      'name': 'Aave AMM UniLINKWETH'},
     {'id': 'aave-amm-unimkrweth',
      'symbol': 'aammunimkrweth',
      'name': 'Aave AMM UniMKRWETH'},
     {'id': 'aave-amm-unirenweth',
      'symbol': 'aammunirenweth',
      'name': 'Aave AMM UniRENWETH'},
     {'id': 'aave-amm-unisnxweth',
      'symbol': 'aammunisnxweth',
      'name': 'Aave AMM UniSNXWETH'},
     {'id': 'aave-amm-uniuniweth',
      'symbol': 'aammuniuniweth',
      'name': 'Aave AMM UniUNIWETH'},
     {'id': 'aave-amm-uniusdcweth',
      'symbol': 'aammuniusdcweth',
      'name': 'Aave AMM UniUSDCWETH'},
     {'id': 'aave-amm-uniwbtcusdc',
      'symbol': 'aammuniwbtcusdc',
      'name': 'Aave AMM UniWBTCUSDC'},
     {'id': 'aave-amm-uniwbtcweth',
      'symbol': 'aammuniwbtcweth',
      'name': 'Aave AMM UniWBTCWETH'},
     {'id': 'aave-amm-uniyfiweth',
      'symbol': 'aammuniyfiweth',
      'name': 'Aave AMM UniYFIWETH'},
     {'id': 'aave-amm-usdc', 'symbol': 'aammusdc', 'name': 'Aave AMM USDC'},
     {'id': 'aave-amm-usdt', 'symbol': 'aammusdt', 'name': 'Aave AMM USDT'},
     {'id': 'aave-amm-wbtc', 'symbol': 'aammwbtc', 'name': 'Aave AMM WBTC'},
     {'id': 'aave-amm-weth', 'symbol': 'aammweth', 'name': 'Aave AMM WETH'},
     {'id': 'aave-bal', 'symbol': 'abal', 'name': 'Aave BAL'},
     {'id': 'aave-balancer-pool-token',
      'symbol': 'abpt',
      'name': 'Aave Balancer Pool Token'},
     {'id': 'aave-bat', 'symbol': 'abat', 'name': 'Aave BAT'},
     {'id': 'aave-bat-v1', 'symbol': 'abat', 'name': 'Aave BAT v1'},
     {'id': 'aave-busd', 'symbol': 'abusd', 'name': 'Aave BUSD'},
     {'id': 'aave-busd-v1', 'symbol': 'abusd', 'name': 'Aave BUSD v1'},
     {'id': 'aave-crv', 'symbol': 'acrv', 'name': 'Aave CRV'},
     {'id': 'aave-dai', 'symbol': 'adai', 'name': 'Aave DAI'},
     {'id': 'aave-dai-v1', 'symbol': 'adai', 'name': 'Aave DAI v1'},
     {'id': 'aave-enj', 'symbol': 'aenj', 'name': 'Aave ENJ'},
     {'id': 'aave-enj-v1', 'symbol': 'aenj', 'name': 'Aave ENJ v1'},
     {'id': 'aave-eth-v1', 'symbol': 'aeth', 'name': 'Aave ETH v1'},
     {'id': 'aavegotchi', 'symbol': 'ghst', 'name': 'Aavegotchi'},
     {'id': 'aavegotchi-alpha', 'symbol': 'alpha', 'name': 'Aavegotchi ALPHA'},
     {'id': 'aavegotchi-fomo', 'symbol': 'fomo', 'name': 'Aavegotchi FOMO'},
     {'id': 'aavegotchi-fud', 'symbol': 'fud', 'name': 'Aavegotchi FUD'},
     {'id': 'aavegotchi-kek', 'symbol': 'kek', 'name': 'Aavegotchi KEK'},
     {'id': 'aave-gusd', 'symbol': 'agusd', 'name': 'Aave GUSD'},
     {'id': 'aave-interest-bearing-steth',
      'symbol': 'asteth',
      'name': 'Aave Interest Bearing STETH'},
     {'id': 'aave-knc', 'symbol': 'aknc', 'name': 'Aave KNC'},
     {'id': 'aave-knc-v1', 'symbol': 'aknc', 'name': 'Aave KNC v1'},
     {'id': 'aave-link', 'symbol': 'alink', 'name': 'Aave LINK'},
     {'id': 'aave-link-v1', 'symbol': 'alink', 'name': 'Aave LINK v1'},
     {'id': 'aave-mana', 'symbol': 'amana', 'name': 'Aave MANA'},
     {'id': 'aave-mana-v1', 'symbol': 'amana', 'name': 'Aave MANA v1'},
     {'id': 'aave-mkr', 'symbol': 'amkr', 'name': 'Aave MKR'},
     {'id': 'aave-mkr-v1', 'symbol': 'amkr', 'name': 'Aave MKR v1'},
     {'id': 'aave-polygon-aave', 'symbol': 'amaave', 'name': 'Aave Polygon AAVE'},
     {'id': 'aave-polygon-dai', 'symbol': 'amdai', 'name': 'Aave Polygon DAI'},
     {'id': 'aave-polygon-usdc', 'symbol': 'amusdc', 'name': 'Aave Polygon USDC'},
     {'id': 'aave-polygon-usdt', 'symbol': 'amusdt', 'name': 'Aave Polygon USDT'},
     {'id': 'aave-polygon-wbtc', 'symbol': 'amwbtc', 'name': 'Aave Polygon WBTC'},
     {'id': 'aave-polygon-weth', 'symbol': 'amweth', 'name': 'Aave Polygon WETH'},
     {'id': 'aave-polygon-wmatic',
      'symbol': 'amwmatic',
      'name': 'Aave Polygon WMATIC'},
     {'id': 'aave-rai', 'symbol': 'arai', 'name': 'Aave RAI'},
     {'id': 'aave-ren', 'symbol': 'aren', 'name': 'Aave REN'},
     {'id': 'aave-ren-v1', 'symbol': 'aren', 'name': 'Aave REN v1'},
     {'id': 'aave-snx', 'symbol': 'asnx', 'name': 'Aave SNX'},
     {'id': 'aave-snx-v1', 'symbol': 'asnx', 'name': 'Aave SNX v1'},
     {'id': 'aave-susd', 'symbol': 'asusd', 'name': 'Aave SUSD'},
     {'id': 'aave-susd-v1', 'symbol': 'asusd', 'name': 'Aave SUSD v1'},
     {'id': 'aave-tusd', 'symbol': 'atusd', 'name': 'Aave TUSD'},
     {'id': 'aave-tusd-v1', 'symbol': 'atusd', 'name': 'Aave TUSD v1'},
     {'id': 'aave-uni', 'symbol': 'auni', 'name': 'Aave UNI'},
     {'id': 'aave-usdc', 'symbol': 'ausdc', 'name': 'Aave USDC'},
     {'id': 'aave-usdc-v1', 'symbol': 'ausdc', 'name': 'Aave USDC v1'},
     {'id': 'aave-usdt', 'symbol': 'ausdt', 'name': 'Aave USDT'},
     {'id': 'aave-usdt-v1', 'symbol': 'ausdt', 'name': 'Aave USDT v1'},
     {'id': 'aave-wbtc', 'symbol': 'awbtc', 'name': 'Aave WBTC'},
     {'id': 'aave-wbtc-v1', 'symbol': 'awbtc', 'name': 'Aave WBTC v1'},
     {'id': 'aave-weth', 'symbol': 'aweth', 'name': 'Aave WETH'},
     {'id': 'aave-xsushi', 'symbol': 'axsushi', 'name': 'Aave XSUSHI'},
     {'id': 'aave-yfi', 'symbol': 'ayfi', 'name': 'Aave YFI'},
     {'id': 'aave-yvault', 'symbol': 'yvaave', 'name': 'Aave yVault'},
     {'id': 'aave-zrx', 'symbol': 'azrx', 'name': 'Aave ZRX'},
     {'id': 'aave-zrx-v1', 'symbol': 'azrx', 'name': 'Aave ZRX v1'},
     {'id': 'abachi-2', 'symbol': 'abi', 'name': 'Abachi'},
     {'id': 'abased', 'symbol': '$abased', 'name': 'aBASED'},
     {'id': 'abcmeta', 'symbol': 'meta', 'name': 'ABCMETA'},
     {'id': 'abc-pos-pool', 'symbol': 'abc', 'name': 'ABC PoS Pool'},
     {'id': 'abel-finance', 'symbol': 'abel', 'name': 'ABEL Finance'},
     {'id': 'abelian', 'symbol': 'abel', 'name': 'Abelian'},
     {'id': 'abey', 'symbol': 'abey', 'name': 'Abey'},
     {'id': 'able-finance', 'symbol': 'able', 'name': 'Able Finance'},
     {'id': 'aboat-token-2', 'symbol': 'aboat', 'name': 'Aboat Token'},
     {'id': 'absolute-sync-token', 'symbol': 'ast', 'name': 'Absolute Sync'},
     {'id': 'abyss-world', 'symbol': 'awt', 'name': 'Abyss World'},
     {'id': 'acala', 'symbol': 'aca', 'name': 'Acala'},
     {'id': 'acala-dollar-acala',
      'symbol': 'ausd',
      'name': 'Acala Dollar (Acala)'},
     {'id': 'access-protocol', 'symbol': 'acs', 'name': 'Access Protocol'},
     {'id': 'acent', 'symbol': 'ace', 'name': 'Acent'},
     {'id': 'acetoken', 'symbol': 'ace', 'name': 'ACEToken'},
     {'id': 'achain', 'symbol': 'act', 'name': 'Achain'},
     {'id': 'acid', 'symbol': 'acid', 'name': 'Acid'},
     {'id': 'acknoledger', 'symbol': 'ack', 'name': 'AcknoLedger'},
     {'id': 'ac-milan-fan-token', 'symbol': 'acm', 'name': 'AC Milan Fan Token'},
     {'id': 'acoconut', 'symbol': 'ac', 'name': 'ACoconut'},
     {'id': 'acorn-protocol', 'symbol': 'acn', 'name': 'Acorn Protocol'},
     {'id': 'acquire-fi', 'symbol': 'acq', 'name': 'Acquire.Fi'},
     {'id': 'acreage-coin', 'symbol': 'acr', 'name': 'Acreage Coin'},
     {'id': 'acria', 'symbol': 'acria', 'name': 'Acria.AI'},
     {'id': 'across-protocol', 'symbol': 'acx', 'name': 'Across Protocol'},
     {'id': 'acryptos', 'symbol': 'acs', 'name': 'ACryptoS'},
     {'id': 'acryptosi', 'symbol': 'acsi', 'name': 'ACryptoSI'},
     {'id': 'actinium', 'symbol': 'acm', 'name': 'Actinium'},
     {'id': 'action-coin', 'symbol': 'actn', 'name': 'Action Coin'},
     {'id': 'acute-angle-cloud', 'symbol': 'aac', 'name': 'Double-A Chain'},
     {'id': 'adacash', 'symbol': 'adacash', 'name': 'ADAcash'},
     {'id': 'adadao', 'symbol': 'adao', 'name': 'ADADao'},
     {'id': 'adamant', 'symbol': 'addy', 'name': 'Adamant'},
     {'id': 'adamant-messenger', 'symbol': 'adm', 'name': 'ADAMANT Messenger'},
     {'id': 'adam-cochran-friends-tech',
      'symbol': 'adam',
      'name': 'Adam Cochran (Friend.tech)'},
     {'id': 'adanaspor-fan-token',
      'symbol': 'adana',
      'name': 'Adanaspor Fan Token'},
     {'id': 'adapad', 'symbol': 'adapad', 'name': 'ADAPad'},
     {'id': 'adappter-token', 'symbol': 'adp', 'name': 'Adappter'},
     {'id': 'adaswap', 'symbol': 'asw', 'name': 'AdaSwap'},
     {'id': 'adax', 'symbol': 'adax', 'name': 'ADAX'},
     {'id': 'adazoo', 'symbol': 'zoo', 'name': 'ADAZOO'},
     {'id': 'add-finance', 'symbol': 'add', 'name': 'Add Finance'},
     {'id': 'addiction', 'symbol': 'add', 'name': 'Addiction'},
     {'id': 'adex', 'symbol': 'adx', 'name': 'AdEx'},
     {'id': 'ad-flex-token', 'symbol': 'adf', 'name': 'Ad Flex'},
     {'id': 'aditus', 'symbol': 'adi', 'name': 'Aditus'},
     {'id': 'adonis-2', 'symbol': 'adon', 'name': 'Adonis'},
     {'id': 'adreward', 'symbol': 'ad', 'name': 'ADreward'},
     {'id': 'adroverse', 'symbol': 'adr', 'name': 'Adroverse'},
     {'id': 'adshares', 'symbol': 'ads', 'name': 'Adshares'},
     {'id': 'adult-playground', 'symbol': 'adult', 'name': 'Adult Playground'},
     {'id': 'adv3nture-xyz-gemstone',
      'symbol': 'gem',
      'name': 'Adv3nture.xyz Gemstone'},
     {'id': 'adv3nture-xyz-gold', 'symbol': 'gold', 'name': 'Adv3nture.xyz Gold'},
     {'id': 'advanced-united-continent',
      'symbol': 'auc',
      'name': 'Advanced United Continent'},
     {'id': 'advantis', 'symbol': 'advt', 'name': 'Advantis'},
     {'id': 'adventure-gold', 'symbol': 'agld', 'name': 'Adventure Gold'},
     {'id': 'adventurer-gold', 'symbol': 'gold', 'name': 'Adventurer Gold'},
     {'id': 'advertise-coin', 'symbol': 'adco', 'name': 'Advertise Coin'},
     {'id': 'aeggs', 'symbol': 'aeggs', 'name': 'aEGGS'},
     {'id': 'aegis', 'symbol': 'ags', 'name': 'Aegis'},
     {'id': 'aegis-token-f7934368-2fb3-4091-9edc-39283e87f55d',
      'symbol': 'on',
      'name': 'Onsen Token'},
     {'id': 'aelf', 'symbol': 'elf', 'name': 'aelf'},
     {'id': 'aelin', 'symbol': 'aelin', 'name': 'Aelin'},
     {'id': 'aelysir', 'symbol': 'ael', 'name': 'Aelysir'},
     {'id': 'aeon', 'symbol': 'aeon', 'name': 'Aeon'},
     {'id': 'aerarium-fi', 'symbol': 'aera', 'name': 'Aerarium Fi'},
     {'id': 'aerdrop', 'symbol': 'aer', 'name': 'Aerdrop'},
     {'id': 'aergo', 'symbol': 'aergo', 'name': 'Aergo'},
     {'id': 'aerie', 'symbol': 'aer', 'name': 'Aerie'},
     {'id': 'aerodrome-finance', 'symbol': 'aero', 'name': 'Aerodrome Finance'},
     {'id': 'aeron', 'symbol': 'arnx', 'name': 'Aeron'},
     {'id': 'aerovek-aviation', 'symbol': 'aero', 'name': 'Aerovek Aviation'},
     {'id': 'aesirx', 'symbol': 'aesirx', 'name': 'AesirX'},
     {'id': 'aeternity', 'symbol': 'ae', 'name': 'Aeternity'},
     {'id': 'aether-games', 'symbol': 'aeg', 'name': 'Aether Games'},
     {'id': 'aeur', 'symbol': 'aeur', 'name': 'AEUR'},
     {'id': 'aevum-ore', 'symbol': 'aevum', 'name': 'Aevum'},
     {'id': 'aezora', 'symbol': 'azr', 'name': 'Azzure'},
     {'id': 'afen-blockchain', 'symbol': 'afen', 'name': 'AFEN Blockchain'},
     {'id': 'affinity', 'symbol': 'afnty', 'name': 'Affinity'},
     {'id': 'affyn', 'symbol': 'fyn', 'name': 'Affyn'},
     {'id': 'aficionadao', 'symbol': 'adao', 'name': 'AficionaDAO'},
     {'id': 'afin-coin', 'symbol': 'afin', 'name': 'Asian Fintech'},
     {'id': 'afkdao', 'symbol': 'afk', 'name': 'AFKDAO'},
     {'id': 'afreum', 'symbol': 'afr', 'name': 'Afreum'},
     {'id': 'afrix', 'symbol': 'afx', 'name': 'Afrix'},
     {'id': 'afrostar', 'symbol': 'afro', 'name': 'Afrostar'},
     {'id': 'a-fund-baby', 'symbol': 'fund', 'name': 'A Fund Baby'},
     {'id': 'afyonspor-fan-token',
      'symbol': 'afyon',
      'name': 'Afyonspor Fan Token'},
     {'id': 'aga-carbon-credit', 'symbol': 'agac', 'name': 'AGA Carbon Credit'},
     {'id': 'aga-carbon-rewards', 'symbol': 'acar', 'name': 'AGA Carbon Rewards'},
     {'id': 'aga-rewards', 'symbol': 'edc', 'name': 'Edcoin'},
     {'id': 'aga-token', 'symbol': 'aga', 'name': 'AGA'},
     {'id': 'agavecoin', 'symbol': 'agvc', 'name': 'AgaveCoin'},
     {'id': 'agave-token', 'symbol': 'agve', 'name': 'Agave'},
     {'id': 'agenor', 'symbol': 'age', 'name': 'Agenor'},
     {'id': 'ageofgods', 'symbol': 'aog', 'name': 'AgeOfGods'},
     {'id': 'age-of-tanks', 'symbol': 'a.o.t', 'name': 'Age Of Tanks'},
     {'id': 'age-of-zalmoxis-koson',
      'symbol': 'koson',
      'name': 'Age of Zalmoxis KOSON'},
     {'id': 'ageur', 'symbol': 'ageur', 'name': 'agEUR'},
     {'id': 'ageur-plenty-bridge',
      'symbol': 'egeur.e',
      'name': 'agEUR (Plenty Bridge)'},
     {'id': 'aggrx', 'symbol': 'aggrx', 'name': 'AggrX'},
     {'id': 'agile', 'symbol': 'agl', 'name': 'Agile'},
     {'id': 'agility', 'symbol': 'agi', 'name': 'Agility'},
     {'id': 'agoras-currency-of-tau',
      'symbol': 'agrs',
      'name': 'Agoras: Currency of Tau'},
     {'id': 'agoric', 'symbol': 'bld', 'name': 'Agoric'},
     {'id': 'agos', 'symbol': 'agos', 'name': 'AGOS'},
     {'id': 'agrello', 'symbol': 'dlt', 'name': 'Agrello'},
     {'id': 'agricoin', 'symbol': 'agn', 'name': 'Agricoin'},
     {'id': 'agrinode', 'symbol': 'agn', 'name': 'AgriNode'},
     {'id': 'agritech', 'symbol': 'agt', 'name': 'Agritech'},
     {'id': 'agro-global', 'symbol': 'agro', 'name': 'Agro Global Token'},
     {'id': 'agx-coin', 'symbol': 'agx', 'name': 'AGX Coin'},
     {'id': 'ahatoken', 'symbol': 'aht', 'name': 'AhaToken'},
     {'id': 'a-hunters-dream', 'symbol': 'caw', 'name': 'A Hunters Dream'},
     {'id': 'aibot', 'symbol': 'aibot', 'name': 'Aibot'},
     {'id': 'aibra', 'symbol': 'abr', 'name': 'AIBRA'},
     {'id': 'aichain', 'symbol': 'ait', 'name': 'AICHAIN'},
     {'id': 'ai-code', 'symbol': 'aicode', 'name': 'AI CODE'},
     {'id': 'aicoin-2', 'symbol': 'ai', 'name': 'AICoin'},
     {'id': 'aicrew', 'symbol': 'aicr', 'name': 'AICrew'},
     {'id': 'aidi-finance-2', 'symbol': 'aidi', 'name': 'Aidi Finance'},
     {'id': 'ai-dogemini', 'symbol': 'aidogemini', 'name': 'AI DogeMini'},
     {'id': 'aidos-kuneen', 'symbol': 'adk', 'name': 'Aidos Kuneen'},
     {'id': 'aiearn', 'symbol': 'aie', 'name': 'AIEarn'},
     {'id': 'aienglish', 'symbol': 'aien', 'name': 'AIENGLISH'},
     {'id': 'ai-floki', 'symbol': 'aifloki', 'name': 'AI Floki'},
     {'id': 'aigentx', 'symbol': 'aix', 'name': 'AIgentX'},
     {'id': 'aimage', 'symbol': 'mage', 'name': 'AIMAGE'},
     {'id': 'aimbot', 'symbol': 'aimbot', 'name': 'AimBot'},
     {'id': 'aimedis-new', 'symbol': 'aimx', 'name': 'Aimedis (NEW)'},
     {'id': 'ai-meta-club', 'symbol': 'amc', 'name': 'AI Meta Club'},
     {'id': 'ai-network', 'symbol': 'ain', 'name': 'AI Network'},
     {'id': 'ainu-token', 'symbol': 'ainu', 'name': 'Ainu'},
     {'id': 'aion', 'symbol': 'aion', 'name': 'Aion'},
     {'id': 'aion-2', 'symbol': 'aion', 'name': 'AION'},
     {'id': 'aione', 'symbol': 'aione', 'name': 'AiONE'},
     {'id': 'aioz-network', 'symbol': 'aioz', 'name': 'AIOZ Network'},
     {'id': 'aipad', 'symbol': 'aipad', 'name': 'AIPad'},
     {'id': 'aipeople', 'symbol': 'aipeople', 'name': 'AIPeople'},
     {'id': 'aiptp', 'symbol': 'atmt', 'name': 'AiPTP'},
     {'id': 'airbloc-protocol', 'symbol': 'abl', 'name': 'Airbloc'},
     {'id': 'airbot', 'symbol': 'airbot', 'name': 'AirBot'},
     {'id': 'airight', 'symbol': 'airi', 'name': 'aiRight'},
     {'id': 'airnft-token', 'symbol': 'airt', 'name': 'AirNFT'},
     {'id': 'airswap', 'symbol': 'ast', 'name': 'AirSwap'},
     {'id': 'airtnt', 'symbol': 'airtnt', 'name': 'AirTnT'},
     {'id': 'airtor-protocol', 'symbol': 'ator', 'name': 'AirTor Protocol'},
     {'id': 'aishiba', 'symbol': 'shibai', 'name': 'AiShiba'},
     {'id': 'ai-supreme', 'symbol': 'aisp', 'name': 'AI Supreme'},
     {'id': 'aiswap', 'symbol': 'aiswap', 'name': 'AISwap'},
     {'id': 'aitom', 'symbol': 'aitom', 'name': 'AITom'},
     {'id': 'ai-trader', 'symbol': 'ait', 'name': 'AI Trader'},
     {'id': 'aitravis', 'symbol': 'tai', 'name': 'AITravis'},
     {'id': 'aiwork', 'symbol': 'awo', 'name': 'AiWork'},
     {'id': 'ai-x', 'symbol': 'x', 'name': 'AI-X'},
     {'id': 'ajna-protocol', 'symbol': 'ajna', 'name': 'Ajna Protocol'},
     {'id': 'ajuna-network', 'symbol': 'baju', 'name': 'Ajuna Network'},
     {'id': 'akash-network', 'symbol': 'akt', 'name': 'Akash Network'},
     {'id': 'akino-inu', 'symbol': 'aki', 'name': 'Akino INU'},
     {'id': 'aki-protocol', 'symbol': 'aki', 'name': 'Aki Protocol'},
     {'id': 'akita-inu', 'symbol': 'akita', 'name': 'Akita Inu'},
     {'id': 'akita-inu-asa', 'symbol': 'akta', 'name': 'Akita Inu ASA'},
     {'id': 'akitavax', 'symbol': 'akitax', 'name': 'Akitavax'},
     {'id': 'akoin', 'symbol': 'akn', 'name': 'Akoin'},
     {'id': 'akropolis', 'symbol': 'akro', 'name': 'Akropolis'},
     {'id': 'akropolis-delphi', 'symbol': 'adel', 'name': 'Delphi'},
     {'id': 'aktio', 'symbol': 'aktio', 'name': 'Aktio'},
     {'id': 'aladdin-cvxcrv', 'symbol': 'acrv', 'name': 'Aladdin cvxCRV'},
     {'id': 'aladdin-dao', 'symbol': 'ald', 'name': 'Aladdin DAO'},
     {'id': 'aladdin-sdcrv', 'symbol': 'asdcrv', 'name': 'Aladdin sdCRV'},
     {'id': 'alanyaspor-fan-token',
      'symbol': 'ala',
      'name': 'Alanyaspor Fan Token'},
     {'id': 'alaska-gold-rush', 'symbol': 'carat', 'name': 'Alaska Gold Rush'},
     {'id': 'alaya', 'symbol': 'atp', 'name': 'Alaya'},
     {'id': 'albedo', 'symbol': 'albedo', 'name': 'ALBEDO'},
     {'id': 'alcatraz', 'symbol': 'alcz', 'name': 'Alcatraz'},
     {'id': 'alcazar-2', 'symbol': 'alcazar', 'name': 'Alcazar'},
     {'id': 'alchemist', 'symbol': 'mist', 'name': 'Alchemist'},
     {'id': 'alchemix', 'symbol': 'alcx', 'name': 'Alchemix'},
     {'id': 'alchemix-eth', 'symbol': 'aleth', 'name': 'Alchemix ETH'},
     {'id': 'alchemix-usd', 'symbol': 'alusd', 'name': 'Alchemix USD'},
     {'id': 'alchemyai', 'symbol': 'acoin', 'name': 'AlchemyAi'},
     {'id': 'alchemy-pay', 'symbol': 'ach', 'name': 'Alchemy Pay'},
     {'id': 'aldrin', 'symbol': 'rin', 'name': 'Aldrin'},
     {'id': 'aleph', 'symbol': 'aleph', 'name': 'Aleph.im'},
     {'id': 'alephium', 'symbol': 'alph', 'name': 'Alephium'},
     {'id': 'aleph-zero', 'symbol': 'azero', 'name': 'Aleph Zero'},
     {'id': 'alert', 'symbol': 'alert', 'name': 'ALERT'},
     {'id': 'alethea-artificial-liquid-intelligence-token',
      'symbol': 'ali',
      'name': 'Artificial Liquid Intelligence'},
     {'id': 'alex-b20', 'symbol': '$b20', 'name': 'ALEX $B20'},
     {'id': 'alexgo', 'symbol': 'alex', 'name': 'ALEX Lab'},
     {'id': 'alex-wrapped-usdt',
      'symbol': 'susdt',
      'name': 'Bridged Tether (Alex Bridge)'},
     {'id': 'alfa-romeo-racing-orlen-fan-token',
      'symbol': 'sauber',
      'name': 'Alfa Romeo Racing ORLEN Fan Token'},
     {'id': 'alfa-society', 'symbol': 'alfa', 'name': 'alfa.society'},
     {'id': 'alfprotocol', 'symbol': 'alf', 'name': 'AlfProtocol'},
     {'id': 'algebra', 'symbol': 'algb', 'name': 'Algebra'},
     {'id': 'algoblocks', 'symbol': 'algoblk', 'name': 'AlgoBlocks'},
     {'id': 'algofund', 'symbol': 'algf', 'name': 'AlgoFund'},
     {'id': 'algomint', 'symbol': 'gomint', 'name': 'Algomint'},
     {'id': 'algorand', 'symbol': 'algo', 'name': 'Algorand'},
     {'id': 'algory', 'symbol': 'alg', 'name': 'Algory'},
     {'id': 'algostable', 'symbol': 'stbl', 'name': 'AlgoStable'},
     {'id': 'algostake', 'symbol': 'stke', 'name': 'AlgoStake'},
     {'id': 'alibabacoin', 'symbol': 'abbc', 'name': 'ABBC'},
     {'id': 'alibaba-tokenized-stock-defichain',
      'symbol': 'dbaba',
      'name': 'Alibaba Tokenized Stock Defichain'},
     {'id': 'alicenet', 'symbol': 'alca', 'name': 'AliceNet'},
     {'id': 'alienbase', 'symbol': 'alb', 'name': 'AlienBase'},
     {'id': 'alien-chain', 'symbol': 'alien', 'name': 'Alien Chain'},
     {'id': 'alien-chicken-farm', 'symbol': 'acf', 'name': 'Alien Chicken Farm'},
     {'id': 'alienfi', 'symbol': 'alien', 'name': 'AlienFi'},
     {'id': 'alien-milady-fumo', 'symbol': 'fumo', 'name': 'Alien Milady Fumo'},
     {'id': 'alienswap', 'symbol': 'alien', 'name': 'AlienSwap'},
     {'id': 'alien-worlds', 'symbol': 'tlm', 'name': 'Alien Worlds'},
     {'id': 'alif-coin', 'symbol': 'alif', 'name': 'AliF Coin'},
     {'id': 'alink-ai', 'symbol': 'alink', 'name': 'ALINK AI'},
     {'id': 'alita', 'symbol': 'ali', 'name': 'Alita'},
     {'id': 'alitas', 'symbol': 'alt', 'name': 'Alitas'},
     {'id': 'alium-finance', 'symbol': 'alm', 'name': 'Alium Finance'},
     {'id': 'alkimi', 'symbol': '$ads', 'name': 'Alkimi'},
     {'id': 'all-art', 'symbol': 'aart', 'name': 'ALL.ART'},
     {'id': 'allbridge', 'symbol': 'abr', 'name': 'Allbridge'},
     {'id': 'all-coins-yield-capital',
      'symbol': 'acyc',
      'name': 'All Coins Yield Capital'},
     {'id': 'alldomains', 'symbol': 'all', 'name': 'AllDomains'},
     {'id': 'allianceblock', 'symbol': 'albt', 'name': 'AllianceBlock'},
     {'id': 'allianceblock-nexera',
      'symbol': 'nxra',
      'name': 'AllianceBlock Nexera'},
     {'id': 'alliance-fan-token', 'symbol': 'all', 'name': 'Alliance Fan Token'},
     {'id': 'alliance-x-trading', 'symbol': 'axt', 'name': 'Alliance X Trading'},
     {'id': 'all-in', 'symbol': 'allin', 'name': 'All In'},
     {'id': 'all-in-ai', 'symbol': 'aiai', 'name': 'ALLINAI'},
     {'id': 'all-in-coin', 'symbol': 'allin', 'name': 'All In Coin'},
     {'id': 'all-in-gpt', 'symbol': 'aigpt', 'name': 'All In GPT'},
     {'id': 'all-in-pepe', 'symbol': 'pepea', 'name': 'ALL IN PEPE'},
     {'id': 'allium-finance', 'symbol': 'alm', 'name': 'Allium Finance'},
     {'id': 'allpaycoin', 'symbol': 'apcg', 'name': 'ALLPAYCOIN'},
     {'id': 'allsafe', 'symbol': 'asafe', 'name': 'AllSafe'},
     {'id': 'alluo', 'symbol': 'alluo', 'name': 'Alluo'},
     {'id': 'ally', 'symbol': 'aly', 'name': 'Ally'},
     {'id': 'almira-wallet', 'symbol': 'almr', 'name': 'Almira Wallet'},
     {'id': 'alongside-crypto-market-index',
      'symbol': 'amkt',
      'name': 'Alongside Crypto Market Index'},
     {'id': 'alon-mars', 'symbol': 'alonmars', 'name': 'Alon Mars'},
     {'id': 'alpaca', 'symbol': 'alpa', 'name': 'Alpaca City'},
     {'id': 'alpaca-finance', 'symbol': 'alpaca', 'name': 'Alpaca Finance'},
     {'id': 'alpha5', 'symbol': 'a5t', 'name': 'Alpha5'},
     {'id': 'alphabet', 'symbol': 'alt', 'name': 'Alphabet'},
     {'id': 'alpha-bot-calls', 'symbol': 'abc', 'name': 'Alpha Bot Calls'},
     {'id': 'alpha-brain-capital-2', 'symbol': 'acap', 'name': 'Alpha Capital'},
     {'id': 'alphacoin', 'symbol': 'alpha', 'name': 'Alpha Coin'},
     {'id': 'alpha-finance', 'symbol': 'alpha', 'name': 'Stella'},
     {'id': 'alpha-gardeners', 'symbol': 'ag', 'name': 'Alpha Gardeners'},
     {'id': 'alphai', 'symbol': 'αai', 'name': 'alphAI'},
     {'id': 'alpha-intelligence', 'symbol': '$ai', 'name': 'Alpha Intelligence'},
     {'id': 'alpha-quark-token', 'symbol': 'aqt', 'name': 'Alpha Quark'},
     {'id': 'alpha-radar-bot', 'symbol': 'arbot', 'name': 'Alpha Radar Bot'},
     {'id': 'alpharushai', 'symbol': 'rushai', 'name': 'AlphaRushAI'},
     {'id': 'alphascan', 'symbol': 'ascn', 'name': 'AlphaScan'},
     {'id': 'alpha-shards', 'symbol': 'alpha', 'name': 'Alpha Shards'},
     {'id': 'alpha-shares-v2', 'symbol': '$alpha', 'name': 'Alpha Shares V2'},
     {'id': 'alphr', 'symbol': 'alphr', 'name': 'Alphr'},
     {'id': 'alpine-f1-team-fan-token',
      'symbol': 'alpine',
      'name': 'Alpine F1 Team Fan Token'},
     {'id': 'altair', 'symbol': 'air', 'name': 'Altair'},
     {'id': 'altava', 'symbol': 'tava', 'name': 'ALTAVA'},
     {'id': 'altbase', 'symbol': 'altb', 'name': 'Altbase'},
     {'id': 'altered-state-token',
      'symbol': 'asto',
      'name': 'Altered State Machine'},
     {'id': 'alterna-network', 'symbol': 'altn', 'name': 'Alterna Network'},
     {'id': 'alternity-cny', 'symbol': 'lcny', 'name': 'Alternity CNY'},
     {'id': 'altfins', 'symbol': 'afins', 'name': 'altFINS'},
     {'id': 'altitude', 'symbol': 'altd', 'name': 'Altitude'},
     {'id': 'alt-markets', 'symbol': 'amx', 'name': 'Alt Markets'},
     {'id': 'altura', 'symbol': 'alu', 'name': 'Altura'},
     {'id': 'aluna', 'symbol': 'aln', 'name': 'Aluna'},
     {'id': 'alva', 'symbol': 'aa', 'name': 'ALVA'},
     {'id': 'alvey-chain', 'symbol': 'walv', 'name': 'Alvey Chain'},
     {'id': 'amasa', 'symbol': 'amas', 'name': 'Amasa'},
     {'id': 'amateras', 'symbol': 'amt', 'name': 'Amateras'},
     {'id': 'amaterasufi-izanagi', 'symbol': 'iza', 'name': 'AmaterasuFi Izanagi'},
     {'id': 'amaterasu-omikami', 'symbol': 'omikami', 'name': 'AMATERASU OMIKAMI'},
     {'id': 'amaurot', 'symbol': 'ama', 'name': 'AMAUROT'},
     {'id': 'amax-network', 'symbol': 'amax', 'name': 'AMAX Network'},
     {'id': 'amazewallet', 'symbol': 'amt', 'name': 'AmazeToken'},
     {'id': 'amazingteamdao', 'symbol': 'amazingteam', 'name': 'AmazingTeamDAO'},
     {'id': 'amazon-tokenized-stock-defichain',
      'symbol': 'damzn',
      'name': 'Amazon Tokenized Stock Defichain'},
     {'id': 'amazy', 'symbol': 'azy', 'name': 'Amazy'},
     {'id': 'amber', 'symbol': 'amb', 'name': 'AirDAO'},
     {'id': 'amber-phantom-butterfly',
      'symbol': 'apb',
      'name': 'Amber Phantom Butterfly'},
     {'id': 'ambire-wallet', 'symbol': 'wallet', 'name': 'Ambire Wallet'},
     {'id': 'ambra', 'symbol': 'ambr', 'name': 'Ambra'},
     {'id': 'amepay', 'symbol': 'ame', 'name': 'AME Chain'},
     {'id': 'american-shiba', 'symbol': 'ushiba', 'name': 'American Shiba'},
     {'id': 'ammyi-coin', 'symbol': 'ami', 'name': 'AMMYI Coin'},
     {'id': 'amo', 'symbol': 'amo', 'name': 'AMO Coin'},
     {'id': 'amond', 'symbol': 'amon', 'name': 'AmonD'},
     {'id': 'ampleforth', 'symbol': 'ampl', 'name': 'Ampleforth'},
     {'id': 'ampleforth-governance-token',
      'symbol': 'forth',
      'name': 'Ampleforth Governance'},
     {'id': 'ampleswap', 'symbol': 'ample', 'name': 'AmpleSwap'},
     {'id': 'amplifi-dao', 'symbol': 'agg', 'name': 'AmpliFi DAO'},
     {'id': 'amp-token', 'symbol': 'amp', 'name': 'Amp'},
     {'id': 'amulet-staked-sol', 'symbol': 'amtsol', 'name': 'Amulet Staked SOL'},
     {'id': 'anarchy', 'symbol': 'anarchy', 'name': 'Anarchy'},
     {'id': 'anchor-protocol', 'symbol': 'anc', 'name': 'Anchor Protocol'},
     {'id': 'anchorswap', 'symbol': 'anchor', 'name': 'AnchorSwap'},
     {'id': 'ancient-raid', 'symbol': 'raid', 'name': 'Ancient Raid'},
     {'id': 'andronodes', 'symbol': 'andro', 'name': 'AndroNodes'},
     {'id': 'anduschain', 'symbol': 'deb', 'name': 'Anduschain'},
     {'id': 'angle-protocol', 'symbol': 'angle', 'name': 'ANGLE'},
     {'id': 'angola', 'symbol': 'agla', 'name': 'Angola'},
     {'id': 'angryb', 'symbol': 'anb', 'name': 'Angryb'},
     {'id': 'angry-birds', 'symbol': 'brd', 'name': 'Angry Birds'},
     {'id': 'angry-bulls-club', 'symbol': 'abc', 'name': 'Angry Bulls Club'},
     {'id': 'angry-doge', 'symbol': 'anfd', 'name': 'Angry Doge'},
     {'id': 'anima', 'symbol': 'anima', 'name': 'ANIMA'},
     {'id': 'animal-concerts-token', 'symbol': 'anml', 'name': 'Animal Concerts'},
     {'id': 'animalfam', 'symbol': 'totofo', 'name': 'AnimalFam'},
     {'id': 'animeswap', 'symbol': 'ani', 'name': 'AnimeSwap'},
     {'id': 'anime-token', 'symbol': 'ani', 'name': 'Anime'},
     {'id': 'aniverse', 'symbol': 'anv', 'name': 'Aniverse'},
     {'id': 'aniverse-metaverse', 'symbol': 'aniv', 'name': 'Aniverse Metaverse'},
     {'id': 'ankaa-exchange', 'symbol': 'ankaa', 'name': 'Ankaa Exchange'},
     {'id': 'ankaragucu-fan-token',
      'symbol': 'anka',
      'name': 'Ankaragücü Fan Token'},
     {'id': 'ankr', 'symbol': 'ankr', 'name': 'Ankr Network'},
     {'id': 'ankreth', 'symbol': 'ankreth', 'name': 'Ankr Staked ETH'},
     {'id': 'ankr-reward-bearing-ftm',
      'symbol': 'ankrftm',
      'name': 'Ankr Staked FTM'},
     {'id': 'ankr-reward-earning-matic',
      'symbol': 'ankrmatic',
      'name': 'Ankr Staked MATIC'},
     {'id': 'ankr-staked-avax', 'symbol': 'ankravax', 'name': 'Ankr Staked AVAX'},
     {'id': 'ankr-staked-bnb', 'symbol': 'ankrbnb', 'name': 'Ankr Staked BNB'},
     {'id': 'anomus-coin', 'symbol': 'anom', 'name': 'Anomus Coin'},
     {'id': 'anon', 'symbol': 'anon', 'name': 'ANON'},
     {'id': 'anon-inu', 'symbol': 'ainu', 'name': 'Anon Inu'},
     {'id': 'anon-web3', 'symbol': 'aw3', 'name': 'Anon Web3'},
     {'id': 'anonzk', 'symbol': 'azk', 'name': 'AnonZK'},
     {'id': 'another-world', 'symbol': 'awm', 'name': 'Another World'},
     {'id': 'anrkey-x', 'symbol': '$anrx', 'name': 'AnRKey X'},
     {'id': 'answer-governance', 'symbol': 'agov', 'name': 'Answer Governance'},
     {'id': 'ante-casino', 'symbol': 'chance', 'name': 'Ante Casino'},
     {'id': 'antfarm-governance-token',
      'symbol': 'agt',
      'name': 'Antfarm Governance Token'},
     {'id': 'antfarm-token', 'symbol': 'atf', 'name': 'Antfarm Token'},
     {'id': 'antimatter', 'symbol': 'matter', 'name': 'AntiMatter'},
     {'id': 'antis-inu', 'symbol': 'antis', 'name': 'Antis Inu'},
     {'id': 'antmons', 'symbol': 'ams', 'name': 'Antmons'},
     {'id': 'antnetworx', 'symbol': 'antx', 'name': 'AntNetworX (OLD)'},
     {'id': 'antnetworx-2', 'symbol': 'antx', 'name': 'AntNetworX'},
     {'id': 'antofy', 'symbol': 'abn', 'name': 'Antofy'},
     {'id': 'antspace', 'symbol': 'ant', 'name': 'Antspace'},
     {'id': 'anubit', 'symbol': 'anb', 'name': 'Anubit'},
     {'id': 'anypad', 'symbol': 'apad', 'name': 'Anypad'},
     {'id': 'anyswap', 'symbol': 'any', 'name': 'Anyswap'},
     {'id': 'aok', 'symbol': 'aok', 'name': 'AOK'},
     {'id': 'apass-coin', 'symbol': 'apc', 'name': 'APass Coin'},
     {'id': 'apch', 'symbol': 'apch', 'name': 'APCH'},
     {'id': 'apecoin', 'symbol': 'ape', 'name': 'ApeCoin'},
     {'id': 'aped', 'symbol': 'aped', 'name': 'Aped'},
     {'id': 'apedoge', 'symbol': 'aped', 'name': 'Apedoge'},
     {'id': 'ape-in', 'symbol': 'apein', 'name': 'Ape In'},
     {'id': 'ape_in_records', 'symbol': 'air', 'name': 'Ape In Records'},
     {'id': 'apemove', 'symbol': 'ape', 'name': 'APEmove'},
     {'id': 'apenft', 'symbol': 'nft', 'name': 'APENFT'},
     {'id': 'apes-go-bananas', 'symbol': 'agb', 'name': 'Apes Go Bananas'},
     {'id': 'apeswap-finance', 'symbol': 'banana', 'name': 'ApeSwap'},
     {'id': 'apexcoin-global', 'symbol': 'acx', 'name': 'Apex Coin'},
     {'id': 'apexit-finance', 'symbol': 'apex', 'name': 'ApeXit Finance'},
     {'id': 'apex-token-2', 'symbol': 'apex', 'name': 'ApeX'},
     {'id': 'apf-coin', 'symbol': 'apfc', 'name': 'APF coin'},
     {'id': 'api3', 'symbol': 'api3', 'name': 'API3'},
     {'id': 'apidae', 'symbol': 'apt', 'name': 'Apidae'},
     {'id': 'apiens', 'symbol': 'apn', 'name': 'Apiens'},
     {'id': 'apin-pulse', 'symbol': 'apc', 'name': 'Apin Pulse'},
     {'id': 'apm-coin', 'symbol': 'apm', 'name': 'apM Coin'},
     {'id': 'apollo', 'symbol': 'apl', 'name': 'Apollo'},
     {'id': 'apollo-crypto', 'symbol': 'apollo', 'name': 'Apollo Crypto'},
     {'id': 'apollon-limassol',
      'symbol': 'apl',
      'name': 'Apollon Limassol Fan Token'},
     {'id': 'apollo-token', 'symbol': 'apollo', 'name': 'Apollo Token'},
     {'id': 'apollox-2', 'symbol': 'apx', 'name': 'ApolloX'},
     {'id': 'appcoins', 'symbol': 'appc', 'name': 'AppCoins'},
     {'id': 'appics', 'symbol': 'apx', 'name': 'Appics'},
     {'id': 'appleswap-ai', 'symbol': 'ap', 'name': 'AppleSwap AI'},
     {'id': 'apple-tokenized-stock-defichain',
      'symbol': 'daapl',
      'name': 'Apple Tokenized Stock Defichain'},
     {'id': 'apricot', 'symbol': 'aprt', 'name': 'Apricot'},
     {'id': 'april', 'symbol': 'april', 'name': 'April'},
     {'id': 'apron', 'symbol': 'apn', 'name': 'Apron'},
     {'id': 'aptopad', 'symbol': 'apd', 'name': 'Aptopad'},
     {'id': 'aptos', 'symbol': 'apt', 'name': 'Aptos'},
     {'id': 'aptos-launch-token', 'symbol': 'alt', 'name': 'AptosLaunch Token'},
     {'id': 'apwine', 'symbol': 'apw', 'name': 'Spectra'},
     {'id': 'apy-finance', 'symbol': 'apy', 'name': 'APY.Finance'},
     {'id': 'apyswap', 'symbol': 'apys', 'name': 'APYSwap'},
     {'id': 'apy-vision', 'symbol': 'vision', 'name': 'APY.vision'},
     {'id': 'aqtis', 'symbol': 'aqtis', 'name': 'AQTIS'},
     {'id': 'aquachain', 'symbol': 'aqua', 'name': 'Aquachain'},
     {'id': 'aquadao', 'symbol': '$aqua', 'name': 'AquaDAO'},
     {'id': 'aqua-goat', 'symbol': 'aquagoat', 'name': 'Aqua Goat'},
     {'id': 'aquanee', 'symbol': 'aqdc', 'name': 'Aquanee'},
     {'id': 'aquari', 'symbol': 'aquari', 'name': 'Aquari'},
     {'id': 'aquarius', 'symbol': 'aqua', 'name': 'Aquarius'},
     {'id': 'aquariuscoin', 'symbol': 'arco', 'name': 'AquariusCoin'},
     {'id': 'aquarius-fi', 'symbol': 'aqu', 'name': 'Aquarius.Fi'},
     {'id': 'aquarius-loan', 'symbol': 'ars', 'name': 'Aquarius Loan'},
     {'id': 'arabic', 'symbol': 'abic', 'name': 'Arabic'},
     {'id': 'arable-protocol', 'symbol': 'acre', 'name': 'Arable Protocol'},
     {'id': 'aradenean-gold', 'symbol': 'ag', 'name': 'Aradenean Gold'},
     {'id': 'aragon', 'symbol': 'ant', 'name': 'Aragon'},
     {'id': 'ara-token', 'symbol': 'ara', 'name': 'Ara'},
     {'id': 'arbdoge-ai', 'symbol': 'aidoge', 'name': 'ArbDoge AI'},
     {'id': 'arb-furbo', 'symbol': 'farb', 'name': 'Arb Furbo'},
     {'id': 'arbidoge', 'symbol': 'adoge', 'name': 'ArbiDoge'},
     {'id': 'arbigoat', 'symbol': 'agt', 'name': 'ArbiGoat'},
     {'id': 'arbinu', 'symbol': 'arbinu', 'name': 'Arbinu'},
     {'id': 'arbinyan', 'symbol': 'nyan', 'name': 'ArbiNYAN'},
     {'id': 'arbipad', 'symbol': 'arbi', 'name': 'ArbiPad'},
     {'id': 'arbismart-token', 'symbol': 'rbis', 'name': 'ArbiSmart'},
     {'id': 'arbisphere-launchpad',
      'symbol': 'arsh',
      'name': 'Arbisphere Launchpad'},
     {'id': 'arbiswap-42983059-37e1-4a8f-b46e-0d908c0d4cc0',
      'symbol': 'arbi',
      'name': 'ArbiSwap'},
     {'id': 'arbiten', 'symbol': 'arbiten', 'name': 'ArbiTen'},
     {'id': 'arbiten-10share', 'symbol': '10share', 'name': 'ArbiTen 10SHARE'},
     {'id': 'arbitrove-alp', 'symbol': 'alp', 'name': 'Arbitrove ALP'},
     {'id': 'arbitrum', 'symbol': 'arb', 'name': 'Arbitrum'},
     {'id': 'arbitrum-charts', 'symbol': 'arcs', 'name': 'Arbitrum Charts'},
     {'id': 'arbitrum-ecosystem-index',
      'symbol': 'arbi',
      'name': 'Arbitrum Ecosystem Index'},
     {'id': 'arbitrum-exchange', 'symbol': 'arx', 'name': 'Arbidex'},
     {'id': 'arbitrumpad', 'symbol': 'arbpad', 'name': 'ArbitrumPad'},
     {'id': 'arbpanda-ai', 'symbol': 'aipanda', 'name': 'ArbPanda AI'},
     {'id': 'arb-protocol', 'symbol': 'arb', 'name': 'ARB Protocol'},
     {'id': 'arbshib', 'symbol': 'aishib', 'name': 'ArbShib'},
     {'id': 'arbswap', 'symbol': 'arbs', 'name': 'Arbswap'},
     {'id': 'arc', 'symbol': 'arc', 'name': 'Arc'},
     {'id': 'arcadeum', 'symbol': 'arc', 'name': 'Arcadeum'},
     {'id': 'arcadium', 'symbol': 'arcadium', 'name': 'Arcadium'},
     {'id': 'arcblock', 'symbol': 'abt', 'name': 'Arcblock'},
     {'id': 'arcc', 'symbol': 'arcc', 'name': 'ARCC'},
     {'id': 'arch-aggressive-portfolio',
      'symbol': 'aagg',
      'name': 'Arch Aggressive Portfolio'},
     {'id': 'archangel-token', 'symbol': 'archa', 'name': 'ArchAngel'},
     {'id': 'arch-balanced-portfolio',
      'symbol': 'abal',
      'name': 'Arch Balanced Portfolio'},
     {'id': 'arch-blockchains', 'symbol': 'chain', 'name': 'Arch Blockchains'},
     {'id': 'archerswap-bow', 'symbol': 'bow', 'name': 'Archerswap BOW'},
     {'id': 'archerswap-hunter', 'symbol': 'hunt', 'name': 'ArcherSwap Hunter'},
     {'id': 'arch-ethereum-div-yield',
      'symbol': 'aedy',
      'name': 'Arch Ethereum Div. Yield'},
     {'id': 'arch-ethereum-web3', 'symbol': 'web3', 'name': 'Arch Ethereum Web3'},
     {'id': 'archethic', 'symbol': 'uco', 'name': 'Archethic'},
     {'id': 'archimedes', 'symbol': 'arch', 'name': 'Archimedes Finance'},
     {'id': 'archi-token', 'symbol': 'archi', 'name': 'Archi Token'},
     {'id': 'archive-ai', 'symbol': 'arcai', 'name': 'Archive AI'},
     {'id': 'archloot', 'symbol': 'alt', 'name': 'ArchLoot'},
     {'id': 'arch-usd-div-yield', 'symbol': 'addy', 'name': 'Arch USD Div. Yield'},
     {'id': 'archway', 'symbol': 'arch', 'name': 'Archway'},
     {'id': 'arcona', 'symbol': 'arcona', 'name': 'Arcona'},
     {'id': 'arcs', 'symbol': 'arx', 'name': 'ARCS'},
     {'id': 'arcstar', 'symbol': 'arcstar', 'name': 'Arcstar'},
     {'id': 'ardana', 'symbol': 'dana', 'name': 'Ardana'},
     {'id': 'ardcoin', 'symbol': 'ardx', 'name': 'ArdCoin'},
     {'id': 'ardor', 'symbol': 'ardr', 'name': 'Ardor'},
     {'id': 'aree-shards', 'symbol': 'aes', 'name': 'Aree Shards'},
     {'id': 'arena-deathmatch', 'symbol': 'arena', 'name': 'Arena Deathmatch'},
     {'id': 'arena-token', 'symbol': 'arena', 'name': 'ArenaSwap'},
     {'id': 'areon-network', 'symbol': 'area', 'name': 'Areon Network'},
     {'id': 'ares3-network', 'symbol': 'ares', 'name': 'Ares3 Network'},
     {'id': 'ares-protocol', 'symbol': 'ares', 'name': 'Ares Protocol'},
     {'id': 'argentine-football-association-fan-token',
      'symbol': 'arg',
      'name': 'Argentine Football Association Fan Token'},
     {'id': 'argo', 'symbol': 'argo', 'name': 'ArGoApp'},
     {'id': 'argo-finance', 'symbol': 'argo', 'name': 'Argo Finance'},
     {'id': 'argon', 'symbol': 'argon', 'name': 'Argon'},
     {'id': 'argonon-helium', 'symbol': 'arg', 'name': 'Argonon Helium'},
     {'id': 'ari10', 'symbol': 'ari10', 'name': 'Ari10'},
     {'id': 'arianee', 'symbol': 'aria20', 'name': 'Arianee'},
     {'id': 'arion', 'symbol': 'arion', 'name': 'Arion'},
     {'id': 'arise-chikun', 'symbol': 'chikun', 'name': 'Arise Chikun'},
     {'id': 'ari-swap', 'symbol': 'ari', 'name': 'Ari Swap'},
     {'id': 'ariva', 'symbol': 'arv', 'name': 'Ariva'},
     {'id': 'arix', 'symbol': 'arix', 'name': 'Arix'},
     {'id': 'ark', 'symbol': 'ark', 'name': 'ARK'},
     {'id': 'arkadiko-protocol', 'symbol': 'diko', 'name': 'Arkadiko'},
     {'id': 'arkadiko-usda', 'symbol': 'usda', 'name': 'Arkadiko USDA'},
     {'id': 'arken-finance', 'symbol': '$arken', 'name': 'Arken Finance'},
     {'id': 'arker-2', 'symbol': 'arker', 'name': 'Arker'},
     {'id': 'arkham', 'symbol': 'arkm', 'name': 'Arkham'},
     {'id': 'ark-innovation-etf-defichain',
      'symbol': 'darkk',
      'name': 'ARK Innovation ETF Defichain'},
     {'id': 'ark-rivals', 'symbol': 'arkn', 'name': 'Ark Rivals'},
     {'id': 'arkstart', 'symbol': 'arks', 'name': 'ArkStart'},
     {'id': 'armor', 'symbol': 'armor', 'name': 'ARMOR'},
     {'id': 'armour-wallet', 'symbol': 'armour', 'name': 'Armour Wallet'},
     {'id': 'arnoya-classic', 'symbol': 'arnc', 'name': 'Arnoya classic'},
     {'id': 'arora', 'symbol': 'aror', 'name': 'Arora'},
     {'id': 'arowana-token', 'symbol': 'arw', 'name': 'Arowana'},
     {'id': 'arpa', 'symbol': 'arpa', 'name': 'ARPA'},
     {'id': 'arqma', 'symbol': 'arq', 'name': 'ArQmA'},
     {'id': 'array', 'symbol': 'array', 'name': 'Array'},
     {'id': 'arrland-arrc', 'symbol': 'arrc', 'name': 'Arrland ARRC'},
     {'id': 'arrland-rum', 'symbol': 'rum', 'name': 'Arrland RUM'},
     {'id': 'arsenal-fan-token', 'symbol': 'afc', 'name': 'Arsenal Fan Token'},
     {'id': 'artbyte', 'symbol': 'aby', 'name': 'ArtByte'},
     {'id': 'art-can-die', 'symbol': 'die', 'name': 'ART CAN DIE'},
     {'id': 'art-de-finance', 'symbol': 'adf', 'name': 'Art de Finance'},
     {'id': 'artem', 'symbol': 'artem', 'name': 'Artem'},
     {'id': 'artemis', 'symbol': 'mis', 'name': 'Artemis'},
     {'id': 'artemis-vision', 'symbol': 'arv', 'name': 'Artemis Vision'},
     {'id': 'arteq-nft-investment-fund',
      'symbol': 'arteq',
      'name': 'artèQ NFT Investment Fund'},
     {'id': 'artery', 'symbol': 'artr', 'name': 'Artery'},
     {'id': 'art-gobblers-goo', 'symbol': 'goo', 'name': 'Art Gobblers Goo'},
     {'id': 'artgpt', 'symbol': 'agpt', 'name': 'artGPT'},
     {'id': 'arth', 'symbol': 'arth', 'name': 'ARTH'},
     {'id': 'arthswap', 'symbol': 'arsw', 'name': 'ArthSwap'},
     {'id': 'artic-foundation', 'symbol': 'artic', 'name': 'ARTIC Foundation'},
     {'id': 'artichoke', 'symbol': 'choke', 'name': 'Artichoke'},
     {'id': 'artificial-intelligence',
      'symbol': 'ai',
      'name': 'Artificial Intelligence'},
     {'id': 'artify', 'symbol': 'afy', 'name': 'Artify'},
     {'id': 'arti-project', 'symbol': 'arti', 'name': 'Arti Project'},
     {'id': 'artizen', 'symbol': 'atnt', 'name': 'Artizen'},
     {'id': 'artl', 'symbol': 'artl', 'name': 'ARTL'},
     {'id': 'artmeta', 'symbol': '$mart', 'name': 'ArtMeta'},
     {'id': 'artrade', 'symbol': 'atr', 'name': 'Artrade'},
     {'id': 'artube', 'symbol': 'att', 'name': 'Artube'},
     {'id': 'artx', 'symbol': 'artx', 'name': 'ARTX'},
     {'id': 'arweave', 'symbol': 'ar', 'name': 'Arweave'},
     {'id': 'aryacoin', 'symbol': 'aya', 'name': 'Aryacoin'},
     {'id': 'asan-verse', 'symbol': 'asan', 'name': 'ASAN VERSE'},
     {'id': 'asap-sniper-bot', 'symbol': 'asap', 'name': 'Asap Sniper Bot'},
     {'id': 'ascend-2', 'symbol': 'asc', 'name': 'Ascend'},
     {'id': 'ascension-protocol',
      'symbol': 'ascend',
      'name': 'Ascension Protocol'},
     {'id': 'asd', 'symbol': 'asd', 'name': 'AscendEx'},
     {'id': 'asenix', 'symbol': 'enix', 'name': 'ASENIX'},
     {'id': 'asgardx', 'symbol': 'odin', 'name': 'AsgardX'},
     {'id': 'ash', 'symbol': 'ash', 'name': 'ASH'},
     {'id': 'ashswap', 'symbol': 'ash', 'name': 'AshSwap'},
     {'id': 'ash-token', 'symbol': 'ash', 'name': 'Ash Token'},
     {'id': 'asia-coin', 'symbol': 'asia', 'name': 'Asia Coin'},
     {'id': 'asic-token', 'symbol': 'asic', 'name': 'ASIC Token'},
     {'id': 'asic-token-pulsechain',
      'symbol': 'asic',
      'name': 'ASIC Token (Pulsechain)'},
     {'id': 'asix', 'symbol': 'asix', 'name': 'ASIX'},
     {'id': 'askobar-network', 'symbol': 'asko', 'name': 'Asko'},
     {'id': 'as-monaco-fan-token', 'symbol': 'asm', 'name': 'AS Monaco Fan Token'},
     {'id': 'aspo-world', 'symbol': 'aspo', 'name': 'ASPO World'},
     {'id': 'as-roma-fan-token', 'symbol': 'asr', 'name': 'AS Roma Fan Token'},
     {'id': 'assangedao', 'symbol': 'justice', 'name': 'AssangeDAO'},
     {'id': 'assaplay', 'symbol': 'assa', 'name': 'AssaPlay'},
     {'id': 'assemble-protocol', 'symbol': 'asm', 'name': 'Assemble Protocol'},
     {'id': 'assent-protocol', 'symbol': 'asnt', 'name': 'Assent Protocol'},
     {'id': 'assetmantle', 'symbol': 'mntl', 'name': 'AssetMantle'},
     {'id': 'asta', 'symbol': 'asta', 'name': 'ASTA'},
     {'id': 'astar', 'symbol': 'astr', 'name': 'Astar'},
     {'id': 'astar-moonbeam', 'symbol': '$xcastr', 'name': 'Astar (Moonbeam)'},
     {'id': 'astarter', 'symbol': 'aa', 'name': 'Astarter'},
     {'id': 'aster', 'symbol': 'atc', 'name': 'Aster'},
     {'id': 'ast-finance', 'symbol': 'ast', 'name': 'AST.finance'},
     {'id': 'aston-martin-cognizant-fan-token',
      'symbol': 'am',
      'name': 'Aston Martin Cognizant Fan Token'},
     {'id': 'aston-villa-fan-token',
      'symbol': 'avl',
      'name': 'Aston Villa Fan Token'},
     {'id': 'astra-dao', 'symbol': 'astradao', 'name': 'Astra DAO'},
     {'id': 'astrafer', 'symbol': 'astrafer', 'name': 'Astrafer'},
     {'id': 'astra-guild-ventures',
      'symbol': 'agv',
      'name': 'Astra Guild Ventures'},
     {'id': 'astral-ai', 'symbol': 'astral', 'name': 'Astral AI'},
     {'id': 'astral-credits', 'symbol': 'xac', 'name': 'Astral Credits'},
     {'id': 'astrals-glxy', 'symbol': 'glxy', 'name': 'Astrals GLXY'},
     {'id': 'astra-nova', 'symbol': '$rvv', 'name': 'Astra Nova'},
     {'id': 'astra-protocol-2', 'symbol': 'astra', 'name': 'Astra Protocol'},
     {'id': 'astrava', 'symbol': 'ast', 'name': 'Astrava'},
     {'id': 'astrazion', 'symbol': 'aznt', 'name': 'AstraZion'},
     {'id': 'astriddao-token', 'symbol': 'atid', 'name': 'AstridDAO'},
     {'id': 'astroai', 'symbol': 'astroai', 'name': 'AstroAI'},
     {'id': 'astro-babies', 'symbol': 'abb', 'name': 'Astro Babies'},
     {'id': 'astro-cash', 'symbol': 'astro', 'name': 'Astro Cash'},
     {'id': 'astroelon', 'symbol': 'elonone', 'name': 'AstroElon'},
     {'id': 'astro-pepe', 'symbol': 'astropepe', 'name': 'Astro Pepe'},
     {'id': 'astropepex', 'symbol': 'apx', 'name': 'AstroPepeX'},
     {'id': 'astroport', 'symbol': 'astroc', 'name': 'Astroport Classic'},
     {'id': 'astroport-fi', 'symbol': 'astro', 'name': 'Astroport'},
     {'id': 'astropup-coin', 'symbol': 'aspc', 'name': 'Astropup Coin'},
     {'id': 'astrospaces-io', 'symbol': 'spaces', 'name': 'AstroSpaces.io'},
     {'id': 'astroswap', 'symbol': 'astro', 'name': 'AstroSwap'},
     {'id': 'astrotools', 'symbol': 'astro', 'name': 'AstroTools'},
     {'id': 'asva', 'symbol': 'asva', 'name': 'Asva Labs'},
     {'id': 'asyagro', 'symbol': 'asy', 'name': 'ASYAGRO'},
     {'id': 'asymetrix', 'symbol': 'asx', 'name': 'Asymetrix'},
     {'id': 'atalexv2', 'symbol': 'atalexv2', 'name': 'atALEXv2'},
     {'id': 'atari', 'symbol': 'atri', 'name': 'Atari'},
     {'id': 'athena-finance', 'symbol': 'ath', 'name': 'Athena Finance'},
     {'id': 'athena-returns-olea', 'symbol': 'olea', 'name': 'Olea Token'},
     {'id': 'athenas', 'symbol': 'athenasv2', 'name': 'Athenas'},
     {'id': 'atheneum', 'symbol': 'aem', 'name': 'Atheneum'},
     {'id': 'athens', 'symbol': 'ath', 'name': 'Athens'},
     {'id': 'athos-finance', 'symbol': 'ath', 'name': 'Athos Finance'},
     {'id': 'athos-finance-usd', 'symbol': 'athusd', 'name': 'Athos Finance USD'},
     {'id': 'atlantis', 'symbol': 'atlas', 'name': 'Atlantis'},
     {'id': 'atlantis-loans', 'symbol': 'atl', 'name': 'Atlantis Loans'},
     {'id': 'atlas-aggregator', 'symbol': 'ata', 'name': 'Atlas Aggregator'},
     {'id': 'atlas-dex', 'symbol': 'ats', 'name': 'Atlas DEX'},
     {'id': 'atlas-fc-fan-token', 'symbol': 'atlas', 'name': 'Atlas FC Fan Token'},
     {'id': 'atlas-navi', 'symbol': 'navi', 'name': 'Atlas Navi'},
     {'id': 'atlas-protocol', 'symbol': 'atp', 'name': 'Atlas Protocol'},
     {'id': 'atlas-usv', 'symbol': 'usv', 'name': 'Atlas USV'},
     {'id': 'atletico-madrid',
      'symbol': 'atm',
      'name': 'Atletico Madrid Fan Token'},
     {'id': 'atomic-wallet-coin', 'symbol': 'awc', 'name': 'Atomic Wallet Coin'},
     {'id': 'atpay', 'symbol': 'atpay', 'name': 'AtPay'},
     {'id': 'atrofarm', 'symbol': 'atrofa', 'name': 'Atrofarm'},
     {'id': 'atromg8', 'symbol': 'ag8', 'name': 'ATROMG8'},
     {'id': 'attack-wagon', 'symbol': 'atk', 'name': 'Attack Wagon'},
     {'id': 'attila', 'symbol': 'att', 'name': 'Attila'},
     {'id': 'auction', 'symbol': 'auction', 'name': 'Bounce'},
     {'id': 'auctus', 'symbol': 'auc', 'name': 'Auctus'},
     {'id': 'audius', 'symbol': 'audio', 'name': 'Audius'},
     {'id': 'audius-wormhole', 'symbol': 'audio', 'name': 'Audius (Wormhole)'},
     {'id': 'augur', 'symbol': 'rep', 'name': 'Augur'},
     {'id': 'augury-finance', 'symbol': 'omen', 'name': 'Augury Finance'},
     {'id': 'aura-bal', 'symbol': 'aurabal', 'name': 'Aura BAL'},
     {'id': 'auradx', 'symbol': 'dalle2', 'name': 'AuradX'},
     {'id': 'aura-finance', 'symbol': 'aura', 'name': 'Aura Finance'},
     {'id': 'auragi', 'symbol': 'agi', 'name': 'Auragi'},
     {'id': 'aura-network', 'symbol': 'aura', 'name': 'Aura Network'},
     {'id': 'aura-network-old', 'symbol': 'aura', 'name': 'Aura Network [OLD]'},
     {'id': 'aureo', 'symbol': 'aur', 'name': 'AUREO'},
     {'id': 'aureus-nummus-gold', 'symbol': 'ang', 'name': 'Aureus Nummus Gold'},
     {'id': 'aurigami', 'symbol': 'ply', 'name': 'Aurigami'},
     {'id': 'aurix', 'symbol': 'aur', 'name': 'Aurix'},
     {'id': 'aurora', 'symbol': 'aoa', 'name': 'Aurora Chain'},
     {'id': 'auroracoin', 'symbol': 'aur', 'name': 'Auroracoin'},
     {'id': 'aurora-dao', 'symbol': 'idex', 'name': 'IDEX'},
     {'id': 'aurora-klay', 'symbol': 'ara', 'name': 'Aurora Klay'},
     {'id': 'aurora-near', 'symbol': 'aurora', 'name': 'Aurora'},
     {'id': 'auroratoken', 'symbol': 'aurora', 'name': 'AuroraToken'},
     {'id': 'aurora-token', 'symbol': '$adtx', 'name': 'Aurora Dimension'},
     {'id': 'aurory', 'symbol': 'aury', 'name': 'Aurory'},
     {'id': 'aurusx', 'symbol': 'ax', 'name': 'AurusX'},
     {'id': 'ausdc', 'symbol': 'ausdc', 'name': 'SpaceShipX aUSDC'},
     {'id': 'ausd-seed-acala', 'symbol': 'aseed', 'name': 'aUSD SEED (Acala)'},
     {'id': 'ausd-seed-karura', 'symbol': 'aseed', 'name': 'aUSD SEED (Karura)'},
     {'id': 'australian-safe-shepherd',
      'symbol': 'ass',
      'name': 'Australian Safe Shepherd'},
     {'id': 'authencity', 'symbol': 'auth', 'name': 'Authencity'},
     {'id': 'auto', 'symbol': 'auto', 'name': 'Auto'},
     {'id': 'autobahn-network', 'symbol': 'txl', 'name': 'Autobahn Network'},
     {'id': 'auto-core', 'symbol': 'acore', 'name': 'Auto Core'},
     {'id': 'autocrypto', 'symbol': 'au', 'name': 'AutoCrypto'},
     {'id': 'autodca', 'symbol': 'dca', 'name': 'AutoDCA'},
     {'id': 'autoearn-token', 'symbol': 'ate', 'name': 'AutoEarn Token'},
     {'id': 'automata', 'symbol': 'ata', 'name': 'Automata'},
     {'id': 'autominingtoken', 'symbol': 'amt', 'name': 'AutoMiningToken'},
     {'id': 'auton', 'symbol': 'atn', 'name': 'Auton'},
     {'id': 'autonio', 'symbol': 'niox', 'name': 'Autonio'},
     {'id': 'autonolas', 'symbol': 'olas', 'name': 'Autonolas'},
     {'id': 'autoshark', 'symbol': 'jaws', 'name': 'AutoShark'},
     {'id': 'autosingle', 'symbol': 'autos', 'name': 'AutoSingle'},
     {'id': 'autumn', 'symbol': 'autumn', 'name': 'Autumn'},
     {'id': 'aux-coin', 'symbol': 'aux', 'name': 'AUX Coin'},
     {'id': 'auxilium', 'symbol': 'aux', 'name': 'Auxilium'},
     {'id': 'auxo', 'symbol': 'auxo', 'name': 'Auxo'},
     {'id': 'avadex-token', 'symbol': 'avex', 'name': 'AvaDex Token'},
     {'id': 'avalanche-2', 'symbol': 'avax', 'name': 'Avalanche'},
     {'id': 'avalanche-wormhole',
      'symbol': 'avax',
      'name': 'Avalanche (Wormhole)'},
     {'id': 'avalaunch', 'symbol': 'xava', 'name': 'Avalaunch'},
     {'id': 'avaocado-dao', 'symbol': 'avg', 'name': 'Avocado DAO'},
     {'id': 'avata-network', 'symbol': 'avat', 'name': 'AVATA Network'},
     {'id': 'avatara-nox', 'symbol': 'nox', 'name': 'AVATARA NOX'},
     {'id': 'avatar-musk-verse', 'symbol': 'amv', 'name': 'Avatar Musk Verse'},
     {'id': 'avatly', 'symbol': 'ava', 'name': 'Avatly'},
     {'id': 'avaxtars', 'symbol': 'avxt', 'name': 'Avaxtars'},
     {'id': 'aventus', 'symbol': 'avt', 'name': 'Aventus'},
     {'id': 'avenue-hamilton-token',
      'symbol': 'aht',
      'name': 'Avenue Hamilton Token'},
     {'id': 'avian-network', 'symbol': 'avn', 'name': 'AVIAN'},
     {'id': 'aviator', 'symbol': 'avi', 'name': 'Aviator'},
     {'id': 'avinoc', 'symbol': 'avinoc', 'name': 'AVINOC'},
     {'id': 'avme', 'symbol': 'avme', 'name': 'AVME'},
     {'id': 'avnrich', 'symbol': 'avn', 'name': 'AVNRich'},
     {'id': 'avoteo', 'symbol': 'avo', 'name': 'Avoteo'},
     {'id': 'awoke', 'symbol': 'awoke', 'name': 'Awoke'},
     {'id': 'axe', 'symbol': 'axe', 'name': 'Axe'},
     {'id': 'axe-2', 'symbol': 'axe', 'name': 'AXE'},
     {'id': 'axe-cap', 'symbol': 'axe', 'name': 'Axe Cap'},
     {'id': 'axel', 'symbol': 'axel', 'name': 'AXEL'},
     {'id': 'axelar', 'symbol': 'axl', 'name': 'Axelar'},
     {'id': 'axelar-usdt', 'symbol': 'axlusdt', 'name': 'Bridged Tether (Axelar)'},
     {'id': 'axia', 'symbol': 'axiav3', 'name': 'Axia'},
     {'id': 'axial-token', 'symbol': 'axial', 'name': 'Axial Token'},
     {'id': 'axie-infinity', 'symbol': 'axs', 'name': 'Axie Infinity'},
     {'id': 'axie-infinity-shard-wormhole',
      'symbol': 'axset',
      'name': 'Axie Infinity Shard (Wormhole)'},
     {'id': 'axion', 'symbol': 'axn', 'name': 'Axion'},
     {'id': 'axis-defi', 'symbol': 'axis', 'name': 'Axis DeFi'},
     {'id': 'axis-token', 'symbol': 'axis', 'name': 'AXIS'},
     {'id': 'axle-games', 'symbol': 'axle', 'name': 'Axle Games'},
     {'id': 'axl-inu', 'symbol': 'axl', 'name': 'AXL INU'},
     {'id': 'axlusdc', 'symbol': 'axlusdc', 'name': 'Bridged USD Coin (Axelar)'},
     {'id': 'axlwbtc', 'symbol': 'axlwbtc', 'name': 'axlWBTC'},
     {'id': 'axlweth', 'symbol': 'axleth', 'name': 'Axelar Wrapped Ether'},
     {'id': 'axpire', 'symbol': 'axpr', 'name': 'Moola'},
     {'id': 'ayin', 'symbol': 'ayin', 'name': 'Ayin'},
     {'id': 'azit', 'symbol': 'azit', 'name': 'azit'},
     {'id': 'azuki', 'symbol': 'azuki', 'name': 'Azuki'},
     {'id': 'azuma-coin', 'symbol': 'azum', 'name': 'Azuma Coin'},
     {'id': 'b20', 'symbol': 'b20', 'name': 'B20'},
     {'id': 'baanx', 'symbol': 'bxx', 'name': 'Baanx'},
     {'id': 'baasid', 'symbol': 'baas', 'name': 'BaaSid'},
     {'id': 'babacoin', 'symbol': 'bbc', 'name': 'Babacoin'},
     {'id': 'babb', 'symbol': 'bax', 'name': 'BABB'},
     {'id': 'baby-alvey', 'symbol': 'balvey', 'name': 'Baby Alvey'},
     {'id': 'babyama', 'symbol': 'bama', 'name': 'BabyAMA'},
     {'id': 'baby-aptos', 'symbol': 'baptos', 'name': 'Baby Aptos'},
     {'id': 'baby-arbitrum', 'symbol': 'barb', 'name': 'Baby Arbitrum'},
     {'id': 'baby-bali', 'symbol': 'bb', 'name': 'Baby Bali'},
     {'id': 'babybnbtiger', 'symbol': 'babybnbtig', 'name': 'BabyBNBTiger'},
     {'id': 'babyboo', 'symbol': 'babyboo', 'name': 'BabyBoo'},
     {'id': 'babydoge2-0', 'symbol': 'babydoge2.0', 'name': 'Babydoge2.0'},
     {'id': 'babydogearmy', 'symbol': 'army', 'name': 'BabyDogeARMY'},
     {'id': 'baby-doge-cash', 'symbol': 'babydogecash', 'name': 'Baby Doge Cash'},
     {'id': 'baby-doge-ceo', 'symbol': 'babyceo', 'name': 'Baby Doge CEO'},
     {'id': 'babydoge-ceo', 'symbol': 'bceo', 'name': 'BabyDoge CEO'},
     {'id': 'baby-doge-coin', 'symbol': 'babydoge', 'name': 'Baby Doge Coin'},
     {'id': 'babydoge-coin-eth', 'symbol': 'babydoge', 'name': 'BabyDoge ETH'},
     {'id': 'baby-doge-inu', 'symbol': '$babydogeinu', 'name': 'Baby Doge Inu'},
     {'id': 'babydot', 'symbol': 'bdot', 'name': 'BabyDot'},
     {'id': 'babyfloki', 'symbol': 'babyfloki', 'name': 'BabyFloki'},
     {'id': 'baby-floki', 'symbol': 'babyfloki', 'name': 'Baby Floki'},
     {'id': 'baby-floki-coin',
      'symbol': 'babyflokicoin',
      'name': 'Baby Floki Coin'},
     {'id': 'baby-floki-erc', 'symbol': 'babyfloki', 'name': 'Baby Floki'},
     {'id': 'baby-floki-inu', 'symbol': 'bfloki', 'name': 'Baby Floki Inu'},
     {'id': 'baby-g', 'symbol': 'babyg', 'name': 'Baby G'},
     {'id': 'babykitty', 'symbol': 'babykitty', 'name': 'BabyKitty'},
     {'id': 'baby-lambo-inu', 'symbol': 'blinu', 'name': 'Baby Lambo Inu'},
     {'id': 'babylons', 'symbol': 'babi', 'name': 'Babylons'},
     {'id': 'baby-lovely-inu', 'symbol': 'blovely', 'name': 'Baby Lovely Inu'},
     {'id': 'babypepe', 'symbol': 'babypepe', 'name': 'BabyPepe'},
     {'id': 'baby-pepe', 'symbol': 'baby pepe', 'name': 'Baby Pepe'},
     {'id': 'babypepeentire', 'symbol': 'babypepe', 'name': 'BabyPepeEntire'},
     {'id': 'baby-pepe-erc20', 'symbol': 'babypepe', 'name': 'Baby Pepe'},
     {'id': 'babyrabbit', 'symbol': 'babyrabbit', 'name': 'Babyrabbit'},
     {'id': 'baby-richard-heart',
      'symbol': '$brich',
      'name': 'Baby Richard Heart'},
     {'id': 'baby-saitama', 'symbol': 'babysaitama', 'name': 'Baby Saitama'},
     {'id': 'baby-samo-coin', 'symbol': 'baby', 'name': 'Baby Samo Coin'},
     {'id': 'baby-shark', 'symbol': 'shark', 'name': 'Baby Shark'},
     {'id': 'baby-shark-tank', 'symbol': 'bashtank', 'name': 'Baby Shark Tank'},
     {'id': 'baby-shiba-coin', 'symbol': 'babyshiba', 'name': 'Baby Shiba Coin'},
     {'id': 'baby-shiba-inu', 'symbol': 'babyshibainu', 'name': 'Baby Shiba Inu'},
     {'id': 'baby-shiba-inu-erc', 'symbol': 'babyshib', 'name': 'Baby Shiba Inu'},
     {'id': 'babyswap', 'symbol': 'baby', 'name': 'BabySwap'},
     {'id': 'babywhale', 'symbol': 'bbw', 'name': 'BabyWhale'},
     {'id': 'babyxrp', 'symbol': 'bbyxrp', 'name': 'BabyXrp'},
     {'id': 'baby-yooshiape', 'symbol': 'byooshiape', 'name': 'Baby YooshiApe'},
     {'id': 'backed-coinbase-global',
      'symbol': 'bcoin',
      'name': 'Backed Coinbase Global'},
     {'id': 'backed-cspx-core-s-p-500',
      'symbol': 'bcspx',
      'name': 'Backed CSPX Core S&P 500'},
     {'id': 'backed-govies-0-6-months-euro',
      'symbol': 'bc3m',
      'name': 'Backed GOVIES 0-6 months EURO'},
     {'id': 'backed-high-high-yield-corp-bond',
      'symbol': 'bhigh',
      'name': 'Backed HIGH € High Yield Corp Bond'},
     {'id': 'backed-ib01-treasury-bond-0-1yr',
      'symbol': 'bib01',
      'name': 'Backed IB01 $ Treasury Bond 0-1yr'},
     {'id': 'backed-ibta-treasury-bond-1-3yr',
      'symbol': 'bibta',
      'name': 'Backed IBTA $ Treasury Bond 1-3yr'},
     {'id': 'backed-niu-technologies',
      'symbol': 'bniu',
      'name': 'Backed NIU Technologies'},
     {'id': 'bacondao', 'symbol': 'bacon', 'name': 'BaconDAO'},
     {'id': 'badger-dao', 'symbol': 'badger', 'name': 'Badger DAO'},
     {'id': 'badger-sett-badger',
      'symbol': 'bbadger',
      'name': 'Badger Sett Badger'},
     {'id': 'bad-idea-ai', 'symbol': 'bad', 'name': 'Bad Idea AI'},
     {'id': 'bae', 'symbol': 'bae', 'name': 'Bae'},
     {'id': 'bafi-finance-token', 'symbol': 'bafi', 'name': 'Bafi Finance'},
     {'id': 'bagholder', 'symbol': 'bag', 'name': 'Bagholder'},
     {'id': 'bahamas-network', 'symbol': 'bn', 'name': 'Bahamas Network'},
     {'id': 'bai-stablecoin', 'symbol': 'bai', 'name': 'BAI Stablecoin'},
     {'id': 'baka-casino', 'symbol': 'bakac', 'name': 'Baka Casino'},
     {'id': 'baked-token', 'symbol': 'baked', 'name': 'Baked'},
     {'id': 'bakerytoken', 'symbol': 'bake', 'name': 'BakerySwap'},
     {'id': 'bakerytools', 'symbol': 'tbake', 'name': 'BakeryTools'},
     {'id': 'baklava', 'symbol': 'bava', 'name': 'Baklava'},
     {'id': 'balanced-dollars', 'symbol': 'bnusd', 'name': 'Balanced Dollars'},
     {'id': 'balancer', 'symbol': 'bal', 'name': 'Balancer'},
     {'id': 'balancer-80-bal-20-weth',
      'symbol': 'b-80bal-20weth',
      'name': 'Balancer 80 BAL 20 WETH'},
     {'id': 'balancer-aave-boosted-wmatic',
      'symbol': 'bb-a-wmatic',
      'name': 'Balancer Aave Boosted WMATIC'},
     {'id': 'balancer-boosted-aave-weth',
      'symbol': 'bb-a-weth',
      'name': 'Balancer Aave v3 Boosted Pool (WETH)'},
     {'id': 'balancer-boosted-aave-weth-2',
      'symbol': 'bb-a-weth',
      'name': 'Balancer Boosted Aave WETH'},
     {'id': 'balancer-maticx-boosted-aave-wmatic',
      'symbol': 'maticx-bb-a-wmatic-bpt',
      'name': 'Balancer MaticX Boosted Aave WMATIC'},
     {'id': 'balancer-savings-dai-boosted-pool',
      'symbol': 'bb-s-dai',
      'name': 'Balancer Savings DAI Boosted Pool'},
     {'id': 'balance-tokens', 'symbol': 'baln', 'name': 'Balanced'},
     {'id': 'bald', 'symbol': 'bald', 'name': 'Bald'},
     {'id': 'bali-token', 'symbol': 'bli', 'name': 'Bali Token'},
     {'id': 'bali-united-fc-fan-token',
      'symbol': 'bufc',
      'name': 'Bali United FC Fan Token'},
     {'id': 'ball-coin', 'symbol': 'ball', 'name': 'BALL Coin'},
     {'id': 'balloonsville-air', 'symbol': 'air', 'name': 'Balloonsville AIR'},
     {'id': 'ballswap', 'symbol': 'bsp', 'name': 'BallSwap'},
     {'id': 'ball-token', 'symbol': 'ball', 'name': 'Ball'},
     {'id': 'balpha', 'symbol': 'balpha', 'name': 'bAlpha'},
     {'id': 'bambi', 'symbol': 'bam', 'name': 'Bambi'},
     {'id': 'bamboo-coin', 'symbol': 'bmbo', 'name': 'Bamboo Coin'},
     {'id': 'bamboo-defi', 'symbol': 'bamboo', 'name': 'Bamboo DeFi'},
     {'id': 'bamboo-token-c90b31ff-8355-41d6-a495-2b16418524c2',
      'symbol': 'bbo',
      'name': 'PandaFarm (BBO)'},
     {'id': 'banana', 'symbol': 'banana', 'name': 'Banana'},
     {'id': 'bananace', 'symbol': 'nana', 'name': 'Bananace'},
     {'id': 'banana-coin', 'symbol': 'banana', 'name': 'BananaCoin'},
     {'id': 'banana-gun', 'symbol': 'banana', 'name': 'Banana Gun'},
     {'id': 'bananatok', 'symbol': 'bna', 'name': 'BananaTok'},
     {'id': 'banana-token', 'symbol': 'bnana', 'name': 'Chimpion'},
     {'id': 'banano', 'symbol': 'ban', 'name': 'Banano'},
     {'id': 'bancor', 'symbol': 'bnt', 'name': 'Bancor Network'},
     {'id': 'bancor-governance-token',
      'symbol': 'vbnt',
      'name': 'Bancor Governance'},
     {'id': 'band-protocol', 'symbol': 'band', 'name': 'Band Protocol'},
     {'id': 'bandzai-token', 'symbol': 'bzai', 'name': 'BandZai Token'},
     {'id': 'bank', 'symbol': '$bank', 'name': 'Bank'},
     {'id': 'bankbrc', 'symbol': 'bank', 'name': 'BANK (Ordinals)'},
     {'id': 'bankera', 'symbol': 'bnk', 'name': 'Bankera'},
     {'id': 'bankercoin', 'symbol': '$bank', 'name': 'Bankercoin'},
     {'id': 'bankers-dream', 'symbol': 'bank$', 'name': 'Bankers Dream'},
     {'id': 'bankless-bed-index', 'symbol': 'bed', 'name': 'Bankless BED Index'},
     {'id': 'bankless-dao', 'symbol': 'bank', 'name': 'Bankless DAO'},
     {'id': 'bankroll-extended-token',
      'symbol': 'bnkrx',
      'name': 'Bankroll Extended'},
     {'id': 'bankroll-vault', 'symbol': 'vlt', 'name': 'Bankroll Vault'},
     {'id': 'banksocial', 'symbol': 'bsl', 'name': 'BankSocial'},
     {'id': 'bantu', 'symbol': 'xbn', 'name': 'Bantu'},
     {'id': 'banus-finance', 'symbol': 'banus', 'name': 'Banus Finance'},
     {'id': 'baoeth-eth-stablepool',
      'symbol': 'b-baoeth-eth-bpt',
      'name': 'baoETH-ETH StablePool'},
     {'id': 'bao-finance', 'symbol': 'bao', 'name': 'Bao Finance'},
     {'id': 'bao-finance-v2', 'symbol': 'bao', 'name': 'Bao Finance V2'},
     {'id': 'baousd-lusd-stablepool',
      'symbol': 'baousd-lusd-stablepool',
      'name': 'baoUSD-LUSD StablePool'},
     {'id': 'barbiecrashbandicootrfk88',
      'symbol': 'solana',
      'name': 'BarbieCrashBandicootRFK88'},
     {'id': 'bark', 'symbol': 'bark', 'name': 'Bark'},
     {'id': 'barking', 'symbol': 'bark', 'name': 'Barking'},
     {'id': 'barnbridge', 'symbol': 'bond', 'name': 'BarnBridge'},
     {'id': 'barter', 'symbol': 'brtr', 'name': 'Barter'},
     {'id': 'bart-simpson-coin', 'symbol': 'bart', 'name': 'Bart Simpson Coin'},
     {'id': 'base', 'symbol': 'base', 'name': 'Base'},
     {'id': 'baseape', 'symbol': 'bape', 'name': 'Baseape'},
     {'id': 'basebank', 'symbol': 'bbank', 'name': 'BaseBank'},
     {'id': 'based-ai', 'symbol': 'bai', 'name': 'Based AI'},
     {'id': 'basedbets', 'symbol': 'bet', 'name': 'BasedBets'},
     {'id': 'based-farm', 'symbol': 'based', 'name': 'Based Farm'},
     {'id': 'based-finance', 'symbol': 'based', 'name': 'Based Finance'},
     {'id': 'based-markets', 'symbol': 'based', 'name': 'based.markets'},
     {'id': 'based-money-finance',
      'symbol': 'based',
      'name': 'Based Money Finance'},
     {'id': 'basedpepe', 'symbol': 'bpepe', 'name': 'BasedPepe'},
     {'id': 'based-shares', 'symbol': 'bshare', 'name': 'BASED Shares'},
     {'id': 'baseinu', 'symbol': 'binu', 'name': 'BaseInu'},
     {'id': 'base-name-service', 'symbol': 'bns', 'name': 'Base Name Service'},
     {'id': 'base-protocol', 'symbol': 'base', 'name': 'Base Protocol'},
     {'id': 'baseswap', 'symbol': 'bswap', 'name': 'BaseSwap'},
     {'id': 'basetools', 'symbol': 'base', 'name': 'BaseTools'},
     {'id': 'base-velocimeter', 'symbol': 'bvm', 'name': 'Base Velocimeter'},
     {'id': 'basex', 'symbol': 'bsx', 'name': 'BaseX'},
     {'id': 'basic-attention-token', 'symbol': 'bat', 'name': 'Basic Attention'},
     {'id': 'basilisk', 'symbol': 'bsx', 'name': 'Basilisk'},
     {'id': 'basin-finance', 'symbol': 'basin', 'name': 'Basin Finance'},
     {'id': 'basis-cash', 'symbol': 'bac', 'name': 'Basis Cash'},
     {'id': 'basis-gold-share-heco',
      'symbol': 'bags',
      'name': 'Basis Gold Share (Heco)'},
     {'id': 'basis-markets', 'symbol': 'basis', 'name': 'basis.markets'},
     {'id': 'basis-share', 'symbol': 'bas', 'name': 'Basis Share'},
     {'id': 'basketball-legends', 'symbol': 'bbl', 'name': 'Basketball Legends'},
     {'id': 'basketcoin', 'symbol': 'bskt', 'name': 'BasketCoin'},
     {'id': 'baskonia-fan-token', 'symbol': 'bkn', 'name': 'Baskonia Fan Token'},
     {'id': 'baso-finance', 'symbol': 'baso', 'name': 'Baso Finance'},
     {'id': 'bass-exchange', 'symbol': '$bass', 'name': 'Bass Exchange'},
     {'id': 'bata', 'symbol': 'bta', 'name': 'Bata'},
     {'id': 'bathtub-protocol', 'symbol': 'bath', 'name': 'Bathtub Protocol'},
     {'id': 'battlefly', 'symbol': 'gfly', 'name': 'BattleFly'},
     {'id': 'battle-for-giostone', 'symbol': 'bfg', 'name': 'Battle For Giostone'},
     {'id': 'battleforten', 'symbol': 'bft', 'name': 'BattleForTEN'},
     {'id': 'battleground', 'symbol': 'battle', 'name': 'Battleground'},
     {'id': 'battle-infinity', 'symbol': 'ibat', 'name': 'Battle Infinity'},
     {'id': 'battle-pets', 'symbol': 'pet', 'name': 'Hello Pets'},
     {'id': 'battle-saga', 'symbol': 'btl', 'name': 'Battle Saga'},
     {'id': 'battleverse', 'symbol': 'bvc', 'name': 'BattleVerse'},
     {'id': 'battle-world', 'symbol': 'bwo', 'name': 'Battle World'},
     {'id': 'bayesian', 'symbol': 'baye', 'name': 'Bayesian'},
     {'id': 'baymax-finance', 'symbol': 'bay', 'name': 'BayMax Finance'},
     {'id': 'bazaars', 'symbol': 'bzr', 'name': 'Bazaars'},
     {'id': 'bazed-games', 'symbol': 'bazed', 'name': 'Bazed Games'},
     {'id': 'bb-gaming', 'symbol': 'bb', 'name': 'BB Gaming'},
     ...]




```python
# getting coin market chart for 'bitcoin' and assigning to variable which 
# is returned (API response) as a JSON file expressed as as a dictionary

bitcoin_data = cg.get_coin_market_chart_by_id(id='bitcoin', vs_currency='usd', days=30)
bitcoin_data
```




    {'prices': [[1693648825935, 25794.334274999826],
      [1693652461970, 25824.644083232386],
      [1693656041070, 25798.91734363616],
      [1693659628425, 25795.438233690857],
      [1693663268552, 25825.01020718762],
      [1693666887711, 25862.02881396863],
      [1693670446590, 25898.432073032756],
      [1693674063262, 25861.182951188555],
      [1693677661040, 25815.832717413177],
      [1693681242294, 25791.936056022405],
      [1693684856557, 25845.216318279246],
      [1693688444033, 25845.562761647394],
      [1693692062997, 25838.89610105248],
      [1693695693194, 25859.36428638706],
      [1693699264592, 25853.65684277757],
      [1693702856775, 25852.496874120287],
      [1693706414406, 25863.6019089],
      [1693710055340, 25861.17109121785],
      [1693713643481, 25850.426267510193],
      [1693717226739, 25875.5583470379],
      [1693720809648, 25892.652704479053],
      [1693724415495, 25909.303712117384],
      [1693728031671, 25948.82742837482],
      [1693731654964, 25894.506471703975],
      [1693735257631, 25900.041715206396],
      [1693738865847, 25931.476334520765],
      [1693742429194, 25940.481769471393],
      [1693746055433, 25980.231275607213],
      [1693749647341, 25927.60903375676],
      [1693753256166, 25927.613106412242],
      [1693756845741, 25870.26909258105],
      [1693760456695, 25836.905638144235],
      [1693764051895, 25867.780778036857],
      [1693767654694, 25928.325279740475],
      [1693771295201, 25991.657453735366],
      [1693774851023, 26054.793419062265],
      [1693778465432, 25965.711747159905],
      [1693782045508, 25948.197964470794],
      [1693785623272, 25959.596311463454],
      [1693789250453, 25905.234164922775],
      [1693792876822, 25889.495816344996],
      [1693796473263, 25988.868344717957],
      [1693800071129, 25998.296229842043],
      [1693803662428, 25973.57802350052],
      [1693807257341, 25942.345376705038],
      [1693810849866, 25965.23324335423],
      [1693814443906, 25982.970118930814],
      [1693818031244, 25972.9327001036],
      [1693821651204, 25934.70132711085],
      [1693825255694, 25895.451327360344],
      [1693828836482, 25881.1448617462],
      [1693832422257, 25847.950276584805],
      [1693836057860, 25884.759729055186],
      [1693839648954, 25856.571092465416],
      [1693843238926, 25804.658557387786],
      [1693846816760, 25830.620485430598],
      [1693850437784, 25898.639012149037],
      [1693854039635, 25920.605857381808],
      [1693857643941, 25871.536494165204],
      [1693861241813, 25818.718627977538],
      [1693864869559, 25659.620573078173],
      [1693868423076, 25749.106735136127],
      [1693872058364, 25829.364772941324],
      [1693875645622, 25749.5169316782],
      [1693879264941, 25778.9861796218],
      [1693882850852, 25684.842993789418],
      [1693886442529, 25652.30731623389],
      [1693890068698, 25680.781263703244],
      [1693893646500, 25715.96025384614],
      [1693897264682, 25700.18282360907],
      [1693900805601, 25705.04566328197],
      [1693904439022, 25670.652934087426],
      [1693908062473, 25735.47814830377],
      [1693911637129, 25741.401975130753],
      [1693915250322, 25765.384374327292],
      [1693918902721, 25806.529233946632],
      [1693922444219, 25745.22408666264],
      [1693926063141, 25679.914480620202],
      [1693929674270, 25765.665470406962],
      [1693933260798, 25736.582543310655],
      [1693936842325, 25735.593860526533],
      [1693940423070, 25726.987761863737],
      [1693944060332, 25706.433839717007],
      [1693947640079, 25707.492443623356],
      [1693951220545, 25736.687755521583],
      [1693954807133, 25753.95929850106],
      [1693958429024, 25770.129054916044],
      [1693962054506, 25785.257103023414],
      [1693965664508, 25775.016869622676],
      [1693969255513, 25835.942668563916],
      [1693972824000, 25767.177178583155],
      [1693976401207, 25748.901195484556],
      [1693980063358, 25723.908179919075],
      [1693983636159, 25763.5066618578],
      [1693987210109, 25736.952419502828],
      [1693990868239, 25744.196797277473],
      [1693994441403, 25739.805878121108],
      [1693998065048, 25711.609000363373],
      [1694001675599, 25714.982106082552],
      [1694005248608, 25685.932228726484],
      [1694008849196, 25738.4322377283],
      [1694012461622, 25576.564268541297],
      [1694016062320, 25602.157018645226],
      [1694019623530, 25581.463757784346],
      [1694023206891, 25684.626007326333],
      [1694026820854, 25657.975653507976],
      [1694030453203, 25643.30464824743],
      [1694034058637, 25672.527450689344],
      [1694037632696, 25723.161474144752],
      [1694041222274, 25725.087827734977],
      [1694044839359, 25752.958418589413],
      [1694048445693, 25722.839541927093],
      [1694052059253, 25733.7521151415],
      [1694055610946, 25747.102850194256],
      [1694059259063, 25822.847798860847],
      [1694062855457, 25794.514811715846],
      [1694066468460, 25793.21162563605],
      [1694070050167, 25762.69564191477],
      [1694073671954, 25753.912752636796],
      [1694077288878, 25728.93651333519],
      [1694080821617, 25743.043162326103],
      [1694084404682, 25714.694356419826],
      [1694088057834, 25691.773412908977],
      [1694091614579, 25647.715450955635],
      [1694095318077, 25704.796266845595],
      [1694098854239, 25726.267628874248],
      [1694102444392, 25761.319903739968],
      [1694106080694, 25833.7115000559],
      [1694109676460, 25922.61422794861],
      [1694113252773, 25880.38248639935],
      [1694116865174, 25871.777070889788],
      [1694120463878, 25937.404672609428],
      [1694124050166, 26172.824176891645],
      [1694127637765, 26387.74791739874],
      [1694131272591, 26192.333433090567],
      [1694134885236, 26355.95434081812],
      [1694138447569, 26247.228457538815],
      [1694142046787, 26216.349095884838],
      [1694145615869, 26261.73123573869],
      [1694149200956, 26327.696162567237],
      [1694152973752, 26235.97622144165],
      [1694156430831, 26213.07688877117],
      [1694160066144, 26244.624045845645],
      [1694163667034, 26190.09050974855],
      [1694167236127, 26047.932268135748],
      [1694170880330, 25837.604838032235],
      [1694174470818, 25830.33368883198],
      [1694178069428, 25863.324420760684],
      [1694181685773, 25910.839595261696],
      [1694185205197, 25877.826172100773],
      [1694188849164, 25843.073060494975],
      [1694192416778, 25764.72345705586],
      [1694196073509, 25828.687287745044],
      [1694199665513, 25796.947102093134],
      [1694203254994, 25880.110917143327],
      [1694206871509, 25892.343360345403],
      [1694210404044, 25906.751304699905],
      [1694214009931, 25905.63785593694],
      [1694217602458, 25907.228137249735],
      [1694221201462, 25857.517155460682],
      [1694224814902, 25856.30593847393],
      [1694228410066, 25878.954649778996],
      [1694232046089, 25864.589688661777],
      [1694235665094, 25862.369844865738],
      [1694239275528, 25836.33337018519],
      [1694242916309, 25868.050964080416],
      [1694246453300, 25861.620547722294],
      [1694250099946, 25883.62221651013],
      [1694253707248, 25877.139709346768],
      [1694257206615, 25850.71864964946],
      [1694260857596, 25854.034556295937],
      [1694264482646, 25852.142215485736],
      [1694268085624, 25813.384607397376],
      [1694271604957, 25846.05141960633],
      [1694275279558, 25907.292127847395],
      [1694278803871, 25888.9569505614],
      [1694282411865, 25873.399748499487],
      [1694286070426, 25853.821763150416],
      [1694289657928, 25857.727875644516],
      [1694293288738, 25854.309353809494],
      [1694296874825, 25865.328687004385],
      [1694300470680, 25900.10190570366],
      [1694304065905, 25889.67163888094],
      [1694307668612, 25862.385734468287],
      [1694311254157, 25845.437062682347],
      [1694314848468, 25847.766906895195],
      [1694318454068, 25857.418912177094],
      [1694322031236, 25820.49583757943],
      [1694325639171, 25845.749902362117],
      [1694329274243, 25855.01896890166],
      [1694332884463, 25849.43842621568],
      [1694336458732, 25854.29418382193],
      [1694340095012, 25839.119252470573],
      [1694343661201, 25802.227046608547],
      [1694347208077, 25806.102340233174],
      [1694350853257, 25801.35852270764],
      [1694354477774, 25824.130911427757],
      [1694358088575, 25768.403294708838],
      [1694361673154, 25774.027318372468],
      [1694365324308, 25779.034351276216],
      [1694368870234, 25682.08207006774],
      [1694372469890, 25719.985920817628],
      [1694376014473, 25738.69385555759],
      [1694379600938, 25798.42633522363],
      [1694383277662, 25862.777279309616],
      [1694386858130, 25857.257728995824],
      [1694390437028, 25834.8856281802],
      [1694394035700, 25704.005403651034],
      [1694397658557, 25685.61508618535],
      [1694401291166, 25727.47751406507],
      [1694404887035, 25730.28169687907],
      [1694408418510, 25772.763725956444],
      [1694412055734, 25836.14289431529],
      [1694415609754, 25830.58628748631],
      [1694419255394, 25805.92480039249],
      [1694422810174, 25811.750276858536],
      [1694426428782, 25709.947962746148],
      [1694430037101, 25689.839562282286],
      [1694433682517, 25591.028360280547],
      [1694437265312, 25691.519296461676],
      [1694440832538, 25630.75014265575],
      [1694444445412, 25135.318421703454],
      [1694448071877, 25104.18201248399],
      [1694451620503, 25178.57009580151],
      [1694455266692, 25196.793481825855],
      [1694458843230, 25164.754034328318],
      [1694462466940, 25023.24918499984],
      [1694466078755, 25081.597675484332],
      [1694469680181, 25131.761556167516],
      [1694473314943, 25140.138898899415],
      [1694476881529, 25133.303106566527],
      [1694480488595, 25192.83559199593],
      [1694484085000, 25134.534999857224],
      [1694487615337, 25195.64876624606],
      [1694491211052, 25787.640719595725],
      [1694494814434, 25783.919031402012],
      [1694498455321, 25751.817562269047],
      [1694502056337, 25750.89041239366],
      [1694505629082, 25812.56016924981],
      [1694509216115, 25774.827931433967],
      [1694512819366, 25819.764344389885],
      [1694516412777, 26124.250641370065],
      [1694520016345, 26082.106968445238],
      [1694523637652, 26158.226466438027],
      [1694527268583, 26288.334884466993],
      [1694530832034, 26108.986672429517],
      [1694534432648, 26203.946997211315],
      [1694538053480, 26175.226537360697],
      [1694541654586, 26000.36514493771],
      [1694545223687, 25957.012894109783],
      [1694548806012, 26100.979330578975],
      [1694552450229, 26097.359658976377],
      [1694556027555, 26094.78130285003],
      [1694559629043, 25979.21538462445],
      [1694563222193, 25850.322299629544],
      [1694566917493, 25912.080800331947],
      [1694570443707, 25937.096199840835],
      [1694574083085, 25920.91324358947],
      [1694577659479, 25843.107804557887],
      [1694581211111, 25913.053069985817],
      [1694584869861, 25899.214193103733],
      [1694588418238, 25950.63889586843],
      [1694592032997, 25886.469496421727],
      [1694595683764, 25942.732085181477],
      [1694599247209, 26122.023893246413],
      [1694602811820, 26105.761078248503],
      [1694606490503, 26180.571209215264],
      [1694610002904, 26186.539893484543],
      [1694613673373, 26181.399852640352],
      [1694617304732, 26188.39626073516],
      [1694620832071, 26240.792627505187],
      [1694624426856, 26304.01546518303],
      [1694628079714, 26091.35049184821],
      [1694631677462, 26133.33058838231],
      [1694635306550, 26145.32151330617],
      [1694638801518, 26226.862815769757],
      [1694642483410, 26231.9493781631],
      [1694646050908, 26234.18982796697],
      [1694649714172, 26222.013303986474],
      [1694653240839, 26488.966008361596],
      [1694656855482, 26208.463348448524],
      [1694660438250, 26249.26511882836],
      [1694664048538, 26258.64482104317],
      [1694667652385, 26213.568845517944],
      [1694671276245, 26193.031945995655],
      [1694674947752, 26289.032017713966],
      [1694678468407, 26355.570038862013],
      [1694682079168, 26293.175851265434],
      [1694685665455, 26279.82107866277],
      [1694689208120, 26298.857189095856],
      [1694692859624, 26418.287932796033],
      [1694696465988, 26479.29027258699],
      [1694700021827, 26542.85915995021],
      [1694703625869, 26751.79664567292],
      [1694707248924, 26688.691714839948],
      [1694710862560, 26583.251622460648],
      [1694714450259, 26619.408529040997],
      [1694718047119, 26601.043663052755],
      [1694721647323, 26636.597761721252],
      [1694725278466, 26576.923372009656],
      [1694728875769, 26544.83468544189],
      [1694732426804, 26615.532123428224],
      [1694736055931, 26531.39556626326],
      [1694739617783, 26529.77638373226],
      [1694743262223, 26506.205835634933],
      [1694746878614, 26599.794162700844],
      [1694750471019, 26619.371827748],
      [1694754083159, 26653.565743786352],
      [1694757677069, 26591.2634436531],
      [1694761234709, 26575.998948235687],
      [1694764895297, 26569.22550324378],
      [1694768402473, 26617.08907084948],
      [1694772011129, 26641.97583856179],
      [1694775652180, 26629.71436109239],
      [1694779251994, 26479.808783650304],
      [1694782856479, 26375.58083976395],
      [1694786454986, 26441.25513890341],
      [1694790009818, 26251.615685201057],
      [1694793674696, 26320.506096171328],
      [1694797225889, 26362.602910709724],
      [1694800870359, 26367.061843983578],
      [1694804444403, 26356.727827118706],
      [1694808002218, 26427.542806322395],
      [1694811666558, 26406.960131317344],
      [1694815273478, 26466.627409553737],
      [1694818857488, 26792.60882462043],
      [1694822447711, 26610.403126161622],
      [1694826058107, 26637.676118192823],
      [1694829649148, 26663.714857986022],
      [1694833267018, 26704.25388242849],
      [1694836881872, 26624.316186014064],
      [1694840419759, 26604.744367280226],
      [1694844070098, 26546.000476745226],
      [1694847657005, 26471.09371981062],
      [1694851245430, 26489.853636572643],
      [1694854846001, 26507.86894063841],
      [1694858459103, 26542.28540876647],
      [1694862049970, 26528.22877496949],
      [1694865653784, 26530.132596770418],
      [1694869207617, 26574.159426883907],
      [1694872851812, 26547.033583330496],
      [1694876467404, 26514.846146933192],
      [1694880082717, 26532.029422507887],
      [1694883666750, 26533.045434751308],
      [1694887250607, 26577.13171683862],
      [1694890880239, 26571.034961764737],
      [1694894445223, 26534.773305412753],
      [1694898088889, 26545.15123574602],
      [1694901629896, 26576.697031424446],
      [1694905264280, 26566.033844441456],
      [1694908851309, 26557.768691994646],
      [1694912461893, 26470.036122923164],
      [1694916072780, 26510.475433966454],
      [1694919623616, 26524.653127846243],
      [1694923210574, 26535.20829753553],
      [1694926855732, 26562.489915752496],
      [1694930432647, 26545.0854242848],
      [1694934086167, 26549.936474136273],
      [1694937668691, 26494.729010798754],
      [1694941259399, 26551.53028796057],
      [1694944860269, 26574.740939582],
      [1694948477497, 26605.36747233914],
      [1694952052810, 26586.475348507603],
      [1694955601392, 26583.778812580116],
      [1694959303815, 26549.705841471747],
      [1694962875743, 26572.60934792332],
      [1694966411022, 26556.08429333667],
      [1694970051327, 26523.239737958964],
      [1694973608434, 26496.59086020322],
      [1694977260752, 26501.904023273473],
      [1694980861168, 26504.032756422563],
      [1694984434885, 26462.58323203275],
      [1694988004732, 26484.21067751066],
      [1694991655674, 26468.617801591503],
      [1694995200732, 26520.988254783886],
      [1694998838971, 26505.771084799046],
      [1695002474748, 26456.81769925053],
      [1695006069155, 26676.032052943723],
      [1695009670759, 26666.378790034138],
      [1695013226979, 26623.769887126396],
      [1695016872385, 26657.999330340524],
      [1695020449169, 26660.428508364123],
      [1695024061307, 26695.936788348576],
      [1695027671042, 26707.637744803884],
      [1695031239845, 26866.544703080435],
      [1695034829890, 27128.867817693306],
      [1695038451785, 27180.197194827022],
      [1695042087909, 27394.588104693972],
      [1695045655879, 27258.995949583415],
      [1695049250228, 27265.78414303009],
      [1695052877062, 27267.443496733686],
      [1695056415522, 27266.969453656227],
      [1695060004008, 26821.851065864783],
      [1695063650349, 26719.579525357352],
      [1695067252745, 26863.187669787494],
      [1695070886761, 26787.33729318315],
      [1695074401030, 26801.832482690246],
      [1695078053710, 26867.0605755984],
      [1695081698935, 26741.461110948952],
      [1695085269505, 26682.841448803098],
      [1695088877096, 26698.107813619576],
      [1695092408017, 26779.1885428471],
      [1695096076629, 26820.77736698705],
      [1695099622098, 26864.929364500967],
      [1695103223115, 26817.178714597805],
      [1695106815064, 26828.934567385746],
      [1695110419806, 26875.902968384416],
      [1695114036701, 27052.095871968973],
      [1695117679832, 27289.4248902988],
      [1695121282809, 27183.994603047813],
      [1695124810966, 27222.58191830418],
      [1695128447573, 27145.730412737612],
      [1695132043410, 27076.486393257255],
      [1695135668460, 27143.212388822172],
      [1695139222823, 27285.48143150427],
      [1695142837205, 27278.936209801446],
      [1695146444033, 27192.599824193756],
      [1695150056393, 27113.69924015732],
      [1695153601055, 27163.178091247963],
      [1695157228217, 27178.37716757279],
      [1695160848717, 27136.97284512376],
      [1695164400975, 27200.83584839815],
      [1695168064203, 27213.18465907596],
      [1695171663284, 27173.66776619467],
      [1695175208607, 27318.242557709546],
      [1695178854556, 27161.87334289422],
      [1695182400876, 27093.36215386263],
      [1695186050046, 27149.351761098074],
      [1695189676784, 27060.883660753127],
      [1695193275641, 27038.933885562554],
      [1695196835448, 27112.464832074555],
      [1695200476704, 27183.312737946195],
      [1695204005800, 27025.22452404166],
      [1695207671348, 27063.877293712478],
      [1695211261367, 27107.755442112102],
      [1695214890479, 27072.451101145525],
      [1695218470716, 27181.891317975704],
      [1695222115762, 27120.178968917484],
      [1695225610681, 27190.18445834599],
      [1695229202276, 27186.05265473318],
      [1695232880415, 27203.95735554073],
      [1695236420122, 27149.589756459616],
      [1695240011084, 26936.571052710085],
      [1695243619413, 27076.340775259883],
      [1695247277558, 27145.01073656103],
      [1695250880706, 27110.600552890646],
      [1695254488050, 27115.846446970816],
      [1695258011493, 27050.541305794104],
      [1695261647004, 27024.914837344724],
      [1695265214100, 26974.56757296705],
      [1695268851479, 27030.236258658922],
      [1695272464248, 27102.020623711906],
      [1695276070457, 27068.20100990383],
      [1695279692762, 27067.514532949186],
      [1695283216498, 26993.699990949342],
      [1695286832893, 26920.45025229596],
      [1695290462370, 26739.995111014814],
      [1695294082215, 26626.573309357234],
      [1695297604793, 26755.584980445696],
      [1695301217597, 26648.834080478802],
      [1695304846808, 26418.52778477277],
      [1695308416465, 26576.97810175096],
      [1695312076058, 26639.52880783224],
      [1695315655980, 26577.034378575376],
      [1695319259336, 26660.435061525113],
      [1695322849394, 26610.05552034763],
      [1695326443371, 26603.939431757222],
      [1695330048069, 26584.396598068863],
      [1695333658482, 26593.195069864574],
      [1695337245237, 26589.232106802505],
      [1695340876770, 26561.133454198716],
      [1695344424140, 26639.641861578562],
      [1695348042198, 26637.636327006938],
      [1695351600787, 26578.905206148003],
      [1695355253016, 26626.378906818343],
      [1695358844050, 26648.00124709664],
      [1695362405337, 26637.914728114418],
      [1695366023000, 26608.789028776486],
      [1695369602489, 26672.355811811238],
      [1695373249394, 26662.581883179126],
      [1695376900161, 26642.19156124197],
      [1695380406103, 26589.562536733414],
      [1695384006363, 26642.349940444896],
      [1695387614279, 26590.721839939364],
      [1695391205061, 26590.318346408505],
      [1695394816160, 26688.33796153136],
      [1695398451954, 26635.9956475043],
      [1695402045900, 26594.50364952432],
      [1695405610328, 26584.86501070471],
      [1695409231493, 26581.657981099415],
      [1695412867797, 26547.829784907477],
      [1695416418610, 26534.177936540287],
      [1695420023207, 26563.985676592565],
      [1695423661624, 26582.589416632578],
      [1695427201859, 26581.967576018324],
      [1695430811253, 26592.91317293783],
      [1695434410132, 26585.290471612167],
      [1695438058561, 26545.492871251507],
      [1695441644699, 26536.561163334205],
      [1695445206991, 26556.352013285596],
      [1695448808438, 26540.550300446146],
      [1695452439871, 26584.65994469058],
      [1695456047770, 26588.0877783081],
      [1695459608638, 26568.05854124356],
      [1695463260402, 26569.61170975327],
      [1695466827539, 26570.72759500637],
      [1695470450048, 26568.85782887614],
      [1695474006333, 26556.154413845245],
      [1695477700146, 26564.64627526254],
      [1695481252606, 26568.125190131854],
      [1695484847029, 26577.180354824755],
      [1695488466338, 26590.201409894365],
      [1695492053864, 26601.829342720674],
      [1695495631342, 26615.098925655053],
      [1695499252245, 26610.27539472885],
      [1695502872078, 26587.030719433697],
      [1695506415356, 26568.478097013893],
      [1695510062533, 26575.52911690974],
      [1695513663505, 26573.9234797301],
      [1695517264824, 26576.201789893425],
      [1695520850765, 26587.336388850297],
      [1695524458287, 26586.008804555724],
      [1695528008432, 26560.723350938522],
      [1695531644700, 26569.875558372973],
      [1695535260830, 26562.281185542444],
      [1695538817963, 26550.45340587291],
      [1695542471024, 26561.17840053706],
      [1695546077698, 26579.929451350046],
      [1695549622074, 26588.80815731327],
      [1695553252441, 26579.491960979794],
      [1695556868895, 26597.32744006094],
      [1695560410462, 26605.1606539787],
      [1695564035623, 26597.821687761414],
      [1695567604844, 26589.797665663824],
      [1695571264473, 26580.92820338404],
      [1695574805796, 26570.733979097706],
      [1695578469402, 26657.753582685626],
      [1695582049432, 26600.275121547336],
      [1695585670396, 26447.45930249158],
      [1695589238846, 26505.53480594746],
      [1695592873976, 26519.93457602045],
      [1695596405135, 26503.235602590674],
      [1695600051058, 26257.58376993293],
      [1695603623800, 26197.46011142378],
      [1695607258182, 26199.403236385315],
      [1695610877802, 26166.655202208483],
      [1695614475167, 26156.621770098798],
      [1695618025607, 26145.617391107404],
      [1695621634966, 26117.151507594062],
      [1695625259023, 26138.4925731258],
      [1695628866670, 26181.383887893517],
      [1695632422994, 26128.669159227582],
      [1695636109197, 26059.043074839537],
      [1695639662839, 26086.860590577646],
      [1695643263383, 26077.019560024095],
      [1695646801447, 26089.099069634845],
      [1695650400482, 26138.435787005466],
      [1695654024293, 26110.04755445133],
      [1695657604804, 26242.580851196097],
      [1695661204413, 26317.635405795543],
      [1695664826153, 26357.55015326377],
      [1695668437733, 26335.400366914426],
      [1695672054179, 26344.908159924624],
      [1695675654169, 26310.628891942943],
      [1695679209652, 26257.316593042888],
      [1695682807114, 26287.076366997982],
      [1695686440433, 26296.92231737691],
      [1695690058692, 26277.764253277604],
      [1695693681785, 26286.125407384083],
      [1695697281459, 26331.579435404343],
      [1695700851398, 26347.306498337617],
      [1695704468510, 26339.181988547076],
      [1695708096777, 26315.66494004243],
      [1695711600956, 26271.546235087877],
      [1695715263432, 26273.770004029095],
      [1695718832620, 26274.95856780814],
      [1695722429980, 26272.560104308588],
      [1695726081051, 26232.387655871495],
      [1695729656720, 26242.655160865525],
      [1695733294836, 26216.589643826963],
      [1695736881037, 26218.81871171417],
      [1695740487097, 26180.78081214982],
      [1695744055159, 26111.574712349553],
      [1695747672991, 26217.795567371588],
      [1695751287665, 26180.151205932874],
      [1695754864358, 26158.96300512369],
      [1695758428680, 26252.577052683107],
      [1695762060076, 26175.70955457768],
      [1695765635786, 26154.819323615397],
      [1695769242778, 26151.495531909033],
      [1695772828684, 26204.75759083597],
      [1695776473902, 26218.080459481796],
      [1695780037371, 26251.30733492169],
      [1695783663393, 26219.37883759674],
      [1695787240532, 26262.327552470317],
      [1695790857263, 26242.486177466555],
      [1695794405022, 26230.37306858725],
      [1695798126255, 26245.07128429413],
      [1695801645086, 26227.05218111046],
      [1695805256499, 26243.852966398415],
      [1695808825366, 26335.634673758457],
      [1695812453484, 26413.18633693111],
      [1695816058049, 26805.628892226956],
      [1695819620887, 26722.206778832646],
      [1695823269425, 26619.937862451417],
      [1695826859141, 26166.382102431195],
      [1695830443438, 26291.838135512997],
      [1695834009021, 26218.667975753804],
      [1695837671798, 26207.252695876075],
      [1695841259012, 26260.32108022661],
      [1695844904485, 26245.585136939553],
      [1695848463884, 26240.244240253738],
      [1695852051010, 26255.8025743061],
      [1695855613344, 26288.209341200014],
      [1695859251089, 26350.146895428057],
      [1695862855029, 26423.81585868406],
      [1695866524625, 26433.30117414558],
      [1695870120091, 26364.823472858556],
      [1695873669851, 26344.99309446877],
      [1695877278049, 26424.745106695722],
      [1695880861843, 26400.93546218415],
      [1695884435169, 26457.099705176435],
      [1695888001200, 26432.352022735326],
      [1695891657517, 26401.789255621257],
      [1695895249545, 26410.42031655413],
      [1695898905569, 26552.149600179502],
      [1695902444917, 26440.35665180219],
      [1695906007648, 26474.326682102797],
      [1695909668621, 26521.080917311945],
      [1695913219912, 26843.000470393086],
      [1695916892726, 26947.840712493125],
      [1695920523289, 27047.201440878565],
      [1695924079824, 27146.515346023432],
      [1695927679175, 26932.85341711542],
      [1695931224463, 27113.030008432663],
      [1695934860956, 27046.149439941382],
      [1695938477716, 26999.71044691884],
      [1695942004837, 27013.05810967051],
      [1695945680668, 27009.01375072488],
      [1695949234445, 27062.49453345404],
      [1695952804028, 27054.71348399084],
      [1695956457809, 26915.54662871539],
      [1695960047602, 26952.410825697847],
      [1695963616290, 26962.12884472754],
      [1695967274253, 26976.21406401507],
      [1695970848452, 27054.674939493554],
      [1695974509105, 27151.16450461917],
      [1695978108793, 26996.371988088595],
      [1695981663917, 27038.187748639983],
      [1695985277368, 27049.592550181787],
      [1695988861584, 26986.582227100895],
      [1695992492790, 26987.886178766308],
      [1695996075869, 26906.477737368154],
      [1695999605113, 26953.220014696042],
      [1696003229780, 26849.05395770183],
      [1696006862930, 26868.732495578864],
      [1696010500195, 26836.0656620818],
      [1696014011138, 26889.316603323634],
      [1696017651019, 26952.94130429872],
      [1696021260829, 26896.868208952477],
      [1696024842530, 26883.6723200753],
      [1696028443941, 26896.650032793077],
      [1696032021706, 26917.199101637976],
      [1696035603969, 26941.22636123318],
      [1696039220353, 26895.989846752356],
      [1696042850105, 26900.63872876152],
      [1696046423490, 26912.934634650363],
      [1696050071338, 26936.480668394885],
      [1696053685241, 26932.993157566954],
      [1696057292882, 26930.693192584335],
      [1696060829818, 26930.393489942126],
      [1696064465278, 26933.011615279058],
      [1696068072686, 26951.281293107586],
      [1696071642668, 26977.088380678837],
      [1696075262175, 26951.018963545335],
      [1696078870153, 26925.963442994766],
      [1696082406404, 26954.910319879204],
      [1696086068075, 27000.023578067856],
      [1696089639083, 26992.512243659046],
      [1696093226395, 27041.311228303777],
      [1696096873260, 27022.477185112835],
      [1696100430508, 27000.04419572114],
      [1696104057999, 27024.703138645218],
      [1696107675248, 27075.965613822682],
      [1696111229350, 27018.02097305404],
      [1696114867486, 27007.09435594733],
      [1696118412787, 26969.876144072576],
      [1696122055648, 26985.184892254794],
      [1696125606963, 27032.99735394441],
      [1696129259802, 27025.892065326865],
      [1696132846597, 27054.63584370287],
      [1696136406046, 27050.357150900814],
      [1696140021032, 27075.14713664131],
      [1696143637837, 27122.212736412184],
      [1696147247021, 27109.991721883533],
      [1696150822576, 27148.48537316538],
      [1696154470008, 27213.65995669072],
      [1696158034315, 27192.90016950977],
      [1696161677515, 27191.282254614976],
      [1696165259839, 27193.14353365275],
      [1696168857312, 27189.32979717231],
      [1696172448798, 27114.132636497096],
      [1696176063103, 27145.365903199057],
      [1696179720064, 27110.71608677514],
      [1696183232460, 27076.567486209256],
      [1696186875227, 27097.773010963676],
      [1696190439412, 27101.52779375529],
      [1696194068323, 27105.926234639555],
      [1696197609820, 27148.257510349395],
      [1696201283550, 27958.086080312773],
      [1696204845057, 27967.510579087113],
      [1696208408007, 27902.79035419223],
      [1696212031053, 27916.599138511272],
      [1696215624962, 27996.40252622468],
      [1696219242253, 28067.477263050456],
      [1696222822959, 28067.838583368306],
      [1696226400313, 27962.989233312983],
      [1696230066163, 28070.284108617798],
      [1696233654512, 28300.12576240112],
      [1696237246967, 28286.560919931067],
      [1696240220000, 28301.572097802455]],
     'market_caps': [[1693648825935, 502579179117.9201],
      [1693652461970, 503341148553.4565],
      [1693656041070, 502512697616.5377],
      [1693659628425, 502487788765.3436],
      [1693663268552, 502929627240.27264],
      [1693666887711, 504204857862.46967],
      [1693670446590, 504230576255.5037],
      [1693674063262, 503606399901.63696],
      [1693677661040, 503195058204.3451],
      [1693681242294, 502400098952.2769],
      [1693684856557, 503104251457.41406],
      [1693688444033, 503103744352.01855],
      [1693692062997, 503662623471.4392],
      [1693695693194, 503597599803.75604],
      [1693699264592, 503679892454.50775],
      [1693702856775, 503377885241.9916],
      [1693706414406, 503444046707.0499],
      [1693710055340, 503721494032.22504],
      [1693713643481, 503495163894.21735],
      [1693717226739, 503832127416.5992],
      [1693720809648, 504277768823.265],
      [1693724415495, 504760426294.62823],
      [1693728031671, 505001727243.42847],
      [1693731654964, 504242754568.02264],
      [1693735257631, 504440615271.891],
      [1693738865847, 504711480029.79926],
      [1693742429194, 505106359568.31494],
      [1693746055433, 507142131897.6528],
      [1693749647341, 504990370461.57416],
      [1693753256166, 504986627550.3454],
      [1693756845741, 504050655388.57513],
      [1693760456695, 503368665883.82825],
      [1693764051895, 503778751319.9852],
      [1693767654694, 505617320630.8237],
      [1693771295201, 506025076855.21814],
      [1693774851023, 506351353431.9607],
      [1693778465432, 505823173361.6407],
      [1693782045508, 505357944267.65015],
      [1693785623272, 505513039060.68445],
      [1693789250453, 505020329822.60657],
      [1693792876822, 504145364765.6368],
      [1693796473263, 505229421117.1735],
      [1693800071129, 506457637470.45184],
      [1693803662428, 506022373818.57733],
      [1693807257341, 505352043737.68945],
      [1693810849866, 505925368865.8924],
      [1693814443906, 505992904123.8837],
      [1693818031244, 505908940151.49524],
      [1693821651204, 505319104067.88],
      [1693825255694, 504124365485.53986],
      [1693828836482, 504392794148.4693],
      [1693832422257, 503282016690.10095],
      [1693836057860, 504238616065.3563],
      [1693839648954, 503837584909.8466],
      [1693843238926, 503278577762.6366],
      [1693846816760, 503290945039.8424],
      [1693850437784, 504020064281.80115],
      [1693854039635, 504608930460.3286],
      [1693857643941, 504398042792.2731],
      [1693861241813, 502713757963.0427],
      [1693864869559, 501244515403.9127],
      [1693868423076, 501736285981.04266],
      [1693872058364, 502409490053.88367],
      [1693875645622, 501250208354.44934],
      [1693879264941, 502089734798.557],
      [1693882850852, 500548501916.9358],
      [1693886442529, 499756744260.59155],
      [1693890068698, 500398121020.16],
      [1693893646500, 500767986322.77167],
      [1693897264682, 500326320548.8864],
      [1693900805601, 501016339319.3472],
      [1693904439022, 499582401107.4365],
      [1693908062473, 501266600208.02045],
      [1693911637129, 501839677241.1962],
      [1693915250322, 501569626431.9173],
      [1693918902721, 502587817041.46735],
      [1693922444219, 501487383099.38086],
      [1693926063141, 499965290945.08905],
      [1693929674270, 501920372363.3323],
      [1693933260798, 502591784102.655],
      [1693936842325, 501669198810.3129],
      [1693940423070, 501143279493.7992],
      [1693944060332, 500845831967.5807],
      [1693947640079, 500527910704.0735],
      [1693951220545, 501238935583.5594],
      [1693954807133, 501476065016.1335],
      [1693958429024, 501979376928.41833],
      [1693962054506, 502043532379.00397],
      [1693965664508, 501997692065.754],
      [1693969255513, 502587443036.3141],
      [1693972824000, 501867996133.2855],
      [1693976401207, 501526024041.821],
      [1693980063358, 501053943695.1513],
      [1693983636159, 501502797511.3941],
      [1693987210109, 501713569526.1038],
      [1693990868239, 501329774179.8214],
      [1693994441403, 501347578257.1722],
      [1693998065048, 500866986196.3277],
      [1694001675599, 501016833679.50586],
      [1694005248608, 500552830751.88965],
      [1694008849196, 500536046366.6948],
      [1694012461622, 498431521376.0827],
      [1694016062320, 498838179321.9639],
      [1694019623530, 498301814935.57996],
      [1694023206891, 499755674616.70074],
      [1694026820854, 500135896959.35693],
      [1694030453203, 500012959633.6669],
      [1694034058637, 500628008558.2111],
      [1694037632696, 501586680608.5082],
      [1694041222274, 501193682218.13556],
      [1694044839359, 501615002105.18665],
      [1694048445693, 501231202302.67487],
      [1694052059253, 501502100839.931],
      [1694055610946, 501471416184.0116],
      [1694059259063, 502502761235.7289],
      [1694062855457, 502134128453.8748],
      [1694066468460, 502106609601.3991],
      [1694070050167, 501691786567.00793],
      [1694073671954, 501507625010.4589],
      [1694077288878, 501289497920.19086],
      [1694080821617, 501486606976.2224],
      [1694084404682, 500783172037.1498],
      [1694088057834, 500542705946.70135],
      [1694091614579, 500105415824.8448],
      [1694095318077, 500862843994.9708],
      [1694098854239, 501051117928.31146],
      [1694102444392, 501797929544.1122],
      [1694106080694, 504292059352.1702],
      [1694109676460, 504899042280.2431],
      [1694113252773, 503936227111.01196],
      [1694116865174, 503791695894.534],
      [1694120463878, 505085827980.69366],
      [1694124050166, 511109329262.21924],
      [1694127637765, 514314601248.5639],
      [1694131272591, 509837705629.17126],
      [1694134885236, 512535615302.4637],
      [1694138447569, 511532091174.0121],
      [1694142046787, 510433915633.93036],
      [1694145615869, 511522393693.26416],
      [1694149200956, 513444776501.7761],
      [1694152973752, 512248135299.4455],
      [1694156430831, 510624928068.21796],
      [1694160066144, 511022802374.12067],
      [1694163667034, 509978681728.89075],
      [1694167236127, 508311333651.81964],
      [1694170880330, 503112004264.0525],
      [1694174470818, 503151505053.1611],
      [1694178069428, 503454798166.20703],
      [1694181685773, 504289979965.4948],
      [1694185205197, 504052103044.6234],
      [1694188849164, 503388814516.2278],
      [1694192416778, 502039368091.1103],
      [1694196073509, 503007460847.8047],
      [1694199665513, 502201470166.6554],
      [1694203254994, 503576909975.8793],
      [1694206871509, 504251769429.3859],
      [1694210404044, 504272369527.896],
      [1694214009931, 504631042773.5634],
      [1694217602458, 504533063388.2184],
      [1694221201462, 503916223086.9722],
      [1694224814902, 504229971925.16693],
      [1694228410066, 504203620364.91187],
      [1694232046089, 503788589917.45154],
      [1694235665094, 503813623089.6166],
      [1694239275528, 503772573683.86084],
      [1694242916309, 503951496195.9437],
      [1694246453300, 503928056760.4959],
      [1694250099946, 504174894797.5232],
      [1694253707248, 504169559890.61646],
      [1694257206615, 503758906908.4444],
      [1694260857596, 503712687384.4723],
      [1694264482646, 503638412458.9224],
      [1694268085624, 502804253606.7894],
      [1694271604957, 503292537865.46814],
      [1694275279558, 504244522250.02563],
      [1694278803871, 504108787882.9613],
      [1694282411865, 504041418150.31494],
      [1694286070426, 503242441361.89655],
      [1694289657928, 503724286986.5162],
      [1694293288738, 503870040068.07153],
      [1694296874825, 503874485049.3279],
      [1694300470680, 504568753073.31885],
      [1694304065905, 504373920218.6837],
      [1694307668612, 503765412166.61633],
      [1694311254157, 503320115407.1701],
      [1694314848468, 503351699766.16174],
      [1694318454068, 503901338888.7927],
      [1694322031236, 502576494754.3946],
      [1694325639171, 503577121351.16974],
      [1694329274243, 503707257798.65814],
      [1694332884463, 503555780158.7291],
      [1694336458732, 503670372298.4291],
      [1694340095012, 503416571652.97516],
      [1694343661201, 502703531104.52954],
      [1694347208077, 502829971242.424],
      [1694350853257, 502670758730.89343],
      [1694354477774, 502906520094.62244],
      [1694358088575, 502088579468.8057],
      [1694361673154, 502203554480.4777],
      [1694365324308, 502097921450.6704],
      [1694368870234, 500970390412.49194],
      [1694372469890, 501056789984.30914],
      [1694376014473, 501636799975.2941],
      [1694379600938, 502455002667.7505],
      [1694383277662, 504118056077.136],
      [1694386858130, 503835241140.5136],
      [1694390437028, 503489661583.33154],
      [1694394035700, 500382350797.03015],
      [1694397658557, 500450291215.4285],
      [1694401291166, 501215604637.72595],
      [1694404887035, 501411720056.0245],
      [1694408418510, 501777860295.0455],
      [1694412055734, 503261842661.50977],
      [1694415609754, 503505505813.6174],
      [1694419255394, 502667797804.47076],
      [1694422810174, 502106565252.9482],
      [1694426428782, 500862106370.9184],
      [1694430037101, 500105308082.69275],
      [1694433682517, 498947547122.2066],
      [1694437265312, 500007919071.3677],
      [1694440832538, 499179824363.76715],
      [1694444445412, 488240704901.0922],
      [1694448071877, 488994305672.36224],
      [1694451620503, 490705166140.5106],
      [1694455266692, 490848656210.1281],
      [1694458843230, 490648315731.7693],
      [1694462466940, 488498825918.9866],
      [1694466078755, 488770903519.582],
      [1694469680181, 489798642989.7171],
      [1694473314943, 489799024593.0164],
      [1694476881529, 489502952545.6269],
      [1694480488595, 491249388947.5619],
      [1694484085000, 489721729936.9592],
      [1694487615337, 490929659225.1481],
      [1694491211052, 501646846279.359],
      [1694494814434, 502881721744.68756],
      [1694498455321, 500808981622.8325],
      [1694502056337, 501573424070.4291],
      [1694505629082, 503329460516.19495],
      [1694509216115, 502632678801.51715],
      [1694512819366, 503040220317.95233],
      [1694516412777, 508260176889.7347],
      [1694520016345, 507643619175.8537],
      [1694523637652, 509494552517.31244],
      [1694527268583, 509950870271.4329],
      [1694530832034, 509070866695.5991],
      [1694534432648, 510077867404.1148],
      [1694538053480, 510193484993.2457],
      [1694541654586, 506570920080.5769],
      [1694545223687, 505424331341.97174],
      [1694548806012, 508509584373.83746],
      [1694552450229, 508625133509.0337],
      [1694556027555, 508310816720.5392],
      [1694559629043, 506471102706.2827],
      [1694563222193, 503997883573.3815],
      [1694566917493, 505215402448.0438],
      [1694570443707, 505375230032.61304],
      [1694574083085, 505218076435.79645],
      [1694577659479, 503537213344.50507],
      [1694581211111, 505200115283.43164],
      [1694584869861, 504415328366.0683],
      [1694588418238, 505063612724.7306],
      [1694592032997, 505378605763.34595],
      [1694595683764, 505788429145.5746],
      [1694599247209, 507851259200.27893],
      [1694602811820, 508515807200.4454],
      [1694606490503, 510326376931.0922],
      [1694610002904, 509874076323.02106],
      [1694613673373, 509721221219.2509],
      [1694617304732, 511356511583.7483],
      [1694620832071, 512779457668.95154],
      [1694624426856, 512875848103.7654],
      [1694628079714, 508852395015.97595],
      [1694631677462, 509382995680.8944],
      [1694635306550, 510365724498.1325],
      [1694638801518, 510941577771.8207],
      [1694642483410, 510973238599.2329],
      [1694646050908, 511385152916.1684],
      [1694649714172, 510909474484.6564],
      [1694653240839, 513230314967.3668],
      [1694656855482, 510840116822.3648],
      [1694660438250, 511535803462.5974],
      [1694664048538, 511555970730.3581],
      [1694667652385, 510640794978.81964],
      [1694671276245, 510371595967.1688],
      [1694674947752, 511779131955.8247],
      [1694678468407, 513821120154.10565],
      [1694682079168, 512464031982.5285],
      [1694685665455, 512025007057.53076],
      [1694689208120, 512400265145.4616],
      [1694692859624, 514504872906.0072],
      [1694696465988, 515224728320.13245],
      [1694700021827, 518803535284.97473],
      [1694703625869, 519654609253.2881],
      [1694707248924, 519683146010.0381],
      [1694710862560, 518794003072.1255],
      [1694714450259, 518671919490.56476],
      [1694718047119, 519541997361.8057],
      [1694721647323, 519067997264.95856],
      [1694725278466, 517816753223.0695],
      [1694728875769, 516819187997.5457],
      [1694732426804, 518701216124.6949],
      [1694736055931, 516823786025.9003],
      [1694739617783, 517135132844.06213],
      [1694743262223, 516341189795.0515],
      [1694746878614, 518299315056.4144],
      [1694750471019, 518124298614.093],
      [1694754083159, 518965066482.01465],
      [1694757677069, 517930418598.37836],
      [1694761234709, 517892494834.1798],
      [1694764895297, 517978432918.1591],
      [1694768402473, 518577161530.4716],
      [1694772011129, 519301274151.4014],
      [1694775652180, 518585410152.73254],
      [1694779251994, 516256511358.13983],
      [1694782856479, 514055321079.9946],
      [1694786454986, 515303958520.1987],
      [1694790009818, 511060269947.8009],
      [1694793674696, 512897494322.3482],
      [1694797225889, 513288979849.40485],
      [1694800870359, 513933932329.99475],
      [1694804444403, 513913951846.7042],
      [1694808002218, 515283178524.17676],
      [1694811666558, 514933905314.5405],
      [1694815273478, 515872872853.6868],
      [1694818857488, 520592614483.7675],
      [1694822447711, 518872387637.1001],
      [1694826058107, 519017768466.9043],
      [1694829649148, 518541882396.8819],
      [1694833267018, 520455488884.3008],
      [1694836881872, 519263235765.2543],
      [1694840419759, 518630016145.4591],
      [1694844070098, 517133969043.80493],
      [1694847657005, 516050570311.63885],
      [1694851245430, 516394108557.4625],
      [1694854846001, 517269066463.65045],
      [1694858459103, 517708544576.97296],
      [1694862049970, 517098860840.31177],
      [1694865653784, 517377322988.2751],
      [1694869207617, 517758972591.95624],
      [1694872851812, 517254524374.18695],
      [1694876467404, 516844718987.0747],
      [1694880082717, 517074444441.4126],
      [1694883666750, 516907852187.23584],
      [1694887250607, 518013430964.2811],
      [1694890880239, 517913787538.2392],
      [1694894445223, 517030026164.97925],
      [1694898088889, 517311095176.19495],
      [1694901629896, 517884688427.03705],
      [1694905264280, 517711860672.01575],
      [1694908851309, 517396850180.9239],
      [1694912461893, 516643062694.42126],
      [1694916072780, 516743739215.2012],
      [1694919623616, 516911096110.4354],
      [1694923210574, 517053454182.8843],
      [1694926855732, 517348821157.3166],
      [1694930432647, 517257415401.24365],
      [1694934086167, 516973649278.4185],
      [1694937668691, 516829561096.4846],
      [1694941259399, 517409994750.14954],
      [1694944860269, 517512673683.55554],
      [1694948477497, 518602721899.40594],
      [1694952052810, 518367660313.9575],
      [1694955601392, 517929315636.9974],
      [1694959303815, 517683475768.307],
      [1694962875743, 517813931548.5727],
      [1694966411022, 517709289435.713],
      [1694970051327, 516877767160.8985],
      [1694973608434, 516752279544.8416],
      [1694977260752, 516910454569.50366],
      [1694980861168, 516741080348.4729],
      [1694984434885, 515842325591.2089],
      [1694988004732, 516312759677.1746],
      [1694991655674, 515708301680.8511],
      [1694995200732, 516614128895.5437],
      [1694998838971, 516464349721.90045],
      [1695002474748, 515954727480.0278],
      [1695006069155, 519244106420.06964],
      [1695009670759, 519590961042.6792],
      [1695013226979, 518084266249.55334],
      [1695016872385, 519896374704.04175],
      [1695020449169, 520096102303.4053],
      [1695024061307, 520372864727.02966],
      [1695027671042, 520107460145.60254],
      [1695031239845, 523816164218.5993],
      [1695034829890, 527841623650.4828],
      [1695038451785, 529331274907.7905],
      [1695042087909, 533375628820.57416],
      [1695045655879, 530974261731.888],
      [1695049250228, 530733730117.95465],
      [1695052877062, 532274577259.7365],
      [1695056415522, 531436080190.43555],
      [1695060004008, 522265297646.1777],
      [1695063650349, 520876340191.7074],
      [1695067252745, 524560178239.93176],
      [1695070886761, 521873827829.6718],
      [1695074401030, 522300230513.10596],
      [1695078053710, 523063268099.8967],
      [1695081698935, 521346975856.46625],
      [1695085269505, 520274744206.75854],
      [1695088877096, 520573816569.33875],
      [1695092408017, 521817402923.59045],
      [1695096076629, 522766784009.74],
      [1695099622098, 523140539435.4059],
      [1695103223115, 523041322259.4171],
      [1695106815064, 522810473575.2714],
      [1695110419806, 523400800839.9677],
      [1695114036701, 525633591848.4466],
      [1695117679832, 531751713447.04663],
      [1695121282809, 529725134461.21173],
      [1695124810966, 529708218132.6283],
      [1695128447573, 528187184853.49695],
      [1695132043410, 529864493407.65906],
      [1695135668460, 528793077357.69653],
      [1695139222823, 531823259393.3038],
      [1695142837205, 532446077881.8178],
      [1695146444033, 530341274254.4169],
      [1695150056393, 528598222004.87756],
      [1695153601055, 529738173738.30096],
      [1695157228217, 530204547744.5222],
      [1695160848717, 528500075650.3101],
      [1695164400975, 530020284479.0638],
      [1695168064203, 530357673731.022],
      [1695171663284, 529382494023.8467],
      [1695175208607, 532071155383.40173],
      [1695178854556, 530159771094.1654],
      [1695182400876, 528356803461.3616],
      [1695186050046, 528901983670.791],
      [1695189676784, 528168949783.83],
      [1695193275641, 526934558962.18445],
      [1695196835448, 528723899780.59656],
      [1695200476704, 529431391974.07446],
      [1695204005800, 526384409342.9135],
      [1695207671348, 527108662754.0009],
      [1695211261367, 528400709659.95776],
      [1695214890479, 527405693669.9619],
      [1695218470716, 529137727284.5486],
      [1695222115762, 528761527903.26056],
      [1695225610681, 530193856147.92334],
      [1695229202276, 529748184012.1564],
      [1695232880415, 530156349384.3579],
      [1695236420122, 529550685776.9631],
      [1695240011084, 524350466316.0012],
      [1695243619413, 526882533538.7348],
      [1695247277558, 529140468404.47943],
      [1695250880706, 528527632681.94586],
      [1695254488050, 529168513966.1614],
      [1695258011493, 528884162859.6201],
      [1695261647004, 526737205874.4239],
      [1695265214100, 525518254940.58765],
      [1695268851479, 526541571477.4285],
      [1695272464248, 528095092156.78986],
      [1695276070457, 527762938102.62427],
      [1695279692762, 527474770651.21063],
      [1695283216498, 526130006006.046],
      [1695286832893, 526119353050.058],
      [1695290462370, 521230363948.64435],
      [1695294082215, 521845950927.9182],
      [1695297604793, 521250703845.5218],
      [1695301217597, 519685468270.97815],
      [1695304846808, 515436605147.5356],
      [1695308416465, 517642706525.2206],
      [1695312076058, 518908725105.44763],
      [1695315655980, 517796879505.2227],
      [1695319259336, 520070200484.0021],
      [1695322849394, 518654907540.2907],
      [1695326443371, 518241616544.5989],
      [1695330048069, 518250344946.26465],
      [1695333658482, 518077777553.20544],
      [1695337245237, 517970775017.6623],
      [1695340876770, 517743774814.63885],
      [1695344424140, 518467626287.699],
      [1695348042198, 518917997063.6134],
      [1695351600787, 517973464321.92334],
      [1695355253016, 518674080516.97876],
      [1695358844050, 519127969021.1476],
      [1695362405337, 519396311563.56696],
      [1695366023000, 518770792039.8923],
      [1695369602489, 518919226825.63025],
      [1695373249394, 520006738584.81494],
      [1695376900161, 519294963026.1704],
      [1695380406103, 518535149616.62756],
      [1695384006363, 519285166620.04407],
      [1695387614279, 518702794950.5156],
      [1695391205061, 518639253682.1302],
      [1695394816160, 518995436027.29456],
      [1695398451954, 519599052207.8553],
      [1695402045900, 518157542795.7728],
      [1695405610328, 517639119289.5904],
      [1695409231493, 518303579024.40015],
      [1695412867797, 517870712424.7748],
      [1695416418610, 517153233080.20715],
      [1695420023207, 517912919651.92694],
      [1695423661624, 517686318162.83673],
      [1695427201859, 518383856096.9625],
      [1695430811253, 518421206610.939],
      [1695434410132, 518246440115.6359],
      [1695438058561, 517534717257.2091],
      [1695441644699, 517396761491.0555],
      [1695445206991, 517413817523.99506],
      [1695448808438, 517663136649.1888],
      [1695452439871, 517880989162.4385],
      [1695456047770, 518006737715.4832],
      [1695459608638, 517620468057.0765],
      [1695463260402, 517858287617.96375],
      [1695466827539, 518083995806.5057],
      [1695470450048, 517785563898.58563],
      [1695474006333, 517871996721.43195],
      [1695477700146, 517958425498.95636],
      [1695481252606, 517855982848.45856],
      [1695484847029, 517827313935.5402],
      [1695488466338, 518129432621.6174],
      [1695492053864, 518520561376.7401],
      [1695495631342, 518894168640.6951],
      [1695499252245, 518753289666.85693],
      [1695502872078, 518408171281.398],
      [1695506415356, 518056286268.49457],
      [1695510062533, 518093474759.7309],
      [1695513663505, 517968304453.25476],
      [1695517264824, 517923896601.62683],
      [1695520850765, 518307609081.58057],
      [1695524458287, 518315861964.0958],
      [1695528008432, 518196376389.9803],
      [1695531644700, 517958418307.2268],
      [1695535260830, 517755862498.1467],
      [1695538817963, 517685135918.39374],
      [1695542471024, 517759151770.9794],
      [1695546077698, 518147386739.9435],
      [1695549622074, 518252724318.21643],
      [1695553252441, 518087093176.7439],
      [1695556868895, 518473612675.03864],
      [1695560410462, 518734376516.9064],
      [1695564035623, 518556184604.4651],
      [1695567604844, 518393876090.05096],
      [1695571264473, 518009965184.26013],
      [1695574805796, 518061708503.47394],
      [1695578469402, 519057859179.4374],
      [1695582049432, 519003560693.3459],
      [1695585670396, 516425768414.5461],
      [1695589238846, 516046775834.19727],
      [1695592873976, 516991510315.686],
      [1695596405135, 516580406882.4642],
      [1695600051058, 511901270302.64154],
      [1695603623800, 509697698936.6358],
      [1695607258182, 511102142210.76984],
      [1695610877802, 510236387551.28986],
      [1695614475167, 509812643040.24066],
      [1695618025607, 509311454736.32605],
      [1695621634966, 508616309554.5954],
      [1695625259023, 509888833172.1865],
      [1695628866670, 510305366581.61176],
      [1695632422994, 508949950799.125],
      [1695636109197, 508629277395.3451],
      [1695639662839, 508791998040.7593],
      [1695643263383, 507883089808.29456],
      [1695646801447, 508567683211.64703],
      [1695650400482, 509022986598.5187],
      [1695654024293, 509582204948.09686],
      [1695657604804, 512339630329.8273],
      [1695661204413, 513526889604.5568],
      [1695664826153, 513317771644.9677],
      [1695668437733, 514241960419.9567],
      [1695672054179, 513187184746.58325],
      [1695675654169, 513241968140.6306],
      [1695679209652, 512105900528.08154],
      [1695682807114, 512453973478.47375],
      [1695686440433, 512103393581.80255],
      [1695690058692, 512245280170.6979],
      [1695693681785, 512109129483.7825],
      [1695697281459, 512983439684.50397],
      [1695700851398, 513849068405.87463],
      [1695704468510, 513368514842.6515],
      [1695708096777, 513351337455.1335],
      [1695711600956, 512218129724.55743],
      [1695715263432, 511694174971.7239],
      [1695718832620, 512282831692.1529],
      [1695722429980, 512403547227.0295],
      [1695726081051, 511774050844.27856],
      [1695729656720, 511374196677.8367],
      [1695733294836, 510804055248.21936],
      [1695736881037, 511677129965.6441],
      [1695740487097, 510379291290.7066],
      [1695744055159, 509114359910.4271],
      [1695747672991, 511724861092.05206],
      [1695751287665, 509884930477.0239],
      [1695754864358, 510234632271.8228],
      [1695758428680, 511761448311.23395],
      [1695762060076, 511350532486.5249],
      [1695765635786, 510478556270.1115],
      [1695769242778, 509689023740.9063],
      [1695772828684, 511054250889.6227],
      [1695776473902, 510876005318.5805],
      [1695780037371, 511569361611.32245],
      [1695783663393, 511029302074.8886],
      [1695787240532, 511933400414.8225],
      [1695790857263, 511669887688.3307],
      [1695794405022, 511423173385.72205],
      [1695798126255, 511489230105.3561],
      [1695801645086, 511374831966.77466],
      [1695805256499, 511684773301.13965],
      [1695808825366, 512767963054.52386],
      [1695812453484, 514853110548.0242],
      [1695816058049, 521167600054.65405],
      [1695819620887, 520487619957.2194],
      [1695823269425, 518961035190.95465],
      [1695826859141, 510054628313.99567],
      [1695830443438, 511868189391.7287],
      [1695834009021, 511663170048.7244],
      [1695837671798, 511404087011.9591],
      [1695841259012, 511868784339.8052],
      [1695844904485, 511575601178.818],
      [1695848463884, 511254737437.66077],
      [1695852051010, 512091310395.4643],
      [1695855613344, 512940779673.2642],
      [1695859251089, 513713645983.85016],
      [1695862855029, 515283760634.3021],
      [1695866524625, 515175840642.3786],
      [1695870120091, 514047716562.1272],
      [1695873669851, 513821704162.67346],
      [1695877278049, 515189145773.11536],
      [1695880861843, 515063401487.8462],
      [1695884435169, 515441037646.5223],
      [1695888001200, 516396649261.04974],
      [1695891657517, 514872190328.4862],
      [1695895249545, 514861295107.97174],
      [1695898905569, 517192235835.681],
      [1695902444917, 515532556179.91534],
      [1695906007648, 515752007728.80707],
      [1695909668621, 516018591874.79315],
      [1695913219912, 523472689341.5397],
      [1695916892726, 524232364377.31537],
      [1695920523289, 527370002133.7073],
      [1695924079824, 529026921454.9354],
      [1695927679175, 524593727249.23505],
      [1695931224463, 527662368189.3169],
      [1695934860956, 528218236782.92834],
      [1695938477716, 526897197972.3523],
      [1695942004837, 526639838514.58606],
      [1695945680668, 526917684460.40546],
      [1695949234445, 528687218731.4266],
      [1695952804028, 527386027165.79663],
      [1695956457809, 525249633376.1853],
      [1695960047602, 525600430990.93945],
      [1695963616290, 525815606956.37195],
      [1695967274253, 525757243531.85815],
      [1695970848452, 527250695309.6295],
      [1695974509105, 528870718892.3787],
      [1695978108793, 527846894827.58386],
      [1695981663917, 526511830668.6107],
      [1695985277368, 527736894994.9085],
      [1695988861584, 526616434728.24207],
      [1695992492790, 526573942455.65076],
      [1695996075869, 524681628114.9908],
      [1695999605113, 527709788215.9784],
      [1696003229780, 524111706711.9328],
      [1696006862930, 523173047168.95447],
      [1696010500195, 523763003097.2029],
      [1696014011138, 524212003988.97015],
      [1696017651019, 525252810042.7312],
      [1696021260829, 524600659326.321],
      [1696024842530, 524506452060.5622],
      [1696028443941, 524006143186.32153],
      [1696032021706, 524946724658.764],
      [1696035603969, 525210794363.9049],
      [1696039220353, 524799992810.5973],
      [1696042850105, 524524516148.1556],
      [1696046423490, 524560228929.1031],
      [1696050071338, 525338921335.48566],
      [1696053685241, 525299217485.24695],
      [1696057292882, 525347326239.3029],
      [1696060829818, 525315488796.70807],
      [1696064465278, 525250665440.385],
      [1696068072686, 525546782498.2934],
      [1696071642668, 526092666584.245],
      [1696075262175, 525548870160.97064],
      [1696078870153, 525265760399.10254],
      [1696082406404, 525234113547.7082],
      [1696086068075, 526380773532.3703],
      [1696089639083, 528140001594.2253],
      [1696093226395, 527245274350.87695],
      [1696096873260, 527020419722.2597],
      [1696100430508, 526465902226.1577],
      [1696104057999, 527000749634.21765],
      [1696107675248, 527888021510.37274],
      [1696111229350, 526578463577.28644],
      [1696114867486, 526562443896.72284],
      [1696118412787, 525936342995.4552],
      [1696122055648, 525853547725.38727],
      [1696125606963, 526826919824.3892],
      [1696129259802, 527184512946.9547],
      [1696132846597, 527150060267.636],
      [1696136406046, 527282640979.876],
      [1696140021032, 527940399236.1895],
      [1696143637837, 529062125336.11163],
      [1696147247021, 528824043805.77686],
      [1696150822576, 529431967021.275],
      [1696154470008, 530410530291.889],
      [1696158034315, 530204532658.09094],
      [1696161677515, 530213632526.95636],
      [1696165259839, 530364830072.21893],
      [1696168857312, 529998468644.9319],
      [1696172448798, 529437940850.94025],
      [1696176063103, 529200989964.35376],
      [1696179720064, 528701605996.14014],
      [1696183232460, 528325134963.34326],
      [1696186875227, 528349802840.6398],
      [1696190439412, 528528994952.36694],
      [1696194068323, 528883080504.4618],
      [1696197609820, 529421100378.23047],
      [1696201283550, 544634423350.87775],
      [1696204845057, 545302108027.2094],
      [1696208408007, 545054201667.29346],
      [1696212031053, 543939173461.23254],
      [1696215624962, 545834527122.39343],
      [1696219242253, 547149345645.58984],
      [1696222822959, 547170945845.89545],
      [1696226400313, 545881040264.0722],
      [1696230066163, 547289100871.5593],
      [1696233654512, 553460645600.3274],
      [1696237246967, 553119177711.1763],
      [1696240220000, 551931061007.054]],
     'total_volumes': [[1693648825935, 17999596699.62693],
      [1693652461970, 18036929353.5415],
      [1693656041070, 15569185025.215366],
      [1693659628425, 13566964524.63137],
      [1693663268552, 14801793107.874704],
      [1693666887711, 11963768678.563025],
      [1693670446590, 11606931981.624285],
      [1693674063262, 9425856143.72856],
      [1693677661040, 11238953696.090527],
      [1693681242294, 10379192505.256763],
      [1693684856557, 9778873549.126001],
      [1693688444033, 9140384759.803263],
      [1693692062997, 6802050061.970332],
      [1693695693194, 8620139954.533278],
      [1693699264592, 8203515572.755595],
      [1693702856775, 5709046017.090389],
      [1693706414406, 4523208395.500145],
      [1693710055340, 6732862138.290528],
      [1693713643481, 7152468943.845966],
      [1693717226739, 8068993424.957455],
      [1693720809648, 6218543217.083172],
      [1693724415495, 7804207832.396353],
      [1693728031671, 7531685627.14165],
      [1693731654964, 5072113581.554426],
      [1693735257631, 6183321576.276406],
      [1693738865847, 7709114922.332492],
      [1693742429194, 6016075149.635753],
      [1693746055433, 7809166647.756655],
      [1693749647341, 7759427307.235495],
      [1693753256166, 6720918996.095062],
      [1693756845741, 4689413209.57826],
      [1693760456695, 6590174452.511596],
      [1693764051895, 4608033085.312326],
      [1693767654694, 6533633780.788207],
      [1693771295201, 7769929765.554307],
      [1693774851023, 8248221079.246746],
      [1693778465432, 8048058805.44904],
      [1693782045508, 8436464205.892942],
      [1693785623272, 8301138495.084562],
      [1693789250453, 8634220684.763163],
      [1693792876822, 8551702243.481846],
      [1693796473263, 7663245356.1915],
      [1693800071129, 7640295968.670014],
      [1693803662428, 8138936008.514482],
      [1693807257341, 9192100058.124155],
      [1693810849866, 5894752363.800718],
      [1693814443906, 7819687856.152967],
      [1693818031244, 6665671076.842949],
      [1693821651204, 9461269768.28648],
      [1693825255694, 3907142392.432289],
      [1693828836482, 9594050022.867336],
      [1693832422257, 9096054816.303648],
      [1693836057860, 3548682372.946631],
      [1693839648954, 9028808420.814003],
      [1693843238926, 7050106308.778136],
      [1693846816760, 10186280877.761194],
      [1693850437784, 10271582855.96663],
      [1693854039635, 10101392062.585632],
      [1693857643941, 10076813352.74386],
      [1693861241813, 3828791491.324168],
      [1693864869559, 3967257001.9155297],
      [1693868423076, 10016158233.55698],
      [1693872058364, 6700578092.438599],
      [1693875645622, 10371371883.089655],
      [1693879264941, 4913196734.434478],
      [1693882850852, 6050911597.890324],
      [1693886442529, 4379484494.646262],
      [1693890068698, 7503972266.182725],
      [1693893646500, 10308899695.720997],
      [1693897264682, 9257841654.163052],
      [1693900805601, 4548820670.611074],
      [1693904439022, 10208867945.971369],
      [1693908062473, 10755053768.12739],
      [1693911637129, 8132631978.776067],
      [1693915250322, 5060850137.856208],
      [1693918902721, 8338955378.98623],
      [1693922444219, 10102002932.680157],
      [1693926063141, 9589157697.312738],
      [1693929674270, 7944969718.91985],
      [1693933260798, 11100116807.625801],
      [1693936842325, 11300353176.62318],
      [1693940423070, 6276202381.694345],
      [1693944060332, 8131231075.861078],
      [1693947640079, 11416710467.722769],
      [1693951220545, 10481647733.578993],
      [1693954807133, 4686640656.001714],
      [1693958429024, 7476000271.8774605],
      [1693962054506, 10716328223.879251],
      [1693965664508, 6506901201.524565],
      [1693969255513, 8306647771.034918],
      [1693972824000, 5395539056.321977],
      [1693976401207, 6879344661.230441],
      [1693980063358, 1724519168.2533977],
      [1693983636159, 8407455579.99431],
      [1693987210109, 10583278282.619495],
      [1693990868239, 2827214715.904758],
      [1693994441403, 4817398758.444937],
      [1693998065048, 9560120487.491705],
      [1694001675599, 6410778689.80681],
      [1694005248608, 9082220176.402552],
      [1694008849196, 9877924625.599663],
      [1694012461622, 10080448160.113983],
      [1694016062320, 3551267126.479026],
      [1694019623530, 9564371478.160484],
      [1694023206891, 8205169222.923536],
      [1694026820854, 11698426431.469112],
      [1694030453203, 12202372340.305641],
      [1694034058637, 9595112218.789145],
      [1694037632696, 11279971552.899046],
      [1694041222274, 12246384731.19008],
      [1694044839359, 12225427270.62692],
      [1694048445693, 11989060638.052563],
      [1694052059253, 11112771168.152021],
      [1694055610946, 7594899165.670312],
      [1694059259063, 11726549194.01224],
      [1694062855457, 9731914185.243385],
      [1694066468460, 11353707968.844818],
      [1694070050167, 9718380256.802496],
      [1694073671954, 7915396056.712667],
      [1694077288878, 11175839184.383566],
      [1694080821617, 8700601537.340282],
      [1694084404682, 8135002738.71468],
      [1694088057834, 2637546656.481237],
      [1694091614579, 11188955669.390213],
      [1694095318077, 7120881857.058625],
      [1694098854239, 10313736606.062737],
      [1694102444392, 9925048264.150642],
      [1694106080694, 9994156577.403366],
      [1694109676460, 8888948481.119217],
      [1694113252773, 7559918729.956034],
      [1694116865174, 2068582916.9695988],
      [1694120463878, 4392525695.334632],
      [1694124050166, 9886313017.044258],
      [1694127637765, 8257711206.525673],
      [1694131272591, 4521997781.160889],
      [1694134885236, 10966279139.57666],
      [1694138447569, 8441236314.858133],
      [1694142046787, 10930671303.784061],
      [1694145615869, 6381160962.9124365],
      [1694149200956, 11254312423.577908],
      [1694152973752, 11533443966.456295],
      [1694156430831, 10760932283.854881],
      [1694160066144, 8425228925.345015],
      [1694163667034, 10312467688.766405],
      [1694167236127, 12691099764.98161],
      [1694170880330, 11688929248.679237],
      [1694174470818, 13666744911.059225],
      [1694178069428, 13929647428.627874],
      [1694181685773, 13368276875.284317],
      [1694185205197, 12137706053.784351],
      [1694188849164, 3828127023.428758],
      [1694192416778, 13565003893.710337],
      [1694196073509, 12969629238.84605],
      [1694199665513, 13231110127.245955],
      [1694203254994, 13155494480.488028],
      [1694206871509, 9245115317.60264],
      [1694210404044, 11514030696.388136],
      [1694214009931, 2757106700.785113],
      [1694217602458, 8058794338.820984],
      [1694221201462, 5854417136.674454],
      [1694224814902, 10026793501.745895],
      [1694228410066, 9790451519.956459],
      [1694232046089, 7516481797.5809355],
      [1694235665094, 8883171214.871027],
      [1694239275528, 7400971202.9463625],
      [1694242916309, 6553996489.034366],
      [1694246453300, 8394127687.257144],
      [1694250099946, 7272434147.356123],
      [1694253707248, 4690052251.391088],
      [1694257206615, 7004610923.967108],
      [1694260857596, 6599653859.6325655],
      [1694264482646, 1133336819.368583],
      [1694268085624, 6070858911.216526],
      [1694271604957, 6253095050.742924],
      [1694275279558, 6062262145.74144],
      [1694278803871, 1603499928.7707856],
      [1694282411865, 5488793131.612562],
      [1694286070426, 5168359439.637434],
      [1694289657928, 3177717423.23699],
      [1694293288738, 5038995493.690307],
      [1694296874825, 4994959513.072227],
      [1694300470680, 4818223818.202241],
      [1694304065905, 1019886354.8130162],
      [1694307668612, 1594152732.5992355],
      [1694311254157, 1938257418.6498153],
      [1694314848468, 4612293929.592334],
      [1694318454068, 4652437330.861648],
      [1694322031236, 5089110810.925258],
      [1694325639171, 3992499832.3184547],
      [1694329274243, 1370550403.7027209],
      [1694332884463, 5155453657.6785755],
      [1694336458732, 4997657668.212445],
      [1694340095012, 3563272961.711569],
      [1694343661201, 1336843161.4092455],
      [1694347208077, 4646119140.875745],
      [1694350853257, 4890684705.861856],
      [1694354477774, 5238525550.859714],
      [1694358088575, 4390306485.027055],
      [1694361673154, 5047717328.473979],
      [1694365324308, 5438046905.686763],
      [1694368870234, 5565862879.204172],
      [1694372469890, 5309299800.655152],
      [1694376014473, 2339828845.431535],
      [1694379600938, 5907315756.34418],
      [1694383277662, 5238087612.284501],
      [1694386858130, 2805396666.0998135],
      [1694390437028, 3169137373.84707],
      [1694394035700, 6987388927.72378],
      [1694397658557, 6258794066.439361],
      [1694401291166, 7751144680.989789],
      [1694404887035, 6193789008.66829],
      [1694408418510, 5332486826.550982],
      [1694412055734, 7358837142.266371],
      [1694415609754, 7896413338.1552],
      [1694419255394, 5375266744.570264],
      [1694422810174, 8278426934.131566],
      [1694426428782, 5440874099.558438],
      [1694430037101, 8286957247.486201],
      [1694433682517, 7627745379.384425],
      [1694437265312, 8637033531.398705],
      [1694440832538, 9397020140.725554],
      [1694444445412, 12427551655.122347],
      [1694448071877, 12588818817.023735],
      [1694451620503, 14237541423.534958],
      [1694455266692, 9698037263.040297],
      [1694458843230, 14589876816.1937],
      [1694462466940, 14918818167.515375],
      [1694466078755, 14387990020.261229],
      [1694469680181, 14450781665.658007],
      [1694473314943, 13682107675.205944],
      [1694476881529, 14859931201.000029],
      [1694480488595, 12303411585.813065],
      [1694484085000, 14194809418.121923],
      [1694487615337, 13757380386.264528],
      [1694491211052, 16438826372.515469],
      [1694494814434, 16731933792.789036],
      [1694498455321, 17779716174.247826],
      [1694502056337, 17707457160.99888],
      [1694505629082, 18396696866.531246],
      [1694509216115, 19274783955.04422],
      [1694512819366, 18618402951.713673],
      [1694516412777, 11603495708.974995],
      [1694520016345, 19946235425.601334],
      [1694523637652, 19202231767.72024],
      [1694527268583, 21395397447.156956],
      [1694530832034, 19586906113.65775],
      [1694534432648, 18583240953.70617],
      [1694538053480, 7002529420.789264],
      [1694541654586, 15103608056.365028],
      [1694545223687, 18134918076.444],
      [1694548806012, 17202158657.40209],
      [1694552450229, 5166397325.462673],
      [1694556027555, 14374541969.900845],
      [1694559629043, 17019167676.789413],
      [1694563222193, 19485145066.69009],
      [1694566917493, 19627608896.672314],
      [1694570443707, 18621701536.819473],
      [1694574083085, 18762279403.003445],
      [1694577659479, 6014563572.83937],
      [1694581211111, 8915572975.414005],
      [1694584869861, 16551067178.48159],
      [1694588418238, 15426763791.44882],
      [1694592032997, 12245285757.24396],
      [1694595683764, 15607364223.156929],
      [1694599247209, 16662298382.871565],
      [1694602811820, 15158264256.195131],
      [1694606490503, 15079253712.326483],
      [1694610002904, 14548412825.9654],
      [1694613673373, 14774908514.812815],
      [1694617304732, 14912469058.416998],
      [1694620832071, 14435158733.5259],
      [1694624426856, 6174211101.893369],
      [1694628079714, 14145474935.43793],
      [1694631677462, 11545294785.02367],
      [1694635306550, 13191514954.240192],
      [1694638801518, 13090413149.673544],
      [1694642483410, 3139878925.5528355],
      [1694646050908, 13390190126.88951],
      [1694649714172, 12145164489.429409],
      [1694653240839, 13508723213.85249],
      [1694656855482, 12600328650.306744],
      [1694660438250, 13544389804.229006],
      [1694664048538, 13113768870.565329],
      [1694667652385, 13109986136.505507],
      [1694671276245, 14265138450.610128],
      [1694674947752, 10789263550.12771],
      [1694678468407, 9445894226.583334],
      [1694682079168, 12310789852.016779],
      [1694685665455, 13042200909.971779],
      [1694689208120, 6944182975.898711],
      [1694692859624, 11941253860.587307],
      [1694696465988, 13035073782.063635],
      [1694700021827, 14205331675.311789],
      [1694703625869, 14350777906.184343],
      [1694707248924, 13897346996.734116],
      [1694710862560, 13613915749.685959],
      [1694714450259, 11791747890.352577],
      [1694718047119, 13995216258.92639],
      [1694721647323, 13987201205.189577],
      [1694725278466, 13581817877.11256],
      [1694728875769, 14183680134.757864],
      [1694732426804, 11392002619.655975],
      [1694736055931, 11739428177.432598],
      [1694739617783, 13517470688.559185],
      [1694743262223, 13007098533.92242],
      [1694746878614, 11293648089.5484],
      [1694750471019, 9561942143.875858],
      [1694754083159, 12117195713.496675],
      [1694757677069, 9859973130.187609],
      [1694761234709, 1368658057.6182826],
      [1694764895297, 12557742803.05702],
      [1694768402473, 11297179260.301949],
      [1694772011129, 7317316173.3381405],
      [1694775652180, 12885379344.405945],
      [1694779251994, 13013866541.680634],
      [1694782856479, 10536080618.72334],
      [1694786454986, 11689579091.233318],
      [1694790009818, 11397737808.373667],
      [1694793674696, 9002330662.383602],
      [1694797225889, 9696382210.856112],
      [1694800870359, 10299684772.384293],
      [1694804444403, 9073837507.101936],
      [1694808002218, 8649053472.540415],
      [1694811666558, 10128513278.84248],
      [1694815273478, 9544702961.774385],
      [1694818857488, 10646027593.810602],
      [1694822447711, 10434050753.611362],
      [1694826058107, 11290179962.398958],
      [1694829649148, 9704781657.673136],
      [1694833267018, 11403147786.798702],
      [1694836881872, 6159607018.695468],
      [1694840419759, 11283069087.815838],
      [1694844070098, 7587474686.4588995],
      [1694847657005, 11373327054.965305],
      [1694851245430, 10771399530.279505],
      [1694854846001, 10858679681.70205],
      [1694858459103, 7603041845.195149],
      [1694862049970, 10912672313.020494],
      [1694865653784, 10468961161.595762],
      [1694869207617, 10282735965.562628],
      [1694872851812, 13062177601.202642],
      [1694876467404, 9116468535.900732],
      [1694880082717, 2075022548.6484237],
      [1694883666750, 6633922375.651478],
      [1694887250607, 8845135087.491877],
      [1694890880239, 6292224348.214037],
      [1694894445223, 8436434143.91755],
      [1694898088889, 3378842468.3725486],
      [1694901629896, 3902921078.4209633],
      [1694905264280, 1495385479.0609534],
      [1694908851309, 1224363671.9175522],
      [1694912461893, 5552723854.67091],
      [1694916072780, 6560687242.961994],
      [1694919623616, 4168928351.595582],
      [1694923210574, 5132405562.113548],
      [1694926855732, 6510977848.221746],
      [1694930432647, 2780424655.7774577],
      [1694934086167, 5674948399.72281],
      [1694937668691, 6067947232.728076],
      [1694941259399, 5725521651.229012],
      [1694944860269, 5909901288.412338],
      [1694948477497, 5728010108.421044],
      [1694952052810, 5192649157.523127],
      [1694955601392, 4183739552.100353],
      [1694959303815, 5487011138.6150255],
      [1694962875743, 611779048.3544747],
      [1694966411022, 5793120245.575601],
      [1694970051327, 4134323720.273496],
      [1694973608434, 3412362030.294274],
      [1694977260752, 4810163760.476462],
      [1694980861168, 5564571695.599791],
      [1694984434885, 5439026229.509544],
      [1694988004732, 1710036860.476786],
      [1694991655674, 4979030609.00074],
      [1694995200732, 5791146184.464804],
      [1694998838971, 5026033429.63762],
      [1695002474748, 5188480790.452037],
      [1695006069155, 4825053412.899597],
      [1695009670759, 4496383894.00738],
      [1695013226979, 7152074800.719186],
      [1695016872385, 6669078642.777902],
      [1695020449169, 7312843940.603716],
      [1695024061307, 5187711198.772847],
      [1695027671042, 7701692179.282515],
      [1695031239845, 8746377387.959333],
      [1695034829890, 9884610567.151896],
      [1695038451785, 10587534343.501535],
      [1695042087909, 11002064207.380764],
      [1695045655879, 12626747092.25609],
      [1695049250228, 13073524747.547476],
      [1695052877062, 13234835555.302473],
      [1695056415522, 1521552870.3637092],
      [1695060004008, 10515996099.30816],
      [1695063650349, 14228289479.2811],
      [1695067252745, 15280652913.598473],
      [1695070886761, 16354348330.964344],
      [1695074401030, 15967901999.094286],
      [1695078053710, 12273402557.972836],
      [1695081698935, 16477839825.058361],
      [1695085269505, 15727050061.685118],
      [1695088877096, 16370355118.670418],
      [1695092408017, 15537855482.650156],
      [1695096076629, 12694561406.153044],
      [1695099622098, 15000952674.146044],
      [1695103223115, 15946766794.6054],
      [1695106815064, 15399849861.263762],
      [1695110419806, 15623901435.211084],
      [1695114036701, 15672493922.77677],
      [1695117679832, 16361184540.617619],
      [1695121282809, 15858189012.25767],
      [1695124810966, 13722688066.127537],
      [1695128447573, 14522378759.47472],
      [1695132043410, 13283161854.895636],
      [1695135668460, 14122982294.797592],
      [1695139222823, 4479483171.696616],
      [1695142837205, 16053261870.700253],
      [1695146444033, 14476114950.143757],
      [1695150056393, 14507370073.815664],
      [1695153601055, 5232982427.739563],
      [1695157228217, 14291117126.582073],
      [1695160848717, 14438970656.608774],
      [1695164400975, 13902740848.939281],
      [1695168064203, 14244915527.20819],
      [1695171663284, 14041523937.183826],
      [1695175208607, 14088417820.58901],
      [1695178854556, 14483959222.09697],
      [1695182400876, 14059838050.939938],
      [1695186050046, 10951343336.275204],
      [1695189676784, 12530819188.351887],
      [1695193275641, 14100126958.636713],
      [1695196835448, 14397336548.074356],
      [1695200476704, 15010599295.71509],
      [1695204005800, 12360511687.613157],
      [1695207671348, 14019719462.582218],
      [1695211261367, 6176159157.513571],
      [1695214890479, 13385717704.89601],
      [1695218470716, 12985283503.577793],
      [1695222115762, 13308310340.491842],
      [1695225610681, 9822644484.014324],
      [1695229202276, 9650709134.027197],
      [1695232880415, 11662235495.936846],
      [1695236420122, 11903063055.29055],
      [1695240011084, 12987731028.144592],
      [1695243619413, 11391268263.695316],
      [1695247277558, 13391576735.527119],
      [1695250880706, 3985923660.905845],
      [1695254488050, 13497179076.831764],
      [1695258011493, 13521566207.866247],
      [1695261647004, 11179228173.795921],
      [1695265214100, 13172404915.018206],
      [1695268851479, 10612209547.470861],
      [1695272464248, 13040912523.90024],
      [1695276070457, 12618216086.495731],
      [1695279692762, 11197853874.726295],
      [1695283216498, 12508639182.409597],
      [1695286832893, 10975271895.736694],
      [1695290462370, 12249385683.08121],
      [1695294082215, 13370810287.425293],
      [1695297604793, 13487381843.75392],
      [1695301217597, 13483725709.98283],
      [1695304846808, 9839308787.663366],
      [1695308416465, 15306140958.736082],
      [1695312076058, 13831837010.800917],
      [1695315655980, 15440097725.212095],
      [1695319259336, 15765037054.411486],
      [1695322849394, 14204102844.26413],
      [1695326443371, 14096333129.061306],
      [1695330048069, 13571540399.80298],
      [1695333658482, 13402460649.73595],
      [1695337245237, 11703400464.438644],
      [1695340876770, 8169328790.751264],
      [1695344424140, 10316777311.64546],
      [1695348042198, 13532987188.388369],
      [1695351600787, 5347516704.164613],
      [1695355253016, 12660741005.799965],
      [1695358844050, 13476740338.628632],
      [1695362405337, 6873089353.018489],
      [1695366023000, 12676714252.445976],
      [1695369602489, 14081422171.051197],
      [1695373249394, 13316409999.355127],
      [1695376900161, 13114387265.2693],
      [1695380406103, 4180486722.2889504],
      [1695384006363, 12241880547.707354],
      [1695387614279, 11934958219.638449],
      [1695391205061, 7559925550.676086],
      [1695394816160, 10592439730.99477],
      [1695398451954, 7379840535.727638],
      [1695402045900, 9182860295.744059],
      [1695405610328, 9983696312.935997],
      [1695409231493, 9999601513.487804],
      [1695412867797, 8746818409.140558],
      [1695416418610, 7333121292.066996],
      [1695420023207, 9207275819.52348],
      [1695423661624, 10111016360.709791],
      [1695427201859, 9864083817.04919],
      [1695430811253, 9149910515.042269],
      [1695434410132, 9054632024.1431],
      [1695438058561, 9619384346.959093],
      [1695441644699, 7725605969.314552],
      [1695445206991, 9566480119.027641],
      [1695448808438, 9434746328.476192],
      [1695452439871, 9356128574.009384],
      [1695456047770, 9192980416.08099],
      [1695459608638, 1120033400.1710901],
      [1695463260402, 8577582216.795439],
      [1695466827539, 3939933833.4069614],
      [1695470450048, 8057709045.981392],
      [1695474006333, 8338950149.34457],
      [1695477700146, 4532282274.491941],
      [1695481252606, 4418169053.797415],
      [1695484847029, 7997135563.293454],
      [1695488466338, 7217134509.80672],
      [1695492053864, 6440059733.384334],
      [1695495631342, 6740431045.248792],
      [1695499252245, 6001538734.166156],
      [1695502872078, 6238136922.165742],
      [1695506415356, 3942217501.5584254],
      [1695510062533, 1166823352.0528607],
      [1695513663505, 6583511185.708387],
      [1695517264824, 5641132610.012867],
      [1695520850765, 5993421323.663519],
      [1695524458287, 5574820997.299333],
      [1695528008432, 6291521455.725308],
      [1695531644700, 4628923655.273057],
      [1695535260830, 5534574511.393888],
      [1695538817963, 5961975388.139025],
      [1695542471024, 5523708062.874935],
      [1695546077698, 5644335987.554123],
      [1695549622074, 4395184031.842928],
      [1695553252441, 5507495166.4189625],
      [1695556868895, 4600900880.507893],
      [1695560410462, 4940214078.947513],
      [1695564035623, 3901019709.0231404],
      [1695567604844, 5749511452.312675],
      [1695571264473, 2620058129.4177527],
      [1695574805796, 5638797486.316157],
      [1695578469402, 6009762561.174963],
      [1695582049432, 6620144568.258539],
      [1695585670396, 7272453658.762521],
      [1695589238846, 3412606497.511905],
      [1695592873976, 7223074184.882379],
      [1695596405135, 6134436371.039383],
      [1695600051058, 7885109783.762632],
      [1695603623800, 7458889246.574322],
      [1695607258182, 9370985755.590975],
      [1695610877802, 9572064256.739264],
      [1695614475167, 6975940050.845434],
      [1695618025607, 9998256656.064848],
      [1695621634966, 10189259144.679945],
      [1695625259023, 10278096381.988226],
      [1695628866670, 10674403421.71373],
      [1695632422994, 9608049609.334812],
      [1695636109197, 11133130513.652828],
      [1695639662839, 10991002325.594372],
      [1695643263383, 11560993790.784998],
      [1695646801447, 11739793450.291708],
      [1695650400482, 11306670528.995327],
      [1695654024293, 12200278742.042707],
      [1695657604804, 12724569068.4563],
      [1695661204413, 13060792133.64665],
      [1695664826153, 12186015572.17823],
      [1695668437733, 13039172947.800747],
      [1695672054179, 11304780815.911001],
      [1695675654169, 8815422529.946556],
      [1695679209652, 12641758363.25169],
      [1695682807114, 10528429877.829844],
      [1695686440433, 10752461272.464678],
      [1695690058692, 10362444992.477169],
      [1695693681785, 9556698203.166286],
      [1695697281459, 10108382622.005741],
      [1695700851398, 9726267639.686098],
      [1695704468510, 10331989826.994062],
      [1695708096777, 10399074375.871727],
      [1695711600956, 8678711156.532326],
      [1695715263432, 10244361526.717342],
      [1695718832620, 7796942363.836824],
      [1695722429980, 9433012946.384392],
      [1695726081051, 9084279464.072578],
      [1695729656720, 9426679963.358929],
      [1695733294836, 9634864753.40078],
      [1695736881037, 9821476655.04399],
      [1695740487097, 7355663377.852698],
      [1695744055159, 7887928030.510652],
      [1695747672991, 9538635761.801369],
      [1695751287665, 9249755864.805986],
      [1695754864358, 4913190794.088723],
      [1695758428680, 8401424914.456384],
      [1695762060076, 8957241190.475302],
      [1695765635786, 9572255323.227074],
      [1695769242778, 9084379076.372597],
      [1695772828684, 9786025048.05344],
      [1695776473902, 9979988712.71213],
      [1695780037371, 9902950501.634214],
      [1695783663393, 6332026882.827392],
      [1695787240532, 8522400559.467075],
      [1695790857263, 8862499394.355812],
      [1695794405022, 9695897240.973577],
      [1695798126255, 9599267831.218525],
      [1695801645086, 7552311298.65885],
      [1695805256499, 4440114027.273421],
      [1695808825366, 9814242130.264154],
      [1695812453484, 4950548078.849976],
      [1695816058049, 11952075598.147253],
      [1695819620887, 12535162527.322147],
      [1695823269425, 12671459362.443087],
      [1695826859141, 13766438474.139925],
      [1695830443438, 10735903484.068079],
      [1695834009021, 13770727641.76291],
      [1695837671798, 11579932739.72404],
      [1695841259012, 14424561406.61854],
      [1695844904485, 12309726555.116074],
      [1695848463884, 13571673617.548426],
      [1695852051010, 12011038197.821743],
      [1695855613344, 12555728398.710869],
      [1695859251089, 12889674588.31686],
      [1695862855029, 13127772801.650188],
      [1695866524625, 14461050306.047565],
      [1695870120091, 14173085651.352562],
      [1695873669851, 14121723821.532166],
      [1695877278049, 14974821933.469025],
      [1695880861843, 15149098246.220184],
      [1695884435169, 14255546926.267466],
      [1695888001200, 15558994126.45367],
      [1695891657517, 14318036982.142296],
      [1695895249545, 13870035196.557804],
      [1695898905569, 14170704055.06971],
      [1695902444917, 12885915489.830833],
      [1695906007648, 13415185789.414907],
      [1695909668621, 13308069168.012642],
      [1695913219912, 12041370436.582138],
      [1695916892726, 12900321282.764055],
      [1695920523289, 15832613785.828434],
      [1695924079824, 14932404431.7731],
      [1695927679175, 14698265403.265755],
      [1695931224463, 16680055623.258331],
      [1695934860956, 17012529929.714357],
      [1695938477716, 17064146964.742361],
      [1695942004837, 13758793545.125423],
      [1695945680668, 16683207554.844349],
      [1695949234445, 16643108849.602064],
      [1695952804028, 16245327992.307463],
      [1695956457809, 11276899533.712732],
      [1695960047602, 16457259384.14911],
      [1695963616290, 16298166306.518526],
      [1695967274253, 16382526502.971106],
      [1695970848452, 15464997641.439434],
      [1695974509105, 14954589848.67747],
      [1695978108793, 17254200564.200478],
      [1695981663917, 17238314356.704014],
      [1695985277368, 16569333514.018583],
      [1695988861584, 15358306603.424957],
      [1695992492790, 16609054278.649292],
      [1695996075869, 15962408912.088776],
      [1695999605113, 16202857669.515133],
      [1696003229780, 15573187772.50299],
      [1696006862930, 14178971404.841576],
      [1696010500195, 12013908082.489603],
      [1696014011138, 11269724885.655428],
      [1696017651019, 11293134703.70772],
      [1696021260829, 10947485214.048367],
      [1696024842530, 11902875094.593527],
      [1696028443941, 12019028501.673735],
      [1696032021706, 9059145545.41355],
      [1696035603969, 11564429934.094185],
      [1696039220353, 11486040710.310585],
      [1696042850105, 10898651536.338327],
      [1696046423490, 8914266478.256878],
      [1696050071338, 10412230030.432428],
      [1696053685241, 8385208990.980992],
      [1696057292882, 4383566249.157408],
      [1696060829818, 8303630658.66476],
      [1696064465278, 5220504535.138493],
      [1696068072686, 1430505604.7944274],
      [1696071642668, 9101813488.062887],
      [1696075262175, 8132475989.709877],
      [1696078870153, 8682295005.598862],
      [1696082406404, 8071718425.921187],
      [1696086068075, 5942532963.778078],
      [1696089639083, 7025237910.548306],
      [1696093226395, 5131610130.473297],
      [1696096873260, 5371361449.58924],
      [1696100430508, 4532398960.725572],
      [1696104057999, 6293909322.886916],
      [1696107675248, 4112055310.582381],
      [1696111229350, 6468248314.47054],
      [1696114867486, 5223288980.477179],
      [1696118412787, 6295435107.555985],
      [1696122055648, 1602718325.6349173],
      [1696125606963, 6311868096.424265],
      [1696129259802, 5971260386.075932],
      [1696132846597, 6377828544.745562],
      [1696136406046, 5981896139.629358],
      [1696140021032, 5528400440.794399],
      [1696143637837, 4253753811.9812584],
      [1696147247021, 6607319430.976781],
      [1696150822576, 1450239282.8158484],
      [1696154470008, 7016147972.456656],
      [1696158034315, 6603161782.123439],
      [1696161677515, 7079732508.246726],
      [1696165259839, 7469424071.793132],
      [1696168857312, 6164313810.375991],
      [1696172448798, 3246757634.5239677],
      [1696176063103, 4500238045.608477],
      [1696179720064, 7124391527.835778],
      [1696183232460, 6020105603.148795],
      [1696186875227, 4582273083.971355],
      [1696190439412, 7125375927.671145],
      [1696194068323, 5256794241.503529],
      [1696197609820, 2528601311.0320754],
      [1696201283550, 7725793486.794606],
      [1696204845057, 9358226524.285364],
      [1696208408007, 11588130162.151697],
      [1696212031053, 12039728579.651636],
      [1696215624962, 10966565220.646324],
      [1696219242253, 11814253733.3279],
      [1696222822959, 13395383890.977379],
      [1696226400313, 13690990931.252645],
      [1696230066163, 10332118043.623663],
      [1696233654512, 15330499296.606834],
      [1696237246967, 16542845440.786224],
      [1696240220000, 15322701413.40756]]}




```python
# getting all keys from dictionary

bitcoin_data.keys()
```




    dict_keys(['prices', 'market_caps', 'total_volumes'])




```python
# creating dataframe from 'prices' values

data = pd.DataFrame(bitcoin_data['prices'], columns=['Timestamp', 'Price'])
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Timestamp</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1693648825935</td>
      <td>25794.334275</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1693652461970</td>
      <td>25824.644083</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1693656041070</td>
      <td>25798.917344</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1693659628425</td>
      <td>25795.438234</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1693663268552</td>
      <td>25825.010207</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>716</th>
      <td>1696226400313</td>
      <td>27962.989233</td>
    </tr>
    <tr>
      <th>717</th>
      <td>1696230066163</td>
      <td>28070.284109</td>
    </tr>
    <tr>
      <th>718</th>
      <td>1696233654512</td>
      <td>28300.125762</td>
    </tr>
    <tr>
      <th>719</th>
      <td>1696237246967</td>
      <td>28286.560920</td>
    </tr>
    <tr>
      <th>720</th>
      <td>1696240220000</td>
      <td>28301.572098</td>
    </tr>
  </tbody>
</table>
<p>721 rows × 2 columns</p>
</div>




```python
# info on pandas 'to_datetime' function

help(pd.to_datetime)
```

    Help on function to_datetime in module pandas.core.tools.datetimes:
    
    to_datetime(arg: 'DatetimeScalarOrArrayConvertible', errors: 'str' = 'raise', dayfirst: 'bool' = False, yearfirst: 'bool' = False, utc: 'bool | None' = None, format: 'str | None' = None, exact: 'bool' = True, unit: 'str | None' = None, infer_datetime_format: 'bool' = False, origin='unix', cache: 'bool' = True) -> 'DatetimeIndex | Series | DatetimeScalar | NaTType | None'
        Convert argument to datetime.
        
        Parameters
        ----------
        arg : int, float, str, datetime, list, tuple, 1-d array, Series, DataFrame/dict-like
            The object to convert to a datetime.
        errors : {'ignore', 'raise', 'coerce'}, default 'raise'
            - If 'raise', then invalid parsing will raise an exception.
            - If 'coerce', then invalid parsing will be set as NaT.
            - If 'ignore', then invalid parsing will return the input.
        dayfirst : bool, default False
            Specify a date parse order if `arg` is str or its list-likes.
            If True, parses dates with the day first, eg 10/11/12 is parsed as
            2012-11-10.
            Warning: dayfirst=True is not strict, but will prefer to parse
            with day first (this is a known bug, based on dateutil behavior).
        yearfirst : bool, default False
            Specify a date parse order if `arg` is str or its list-likes.
        
            - If True parses dates with the year first, eg 10/11/12 is parsed as
              2010-11-12.
            - If both dayfirst and yearfirst are True, yearfirst is preceded (same
              as dateutil).
        
            Warning: yearfirst=True is not strict, but will prefer to parse
            with year first (this is a known bug, based on dateutil behavior).
        utc : bool, default None
            Return UTC DatetimeIndex if True (converting any tz-aware
            datetime.datetime objects as well).
        format : str, default None
            The strftime to parse time, eg "%d/%m/%Y", note that "%f" will parse
            all the way up to nanoseconds.
            See strftime documentation for more information on choices:
            https://docs.python.org/3/library/datetime.html#strftime-and-strptime-behavior.
        exact : bool, True by default
            Behaves as:
            - If True, require an exact format match.
            - If False, allow the format to match anywhere in the target string.
        
        unit : str, default 'ns'
            The unit of the arg (D,s,ms,us,ns) denote the unit, which is an
            integer or float number. This will be based off the origin.
            Example, with unit='ms' and origin='unix' (the default), this
            would calculate the number of milliseconds to the unix epoch start.
        infer_datetime_format : bool, default False
            If True and no `format` is given, attempt to infer the format of the
            datetime strings based on the first non-NaN element,
            and if it can be inferred, switch to a faster method of parsing them.
            In some cases this can increase the parsing speed by ~5-10x.
        origin : scalar, default 'unix'
            Define the reference date. The numeric values would be parsed as number
            of units (defined by `unit`) since this reference date.
        
            - If 'unix' (or POSIX) time; origin is set to 1970-01-01.
            - If 'julian', unit must be 'D', and origin is set to beginning of
              Julian Calendar. Julian day number 0 is assigned to the day starting
              at noon on January 1, 4713 BC.
            - If Timestamp convertible, origin is set to Timestamp identified by
              origin.
        cache : bool, default True
            If True, use a cache of unique, converted dates to apply the datetime
            conversion. May produce significant speed-up when parsing duplicate
            date strings, especially ones with timezone offsets. The cache is only
            used when there are at least 50 values. The presence of out-of-bounds
            values will render the cache unusable and may slow down parsing.
        
            .. versionchanged:: 0.25.0
                - changed default value from False to True.
        
        Returns
        -------
        datetime
            If parsing succeeded.
            Return type depends on input:
        
            - list-like: DatetimeIndex
            - Series: Series of datetime64 dtype
            - scalar: Timestamp
        
            In case when it is not possible to return designated types (e.g. when
            any element of input is before Timestamp.min or after Timestamp.max)
            return will have datetime.datetime type (or corresponding
            array/Series).
        
        See Also
        --------
        DataFrame.astype : Cast argument to a specified dtype.
        to_timedelta : Convert argument to timedelta.
        convert_dtypes : Convert dtypes.
        
        Examples
        --------
        Assembling a datetime from multiple columns of a DataFrame. The keys can be
        common abbreviations like ['year', 'month', 'day', 'minute', 'second',
        'ms', 'us', 'ns']) or plurals of the same
        
        >>> df = pd.DataFrame({'year': [2015, 2016],
        ...                    'month': [2, 3],
        ...                    'day': [4, 5]})
        >>> pd.to_datetime(df)
        0   2015-02-04
        1   2016-03-05
        dtype: datetime64[ns]
        
        If a date does not meet the `timestamp limitations
        <https://pandas.pydata.org/pandas-docs/stable/user_guide/timeseries.html
        #timeseries-timestamp-limits>`_, passing errors='ignore'
        will return the original input instead of raising any exception.
        
        Passing errors='coerce' will force an out-of-bounds date to NaT,
        in addition to forcing non-dates (or non-parseable dates) to NaT.
        
        >>> pd.to_datetime('13000101', format='%Y%m%d', errors='ignore')
        datetime.datetime(1300, 1, 1, 0, 0)
        >>> pd.to_datetime('13000101', format='%Y%m%d', errors='coerce')
        NaT
        
        Passing infer_datetime_format=True can often-times speedup a parsing
        if its not an ISO8601 format exactly, but in a regular format.
        
        >>> s = pd.Series(['3/11/2000', '3/12/2000', '3/13/2000'] * 1000)
        >>> s.head()
        0    3/11/2000
        1    3/12/2000
        2    3/13/2000
        3    3/11/2000
        4    3/12/2000
        dtype: object
        
        >>> %timeit pd.to_datetime(s, infer_datetime_format=True)  # doctest: +SKIP
        100 loops, best of 3: 10.4 ms per loop
        
        >>> %timeit pd.to_datetime(s, infer_datetime_format=False)  # doctest: +SKIP
        1 loop, best of 3: 471 ms per loop
        
        Using a unix epoch time
        
        >>> pd.to_datetime(1490195805, unit='s')
        Timestamp('2017-03-22 15:16:45')
        >>> pd.to_datetime(1490195805433502912, unit='ns')
        Timestamp('2017-03-22 15:16:45.433502912')
        
        .. warning:: For float arg, precision rounding might happen. To prevent
            unexpected behavior use a fixed-width exact type.
        
        Using a non-unix epoch origin
        
        >>> pd.to_datetime([1, 2, 3], unit='D',
        ...                origin=pd.Timestamp('1960-01-01'))
        DatetimeIndex(['1960-01-02', '1960-01-03', '1960-01-04'],
                      dtype='datetime64[ns]', freq=None)
        
        In case input is list-like and the elements of input are of mixed
        timezones, return will have object type Index if utc=False.
        
        >>> pd.to_datetime(['2018-10-26 12:00 -0530', '2018-10-26 12:00 -0500'])
        Index([2018-10-26 12:00:00-05:30, 2018-10-26 12:00:00-05:00], dtype='object')
        
        >>> pd.to_datetime(['2018-10-26 12:00 -0530', '2018-10-26 12:00 -0500'],
        ...                utc=True)
        DatetimeIndex(['2018-10-26 17:30:00+00:00', '2018-10-26 17:00:00+00:00'],
                      dtype='datetime64[ns, UTC]', freq=None)
    
    


```python
# using pandas 'to_datetime' function to convert timestamp 
# column to a readable date time format and append the new column

data['Date'] = pd.to_datetime(data['Timestamp'], unit='ms')
data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Timestamp</th>
      <th>Price</th>
      <th>Date</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1693648825935</td>
      <td>25794.334275</td>
      <td>2023-09-02 10:00:25.935</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1693652461970</td>
      <td>25824.644083</td>
      <td>2023-09-02 11:01:01.970</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1693656041070</td>
      <td>25798.917344</td>
      <td>2023-09-02 12:00:41.070</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1693659628425</td>
      <td>25795.438234</td>
      <td>2023-09-02 13:00:28.425</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1693663268552</td>
      <td>25825.010207</td>
      <td>2023-09-02 14:01:08.552</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>716</th>
      <td>1696226400313</td>
      <td>27962.989233</td>
      <td>2023-10-02 06:00:00.313</td>
    </tr>
    <tr>
      <th>717</th>
      <td>1696230066163</td>
      <td>28070.284109</td>
      <td>2023-10-02 07:01:06.163</td>
    </tr>
    <tr>
      <th>718</th>
      <td>1696233654512</td>
      <td>28300.125762</td>
      <td>2023-10-02 08:00:54.512</td>
    </tr>
    <tr>
      <th>719</th>
      <td>1696237246967</td>
      <td>28286.560920</td>
      <td>2023-10-02 09:00:46.967</td>
    </tr>
    <tr>
      <th>720</th>
      <td>1696240220000</td>
      <td>28301.572098</td>
      <td>2023-10-02 09:50:20.000</td>
    </tr>
  </tbody>
</table>
<p>721 rows × 3 columns</p>
</div>




```python
# getting candlestick data and assigning to variable
# grouping by date we are obtaining min, max, first and last values of each day

candlestick_data = data.groupby(data.Date.dt.date).agg({'Price': ['min', 'max', 'first', 'last']})
candlestick_data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead tr th {
        text-align: left;
    }

    .dataframe thead tr:last-of-type th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th colspan="4" halign="left">Price</th>
    </tr>
    <tr>
      <th></th>
      <th>min</th>
      <th>max</th>
      <th>first</th>
      <th>last</th>
    </tr>
    <tr>
      <th>Date</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2023-09-02</th>
      <td>25791.936056</td>
      <td>25898.432073</td>
      <td>25794.334275</td>
      <td>25859.364286</td>
    </tr>
    <tr>
      <th>2023-09-03</th>
      <td>25836.905638</td>
      <td>26054.793419</td>
      <td>25853.656843</td>
      <td>25948.197964</td>
    </tr>
    <tr>
      <th>2023-09-04</th>
      <td>25659.620573</td>
      <td>25998.296230</td>
      <td>25959.596311</td>
      <td>25749.106735</td>
    </tr>
    <tr>
      <th>2023-09-05</th>
      <td>25652.307316</td>
      <td>25829.364773</td>
      <td>25829.364773</td>
      <td>25753.959299</td>
    </tr>
    <tr>
      <th>2023-09-06</th>
      <td>25576.564269</td>
      <td>25835.942669</td>
      <td>25770.129055</td>
      <td>25725.087828</td>
    </tr>
    <tr>
      <th>2023-09-07</th>
      <td>25647.715451</td>
      <td>26387.747917</td>
      <td>25752.958419</td>
      <td>26387.747917</td>
    </tr>
    <tr>
      <th>2023-09-08</th>
      <td>25764.723457</td>
      <td>26355.954341</td>
      <td>26192.333433</td>
      <td>25905.637856</td>
    </tr>
    <tr>
      <th>2023-09-09</th>
      <td>25813.384607</td>
      <td>25907.292128</td>
      <td>25907.228137</td>
      <td>25900.101906</td>
    </tr>
    <tr>
      <th>2023-09-10</th>
      <td>25682.082070</td>
      <td>25889.671639</td>
      <td>25889.671639</td>
      <td>25857.257729</td>
    </tr>
    <tr>
      <th>2023-09-11</th>
      <td>25023.249185</td>
      <td>25836.142894</td>
      <td>25834.885628</td>
      <td>25140.138899</td>
    </tr>
    <tr>
      <th>2023-09-12</th>
      <td>25133.303107</td>
      <td>26288.334884</td>
      <td>25133.303107</td>
      <td>25979.215385</td>
    </tr>
    <tr>
      <th>2023-09-13</th>
      <td>25843.107805</td>
      <td>26304.015465</td>
      <td>25850.322300</td>
      <td>26234.189828</td>
    </tr>
    <tr>
      <th>2023-09-14</th>
      <td>26193.031946</td>
      <td>26751.796646</td>
      <td>26222.013304</td>
      <td>26615.532123</td>
    </tr>
    <tr>
      <th>2023-09-15</th>
      <td>26251.615685</td>
      <td>26792.608825</td>
      <td>26531.395566</td>
      <td>26792.608825</td>
    </tr>
    <tr>
      <th>2023-09-16</th>
      <td>26471.093720</td>
      <td>26704.253882</td>
      <td>26610.403126</td>
      <td>26566.033844</td>
    </tr>
    <tr>
      <th>2023-09-17</th>
      <td>26462.583232</td>
      <td>26605.367472</td>
      <td>26557.768692</td>
      <td>26468.617802</td>
    </tr>
    <tr>
      <th>2023-09-18</th>
      <td>26456.817699</td>
      <td>27394.588105</td>
      <td>26520.988255</td>
      <td>26867.060576</td>
    </tr>
    <tr>
      <th>2023-09-19</th>
      <td>26682.841449</td>
      <td>27289.424890</td>
      <td>26741.461111</td>
      <td>27200.835848</td>
    </tr>
    <tr>
      <th>2023-09-20</th>
      <td>26936.571053</td>
      <td>27318.242558</td>
      <td>27213.184659</td>
      <td>27110.600553</td>
    </tr>
    <tr>
      <th>2023-09-21</th>
      <td>26418.527785</td>
      <td>27115.846447</td>
      <td>27115.846447</td>
      <td>26589.232107</td>
    </tr>
    <tr>
      <th>2023-09-22</th>
      <td>26534.177937</td>
      <td>26688.337962</td>
      <td>26561.133454</td>
      <td>26582.589417</td>
    </tr>
    <tr>
      <th>2023-09-23</th>
      <td>26536.561163</td>
      <td>26615.098926</td>
      <td>26581.967576</td>
      <td>26575.529117</td>
    </tr>
    <tr>
      <th>2023-09-24</th>
      <td>26447.459302</td>
      <td>26657.753583</td>
      <td>26573.923480</td>
      <td>26503.235603</td>
    </tr>
    <tr>
      <th>2023-09-25</th>
      <td>26059.043075</td>
      <td>26357.550153</td>
      <td>26257.583770</td>
      <td>26287.076367</td>
    </tr>
    <tr>
      <th>2023-09-26</th>
      <td>26111.574712</td>
      <td>26347.306498</td>
      <td>26296.922317</td>
      <td>26151.495532</td>
    </tr>
    <tr>
      <th>2023-09-27</th>
      <td>26166.382102</td>
      <td>26805.628892</td>
      <td>26204.757591</td>
      <td>26288.209341</td>
    </tr>
    <tr>
      <th>2023-09-28</th>
      <td>26344.993094</td>
      <td>27146.515346</td>
      <td>26350.146895</td>
      <td>27013.058110</td>
    </tr>
    <tr>
      <th>2023-09-29</th>
      <td>26836.065662</td>
      <td>27151.164505</td>
      <td>27009.013751</td>
      <td>26896.650033</td>
    </tr>
    <tr>
      <th>2023-09-30</th>
      <td>26895.989847</td>
      <td>27075.965614</td>
      <td>26917.199102</td>
      <td>27007.094356</td>
    </tr>
    <tr>
      <th>2023-10-01</th>
      <td>26969.876144</td>
      <td>27958.086080</td>
      <td>26969.876144</td>
      <td>27958.086080</td>
    </tr>
    <tr>
      <th>2023-10-02</th>
      <td>27902.790354</td>
      <td>28301.572098</td>
      <td>27967.510579</td>
      <td>28301.572098</td>
    </tr>
  </tbody>
</table>
</div>




```python
# using pip to install plotly library which will draw the candlestick diagram
# importing graph_objects module and assinging to standard abbreviation 'go'

!pip install plotly==4.14.3

import plotly.graph_objects as go
```

    Requirement already satisfied: plotly==4.14.3 in c:\users\ajdpi\anaconda3\lib\site-packages (4.14.3)
    Requirement already satisfied: six in c:\users\ajdpi\anaconda3\lib\site-packages (from plotly==4.14.3) (1.16.0)
    Requirement already satisfied: retrying>=1.3.3 in c:\users\ajdpi\anaconda3\lib\site-packages (from plotly==4.14.3) (1.3.3)
    


```python
# using plotly to plot and draw candlestick diagram

fig = go.Figure(data=[go.Candlestick(x= candlestick_data.index, 
                open=candlestick_data['Price']['first'], 
                high=candlestick_data['Price']['max'], 
                low=candlestick_data['Price']['min'], 
                close=candlestick_data['Price']['last'])
                ])

fig.update_layout(xaxis_rangeslider_visible=False, xaxis_title='Date', 
yaxis_title='Price (USD $)', title='Bitcoin Candlestick Chart Over Past 30 Days')

fig.show()
```


        <script type="text/javascript">
        window.PlotlyConfig = {MathJaxConfig: 'local'};
        if (window.MathJax) {MathJax.Hub.Config({SVG: {font: "STIX-Web"}});}
        if (typeof require !== 'undefined') {
        require.undef("plotly");
        define('plotly', function(require, exports, module) {
            /**
* plotly.js v1.58.4
* Copyright 2012-2020, Plotly, Inc.
* All rights reserved.
* Licensed under the MIT license
*/
!function(t){if("object"==typeof exports&&"undefined"!=typeof module)module.exports=t();else if("function"==typeof define&&define.amd)define([],t);else{("undefined"!=typeof window?window:"undefined"!=typeof global?global:"undefined"!=typeof self?self:this).Plotly=t()}}((function(){return function t(e,r,n){function i(o,s){if(!r[o]){if(!e[o]){var l="function"==typeof require&&require;if(!s&&l)return l(o,!0);if(a)return a(o,!0);var c=new Error("Cannot find module '"+o+"'");throw c.code="MODULE_NOT_FOUND",c}var u=r[o]={exports:{}};e[o][0].call(u.exports,(function(t){return i(e[o][1][t]||t)}),u,u.exports,t,e,r,n)}return r[o].exports}for(var a="function"==typeof require&&require,o=0;o<n.length;o++)i(n[o]);return i}({1:[function(t,e,r){"use strict";var n=t("../src/lib"),i={"X,X div":"direction:ltr;font-family:'Open Sans', verdana, arial, sans-serif;margin:0;padding:0;","X input,X button":"font-family:'Open Sans', verdana, arial, sans-serif;","X input:focus,X button:focus":"outline:none;","X a":"text-decoration:none;","X a:hover":"text-decoration:none;","X .crisp":"shape-rendering:crispEdges;","X .user-select-none":"-webkit-user-select:none;-moz-user-select:none;-ms-user-select:none;-o-user-select:none;user-select:none;","X svg":"overflow:hidden;","X svg a":"fill:#447adb;","X svg a:hover":"fill:#3c6dc5;","X .main-svg":"position:absolute;top:0;left:0;pointer-events:none;","X .main-svg .draglayer":"pointer-events:all;","X .cursor-default":"cursor:default;","X .cursor-pointer":"cursor:pointer;","X .cursor-crosshair":"cursor:crosshair;","X .cursor-move":"cursor:move;","X .cursor-col-resize":"cursor:col-resize;","X .cursor-row-resize":"cursor:row-resize;","X .cursor-ns-resize":"cursor:ns-resize;","X .cursor-ew-resize":"cursor:ew-resize;","X .cursor-sw-resize":"cursor:sw-resize;","X .cursor-s-resize":"cursor:s-resize;","X .cursor-se-resize":"cursor:se-resize;","X .cursor-w-resize":"cursor:w-resize;","X .cursor-e-resize":"cursor:e-resize;","X .cursor-nw-resize":"cursor:nw-resize;","X .cursor-n-resize":"cursor:n-resize;","X .cursor-ne-resize":"cursor:ne-resize;","X .cursor-grab":"cursor:-webkit-grab;cursor:grab;","X .modebar":"position:absolute;top:2px;right:2px;","X .ease-bg":"-webkit-transition:background-color 0.3s ease 0s;-moz-transition:background-color 0.3s ease 0s;-ms-transition:background-color 0.3s ease 0s;-o-transition:background-color 0.3s ease 0s;transition:background-color 0.3s ease 0s;","X .modebar--hover>:not(.watermark)":"opacity:0;-webkit-transition:opacity 0.3s ease 0s;-moz-transition:opacity 0.3s ease 0s;-ms-transition:opacity 0.3s ease 0s;-o-transition:opacity 0.3s ease 0s;transition:opacity 0.3s ease 0s;","X:hover .modebar--hover .modebar-group":"opacity:1;","X .modebar-group":"float:left;display:inline-block;box-sizing:border-box;padding-left:8px;position:relative;vertical-align:middle;white-space:nowrap;","X .modebar-btn":"position:relative;font-size:16px;padding:3px 4px;height:22px;cursor:pointer;line-height:normal;box-sizing:border-box;","X .modebar-btn svg":"position:relative;top:2px;","X .modebar.vertical":"display:flex;flex-direction:column;flex-wrap:wrap;align-content:flex-end;max-height:100%;","X .modebar.vertical svg":"top:-1px;","X .modebar.vertical .modebar-group":"display:block;float:none;padding-left:0px;padding-bottom:8px;","X .modebar.vertical .modebar-group .modebar-btn":"display:block;text-align:center;","X [data-title]:before,X [data-title]:after":"position:absolute;-webkit-transform:translate3d(0, 0, 0);-moz-transform:translate3d(0, 0, 0);-ms-transform:translate3d(0, 0, 0);-o-transform:translate3d(0, 0, 0);transform:translate3d(0, 0, 0);display:none;opacity:0;z-index:1001;pointer-events:none;top:110%;right:50%;","X [data-title]:hover:before,X [data-title]:hover:after":"display:block;opacity:1;","X [data-title]:before":"content:'';position:absolute;background:transparent;border:6px solid transparent;z-index:1002;margin-top:-12px;border-bottom-color:#69738a;margin-right:-6px;","X [data-title]:after":"content:attr(data-title);background:#69738a;color:white;padding:8px 10px;font-size:12px;line-height:12px;white-space:nowrap;margin-right:-18px;border-radius:2px;","X .vertical [data-title]:before,X .vertical [data-title]:after":"top:0%;right:200%;","X .vertical [data-title]:before":"border:6px solid transparent;border-left-color:#69738a;margin-top:8px;margin-right:-30px;","X .select-outline":"fill:none;stroke-width:1;shape-rendering:crispEdges;","X .select-outline-1":"stroke:white;","X .select-outline-2":"stroke:black;stroke-dasharray:2px 2px;",Y:"font-family:'Open Sans', verdana, arial, sans-serif;position:fixed;top:50px;right:20px;z-index:10000;font-size:10pt;max-width:180px;","Y p":"margin:0;","Y .notifier-note":"min-width:180px;max-width:250px;border:1px solid #fff;z-index:3000;margin:0;background-color:#8c97af;background-color:rgba(140,151,175,0.9);color:#fff;padding:10px;overflow-wrap:break-word;word-wrap:break-word;-ms-hyphens:auto;-webkit-hyphens:auto;hyphens:auto;","Y .notifier-close":"color:#fff;opacity:0.8;float:right;padding:0 5px;background:none;border:none;font-size:20px;font-weight:bold;line-height:20px;","Y .notifier-close:hover":"color:#444;text-decoration:none;cursor:pointer;"};for(var a in i){var o=a.replace(/^,/," ,").replace(/X/g,".js-plotly-plot .plotly").replace(/Y/g,".plotly-notifier");n.addStyleRule(o,i[a])}},{"../src/lib":778}],2:[function(t,e,r){"use strict";e.exports=t("../src/transforms/aggregate")},{"../src/transforms/aggregate":1365}],3:[function(t,e,r){"use strict";e.exports=t("../src/traces/bar")},{"../src/traces/bar":929}],4:[function(t,e,r){"use strict";e.exports=t("../src/traces/barpolar")},{"../src/traces/barpolar":942}],5:[function(t,e,r){"use strict";e.exports=t("../src/traces/box")},{"../src/traces/box":952}],6:[function(t,e,r){"use strict";e.exports=t("../src/components/calendars")},{"../src/components/calendars":641}],7:[function(t,e,r){"use strict";e.exports=t("../src/traces/candlestick")},{"../src/traces/candlestick":961}],8:[function(t,e,r){"use strict";e.exports=t("../src/traces/carpet")},{"../src/traces/carpet":980}],9:[function(t,e,r){"use strict";e.exports=t("../src/traces/choropleth")},{"../src/traces/choropleth":994}],10:[function(t,e,r){"use strict";e.exports=t("../src/traces/choroplethmapbox")},{"../src/traces/choroplethmapbox":1001}],11:[function(t,e,r){"use strict";e.exports=t("../src/traces/cone")},{"../src/traces/cone":1007}],12:[function(t,e,r){"use strict";e.exports=t("../src/traces/contour")},{"../src/traces/contour":1022}],13:[function(t,e,r){"use strict";e.exports=t("../src/traces/contourcarpet")},{"../src/traces/contourcarpet":1033}],14:[function(t,e,r){"use strict";e.exports=t("../src/core")},{"../src/core":755}],15:[function(t,e,r){"use strict";e.exports=t("../src/traces/densitymapbox")},{"../src/traces/densitymapbox":1041}],16:[function(t,e,r){"use strict";e.exports=t("../src/transforms/filter")},{"../src/transforms/filter":1366}],17:[function(t,e,r){"use strict";e.exports=t("../src/traces/funnel")},{"../src/traces/funnel":1051}],18:[function(t,e,r){"use strict";e.exports=t("../src/traces/funnelarea")},{"../src/traces/funnelarea":1060}],19:[function(t,e,r){"use strict";e.exports=t("../src/transforms/groupby")},{"../src/transforms/groupby":1367}],20:[function(t,e,r){"use strict";e.exports=t("../src/traces/heatmap")},{"../src/traces/heatmap":1073}],21:[function(t,e,r){"use strict";e.exports=t("../src/traces/heatmapgl")},{"../src/traces/heatmapgl":1083}],22:[function(t,e,r){"use strict";e.exports=t("../src/traces/histogram")},{"../src/traces/histogram":1095}],23:[function(t,e,r){"use strict";e.exports=t("../src/traces/histogram2d")},{"../src/traces/histogram2d":1101}],24:[function(t,e,r){"use strict";e.exports=t("../src/traces/histogram2dcontour")},{"../src/traces/histogram2dcontour":1105}],25:[function(t,e,r){"use strict";e.exports=t("../src/traces/image")},{"../src/traces/image":1113}],26:[function(t,e,r){"use strict";var n=t("./core");n.register([t("./bar"),t("./box"),t("./heatmap"),t("./histogram"),t("./histogram2d"),t("./histogram2dcontour"),t("./contour"),t("./scatterternary"),t("./violin"),t("./funnel"),t("./waterfall"),t("./image"),t("./pie"),t("./sunburst"),t("./treemap"),t("./funnelarea"),t("./scatter3d"),t("./surface"),t("./isosurface"),t("./volume"),t("./mesh3d"),t("./cone"),t("./streamtube"),t("./scattergeo"),t("./choropleth"),t("./scattergl"),t("./splom"),t("./pointcloud"),t("./heatmapgl"),t("./parcoords"),t("./parcats"),t("./scattermapbox"),t("./choroplethmapbox"),t("./densitymapbox"),t("./sankey"),t("./indicator"),t("./table"),t("./carpet"),t("./scattercarpet"),t("./contourcarpet"),t("./ohlc"),t("./candlestick"),t("./scatterpolar"),t("./scatterpolargl"),t("./barpolar")]),n.register([t("./aggregate"),t("./filter"),t("./groupby"),t("./sort")]),n.register([t("./calendars")]),e.exports=n},{"./aggregate":2,"./bar":3,"./barpolar":4,"./box":5,"./calendars":6,"./candlestick":7,"./carpet":8,"./choropleth":9,"./choroplethmapbox":10,"./cone":11,"./contour":12,"./contourcarpet":13,"./core":14,"./densitymapbox":15,"./filter":16,"./funnel":17,"./funnelarea":18,"./groupby":19,"./heatmap":20,"./heatmapgl":21,"./histogram":22,"./histogram2d":23,"./histogram2dcontour":24,"./image":25,"./indicator":27,"./isosurface":28,"./mesh3d":29,"./ohlc":30,"./parcats":31,"./parcoords":32,"./pie":33,"./pointcloud":34,"./sankey":35,"./scatter3d":36,"./scattercarpet":37,"./scattergeo":38,"./scattergl":39,"./scattermapbox":40,"./scatterpolar":41,"./scatterpolargl":42,"./scatterternary":43,"./sort":44,"./splom":45,"./streamtube":46,"./sunburst":47,"./surface":48,"./table":49,"./treemap":50,"./violin":51,"./volume":52,"./waterfall":53}],27:[function(t,e,r){"use strict";e.exports=t("../src/traces/indicator")},{"../src/traces/indicator":1121}],28:[function(t,e,r){"use strict";e.exports=t("../src/traces/isosurface")},{"../src/traces/isosurface":1127}],29:[function(t,e,r){"use strict";e.exports=t("../src/traces/mesh3d")},{"../src/traces/mesh3d":1132}],30:[function(t,e,r){"use strict";e.exports=t("../src/traces/ohlc")},{"../src/traces/ohlc":1137}],31:[function(t,e,r){"use strict";e.exports=t("../src/traces/parcats")},{"../src/traces/parcats":1146}],32:[function(t,e,r){"use strict";e.exports=t("../src/traces/parcoords")},{"../src/traces/parcoords":1156}],33:[function(t,e,r){"use strict";e.exports=t("../src/traces/pie")},{"../src/traces/pie":1167}],34:[function(t,e,r){"use strict";e.exports=t("../src/traces/pointcloud")},{"../src/traces/pointcloud":1176}],35:[function(t,e,r){"use strict";e.exports=t("../src/traces/sankey")},{"../src/traces/sankey":1182}],36:[function(t,e,r){"use strict";e.exports=t("../src/traces/scatter3d")},{"../src/traces/scatter3d":1220}],37:[function(t,e,r){"use strict";e.exports=t("../src/traces/scattercarpet")},{"../src/traces/scattercarpet":1227}],38:[function(t,e,r){"use strict";e.exports=t("../src/traces/scattergeo")},{"../src/traces/scattergeo":1235}],39:[function(t,e,r){"use strict";e.exports=t("../src/traces/scattergl")},{"../src/traces/scattergl":1248}],40:[function(t,e,r){"use strict";e.exports=t("../src/traces/scattermapbox")},{"../src/traces/scattermapbox":1258}],41:[function(t,e,r){"use strict";e.exports=t("../src/traces/scatterpolar")},{"../src/traces/scatterpolar":1266}],42:[function(t,e,r){"use strict";e.exports=t("../src/traces/scatterpolargl")},{"../src/traces/scatterpolargl":1273}],43:[function(t,e,r){"use strict";e.exports=t("../src/traces/scatterternary")},{"../src/traces/scatterternary":1281}],44:[function(t,e,r){"use strict";e.exports=t("../src/transforms/sort")},{"../src/transforms/sort":1369}],45:[function(t,e,r){"use strict";e.exports=t("../src/traces/splom")},{"../src/traces/splom":1290}],46:[function(t,e,r){"use strict";e.exports=t("../src/traces/streamtube")},{"../src/traces/streamtube":1298}],47:[function(t,e,r){"use strict";e.exports=t("../src/traces/sunburst")},{"../src/traces/sunburst":1306}],48:[function(t,e,r){"use strict";e.exports=t("../src/traces/surface")},{"../src/traces/surface":1315}],49:[function(t,e,r){"use strict";e.exports=t("../src/traces/table")},{"../src/traces/table":1323}],50:[function(t,e,r){"use strict";e.exports=t("../src/traces/treemap")},{"../src/traces/treemap":1332}],51:[function(t,e,r){"use strict";e.exports=t("../src/traces/violin")},{"../src/traces/violin":1344}],52:[function(t,e,r){"use strict";e.exports=t("../src/traces/volume")},{"../src/traces/volume":1352}],53:[function(t,e,r){"use strict";e.exports=t("../src/traces/waterfall")},{"../src/traces/waterfall":1360}],54:[function(t,e,r){"use strict";e.exports=function(t){var e=(t=t||{}).eye||[0,0,1],r=t.center||[0,0,0],s=t.up||[0,1,0],l=t.distanceLimits||[0,1/0],c=t.mode||"turntable",u=n(),f=i(),h=a();return u.setDistanceLimits(l[0],l[1]),u.lookAt(0,e,r,s),f.setDistanceLimits(l[0],l[1]),f.lookAt(0,e,r,s),h.setDistanceLimits(l[0],l[1]),h.lookAt(0,e,r,s),new o({turntable:u,orbit:f,matrix:h},c)};var n=t("turntable-camera-controller"),i=t("orbit-camera-controller"),a=t("matrix-camera-controller");function o(t,e){this._controllerNames=Object.keys(t),this._controllerList=this._controllerNames.map((function(e){return t[e]})),this._mode=e,this._active=t[e],this._active||(this._mode="turntable",this._active=t.turntable),this.modes=this._controllerNames,this.computedMatrix=this._active.computedMatrix,this.computedEye=this._active.computedEye,this.computedUp=this._active.computedUp,this.computedCenter=this._active.computedCenter,this.computedRadius=this._active.computedRadius}var s=o.prototype;[["flush",1],["idle",1],["lookAt",4],["rotate",4],["pan",4],["translate",4],["setMatrix",2],["setDistanceLimits",2],["setDistance",2]].forEach((function(t){for(var e=t[0],r=[],n=0;n<t[1];++n)r.push("a"+n);var i="var cc=this._controllerList;for(var i=0;i<cc.length;++i){cc[i]."+t[0]+"("+r.join()+")}";s[e]=Function.apply(null,r.concat(i))})),s.recalcMatrix=function(t){this._active.recalcMatrix(t)},s.getDistance=function(t){return this._active.getDistance(t)},s.getDistanceLimits=function(t){return this._active.getDistanceLimits(t)},s.lastT=function(){return this._active.lastT()},s.setMode=function(t){if(t!==this._mode){var e=this._controllerNames.indexOf(t);if(!(e<0)){var r=this._active,n=this._controllerList[e],i=Math.max(r.lastT(),n.lastT());r.recalcMatrix(i),n.setMatrix(i,r.computedMatrix),this._active=n,this._mode=t,this.computedMatrix=this._active.computedMatrix,this.computedEye=this._active.computedEye,this.computedUp=this._active.computedUp,this.computedCenter=this._active.computedCenter,this.computedRadius=this._active.computedRadius}}},s.getMode=function(){return this._mode}},{"matrix-camera-controller":480,"orbit-camera-controller":501,"turntable-camera-controller":581}],55:[function(t,e,r){!function(n,i){"object"==typeof r&&"undefined"!=typeof e?i(r,t("d3-array"),t("d3-collection"),t("d3-shape"),t("elementary-circuits-directed-graph")):i(n.d3=n.d3||{},n.d3,n.d3,n.d3,null)}(this,(function(t,e,r,n,i){"use strict";function a(t){return t.target.depth}function o(t,e){return t.sourceLinks.length?t.depth:e-1}function s(t){return function(){return t}}i=i&&i.hasOwnProperty("default")?i.default:i;var l="function"==typeof Symbol&&"symbol"==typeof Symbol.iterator?function(t){return typeof t}:function(t){return t&&"function"==typeof Symbol&&t.constructor===Symbol&&t!==Symbol.prototype?"symbol":typeof t};function c(t,e){return f(t.source,e.source)||t.index-e.index}function u(t,e){return f(t.target,e.target)||t.index-e.index}function f(t,e){return t.partOfCycle===e.partOfCycle?t.y0-e.y0:"top"===t.circularLinkType||"bottom"===e.circularLinkType?-1:1}function h(t){return t.value}function p(t){return(t.y0+t.y1)/2}function d(t){return p(t.source)}function g(t){return p(t.target)}function m(t){return t.index}function v(t){return t.nodes}function y(t){return t.links}function x(t,e){var r=t.get(e);if(!r)throw new Error("missing: "+e);return r}function b(t,e){return e(t)}function _(t,e,r){var n=0;if(null===r){for(var a=[],o=0;o<t.links.length;o++){var s=t.links[o],l=s.source.index,c=s.target.index;a[l]||(a[l]=[]),a[c]||(a[c]=[]),-1===a[l].indexOf(c)&&a[l].push(c)}var u=i(a);u.sort((function(t,e){return t.length-e.length}));var f={};for(o=0;o<u.length;o++){var h=u[o].slice(-2);f[h[0]]||(f[h[0]]={}),f[h[0]][h[1]]=!0}t.links.forEach((function(t){var e=t.target.index,r=t.source.index;e===r||f[r]&&f[r][e]?(t.circular=!0,t.circularLinkID=n,n+=1):t.circular=!1}))}else t.links.forEach((function(t){t.source[r]<t.target[r]?t.circular=!1:(t.circular=!0,t.circularLinkID=n,n+=1)}))}function w(t,e){var r=0,n=0;t.links.forEach((function(i){i.circular&&(i.source.circularLinkType||i.target.circularLinkType?i.circularLinkType=i.source.circularLinkType?i.source.circularLinkType:i.target.circularLinkType:i.circularLinkType=r<n?"top":"bottom","top"==i.circularLinkType?r+=1:n+=1,t.nodes.forEach((function(t){b(t,e)!=b(i.source,e)&&b(t,e)!=b(i.target,e)||(t.circularLinkType=i.circularLinkType)})))})),t.links.forEach((function(t){t.circular&&(t.source.circularLinkType==t.target.circularLinkType&&(t.circularLinkType=t.source.circularLinkType),H(t,e)&&(t.circularLinkType=t.source.circularLinkType))}))}function T(t){var e=Math.abs(t.y1-t.y0),r=Math.abs(t.target.x0-t.source.x1);return Math.atan(r/e)}function k(t,e){var r=0;t.sourceLinks.forEach((function(t){r=t.circular&&!H(t,e)?r+1:r}));var n=0;return t.targetLinks.forEach((function(t){n=t.circular&&!H(t,e)?n+1:n})),r+n}function M(t){var e=t.source.sourceLinks,r=0;e.forEach((function(t){r=t.circular?r+1:r}));var n=t.target.targetLinks,i=0;return n.forEach((function(t){i=t.circular?i+1:i})),!(r>1||i>1)}function A(t,e,r){return t.sort(E),t.forEach((function(n,i){var a,o,s=0;if(H(n,r)&&M(n))n.circularPathData.verticalBuffer=s+n.width/2;else{for(var l=0;l<i;l++)if(a=t[i],o=t[l],!(a.source.column<o.target.column||a.target.column>o.source.column)){var c=t[l].circularPathData.verticalBuffer+t[l].width/2+e;s=c>s?c:s}n.circularPathData.verticalBuffer=s+n.width/2}})),t}function S(t,r,i,a){var o=e.min(t.links,(function(t){return t.source.y0}));t.links.forEach((function(t){t.circular&&(t.circularPathData={})})),A(t.links.filter((function(t){return"top"==t.circularLinkType})),r,a),A(t.links.filter((function(t){return"bottom"==t.circularLinkType})),r,a),t.links.forEach((function(e){if(e.circular){if(e.circularPathData.arcRadius=e.width+10,e.circularPathData.leftNodeBuffer=5,e.circularPathData.rightNodeBuffer=5,e.circularPathData.sourceWidth=e.source.x1-e.source.x0,e.circularPathData.sourceX=e.source.x0+e.circularPathData.sourceWidth,e.circularPathData.targetX=e.target.x0,e.circularPathData.sourceY=e.y0,e.circularPathData.targetY=e.y1,H(e,a)&&M(e))e.circularPathData.leftSmallArcRadius=10+e.width/2,e.circularPathData.leftLargeArcRadius=10+e.width/2,e.circularPathData.rightSmallArcRadius=10+e.width/2,e.circularPathData.rightLargeArcRadius=10+e.width/2,"bottom"==e.circularLinkType?(e.circularPathData.verticalFullExtent=e.source.y1+25+e.circularPathData.verticalBuffer,e.circularPathData.verticalLeftInnerExtent=e.circularPathData.verticalFullExtent-e.circularPathData.leftLargeArcRadius,e.circularPathData.verticalRightInnerExtent=e.circularPathData.verticalFullExtent-e.circularPathData.rightLargeArcRadius):(e.circularPathData.verticalFullExtent=e.source.y0-25-e.circularPathData.verticalBuffer,e.circularPathData.verticalLeftInnerExtent=e.circularPathData.verticalFullExtent+e.circularPathData.leftLargeArcRadius,e.circularPathData.verticalRightInnerExtent=e.circularPathData.verticalFullExtent+e.circularPathData.rightLargeArcRadius);else{var s=e.source.column,l=e.circularLinkType,c=t.links.filter((function(t){return t.source.column==s&&t.circularLinkType==l}));"bottom"==e.circularLinkType?c.sort(L):c.sort(C);var u=0;c.forEach((function(t,n){t.circularLinkID==e.circularLinkID&&(e.circularPathData.leftSmallArcRadius=10+e.width/2+u,e.circularPathData.leftLargeArcRadius=10+e.width/2+n*r+u),u+=t.width})),s=e.target.column,c=t.links.filter((function(t){return t.target.column==s&&t.circularLinkType==l})),"bottom"==e.circularLinkType?c.sort(P):c.sort(I),u=0,c.forEach((function(t,n){t.circularLinkID==e.circularLinkID&&(e.circularPathData.rightSmallArcRadius=10+e.width/2+u,e.circularPathData.rightLargeArcRadius=10+e.width/2+n*r+u),u+=t.width})),"bottom"==e.circularLinkType?(e.circularPathData.verticalFullExtent=Math.max(i,e.source.y1,e.target.y1)+25+e.circularPathData.verticalBuffer,e.circularPathData.verticalLeftInnerExtent=e.circularPathData.verticalFullExtent-e.circularPathData.leftLargeArcRadius,e.circularPathData.verticalRightInnerExtent=e.circularPathData.verticalFullExtent-e.circularPathData.rightLargeArcRadius):(e.circularPathData.verticalFullExtent=o-25-e.circularPathData.verticalBuffer,e.circularPathData.verticalLeftInnerExtent=e.circularPathData.verticalFullExtent+e.circularPathData.leftLargeArcRadius,e.circularPathData.verticalRightInnerExtent=e.circularPathData.verticalFullExtent+e.circularPathData.rightLargeArcRadius)}e.circularPathData.leftInnerExtent=e.circularPathData.sourceX+e.circularPathData.leftNodeBuffer,e.circularPathData.rightInnerExtent=e.circularPathData.targetX-e.circularPathData.rightNodeBuffer,e.circularPathData.leftFullExtent=e.circularPathData.sourceX+e.circularPathData.leftLargeArcRadius+e.circularPathData.leftNodeBuffer,e.circularPathData.rightFullExtent=e.circularPathData.targetX-e.circularPathData.rightLargeArcRadius-e.circularPathData.rightNodeBuffer}if(e.circular)e.path=function(t){var e="";e="top"==t.circularLinkType?"M"+t.circularPathData.sourceX+" "+t.circularPathData.sourceY+" L"+t.circularPathData.leftInnerExtent+" "+t.circularPathData.sourceY+" A"+t.circularPathData.leftLargeArcRadius+" "+t.circularPathData.leftSmallArcRadius+" 0 0 0 "+t.circularPathData.leftFullExtent+" "+(t.circularPathData.sourceY-t.circularPathData.leftSmallArcRadius)+" L"+t.circularPathData.leftFullExtent+" "+t.circularPathData.verticalLeftInnerExtent+" A"+t.circularPathData.leftLargeArcRadius+" "+t.circularPathData.leftLargeArcRadius+" 0 0 0 "+t.circularPathData.leftInnerExtent+" "+t.circularPathData.verticalFullExtent+" L"+t.circularPathData.rightInnerExtent+" "+t.circularPathData.verticalFullExtent+" A"+t.circularPathData.rightLargeArcRadius+" "+t.circularPathData.rightLargeArcRadius+" 0 0 0 "+t.circularPathData.rightFullExtent+" "+t.circularPathData.verticalRightInnerExtent+" L"+t.circularPathData.rightFullExtent+" "+(t.circularPathData.targetY-t.circularPathData.rightSmallArcRadius)+" A"+t.circularPathData.rightLargeArcRadius+" "+t.circularPathData.rightSmallArcRadius+" 0 0 0 "+t.circularPathData.rightInnerExtent+" "+t.circularPathData.targetY+" L"+t.circularPathData.targetX+" "+t.circularPathData.targetY:"M"+t.circularPathData.sourceX+" "+t.circularPathData.sourceY+" L"+t.circularPathData.leftInnerExtent+" "+t.circularPathData.sourceY+" A"+t.circularPathData.leftLargeArcRadius+" "+t.circularPathData.leftSmallArcRadius+" 0 0 1 "+t.circularPathData.leftFullExtent+" "+(t.circularPathData.sourceY+t.circularPathData.leftSmallArcRadius)+" L"+t.circularPathData.leftFullExtent+" "+t.circularPathData.verticalLeftInnerExtent+" A"+t.circularPathData.leftLargeArcRadius+" "+t.circularPathData.leftLargeArcRadius+" 0 0 1 "+t.circularPathData.leftInnerExtent+" "+t.circularPathData.verticalFullExtent+" L"+t.circularPathData.rightInnerExtent+" "+t.circularPathData.verticalFullExtent+" A"+t.circularPathData.rightLargeArcRadius+" "+t.circularPathData.rightLargeArcRadius+" 0 0 1 "+t.circularPathData.rightFullExtent+" "+t.circularPathData.verticalRightInnerExtent+" L"+t.circularPathData.rightFullExtent+" "+(t.circularPathData.targetY+t.circularPathData.rightSmallArcRadius)+" A"+t.circularPathData.rightLargeArcRadius+" "+t.circularPathData.rightSmallArcRadius+" 0 0 1 "+t.circularPathData.rightInnerExtent+" "+t.circularPathData.targetY+" L"+t.circularPathData.targetX+" "+t.circularPathData.targetY;return e}(e);else{var f=n.linkHorizontal().source((function(t){return[t.source.x0+(t.source.x1-t.source.x0),t.y0]})).target((function(t){return[t.target.x0,t.y1]}));e.path=f(e)}}))}function E(t,e){return z(t)==z(e)?"bottom"==t.circularLinkType?L(t,e):C(t,e):z(e)-z(t)}function C(t,e){return t.y0-e.y0}function L(t,e){return e.y0-t.y0}function I(t,e){return t.y1-e.y1}function P(t,e){return e.y1-t.y1}function z(t){return t.target.column-t.source.column}function O(t){return t.target.x0-t.source.x1}function D(t,e){var r=T(t),n=O(e)/Math.tan(r);return"up"==q(t)?t.y1+n:t.y1-n}function R(t,e){var r=T(t),n=O(e)/Math.tan(r);return"up"==q(t)?t.y1-n:t.y1+n}function F(t,e,r,n){t.links.forEach((function(i){if(!i.circular&&i.target.column-i.source.column>1){var a=i.source.column+1,o=i.target.column-1,s=1,l=o-a+1;for(s=1;a<=o;a++,s++)t.nodes.forEach((function(o){if(o.column==a){var c,u=s/(l+1),f=Math.pow(1-u,3),h=3*u*Math.pow(1-u,2),p=3*Math.pow(u,2)*(1-u),d=Math.pow(u,3),g=f*i.y0+h*i.y0+p*i.y1+d*i.y1,m=g-i.width/2,v=g+i.width/2;m>o.y0&&m<o.y1?(c=o.y1-m+10,c="bottom"==o.circularLinkType?c:-c,o=N(o,c,e,r),t.nodes.forEach((function(t){b(t,n)!=b(o,n)&&t.column==o.column&&B(o,t)&&N(t,c,e,r)}))):(v>o.y0&&v<o.y1||m<o.y0&&v>o.y1)&&(c=v-o.y0+10,o=N(o,c,e,r),t.nodes.forEach((function(t){b(t,n)!=b(o,n)&&t.column==o.column&&t.y0<o.y1&&t.y1>o.y1&&N(t,c,e,r)})))}}))}}))}function B(t,e){return t.y0>e.y0&&t.y0<e.y1||(t.y1>e.y0&&t.y1<e.y1||t.y0<e.y0&&t.y1>e.y1)}function N(t,e,r,n){return t.y0+e>=r&&t.y1+e<=n&&(t.y0=t.y0+e,t.y1=t.y1+e,t.targetLinks.forEach((function(t){t.y1=t.y1+e})),t.sourceLinks.forEach((function(t){t.y0=t.y0+e}))),t}function j(t,e,r,n){t.nodes.forEach((function(i){n&&i.y+(i.y1-i.y0)>e&&(i.y=i.y-(i.y+(i.y1-i.y0)-e));var a=t.links.filter((function(t){return b(t.source,r)==b(i,r)})),o=a.length;o>1&&a.sort((function(t,e){if(!t.circular&&!e.circular){if(t.target.column==e.target.column)return t.y1-e.y1;if(!V(t,e))return t.y1-e.y1;if(t.target.column>e.target.column){var r=R(e,t);return t.y1-r}if(e.target.column>t.target.column)return R(t,e)-e.y1}return t.circular&&!e.circular?"top"==t.circularLinkType?-1:1:e.circular&&!t.circular?"top"==e.circularLinkType?1:-1:t.circular&&e.circular?t.circularLinkType===e.circularLinkType&&"top"==t.circularLinkType?t.target.column===e.target.column?t.target.y1-e.target.y1:e.target.column-t.target.column:t.circularLinkType===e.circularLinkType&&"bottom"==t.circularLinkType?t.target.column===e.target.column?e.target.y1-t.target.y1:t.target.column-e.target.column:"top"==t.circularLinkType?-1:1:void 0}));var s=i.y0;a.forEach((function(t){t.y0=s+t.width/2,s+=t.width})),a.forEach((function(t,e){if("bottom"==t.circularLinkType){for(var r=e+1,n=0;r<o;r++)n+=a[r].width;t.y0=i.y1-n-t.width/2}}))}))}function U(t,e,r){t.nodes.forEach((function(e){var n=t.links.filter((function(t){return b(t.target,r)==b(e,r)})),i=n.length;i>1&&n.sort((function(t,e){if(!t.circular&&!e.circular){if(t.source.column==e.source.column)return t.y0-e.y0;if(!V(t,e))return t.y0-e.y0;if(e.source.column<t.source.column){var r=D(e,t);return t.y0-r}if(t.source.column<e.source.column)return D(t,e)-e.y0}return t.circular&&!e.circular?"top"==t.circularLinkType?-1:1:e.circular&&!t.circular?"top"==e.circularLinkType?1:-1:t.circular&&e.circular?t.circularLinkType===e.circularLinkType&&"top"==t.circularLinkType?t.source.column===e.source.column?t.source.y1-e.source.y1:t.source.column-e.source.column:t.circularLinkType===e.circularLinkType&&"bottom"==t.circularLinkType?t.source.column===e.source.column?t.source.y1-e.source.y1:e.source.column-t.source.column:"top"==t.circularLinkType?-1:1:void 0}));var a=e.y0;n.forEach((function(t){t.y1=a+t.width/2,a+=t.width})),n.forEach((function(t,r){if("bottom"==t.circularLinkType){for(var a=r+1,o=0;a<i;a++)o+=n[a].width;t.y1=e.y1-o-t.width/2}}))}))}function V(t,e){return q(t)==q(e)}function q(t){return t.y0-t.y1>0?"up":"down"}function H(t,e){return b(t.source,e)==b(t.target,e)}function G(t,r,n){var i=t.nodes,a=t.links,o=!1,s=!1;if(a.forEach((function(t){"top"==t.circularLinkType?o=!0:"bottom"==t.circularLinkType&&(s=!0)})),0==o||0==s){var l=e.min(i,(function(t){return t.y0})),c=(n-r)/(e.max(i,(function(t){return t.y1}))-l);i.forEach((function(t){var e=(t.y1-t.y0)*c;t.y0=(t.y0-l)*c,t.y1=t.y0+e})),a.forEach((function(t){t.y0=(t.y0-l)*c,t.y1=(t.y1-l)*c,t.width=t.width*c}))}}t.sankeyCircular=function(){var t,n,i=0,a=0,b=1,T=1,M=24,A=m,E=o,C=v,L=y,I=32,P=2,z=null;function O(){var t={nodes:C.apply(null,arguments),links:L.apply(null,arguments)};D(t),_(t,A,z),R(t),B(t),w(t,A),N(t,I,A),V(t);for(var e=4,r=0;r<e;r++)j(t,T,A),U(t,T,A),F(t,a,T,A),j(t,T,A),U(t,T,A);return G(t,a,T),S(t,P,T,A),t}function D(t){t.nodes.forEach((function(t,e){t.index=e,t.sourceLinks=[],t.targetLinks=[]}));var e=r.map(t.nodes,A);return t.links.forEach((function(t,r){t.index=r;var n=t.source,i=t.target;"object"!==("undefined"==typeof n?"undefined":l(n))&&(n=t.source=x(e,n)),"object"!==("undefined"==typeof i?"undefined":l(i))&&(i=t.target=x(e,i)),n.sourceLinks.push(t),i.targetLinks.push(t)})),t}function R(t){t.nodes.forEach((function(t){t.partOfCycle=!1,t.value=Math.max(e.sum(t.sourceLinks,h),e.sum(t.targetLinks,h)),t.sourceLinks.forEach((function(e){e.circular&&(t.partOfCycle=!0,t.circularLinkType=e.circularLinkType)})),t.targetLinks.forEach((function(e){e.circular&&(t.partOfCycle=!0,t.circularLinkType=e.circularLinkType)}))}))}function B(t){var e,r,n;for(e=t.nodes,r=[],n=0;e.length;++n,e=r,r=[])e.forEach((function(t){t.depth=n,t.sourceLinks.forEach((function(t){r.indexOf(t.target)<0&&!t.circular&&r.push(t.target)}))}));for(e=t.nodes,r=[],n=0;e.length;++n,e=r,r=[])e.forEach((function(t){t.height=n,t.targetLinks.forEach((function(t){r.indexOf(t.source)<0&&!t.circular&&r.push(t.source)}))}));t.nodes.forEach((function(t){t.column=Math.floor(E.call(null,t,n))}))}function N(o,s,l){var c=r.nest().key((function(t){return t.column})).sortKeys(e.ascending).entries(o.nodes).map((function(t){return t.values}));!function(r){if(n){var s=1/0;c.forEach((function(t){var e=T*n/(t.length+1);s=e<s?e:s})),t=s}var l=e.min(c,(function(r){return(T-a-(r.length-1)*t)/e.sum(r,h)}));l*=.3,o.links.forEach((function(t){t.width=t.value*l}));var u=function(t){var r=0,n=0,i=0,a=0,o=e.max(t.nodes,(function(t){return t.column}));return t.links.forEach((function(t){t.circular&&("top"==t.circularLinkType?r+=t.width:n+=t.width,0==t.target.column&&(a+=t.width),t.source.column==o&&(i+=t.width))})),{top:r=r>0?r+25+10:r,bottom:n=n>0?n+25+10:n,left:a=a>0?a+25+10:a,right:i=i>0?i+25+10:i}}(o),f=function(t,r){var n=e.max(t.nodes,(function(t){return t.column})),o=b-i,s=T-a,l=o/(o+r.right+r.left),c=s/(s+r.top+r.bottom);return i=i*l+r.left,b=0==r.right?b:b*l,a=a*c+r.top,T*=c,t.nodes.forEach((function(t){t.x0=i+t.column*((b-i-M)/n),t.x1=t.x0+M})),c}(o,u);l*=f,o.links.forEach((function(t){t.width=t.value*l})),c.forEach((function(t){var e=t.length;t.forEach((function(t,n){t.depth==c.length-1&&1==e||0==t.depth&&1==e?(t.y0=T/2-t.value*l,t.y1=t.y0+t.value*l):t.partOfCycle?0==k(t,r)?(t.y0=T/2+n,t.y1=t.y0+t.value*l):"top"==t.circularLinkType?(t.y0=a+n,t.y1=t.y0+t.value*l):(t.y0=T-t.value*l-n,t.y1=t.y0+t.value*l):0==u.top||0==u.bottom?(t.y0=(T-a)/e*n,t.y1=t.y0+t.value*l):(t.y0=(T-a)/2-e/2+n,t.y1=t.y0+t.value*l)}))}))}(l),y();for(var u=1,m=s;m>0;--m)v(u*=.99,l),y();function v(t,r){var n=c.length;c.forEach((function(i){var a=i.length,o=i[0].depth;i.forEach((function(i){var s;if(i.sourceLinks.length||i.targetLinks.length)if(i.partOfCycle&&k(i,r)>0);else if(0==o&&1==a)s=i.y1-i.y0,i.y0=T/2-s/2,i.y1=T/2+s/2;else if(o==n-1&&1==a)s=i.y1-i.y0,i.y0=T/2-s/2,i.y1=T/2+s/2;else{var l=e.mean(i.sourceLinks,g),c=e.mean(i.targetLinks,d),u=((l&&c?(l+c)/2:l||c)-p(i))*t;i.y0+=u,i.y1+=u}}))}))}function y(){c.forEach((function(e){var r,n,i,o=a,s=e.length;for(e.sort(f),i=0;i<s;++i)(n=o-(r=e[i]).y0)>0&&(r.y0+=n,r.y1+=n),o=r.y1+t;if((n=o-t-T)>0)for(o=r.y0-=n,r.y1-=n,i=s-2;i>=0;--i)(n=(r=e[i]).y1+t-o)>0&&(r.y0-=n,r.y1-=n),o=r.y0}))}}function V(t){t.nodes.forEach((function(t){t.sourceLinks.sort(u),t.targetLinks.sort(c)})),t.nodes.forEach((function(t){var e=t.y0,r=e,n=t.y1,i=n;t.sourceLinks.forEach((function(t){t.circular?(t.y0=n-t.width/2,n-=t.width):(t.y0=e+t.width/2,e+=t.width)})),t.targetLinks.forEach((function(t){t.circular?(t.y1=i-t.width/2,i-=t.width):(t.y1=r+t.width/2,r+=t.width)}))}))}return O.nodeId=function(t){return arguments.length?(A="function"==typeof t?t:s(t),O):A},O.nodeAlign=function(t){return arguments.length?(E="function"==typeof t?t:s(t),O):E},O.nodeWidth=function(t){return arguments.length?(M=+t,O):M},O.nodePadding=function(e){return arguments.length?(t=+e,O):t},O.nodes=function(t){return arguments.length?(C="function"==typeof t?t:s(t),O):C},O.links=function(t){return arguments.length?(L="function"==typeof t?t:s(t),O):L},O.size=function(t){return arguments.length?(i=a=0,b=+t[0],T=+t[1],O):[b-i,T-a]},O.extent=function(t){return arguments.length?(i=+t[0][0],b=+t[1][0],a=+t[0][1],T=+t[1][1],O):[[i,a],[b,T]]},O.iterations=function(t){return arguments.length?(I=+t,O):I},O.circularLinkGap=function(t){return arguments.length?(P=+t,O):P},O.nodePaddingRatio=function(t){return arguments.length?(n=+t,O):n},O.sortNodes=function(t){return arguments.length?(z=t,O):z},O.update=function(t){return w(t,A),V(t),t.links.forEach((function(t){t.circular&&(t.circularLinkType=t.y0+t.y1<T?"top":"bottom",t.source.circularLinkType=t.circularLinkType,t.target.circularLinkType=t.circularLinkType)})),j(t,T,A,!1),U(t,T,A),S(t,P,T,A),t},O},t.sankeyCenter=function(t){return t.targetLinks.length?t.depth:t.sourceLinks.length?e.min(t.sourceLinks,a)-1:0},t.sankeyLeft=function(t){return t.depth},t.sankeyRight=function(t,e){return e-1-t.height},t.sankeyJustify=o,Object.defineProperty(t,"__esModule",{value:!0})}))},{"d3-array":156,"d3-collection":157,"d3-shape":165,"elementary-circuits-directed-graph":179}],56:[function(t,e,r){!function(n,i){"object"==typeof r&&"undefined"!=typeof e?i(r,t("d3-array"),t("d3-collection"),t("d3-shape")):i(n.d3=n.d3||{},n.d3,n.d3,n.d3)}(this,(function(t,e,r,n){"use strict";function i(t){return t.target.depth}function a(t,e){return t.sourceLinks.length?t.depth:e-1}function o(t){return function(){return t}}function s(t,e){return c(t.source,e.source)||t.index-e.index}function l(t,e){return c(t.target,e.target)||t.index-e.index}function c(t,e){return t.y0-e.y0}function u(t){return t.value}function f(t){return(t.y0+t.y1)/2}function h(t){return f(t.source)*t.value}function p(t){return f(t.target)*t.value}function d(t){return t.index}function g(t){return t.nodes}function m(t){return t.links}function v(t,e){var r=t.get(e);if(!r)throw new Error("missing: "+e);return r}function y(t){return[t.source.x1,t.y0]}function x(t){return[t.target.x0,t.y1]}t.sankey=function(){var t=0,n=0,i=1,y=1,x=24,b=8,_=d,w=a,T=g,k=m,M=32;function A(){var t={nodes:T.apply(null,arguments),links:k.apply(null,arguments)};return S(t),E(t),C(t),L(t),I(t),t}function S(t){t.nodes.forEach((function(t,e){t.index=e,t.sourceLinks=[],t.targetLinks=[]}));var e=r.map(t.nodes,_);t.links.forEach((function(t,r){t.index=r;var n=t.source,i=t.target;"object"!=typeof n&&(n=t.source=v(e,n)),"object"!=typeof i&&(i=t.target=v(e,i)),n.sourceLinks.push(t),i.targetLinks.push(t)}))}function E(t){t.nodes.forEach((function(t){t.value=Math.max(e.sum(t.sourceLinks,u),e.sum(t.targetLinks,u))}))}function C(e){var r,n,a;for(r=e.nodes,n=[],a=0;r.length;++a,r=n,n=[])r.forEach((function(t){t.depth=a,t.sourceLinks.forEach((function(t){n.indexOf(t.target)<0&&n.push(t.target)}))}));for(r=e.nodes,n=[],a=0;r.length;++a,r=n,n=[])r.forEach((function(t){t.height=a,t.targetLinks.forEach((function(t){n.indexOf(t.source)<0&&n.push(t.source)}))}));var o=(i-t-x)/(a-1);e.nodes.forEach((function(e){e.x1=(e.x0=t+Math.max(0,Math.min(a-1,Math.floor(w.call(null,e,a))))*o)+x}))}function L(t){var i=r.nest().key((function(t){return t.x0})).sortKeys(e.ascending).entries(t.nodes).map((function(t){return t.values}));!function(){var r=e.max(i,(function(t){return t.length})),a=2/3*(y-n)/(r-1);b>a&&(b=a);var o=e.min(i,(function(t){return(y-n-(t.length-1)*b)/e.sum(t,u)}));i.forEach((function(t){t.forEach((function(t,e){t.y1=(t.y0=e)+t.value*o}))})),t.links.forEach((function(t){t.width=t.value*o}))}(),d();for(var a=1,o=M;o>0;--o)l(a*=.99),d(),s(a),d();function s(t){i.forEach((function(r){r.forEach((function(r){if(r.targetLinks.length){var n=(e.sum(r.targetLinks,h)/e.sum(r.targetLinks,u)-f(r))*t;r.y0+=n,r.y1+=n}}))}))}function l(t){i.slice().reverse().forEach((function(r){r.forEach((function(r){if(r.sourceLinks.length){var n=(e.sum(r.sourceLinks,p)/e.sum(r.sourceLinks,u)-f(r))*t;r.y0+=n,r.y1+=n}}))}))}function d(){i.forEach((function(t){var e,r,i,a=n,o=t.length;for(t.sort(c),i=0;i<o;++i)(r=a-(e=t[i]).y0)>0&&(e.y0+=r,e.y1+=r),a=e.y1+b;if((r=a-b-y)>0)for(a=e.y0-=r,e.y1-=r,i=o-2;i>=0;--i)(r=(e=t[i]).y1+b-a)>0&&(e.y0-=r,e.y1-=r),a=e.y0}))}}function I(t){t.nodes.forEach((function(t){t.sourceLinks.sort(l),t.targetLinks.sort(s)})),t.nodes.forEach((function(t){var e=t.y0,r=e;t.sourceLinks.forEach((function(t){t.y0=e+t.width/2,e+=t.width})),t.targetLinks.forEach((function(t){t.y1=r+t.width/2,r+=t.width}))}))}return A.update=function(t){return I(t),t},A.nodeId=function(t){return arguments.length?(_="function"==typeof t?t:o(t),A):_},A.nodeAlign=function(t){return arguments.length?(w="function"==typeof t?t:o(t),A):w},A.nodeWidth=function(t){return arguments.length?(x=+t,A):x},A.nodePadding=function(t){return arguments.length?(b=+t,A):b},A.nodes=function(t){return arguments.length?(T="function"==typeof t?t:o(t),A):T},A.links=function(t){return arguments.length?(k="function"==typeof t?t:o(t),A):k},A.size=function(e){return arguments.length?(t=n=0,i=+e[0],y=+e[1],A):[i-t,y-n]},A.extent=function(e){return arguments.length?(t=+e[0][0],i=+e[1][0],n=+e[0][1],y=+e[1][1],A):[[t,n],[i,y]]},A.iterations=function(t){return arguments.length?(M=+t,A):M},A},t.sankeyCenter=function(t){return t.targetLinks.length?t.depth:t.sourceLinks.length?e.min(t.sourceLinks,i)-1:0},t.sankeyLeft=function(t){return t.depth},t.sankeyRight=function(t,e){return e-1-t.height},t.sankeyJustify=a,t.sankeyLinkHorizontal=function(){return n.linkHorizontal().source(y).target(x)},Object.defineProperty(t,"__esModule",{value:!0})}))},{"d3-array":156,"d3-collection":157,"d3-shape":165}],57:[function(t,e,r){"use strict";e.exports=t("./quad")},{"./quad":58}],58:[function(t,e,r){"use strict";var n=t("binary-search-bounds"),i=t("clamp"),a=t("parse-rect"),o=t("array-bounds"),s=t("pick-by-alias"),l=t("defined"),c=t("flatten-vertex-data"),u=t("is-obj"),f=t("dtype"),h=t("math-log2");function p(t,e){for(var r=e[0],n=e[1],a=1/(e[2]-r),o=1/(e[3]-n),s=new Array(t.length),l=0,c=t.length/2;l<c;l++)s[2*l]=i((t[2*l]-r)*a,0,1),s[2*l+1]=i((t[2*l+1]-n)*o,0,1);return s}e.exports=function(t,e){e||(e={}),t=c(t,"float64"),e=s(e,{bounds:"range bounds dataBox databox",maxDepth:"depth maxDepth maxdepth level maxLevel maxlevel levels",dtype:"type dtype format out dst output destination"});var r=l(e.maxDepth,255),i=l(e.bounds,o(t,2));i[0]===i[2]&&i[2]++,i[1]===i[3]&&i[3]++;var d,g=p(t,i),m=t.length>>>1;e.dtype||(e.dtype="array"),"string"==typeof e.dtype?d=new(f(e.dtype))(m):e.dtype&&(d=e.dtype,Array.isArray(d)&&(d.length=m));for(var v=0;v<m;++v)d[v]=v;var y=[],x=[],b=[],_=[];!function t(e,n,i,a,o,s){if(!a.length)return null;var l=y[o]||(y[o]=[]),c=b[o]||(b[o]=[]),u=x[o]||(x[o]=[]),f=l.length;if(++o>r||s>1073741824){for(var h=0;h<a.length;h++)l.push(a[h]),c.push(s),u.push(null,null,null,null);return f}if(l.push(a[0]),c.push(s),a.length<=1)return u.push(null,null,null,null),f;for(var p=.5*i,d=e+p,m=n+p,v=[],_=[],w=[],T=[],k=1,M=a.length;k<M;k++){var A=a[k],S=g[2*A],E=g[2*A+1];S<d?E<m?v.push(A):_.push(A):E<m?w.push(A):T.push(A)}return s<<=2,u.push(t(e,n,p,v,o,s),t(e,m,p,_,o,s+1),t(d,n,p,w,o,s+2),t(d,m,p,T,o,s+3)),f}(0,0,1,d,0,1);for(var w=0,T=0;T<y.length;T++){var k=y[T];if(d.set)d.set(k,w);else for(var M=0,A=k.length;M<A;M++)d[M+w]=k[M];var S=w+y[T].length;_[T]=[w,S],w=S}return d.range=function(){var e,r=[],n=arguments.length;for(;n--;)r[n]=arguments[n];if(u(r[r.length-1])){var o=r.pop();r.length||null==o.x&&null==o.l&&null==o.left||(r=[o],e={}),e=s(o,{level:"level maxLevel",d:"d diam diameter r radius px pxSize pixel pixelSize maxD size minSize",lod:"lod details ranges offsets"})}else e={};r.length||(r=i);var c=a.apply(void 0,r),f=[Math.min(c.x,c.x+c.width),Math.min(c.y,c.y+c.height),Math.max(c.x,c.x+c.width),Math.max(c.y,c.y+c.height)],d=f[0],g=f[1],m=f[2],v=f[3],b=p([d,g,m,v],i),_=b[0],w=b[1],T=b[2],k=b[3],M=l(e.level,y.length);if(null!=e.d){var A;"number"==typeof e.d?A=[e.d,e.d]:e.d.length&&(A=e.d),M=Math.min(Math.max(Math.ceil(-h(Math.abs(A[0])/(i[2]-i[0]))),Math.ceil(-h(Math.abs(A[1])/(i[3]-i[1])))),M)}if(M=Math.min(M,y.length),e.lod)return E(_,w,T,k,M);var S=[];function C(e,r,n,i,a,o){if(null!==a&&null!==o&&!(_>e+n||w>r+n||T<e||k<r||i>=M||a===o)){var s=y[i];void 0===o&&(o=s.length);for(var l=a;l<o;l++){var c=s[l],u=t[2*c],f=t[2*c+1];u>=d&&u<=m&&f>=g&&f<=v&&S.push(c)}var h=x[i],p=h[4*a+0],b=h[4*a+1],A=h[4*a+2],E=h[4*a+3],I=L(h,a+1),P=.5*n,z=i+1;C(e,r,P,z,p,b||A||E||I),C(e,r+P,P,z,b,A||E||I),C(e+P,r,P,z,A,E||I),C(e+P,r+P,P,z,E,I)}}function L(t,e){for(var r=null,n=0;null===r;)if(r=t[4*e+n],++n>t.length)return null;return r}return C(0,0,1,0,0,1),S},d;function E(t,e,r,i,a){for(var o=[],s=0;s<a;s++){var l=b[s],c=_[s][0],u=C(t,e,s),f=C(r,i,s),h=n.ge(l,u),p=n.gt(l,f,h,l.length-1);o[s]=[h+c,p+c]}return o}function C(t,e,r){for(var n=1,i=.5,a=.5,o=.5,s=0;s<r;s++)n<<=2,n+=t<i?e<a?0:1:e<a?2:3,o*=.5,i+=t<i?-o:o,a+=e<a?-o:o;return n}}},{"array-bounds":70,"binary-search-bounds":96,clamp:120,defined:170,dtype:175,"flatten-vertex-data":244,"is-obj":468,"math-log2":479,"parse-rect":504,"pick-by-alias":511}],59:[function(t,e,r){"use strict";Object.defineProperty(r,"__esModule",{value:!0});var n=t("@turf/meta");function i(t){var e=0;if(t&&t.length>0){e+=Math.abs(a(t[0]));for(var r=1;r<t.length;r++)e-=Math.abs(a(t[r]))}return e}function a(t){var e,r,n,i,a,s,l=0,c=t.length;if(c>2){for(s=0;s<c;s++)s===c-2?(n=c-2,i=c-1,a=0):s===c-1?(n=c-1,i=0,a=1):(n=s,i=s+1,a=s+2),e=t[n],r=t[i],l+=(o(t[a][0])-o(e[0]))*Math.sin(o(r[1]));l=6378137*l*6378137/2}return l}function o(t){return t*Math.PI/180}r.default=function(t){return n.geomReduce(t,(function(t,e){return t+function(t){var e,r=0;switch(t.type){case"Polygon":return i(t.coordinates);case"MultiPolygon":for(e=0;e<t.coordinates.length;e++)r+=i(t.coordinates[e]);return r;case"Point":case"MultiPoint":case"LineString":case"MultiLineString":return 0}return 0}(e)}),0)}},{"@turf/meta":63}],60:[function(t,e,r){"use strict";Object.defineProperty(r,"__esModule",{value:!0});var n=t("@turf/meta");r.default=function(t){var e=[1/0,1/0,-1/0,-1/0];return n.coordEach(t,(function(t){e[0]>t[0]&&(e[0]=t[0]),e[1]>t[1]&&(e[1]=t[1]),e[2]<t[0]&&(e[2]=t[0]),e[3]<t[1]&&(e[3]=t[1])})),e}},{"@turf/meta":63}],61:[function(t,e,r){"use strict";Object.defineProperty(r,"__esModule",{value:!0});var n=t("@turf/meta"),i=t("@turf/helpers");r.default=function(t,e){void 0===e&&(e={});var r=0,a=0,o=0;return n.coordEach(t,(function(t){r+=t[0],a+=t[1],o++})),i.point([r/o,a/o],e.properties)}},{"@turf/helpers":62,"@turf/meta":63}],62:[function(t,e,r){"use strict";function n(t,e,r){void 0===r&&(r={});var n={type:"Feature"};return(0===r.id||r.id)&&(n.id=r.id),r.bbox&&(n.bbox=r.bbox),n.properties=e||{},n.geometry=t,n}function i(t,e,r){return void 0===r&&(r={}),n({type:"Point",coordinates:t},e,r)}function a(t,e,r){void 0===r&&(r={});for(var i=0,a=t;i<a.length;i++){var o=a[i];if(o.length<4)throw new Error("Each LinearRing of a Polygon must have 4 or more Positions.");for(var s=0;s<o[o.length-1].length;s++)if(o[o.length-1][s]!==o[0][s])throw new Error("First and last Position are not equivalent.")}return n({type:"Polygon",coordinates:t},e,r)}function o(t,e,r){if(void 0===r&&(r={}),t.length<2)throw new Error("coordinates must be an array of two or more positions");return n({type:"LineString",coordinates:t},e,r)}function s(t,e){void 0===e&&(e={});var r={type:"FeatureCollection"};return e.id&&(r.id=e.id),e.bbox&&(r.bbox=e.bbox),r.features=t,r}function l(t,e,r){return void 0===r&&(r={}),n({type:"MultiLineString",coordinates:t},e,r)}function c(t,e,r){return void 0===r&&(r={}),n({type:"MultiPoint",coordinates:t},e,r)}function u(t,e,r){return void 0===r&&(r={}),n({type:"MultiPolygon",coordinates:t},e,r)}function f(t,e){void 0===e&&(e="kilometers");var n=r.factors[e];if(!n)throw new Error(e+" units is invalid");return t*n}function h(t,e){void 0===e&&(e="kilometers");var n=r.factors[e];if(!n)throw new Error(e+" units is invalid");return t/n}function p(t){return 180*(t%(2*Math.PI))/Math.PI}function d(t){return!isNaN(t)&&null!==t&&!Array.isArray(t)&&!/^\s*$/.test(t)}Object.defineProperty(r,"__esModule",{value:!0}),r.earthRadius=6371008.8,r.factors={centimeters:100*r.earthRadius,centimetres:100*r.earthRadius,degrees:r.earthRadius/111325,feet:3.28084*r.earthRadius,inches:39.37*r.earthRadius,kilometers:r.earthRadius/1e3,kilometres:r.earthRadius/1e3,meters:r.earthRadius,metres:r.earthRadius,miles:r.earthRadius/1609.344,millimeters:1e3*r.earthRadius,millimetres:1e3*r.earthRadius,nauticalmiles:r.earthRadius/1852,radians:1,yards:r.earthRadius/1.0936},r.unitsFactors={centimeters:100,centimetres:100,degrees:1/111325,feet:3.28084,inches:39.37,kilometers:.001,kilometres:.001,meters:1,metres:1,miles:1/1609.344,millimeters:1e3,millimetres:1e3,nauticalmiles:1/1852,radians:1/r.earthRadius,yards:1/1.0936},r.areaFactors={acres:247105e-9,centimeters:1e4,centimetres:1e4,feet:10.763910417,inches:1550.003100006,kilometers:1e-6,kilometres:1e-6,meters:1,metres:1,miles:386e-9,millimeters:1e6,millimetres:1e6,yards:1.195990046},r.feature=n,r.geometry=function(t,e,r){switch(void 0===r&&(r={}),t){case"Point":return i(e).geometry;case"LineString":return o(e).geometry;case"Polygon":return a(e).geometry;case"MultiPoint":return c(e).geometry;case"MultiLineString":return l(e).geometry;case"MultiPolygon":return u(e).geometry;default:throw new Error(t+" is invalid")}},r.point=i,r.points=function(t,e,r){return void 0===r&&(r={}),s(t.map((function(t){return i(t,e)})),r)},r.polygon=a,r.polygons=function(t,e,r){return void 0===r&&(r={}),s(t.map((function(t){return a(t,e)})),r)},r.lineString=o,r.lineStrings=function(t,e,r){return void 0===r&&(r={}),s(t.map((function(t){return o(t,e)})),r)},r.featureCollection=s,r.multiLineString=l,r.multiPoint=c,r.multiPolygon=u,r.geometryCollection=function(t,e,r){return void 0===r&&(r={}),n({type:"GeometryCollection",geometries:t},e,r)},r.round=function(t,e){if(void 0===e&&(e=0),e&&!(e>=0))throw new Error("precision must be a positive number");var r=Math.pow(10,e||0);return Math.round(t*r)/r},r.radiansToLength=f,r.lengthToRadians=h,r.lengthToDegrees=function(t,e){return p(h(t,e))},r.bearingToAzimuth=function(t){var e=t%360;return e<0&&(e+=360),e},r.radiansToDegrees=p,r.degreesToRadians=function(t){return t%360*Math.PI/180},r.convertLength=function(t,e,r){if(void 0===e&&(e="kilometers"),void 0===r&&(r="kilometers"),!(t>=0))throw new Error("length must be a positive number");return f(h(t,e),r)},r.convertArea=function(t,e,n){if(void 0===e&&(e="meters"),void 0===n&&(n="kilometers"),!(t>=0))throw new Error("area must be a positive number");var i=r.areaFactors[e];if(!i)throw new Error("invalid original units");var a=r.areaFactors[n];if(!a)throw new Error("invalid final units");return t/i*a},r.isNumber=d,r.isObject=function(t){return!!t&&t.constructor===Object},r.validateBBox=function(t){if(!t)throw new Error("bbox is required");if(!Array.isArray(t))throw new Error("bbox must be an Array");if(4!==t.length&&6!==t.length)throw new Error("bbox must be an Array of 4 or 6 numbers");t.forEach((function(t){if(!d(t))throw new Error("bbox must only contain numbers")}))},r.validateId=function(t){if(!t)throw new Error("id is required");if(-1===["string","number"].indexOf(typeof t))throw new Error("id must be a number or a string")},r.radians2degrees=function(){throw new Error("method has been renamed to `radiansToDegrees`")},r.degrees2radians=function(){throw new Error("method has been renamed to `degreesToRadians`")},r.distanceToDegrees=function(){throw new Error("method has been renamed to `lengthToDegrees`")},r.distanceToRadians=function(){throw new Error("method has been renamed to `lengthToRadians`")},r.radiansToDistance=function(){throw new Error("method has been renamed to `radiansToLength`")},r.bearingToAngle=function(){throw new Error("method has been renamed to `bearingToAzimuth`")},r.convertDistance=function(){throw new Error("method has been renamed to `convertLength`")}},{}],63:[function(t,e,r){"use strict";Object.defineProperty(r,"__esModule",{value:!0});var n=t("@turf/helpers");function i(t,e,r){if(null!==t)for(var n,a,o,s,l,c,u,f,h=0,p=0,d=t.type,g="FeatureCollection"===d,m="Feature"===d,v=g?t.features.length:1,y=0;y<v;y++){l=(f=!!(u=g?t.features[y].geometry:m?t.geometry:t)&&"GeometryCollection"===u.type)?u.geometries.length:1;for(var x=0;x<l;x++){var b=0,_=0;if(null!==(s=f?u.geometries[x]:u)){c=s.coordinates;var w=s.type;switch(h=!r||"Polygon"!==w&&"MultiPolygon"!==w?0:1,w){case null:break;case"Point":if(!1===e(c,p,y,b,_))return!1;p++,b++;break;case"LineString":case"MultiPoint":for(n=0;n<c.length;n++){if(!1===e(c[n],p,y,b,_))return!1;p++,"MultiPoint"===w&&b++}"LineString"===w&&b++;break;case"Polygon":case"MultiLineString":for(n=0;n<c.length;n++){for(a=0;a<c[n].length-h;a++){if(!1===e(c[n][a],p,y,b,_))return!1;p++}"MultiLineString"===w&&b++,"Polygon"===w&&_++}"Polygon"===w&&b++;break;case"MultiPolygon":for(n=0;n<c.length;n++){for(_=0,a=0;a<c[n].length;a++){for(o=0;o<c[n][a].length-h;o++){if(!1===e(c[n][a][o],p,y,b,_))return!1;p++}_++}b++}break;case"GeometryCollection":for(n=0;n<s.geometries.length;n++)if(!1===i(s.geometries[n],e,r))return!1;break;default:throw new Error("Unknown Geometry Type")}}}}}function a(t,e){var r;switch(t.type){case"FeatureCollection":for(r=0;r<t.features.length&&!1!==e(t.features[r].properties,r);r++);break;case"Feature":e(t.properties,0)}}function o(t,e){if("Feature"===t.type)e(t,0);else if("FeatureCollection"===t.type)for(var r=0;r<t.features.length&&!1!==e(t.features[r],r);r++);}function s(t,e){var r,n,i,a,o,s,l,c,u,f,h=0,p="FeatureCollection"===t.type,d="Feature"===t.type,g=p?t.features.length:1;for(r=0;r<g;r++){for(s=p?t.features[r].geometry:d?t.geometry:t,c=p?t.features[r].properties:d?t.properties:{},u=p?t.features[r].bbox:d?t.bbox:void 0,f=p?t.features[r].id:d?t.id:void 0,o=(l=!!s&&"GeometryCollection"===s.type)?s.geometries.length:1,i=0;i<o;i++)if(null!==(a=l?s.geometries[i]:s))switch(a.type){case"Point":case"LineString":case"MultiPoint":case"Polygon":case"MultiLineString":case"MultiPolygon":if(!1===e(a,h,c,u,f))return!1;break;case"GeometryCollection":for(n=0;n<a.geometries.length;n++)if(!1===e(a.geometries[n],h,c,u,f))return!1;break;default:throw new Error("Unknown Geometry Type")}else if(!1===e(null,h,c,u,f))return!1;h++}}function l(t,e){s(t,(function(t,r,i,a,o){var s,l=null===t?null:t.type;switch(l){case null:case"Point":case"LineString":case"Polygon":return!1!==e(n.feature(t,i,{bbox:a,id:o}),r,0)&&void 0}switch(l){case"MultiPoint":s="Point";break;case"MultiLineString":s="LineString";break;case"MultiPolygon":s="Polygon"}for(var c=0;c<t.coordinates.length;c++){var u={type:s,coordinates:t.coordinates[c]};if(!1===e(n.feature(u,i),r,c))return!1}}))}function c(t,e){l(t,(function(t,r,a){var o=0;if(t.geometry){var s=t.geometry.type;if("Point"!==s&&"MultiPoint"!==s){var l,c=0,u=0,f=0;return!1!==i(t,(function(i,s,h,p,d){if(void 0===l||r>c||p>u||d>f)return l=i,c=r,u=p,f=d,void(o=0);var g=n.lineString([l,i],t.properties);if(!1===e(g,r,a,d,o))return!1;o++,l=i}))&&void 0}}}))}function u(t,e){if(!t)throw new Error("geojson is required");l(t,(function(t,r,i){if(null!==t.geometry){var a=t.geometry.type,o=t.geometry.coordinates;switch(a){case"LineString":if(!1===e(t,r,i,0,0))return!1;break;case"Polygon":for(var s=0;s<o.length;s++)if(!1===e(n.lineString(o[s],t.properties),r,i,s))return!1}}}))}r.coordEach=i,r.coordReduce=function(t,e,r,n){var a=r;return i(t,(function(t,n,i,o,s){a=0===n&&void 0===r?t:e(a,t,n,i,o,s)}),n),a},r.propEach=a,r.propReduce=function(t,e,r){var n=r;return a(t,(function(t,i){n=0===i&&void 0===r?t:e(n,t,i)})),n},r.featureEach=o,r.featureReduce=function(t,e,r){var n=r;return o(t,(function(t,i){n=0===i&&void 0===r?t:e(n,t,i)})),n},r.coordAll=function(t){var e=[];return i(t,(function(t){e.push(t)})),e},r.geomEach=s,r.geomReduce=function(t,e,r){var n=r;return s(t,(function(t,i,a,o,s){n=0===i&&void 0===r?t:e(n,t,i,a,o,s)})),n},r.flattenEach=l,r.flattenReduce=function(t,e,r){var n=r;return l(t,(function(t,i,a){n=0===i&&0===a&&void 0===r?t:e(n,t,i,a)})),n},r.segmentEach=c,r.segmentReduce=function(t,e,r){var n=r,i=!1;return c(t,(function(t,a,o,s,l){n=!1===i&&void 0===r?t:e(n,t,a,o,s,l),i=!0})),n},r.lineEach=u,r.lineReduce=function(t,e,r){var n=r;return u(t,(function(t,i,a,o){n=0===i&&void 0===r?t:e(n,t,i,a,o)})),n},r.findSegment=function(t,e){if(e=e||{},!n.isObject(e))throw new Error("options is invalid");var r,i=e.featureIndex||0,a=e.multiFeatureIndex||0,o=e.geometryIndex||0,s=e.segmentIndex||0,l=e.properties;switch(t.type){case"FeatureCollection":i<0&&(i=t.features.length+i),l=l||t.features[i].properties,r=t.features[i].geometry;break;case"Feature":l=l||t.properties,r=t.geometry;break;case"Point":case"MultiPoint":return null;case"LineString":case"Polygon":case"MultiLineString":case"MultiPolygon":r=t;break;default:throw new Error("geojson is invalid")}if(null===r)return null;var c=r.coordinates;switch(r.type){case"Point":case"MultiPoint":return null;case"LineString":return s<0&&(s=c.length+s-1),n.lineString([c[s],c[s+1]],l,e);case"Polygon":return o<0&&(o=c.length+o),s<0&&(s=c[o].length+s-1),n.lineString([c[o][s],c[o][s+1]],l,e);case"MultiLineString":return a<0&&(a=c.length+a),s<0&&(s=c[a].length+s-1),n.lineString([c[a][s],c[a][s+1]],l,e);case"MultiPolygon":return a<0&&(a=c.length+a),o<0&&(o=c[a].length+o),s<0&&(s=c[a][o].length-s-1),n.lineString([c[a][o][s],c[a][o][s+1]],l,e)}throw new Error("geojson is invalid")},r.findPoint=function(t,e){if(e=e||{},!n.isObject(e))throw new Error("options is invalid");var r,i=e.featureIndex||0,a=e.multiFeatureIndex||0,o=e.geometryIndex||0,s=e.coordIndex||0,l=e.properties;switch(t.type){case"FeatureCollection":i<0&&(i=t.features.length+i),l=l||t.features[i].properties,r=t.features[i].geometry;break;case"Feature":l=l||t.properties,r=t.geometry;break;case"Point":case"MultiPoint":return null;case"LineString":case"Polygon":case"MultiLineString":case"MultiPolygon":r=t;break;default:throw new Error("geojson is invalid")}if(null===r)return null;var c=r.coordinates;switch(r.type){case"Point":return n.point(c,l,e);case"MultiPoint":return a<0&&(a=c.length+a),n.point(c[a],l,e);case"LineString":return s<0&&(s=c.length+s),n.point(c[s],l,e);case"Polygon":return o<0&&(o=c.length+o),s<0&&(s=c[o].length+s),n.point(c[o][s],l,e);case"MultiLineString":return a<0&&(a=c.length+a),s<0&&(s=c[a].length+s),n.point(c[a][s],l,e);case"MultiPolygon":return a<0&&(a=c.length+a),o<0&&(o=c[a].length+o),s<0&&(s=c[a][o].length-s),n.point(c[a][o][s],l,e)}throw new Error("geojson is invalid")}},{"@turf/helpers":62}],64:[function(t,e,r){"use strict";var n="undefined"==typeof WeakMap?t("weak-map"):WeakMap,i=t("gl-buffer"),a=t("gl-vao"),o=new n;e.exports=function(t){var e=o.get(t),r=e&&(e._triangleBuffer.handle||e._triangleBuffer.buffer);if(!r||!t.isBuffer(r)){var n=i(t,new Float32Array([-1,-1,-1,4,4,-1]));(e=a(t,[{buffer:n,type:t.FLOAT,size:2}]))._triangleBuffer=n,o.set(t,e)}e.bind(),t.drawArrays(t.TRIANGLES,0,3),e.unbind()}},{"gl-buffer":259,"gl-vao":358,"weak-map":602}],65:[function(t,e,r){e.exports=function(t){var e=0,r=0,n=0,i=0;return t.map((function(t){var a=(t=t.slice())[0],o=a.toUpperCase();if(a!=o)switch(t[0]=o,a){case"a":t[6]+=n,t[7]+=i;break;case"v":t[1]+=i;break;case"h":t[1]+=n;break;default:for(var s=1;s<t.length;)t[s++]+=n,t[s++]+=i}switch(o){case"Z":n=e,i=r;break;case"H":n=t[1];break;case"V":i=t[1];break;case"M":n=e=t[1],i=r=t[2];break;default:n=t[t.length-2],i=t[t.length-1]}return t}))}},{}],66:[function(t,e,r){var n=t("pad-left");e.exports=function(t,e,r){e="number"==typeof e?e:1,r=r||": ";var i=t.split(/\r?\n/),a=String(i.length+e-1).length;return i.map((function(t,i){var o=i+e,s=String(o).length;return n(o,a-s)+r+t})).join("\n")}},{"pad-left":502}],67:[function(t,e,r){"use strict";e.exports=function(t){var e=t.length;if(0===e)return[];if(1===e)return[0];for(var r=t[0].length,n=[t[0]],a=[0],o=1;o<e;++o)if(n.push(t[o]),i(n,r)){if(a.push(o),a.length===r+1)return a}else n.pop();return a};var n=t("robust-orientation");function i(t,e){for(var r=new Array(e+1),i=0;i<t.length;++i)r[i]=t[i];for(i=0;i<=t.length;++i){for(var a=t.length;a<=e;++a){for(var o=new Array(e),s=0;s<e;++s)o[s]=Math.pow(a+1-i,s);r[a]=o}if(n.apply(void 0,r))return!0}return!1}},{"robust-orientation":548}],68:[function(t,e,r){"use strict";e.exports=function(t,e){return n(e).filter((function(r){for(var n=new Array(r.length),a=0;a<r.length;++a)n[a]=e[r[a]];return i(n)*t<1}))};var n=t("delaunay-triangulate"),i=t("circumradius")},{circumradius:119,"delaunay-triangulate":171}],69:[function(t,e,r){e.exports=function(t,e){return i(n(t,e))};var n=t("alpha-complex"),i=t("simplicial-complex-boundary")},{"alpha-complex":68,"simplicial-complex-boundary":555}],70:[function(t,e,r){"use strict";e.exports=function(t,e){if(!t||null==t.length)throw Error("Argument should be an array");e=null==e?1:Math.floor(e);for(var r=Array(2*e),n=0;n<e;n++){for(var i=-1/0,a=1/0,o=n,s=t.length;o<s;o+=e)t[o]>i&&(i=t[o]),t[o]<a&&(a=t[o]);r[n]=a,r[e+n]=i}return r}},{}],71:[function(t,e,r){"use strict";var n=t("array-bounds");e.exports=function(t,e,r){if(!t||null==t.length)throw Error("Argument should be an array");null==e&&(e=1);null==r&&(r=n(t,e));for(var i=0;i<e;i++){var a=r[e+i],o=r[i],s=i,l=t.length;if(a===1/0&&o===-1/0)for(s=i;s<l;s+=e)t[s]=t[s]===a?1:t[s]===o?0:.5;else if(a===1/0)for(s=i;s<l;s+=e)t[s]=t[s]===a?1:0;else if(o===-1/0)for(s=i;s<l;s+=e)t[s]=t[s]===o?0:1;else{var c=a-o;for(s=i;s<l;s+=e)isNaN(t[s])||(t[s]=0===c?.5:(t[s]-o)/c)}}return t}},{"array-bounds":70}],72:[function(t,e,r){e.exports=function(t,e){var r="number"==typeof t,n="number"==typeof e;r&&!n?(e=t,t=0):r||n||(t=0,e=0);var i=(e|=0)-(t|=0);if(i<0)throw new Error("array length must be positive");for(var a=new Array(i),o=0,s=t;o<i;o++,s++)a[o]=s;return a}},{}],73:[function(t,e,r){(function(r){(function(){"use strict";var n=t("object-assign");
/*!
 * The buffer module from node.js, for the browser.
 *
 * @author   Feross Aboukhadijeh <feross@feross.org> <http://feross.org>
 * @license  MIT
 */function i(t,e){if(t===e)return 0;for(var r=t.length,n=e.length,i=0,a=Math.min(r,n);i<a;++i)if(t[i]!==e[i]){r=t[i],n=e[i];break}return r<n?-1:n<r?1:0}function a(t){return r.Buffer&&"function"==typeof r.Buffer.isBuffer?r.Buffer.isBuffer(t):!(null==t||!t._isBuffer)}var o=t("util/"),s=Object.prototype.hasOwnProperty,l=Array.prototype.slice,c="foo"===function(){}.name;function u(t){return Object.prototype.toString.call(t)}function f(t){return!a(t)&&("function"==typeof r.ArrayBuffer&&("function"==typeof ArrayBuffer.isView?ArrayBuffer.isView(t):!!t&&(t instanceof DataView||!!(t.buffer&&t.buffer instanceof ArrayBuffer))))}var h=e.exports=y,p=/\s*function\s+([^\(\s]*)\s*/;function d(t){if(o.isFunction(t)){if(c)return t.name;var e=t.toString().match(p);return e&&e[1]}}function g(t,e){return"string"==typeof t?t.length<e?t:t.slice(0,e):t}function m(t){if(c||!o.isFunction(t))return o.inspect(t);var e=d(t);return"[Function"+(e?": "+e:"")+"]"}function v(t,e,r,n,i){throw new h.AssertionError({message:r,actual:t,expected:e,operator:n,stackStartFunction:i})}function y(t,e){t||v(t,!0,e,"==",h.ok)}function x(t,e,r,n){if(t===e)return!0;if(a(t)&&a(e))return 0===i(t,e);if(o.isDate(t)&&o.isDate(e))return t.getTime()===e.getTime();if(o.isRegExp(t)&&o.isRegExp(e))return t.source===e.source&&t.global===e.global&&t.multiline===e.multiline&&t.lastIndex===e.lastIndex&&t.ignoreCase===e.ignoreCase;if(null!==t&&"object"==typeof t||null!==e&&"object"==typeof e){if(f(t)&&f(e)&&u(t)===u(e)&&!(t instanceof Float32Array||t instanceof Float64Array))return 0===i(new Uint8Array(t.buffer),new Uint8Array(e.buffer));if(a(t)!==a(e))return!1;var s=(n=n||{actual:[],expected:[]}).actual.indexOf(t);return-1!==s&&s===n.expected.indexOf(e)||(n.actual.push(t),n.expected.push(e),function(t,e,r,n){if(null==t||null==e)return!1;if(o.isPrimitive(t)||o.isPrimitive(e))return t===e;if(r&&Object.getPrototypeOf(t)!==Object.getPrototypeOf(e))return!1;var i=b(t),a=b(e);if(i&&!a||!i&&a)return!1;if(i)return t=l.call(t),e=l.call(e),x(t,e,r);var s,c,u=T(t),f=T(e);if(u.length!==f.length)return!1;for(u.sort(),f.sort(),c=u.length-1;c>=0;c--)if(u[c]!==f[c])return!1;for(c=u.length-1;c>=0;c--)if(s=u[c],!x(t[s],e[s],r,n))return!1;return!0}(t,e,r,n))}return r?t===e:t==e}function b(t){return"[object Arguments]"==Object.prototype.toString.call(t)}function _(t,e){if(!t||!e)return!1;if("[object RegExp]"==Object.prototype.toString.call(e))return e.test(t);try{if(t instanceof e)return!0}catch(t){}return!Error.isPrototypeOf(e)&&!0===e.call({},t)}function w(t,e,r,n){var i;if("function"!=typeof e)throw new TypeError('"block" argument must be a function');"string"==typeof r&&(n=r,r=null),i=function(t){var e;try{t()}catch(t){e=t}return e}(e),n=(r&&r.name?" ("+r.name+").":".")+(n?" "+n:"."),t&&!i&&v(i,r,"Missing expected exception"+n);var a="string"==typeof n,s=!t&&i&&!r;if((!t&&o.isError(i)&&a&&_(i,r)||s)&&v(i,r,"Got unwanted exception"+n),t&&i&&r&&!_(i,r)||!t&&i)throw i}h.AssertionError=function(t){this.name="AssertionError",this.actual=t.actual,this.expected=t.expected,this.operator=t.operator,t.message?(this.message=t.message,this.generatedMessage=!1):(this.message=function(t){return g(m(t.actual),128)+" "+t.operator+" "+g(m(t.expected),128)}(this),this.generatedMessage=!0);var e=t.stackStartFunction||v;if(Error.captureStackTrace)Error.captureStackTrace(this,e);else{var r=new Error;if(r.stack){var n=r.stack,i=d(e),a=n.indexOf("\n"+i);if(a>=0){var o=n.indexOf("\n",a+1);n=n.substring(o+1)}this.stack=n}}},o.inherits(h.AssertionError,Error),h.fail=v,h.ok=y,h.equal=function(t,e,r){t!=e&&v(t,e,r,"==",h.equal)},h.notEqual=function(t,e,r){t==e&&v(t,e,r,"!=",h.notEqual)},h.deepEqual=function(t,e,r){x(t,e,!1)||v(t,e,r,"deepEqual",h.deepEqual)},h.deepStrictEqual=function(t,e,r){x(t,e,!0)||v(t,e,r,"deepStrictEqual",h.deepStrictEqual)},h.notDeepEqual=function(t,e,r){x(t,e,!1)&&v(t,e,r,"notDeepEqual",h.notDeepEqual)},h.notDeepStrictEqual=function t(e,r,n){x(e,r,!0)&&v(e,r,n,"notDeepStrictEqual",t)},h.strictEqual=function(t,e,r){t!==e&&v(t,e,r,"===",h.strictEqual)},h.notStrictEqual=function(t,e,r){t===e&&v(t,e,r,"!==",h.notStrictEqual)},h.throws=function(t,e,r){w(!0,t,e,r)},h.doesNotThrow=function(t,e,r){w(!1,t,e,r)},h.ifError=function(t){if(t)throw t},h.strict=n((function t(e,r){e||v(e,!0,r,"==",t)}),h,{equal:h.strictEqual,deepEqual:h.deepStrictEqual,notEqual:h.notStrictEqual,notDeepEqual:h.notDeepStrictEqual}),h.strict.strict=h.strict;var T=Object.keys||function(t){var e=[];for(var r in t)s.call(t,r)&&e.push(r);return e}}).call(this)}).call(this,"undefined"!=typeof global?global:"undefined"!=typeof self?self:"undefined"!=typeof window?window:{})},{"object-assign":499,"util/":76}],74:[function(t,e,r){"function"==typeof Object.create?e.exports=function(t,e){t.super_=e,t.prototype=Object.create(e.prototype,{constructor:{value:t,enumerable:!1,writable:!0,configurable:!0}})}:e.exports=function(t,e){t.super_=e;var r=function(){};r.prototype=e.prototype,t.prototype=new r,t.prototype.constructor=t}},{}],75:[function(t,e,r){e.exports=function(t){return t&&"object"==typeof t&&"function"==typeof t.copy&&"function"==typeof t.fill&&"function"==typeof t.readUInt8}},{}],76:[function(t,e,r){(function(e,n){(function(){var i=/%[sdj%]/g;r.format=function(t){if(!v(t)){for(var e=[],r=0;r<arguments.length;r++)e.push(s(arguments[r]));return e.join(" ")}r=1;for(var n=arguments,a=n.length,o=String(t).replace(i,(function(t){if("%%"===t)return"%";if(r>=a)return t;switch(t){case"%s":return String(n[r++]);case"%d":return Number(n[r++]);case"%j":try{return JSON.stringify(n[r++])}catch(t){return"[Circular]"}default:return t}})),l=n[r];r<a;l=n[++r])g(l)||!b(l)?o+=" "+l:o+=" "+s(l);return o},r.deprecate=function(t,i){if(y(n.process))return function(){return r.deprecate(t,i).apply(this,arguments)};if(!0===e.noDeprecation)return t;var a=!1;return function(){if(!a){if(e.throwDeprecation)throw new Error(i);e.traceDeprecation?console.trace(i):console.error(i),a=!0}return t.apply(this,arguments)}};var a,o={};function s(t,e){var n={seen:[],stylize:c};return arguments.length>=3&&(n.depth=arguments[2]),arguments.length>=4&&(n.colors=arguments[3]),d(e)?n.showHidden=e:e&&r._extend(n,e),y(n.showHidden)&&(n.showHidden=!1),y(n.depth)&&(n.depth=2),y(n.colors)&&(n.colors=!1),y(n.customInspect)&&(n.customInspect=!0),n.colors&&(n.stylize=l),u(n,t,n.depth)}function l(t,e){var r=s.styles[e];return r?"\x1b["+s.colors[r][0]+"m"+t+"\x1b["+s.colors[r][1]+"m":t}function c(t,e){return t}function u(t,e,n){if(t.customInspect&&e&&T(e.inspect)&&e.inspect!==r.inspect&&(!e.constructor||e.constructor.prototype!==e)){var i=e.inspect(n,t);return v(i)||(i=u(t,i,n)),i}var a=function(t,e){if(y(e))return t.stylize("undefined","undefined");if(v(e)){var r="'"+JSON.stringify(e).replace(/^"|"$/g,"").replace(/'/g,"\\'").replace(/\\"/g,'"')+"'";return t.stylize(r,"string")}if(m(e))return t.stylize(""+e,"number");if(d(e))return t.stylize(""+e,"boolean");if(g(e))return t.stylize("null","null")}(t,e);if(a)return a;var o=Object.keys(e),s=function(t){var e={};return t.forEach((function(t,r){e[t]=!0})),e}(o);if(t.showHidden&&(o=Object.getOwnPropertyNames(e)),w(e)&&(o.indexOf("message")>=0||o.indexOf("description")>=0))return f(e);if(0===o.length){if(T(e)){var l=e.name?": "+e.name:"";return t.stylize("[Function"+l+"]","special")}if(x(e))return t.stylize(RegExp.prototype.toString.call(e),"regexp");if(_(e))return t.stylize(Date.prototype.toString.call(e),"date");if(w(e))return f(e)}var c,b="",k=!1,M=["{","}"];(p(e)&&(k=!0,M=["[","]"]),T(e))&&(b=" [Function"+(e.name?": "+e.name:"")+"]");return x(e)&&(b=" "+RegExp.prototype.toString.call(e)),_(e)&&(b=" "+Date.prototype.toUTCString.call(e)),w(e)&&(b=" "+f(e)),0!==o.length||k&&0!=e.length?n<0?x(e)?t.stylize(RegExp.prototype.toString.call(e),"regexp"):t.stylize("[Object]","special"):(t.seen.push(e),c=k?function(t,e,r,n,i){for(var a=[],o=0,s=e.length;o<s;++o)E(e,String(o))?a.push(h(t,e,r,n,String(o),!0)):a.push("");return i.forEach((function(i){i.match(/^\d+$/)||a.push(h(t,e,r,n,i,!0))})),a}(t,e,n,s,o):o.map((function(r){return h(t,e,n,s,r,k)})),t.seen.pop(),function(t,e,r){if(t.reduce((function(t,e){return e.indexOf("\n")>=0&&0,t+e.replace(/\u001b\[\d\d?m/g,"").length+1}),0)>60)return r[0]+(""===e?"":e+"\n ")+" "+t.join(",\n  ")+" "+r[1];return r[0]+e+" "+t.join(", ")+" "+r[1]}(c,b,M)):M[0]+b+M[1]}function f(t){return"["+Error.prototype.toString.call(t)+"]"}function h(t,e,r,n,i,a){var o,s,l;if((l=Object.getOwnPropertyDescriptor(e,i)||{value:e[i]}).get?s=l.set?t.stylize("[Getter/Setter]","special"):t.stylize("[Getter]","special"):l.set&&(s=t.stylize("[Setter]","special")),E(n,i)||(o="["+i+"]"),s||(t.seen.indexOf(l.value)<0?(s=g(r)?u(t,l.value,null):u(t,l.value,r-1)).indexOf("\n")>-1&&(s=a?s.split("\n").map((function(t){return"  "+t})).join("\n").substr(2):"\n"+s.split("\n").map((function(t){return"   "+t})).join("\n")):s=t.stylize("[Circular]","special")),y(o)){if(a&&i.match(/^\d+$/))return s;(o=JSON.stringify(""+i)).match(/^"([a-zA-Z_][a-zA-Z_0-9]*)"$/)?(o=o.substr(1,o.length-2),o=t.stylize(o,"name")):(o=o.replace(/'/g,"\\'").replace(/\\"/g,'"').replace(/(^"|"$)/g,"'"),o=t.stylize(o,"string"))}return o+": "+s}function p(t){return Array.isArray(t)}function d(t){return"boolean"==typeof t}function g(t){return null===t}function m(t){return"number"==typeof t}function v(t){return"string"==typeof t}function y(t){return void 0===t}function x(t){return b(t)&&"[object RegExp]"===k(t)}function b(t){return"object"==typeof t&&null!==t}function _(t){return b(t)&&"[object Date]"===k(t)}function w(t){return b(t)&&("[object Error]"===k(t)||t instanceof Error)}function T(t){return"function"==typeof t}function k(t){return Object.prototype.toString.call(t)}function M(t){return t<10?"0"+t.toString(10):t.toString(10)}r.debuglog=function(t){if(y(a)&&(a=e.env.NODE_DEBUG||""),t=t.toUpperCase(),!o[t])if(new RegExp("\\b"+t+"\\b","i").test(a)){var n=e.pid;o[t]=function(){var e=r.format.apply(r,arguments);console.error("%s %d: %s",t,n,e)}}else o[t]=function(){};return o[t]},r.inspect=s,s.colors={bold:[1,22],italic:[3,23],underline:[4,24],inverse:[7,27],white:[37,39],grey:[90,39],black:[30,39],blue:[34,39],cyan:[36,39],green:[32,39],magenta:[35,39],red:[31,39],yellow:[33,39]},s.styles={special:"cyan",number:"yellow",boolean:"yellow",undefined:"grey",null:"bold",string:"green",date:"magenta",regexp:"red"},r.isArray=p,r.isBoolean=d,r.isNull=g,r.isNullOrUndefined=function(t){return null==t},r.isNumber=m,r.isString=v,r.isSymbol=function(t){return"symbol"==typeof t},r.isUndefined=y,r.isRegExp=x,r.isObject=b,r.isDate=_,r.isError=w,r.isFunction=T,r.isPrimitive=function(t){return null===t||"boolean"==typeof t||"number"==typeof t||"string"==typeof t||"symbol"==typeof t||"undefined"==typeof t},r.isBuffer=t("./support/isBuffer");var A=["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"];function S(){var t=new Date,e=[M(t.getHours()),M(t.getMinutes()),M(t.getSeconds())].join(":");return[t.getDate(),A[t.getMonth()],e].join(" ")}function E(t,e){return Object.prototype.hasOwnProperty.call(t,e)}r.log=function(){console.log("%s - %s",S(),r.format.apply(r,arguments))},r.inherits=t("inherits"),r._extend=function(t,e){if(!e||!b(e))return t;for(var r=Object.keys(e),n=r.length;n--;)t[r[n]]=e[r[n]];return t}}).call(this)}).call(this,t("_process"),"undefined"!=typeof global?global:"undefined"!=typeof self?self:"undefined"!=typeof window?window:{})},{"./support/isBuffer":75,_process:526,inherits:74}],77:[function(t,e,r){e.exports=function(t){return atob(t)}},{}],78:[function(t,e,r){"use strict";e.exports=function(t,e){for(var r=e.length,a=new Array(r+1),o=0;o<r;++o){for(var s=new Array(r+1),l=0;l<=r;++l)s[l]=t[l][o];a[o]=s}a[r]=new Array(r+1);for(o=0;o<=r;++o)a[r][o]=1;var c=new Array(r+1);for(o=0;o<r;++o)c[o]=e[o];c[r]=1;var u=n(a,c),f=i(u[r+1]);0===f&&(f=1);var h=new Array(r+1);for(o=0;o<=r;++o)h[o]=i(u[o])/f;return h};var n=t("robust-linear-solve");function i(t){for(var e=0,r=0;r<t.length;++r)e+=t[r];return e}},{"robust-linear-solve":547}],79:[function(t,e,r){"use strict";r.byteLength=function(t){var e=c(t),r=e[0],n=e[1];return 3*(r+n)/4-n},r.toByteArray=function(t){var e,r,n=c(t),o=n[0],s=n[1],l=new a(function(t,e,r){return 3*(e+r)/4-r}(0,o,s)),u=0,f=s>0?o-4:o;for(r=0;r<f;r+=4)e=i[t.charCodeAt(r)]<<18|i[t.charCodeAt(r+1)]<<12|i[t.charCodeAt(r+2)]<<6|i[t.charCodeAt(r+3)],l[u++]=e>>16&255,l[u++]=e>>8&255,l[u++]=255&e;2===s&&(e=i[t.charCodeAt(r)]<<2|i[t.charCodeAt(r+1)]>>4,l[u++]=255&e);1===s&&(e=i[t.charCodeAt(r)]<<10|i[t.charCodeAt(r+1)]<<4|i[t.charCodeAt(r+2)]>>2,l[u++]=e>>8&255,l[u++]=255&e);return l},r.fromByteArray=function(t){for(var e,r=t.length,i=r%3,a=[],o=0,s=r-i;o<s;o+=16383)a.push(u(t,o,o+16383>s?s:o+16383));1===i?(e=t[r-1],a.push(n[e>>2]+n[e<<4&63]+"==")):2===i&&(e=(t[r-2]<<8)+t[r-1],a.push(n[e>>10]+n[e>>4&63]+n[e<<2&63]+"="));return a.join("")};for(var n=[],i=[],a="undefined"!=typeof Uint8Array?Uint8Array:Array,o="ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/",s=0,l=o.length;s<l;++s)n[s]=o[s],i[o.charCodeAt(s)]=s;function c(t){var e=t.length;if(e%4>0)throw new Error("Invalid string. Length must be a multiple of 4");var r=t.indexOf("=");return-1===r&&(r=e),[r,r===e?0:4-r%4]}function u(t,e,r){for(var i,a,o=[],s=e;s<r;s+=3)i=(t[s]<<16&16711680)+(t[s+1]<<8&65280)+(255&t[s+2]),o.push(n[(a=i)>>18&63]+n[a>>12&63]+n[a>>6&63]+n[63&a]);return o.join("")}i["-".charCodeAt(0)]=62,i["_".charCodeAt(0)]=63},{}],80:[function(t,e,r){"use strict";var n=t("./lib/rationalize");e.exports=function(t,e){return n(t[0].mul(e[1]).add(e[0].mul(t[1])),t[1].mul(e[1]))}},{"./lib/rationalize":90}],81:[function(t,e,r){"use strict";e.exports=function(t,e){return t[0].mul(e[1]).cmp(e[0].mul(t[1]))}},{}],82:[function(t,e,r){"use strict";var n=t("./lib/rationalize");e.exports=function(t,e){return n(t[0].mul(e[1]),t[1].mul(e[0]))}},{"./lib/rationalize":90}],83:[function(t,e,r){"use strict";var n=t("./is-rat"),i=t("./lib/is-bn"),a=t("./lib/num-to-bn"),o=t("./lib/str-to-bn"),s=t("./lib/rationalize"),l=t("./div");e.exports=function t(e,r){if(n(e))return r?l(e,t(r)):[e[0].clone(),e[1].clone()];var c,u,f=0;if(i(e))c=e.clone();else if("string"==typeof e)c=o(e);else{if(0===e)return[a(0),a(1)];if(e===Math.floor(e))c=a(e);else{for(;e!==Math.floor(e);)e*=Math.pow(2,256),f-=256;c=a(e)}}if(n(r))c.mul(r[1]),u=r[0].clone();else if(i(r))u=r.clone();else if("string"==typeof r)u=o(r);else if(r)if(r===Math.floor(r))u=a(r);else{for(;r!==Math.floor(r);)r*=Math.pow(2,256),f+=256;u=a(r)}else u=a(1);f>0?c=c.ushln(f):f<0&&(u=u.ushln(-f));return s(c,u)}},{"./div":82,"./is-rat":84,"./lib/is-bn":88,"./lib/num-to-bn":89,"./lib/rationalize":90,"./lib/str-to-bn":91}],84:[function(t,e,r){"use strict";var n=t("./lib/is-bn");e.exports=function(t){return Array.isArray(t)&&2===t.length&&n(t[0])&&n(t[1])}},{"./lib/is-bn":88}],85:[function(t,e,r){"use strict";var n=t("bn.js");e.exports=function(t){return t.cmp(new n(0))}},{"bn.js":99}],86:[function(t,e,r){"use strict";var n=t("./bn-sign");e.exports=function(t){var e=t.length,r=t.words,i=0;if(1===e)i=r[0];else if(2===e)i=r[0]+67108864*r[1];else for(var a=0;a<e;a++){var o=r[a];i+=o*Math.pow(67108864,a)}return n(t)*i}},{"./bn-sign":85}],87:[function(t,e,r){"use strict";var n=t("double-bits"),i=t("bit-twiddle").countTrailingZeros;e.exports=function(t){var e=i(n.lo(t));if(e<32)return e;var r=i(n.hi(t));if(r>20)return 52;return r+32}},{"bit-twiddle":97,"double-bits":173}],88:[function(t,e,r){"use strict";t("bn.js");e.exports=function(t){return t&&"object"==typeof t&&Boolean(t.words)}},{"bn.js":99}],89:[function(t,e,r){"use strict";var n=t("bn.js"),i=t("double-bits");e.exports=function(t){var e=i.exponent(t);return e<52?new n(t):new n(t*Math.pow(2,52-e)).ushln(e-52)}},{"bn.js":99,"double-bits":173}],90:[function(t,e,r){"use strict";var n=t("./num-to-bn"),i=t("./bn-sign");e.exports=function(t,e){var r=i(t),a=i(e);if(0===r)return[n(0),n(1)];if(0===a)return[n(0),n(0)];a<0&&(t=t.neg(),e=e.neg());var o=t.gcd(e);if(o.cmpn(1))return[t.div(o),e.div(o)];return[t,e]}},{"./bn-sign":85,"./num-to-bn":89}],91:[function(t,e,r){"use strict";var n=t("bn.js");e.exports=function(t){return new n(t)}},{"bn.js":99}],92:[function(t,e,r){"use strict";var n=t("./lib/rationalize");e.exports=function(t,e){return n(t[0].mul(e[0]),t[1].mul(e[1]))}},{"./lib/rationalize":90}],93:[function(t,e,r){"use strict";var n=t("./lib/bn-sign");e.exports=function(t){return n(t[0])*n(t[1])}},{"./lib/bn-sign":85}],94:[function(t,e,r){"use strict";var n=t("./lib/rationalize");e.exports=function(t,e){return n(t[0].mul(e[1]).sub(t[1].mul(e[0])),t[1].mul(e[1]))}},{"./lib/rationalize":90}],95:[function(t,e,r){"use strict";var n=t("./lib/bn-to-num"),i=t("./lib/ctz");e.exports=function(t){var e=t[0],r=t[1];if(0===e.cmpn(0))return 0;var a=e.abs().divmod(r.abs()),o=a.div,s=n(o),l=a.mod,c=e.negative!==r.negative?-1:1;if(0===l.cmpn(0))return c*s;if(s){var u=i(s)+4,f=n(l.ushln(u).divRound(r));return c*(s+f*Math.pow(2,-u))}var h=r.bitLength()-l.bitLength()+53;f=n(l.ushln(h).divRound(r));return h<1023?c*f*Math.pow(2,-h):(f*=Math.pow(2,-1023),c*f*Math.pow(2,1023-h))}},{"./lib/bn-to-num":86,"./lib/ctz":87}],96:[function(t,e,r){"use strict";function n(t,e,r,n,i){var a=["function ",t,"(a,l,h,",n.join(","),"){",i?"":"var i=",r?"l-1":"h+1",";while(l<=h){var m=(l+h)>>>1,x=a[m]"];return i?e.indexOf("c")<0?a.push(";if(x===y){return m}else if(x<=y){"):a.push(";var p=c(x,y);if(p===0){return m}else if(p<=0){"):a.push(";if(",e,"){i=m;"),r?a.push("l=m+1}else{h=m-1}"):a.push("h=m-1}else{l=m+1}"),a.push("}"),i?a.push("return -1};"):a.push("return i};"),a.join("")}function i(t,e,r,i){return new Function([n("A","x"+t+"y",e,["y"],i),n("P","c(x,y)"+t+"0",e,["y","c"],i),"function dispatchBsearch",r,"(a,y,c,l,h){if(typeof(c)==='function'){return P(a,(l===void 0)?0:l|0,(h===void 0)?a.length-1:h|0,y,c)}else{return A(a,(c===void 0)?0:c|0,(l===void 0)?a.length-1:l|0,y)}}return dispatchBsearch",r].join(""))()}e.exports={ge:i(">=",!1,"GE"),gt:i(">",!1,"GT"),lt:i("<",!0,"LT"),le:i("<=",!0,"LE"),eq:i("-",!0,"EQ",!0)}},{}],97:[function(t,e,r){"use strict";function n(t){var e=32;return(t&=-t)&&e--,65535&t&&(e-=16),16711935&t&&(e-=8),252645135&t&&(e-=4),858993459&t&&(e-=2),1431655765&t&&(e-=1),e}r.INT_BITS=32,r.INT_MAX=2147483647,r.INT_MIN=-1<<31,r.sign=function(t){return(t>0)-(t<0)},r.abs=function(t){var e=t>>31;return(t^e)-e},r.min=function(t,e){return e^(t^e)&-(t<e)},r.max=function(t,e){return t^(t^e)&-(t<e)},r.isPow2=function(t){return!(t&t-1||!t)},r.log2=function(t){var e,r;return e=(t>65535)<<4,e|=r=((t>>>=e)>255)<<3,e|=r=((t>>>=r)>15)<<2,(e|=r=((t>>>=r)>3)<<1)|(t>>>=r)>>1},r.log10=function(t){return t>=1e9?9:t>=1e8?8:t>=1e7?7:t>=1e6?6:t>=1e5?5:t>=1e4?4:t>=1e3?3:t>=100?2:t>=10?1:0},r.popCount=function(t){return 16843009*((t=(858993459&(t-=t>>>1&1431655765))+(t>>>2&858993459))+(t>>>4)&252645135)>>>24},r.countTrailingZeros=n,r.nextPow2=function(t){return t+=0===t,--t,t|=t>>>1,t|=t>>>2,t|=t>>>4,t|=t>>>8,(t|=t>>>16)+1},r.prevPow2=function(t){return t|=t>>>1,t|=t>>>2,t|=t>>>4,t|=t>>>8,(t|=t>>>16)-(t>>>1)},r.parity=function(t){return t^=t>>>16,t^=t>>>8,t^=t>>>4,27030>>>(t&=15)&1};var i=new Array(256);!function(t){for(var e=0;e<256;++e){var r=e,n=e,i=7;for(r>>>=1;r;r>>>=1)n<<=1,n|=1&r,--i;t[e]=n<<i&255}}(i),r.reverse=function(t){return i[255&t]<<24|i[t>>>8&255]<<16|i[t>>>16&255]<<8|i[t>>>24&255]},r.interleave2=function(t,e){return(t=1431655765&((t=858993459&((t=252645135&((t=16711935&((t&=65535)|t<<8))|t<<4))|t<<2))|t<<1))|(e=1431655765&((e=858993459&((e=252645135&((e=16711935&((e&=65535)|e<<8))|e<<4))|e<<2))|e<<1))<<1},r.deinterleave2=function(t,e){return(t=65535&((t=16711935&((t=252645135&((t=858993459&((t=t>>>e&1431655765)|t>>>1))|t>>>2))|t>>>4))|t>>>16))<<16>>16},r.interleave3=function(t,e,r){return t=1227133513&((t=3272356035&((t=251719695&((t=4278190335&((t&=1023)|t<<16))|t<<8))|t<<4))|t<<2),(t|=(e=1227133513&((e=3272356035&((e=251719695&((e=4278190335&((e&=1023)|e<<16))|e<<8))|e<<4))|e<<2))<<1)|(r=1227133513&((r=3272356035&((r=251719695&((r=4278190335&((r&=1023)|r<<16))|r<<8))|r<<4))|r<<2))<<2},r.deinterleave3=function(t,e){return(t=1023&((t=4278190335&((t=251719695&((t=3272356035&((t=t>>>e&1227133513)|t>>>2))|t>>>4))|t>>>8))|t>>>16))<<22>>22},r.nextCombination=function(t){var e=t|t-1;return e+1|(~e&-~e)-1>>>n(t)+1}},{}],98:[function(t,e,r){"use strict";var n=t("clamp");e.exports=function(t,e){e||(e={});var r,o,s,l,c,u,f,h,p,d,g,m=null==e.cutoff?.25:e.cutoff,v=null==e.radius?8:e.radius,y=e.channel||0;if(ArrayBuffer.isView(t)||Array.isArray(t)){if(!e.width||!e.height)throw Error("For raw data width and height should be provided by options");r=e.width,o=e.height,l=t,u=e.stride?e.stride:Math.floor(t.length/r/o)}else window.HTMLCanvasElement&&t instanceof window.HTMLCanvasElement?(f=(h=t).getContext("2d"),r=h.width,o=h.height,p=f.getImageData(0,0,r,o),l=p.data,u=4):window.CanvasRenderingContext2D&&t instanceof window.CanvasRenderingContext2D?(h=t.canvas,f=t,r=h.width,o=h.height,p=f.getImageData(0,0,r,o),l=p.data,u=4):window.ImageData&&t instanceof window.ImageData&&(p=t,r=t.width,o=t.height,l=p.data,u=4);if(s=Math.max(r,o),window.Uint8ClampedArray&&l instanceof window.Uint8ClampedArray||window.Uint8Array&&l instanceof window.Uint8Array)for(c=l,l=Array(r*o),d=0,g=c.length;d<g;d++)l[d]=c[d*u+y]/255;else if(1!==u)throw Error("Raw data can have only 1 value per pixel");var x=Array(r*o),b=Array(r*o),_=Array(s),w=Array(s),T=Array(s+1),k=Array(s);for(d=0,g=r*o;d<g;d++){var M=l[d];x[d]=1===M?0:0===M?i:Math.pow(Math.max(0,.5-M),2),b[d]=1===M?i:0===M?0:Math.pow(Math.max(0,M-.5),2)}a(x,r,o,_,w,k,T),a(b,r,o,_,w,k,T);var A=window.Float32Array?new Float32Array(r*o):new Array(r*o);for(d=0,g=r*o;d<g;d++)A[d]=n(1-((x[d]-b[d])/v+m),0,1);return A};var i=1e20;function a(t,e,r,n,i,a,s){for(var l=0;l<e;l++){for(var c=0;c<r;c++)n[c]=t[c*e+l];for(o(n,i,a,s,r),c=0;c<r;c++)t[c*e+l]=i[c]}for(c=0;c<r;c++){for(l=0;l<e;l++)n[l]=t[c*e+l];for(o(n,i,a,s,e),l=0;l<e;l++)t[c*e+l]=Math.sqrt(i[l])}}function o(t,e,r,n,a){r[0]=0,n[0]=-i,n[1]=+i;for(var o=1,s=0;o<a;o++){for(var l=(t[o]+o*o-(t[r[s]]+r[s]*r[s]))/(2*o-2*r[s]);l<=n[s];)s--,l=(t[o]+o*o-(t[r[s]]+r[s]*r[s]))/(2*o-2*r[s]);r[++s]=o,n[s]=l,n[s+1]=+i}for(o=0,s=0;o<a;o++){for(;n[s+1]<o;)s++;e[o]=(o-r[s])*(o-r[s])+t[r[s]]}}},{clamp:120}],99:[function(t,e,r){!function(e,r){"use strict";function n(t,e){if(!t)throw new Error(e||"Assertion failed")}function i(t,e){t.super_=e;var r=function(){};r.prototype=e.prototype,t.prototype=new r,t.prototype.constructor=t}function a(t,e,r){if(a.isBN(t))return t;this.negative=0,this.words=null,this.length=0,this.red=null,null!==t&&("le"!==e&&"be"!==e||(r=e,e=10),this._init(t||0,e||10,r||"be"))}var o;"object"==typeof e?e.exports=a:r.BN=a,a.BN=a,a.wordSize=26;try{o=t("buffer").Buffer}catch(t){}function s(t,e,r){for(var n=0,i=Math.min(t.length,r),a=e;a<i;a++){var o=t.charCodeAt(a)-48;n<<=4,n|=o>=49&&o<=54?o-49+10:o>=17&&o<=22?o-17+10:15&o}return n}function l(t,e,r,n){for(var i=0,a=Math.min(t.length,r),o=e;o<a;o++){var s=t.charCodeAt(o)-48;i*=n,i+=s>=49?s-49+10:s>=17?s-17+10:s}return i}a.isBN=function(t){return t instanceof a||null!==t&&"object"==typeof t&&t.constructor.wordSize===a.wordSize&&Array.isArray(t.words)},a.max=function(t,e){return t.cmp(e)>0?t:e},a.min=function(t,e){return t.cmp(e)<0?t:e},a.prototype._init=function(t,e,r){if("number"==typeof t)return this._initNumber(t,e,r);if("object"==typeof t)return this._initArray(t,e,r);"hex"===e&&(e=16),n(e===(0|e)&&e>=2&&e<=36);var i=0;"-"===(t=t.toString().replace(/\s+/g,""))[0]&&i++,16===e?this._parseHex(t,i):this._parseBase(t,e,i),"-"===t[0]&&(this.negative=1),this.strip(),"le"===r&&this._initArray(this.toArray(),e,r)},a.prototype._initNumber=function(t,e,r){t<0&&(this.negative=1,t=-t),t<67108864?(this.words=[67108863&t],this.length=1):t<4503599627370496?(this.words=[67108863&t,t/67108864&67108863],this.length=2):(n(t<9007199254740992),this.words=[67108863&t,t/67108864&67108863,1],this.length=3),"le"===r&&this._initArray(this.toArray(),e,r)},a.prototype._initArray=function(t,e,r){if(n("number"==typeof t.length),t.length<=0)return this.words=[0],this.length=1,this;this.length=Math.ceil(t.length/3),this.words=new Array(this.length);for(var i=0;i<this.length;i++)this.words[i]=0;var a,o,s=0;if("be"===r)for(i=t.length-1,a=0;i>=0;i-=3)o=t[i]|t[i-1]<<8|t[i-2]<<16,this.words[a]|=o<<s&67108863,this.words[a+1]=o>>>26-s&67108863,(s+=24)>=26&&(s-=26,a++);else if("le"===r)for(i=0,a=0;i<t.length;i+=3)o=t[i]|t[i+1]<<8|t[i+2]<<16,this.words[a]|=o<<s&67108863,this.words[a+1]=o>>>26-s&67108863,(s+=24)>=26&&(s-=26,a++);return this.strip()},a.prototype._parseHex=function(t,e){this.length=Math.ceil((t.length-e)/6),this.words=new Array(this.length);for(var r=0;r<this.length;r++)this.words[r]=0;var n,i,a=0;for(r=t.length-6,n=0;r>=e;r-=6)i=s(t,r,r+6),this.words[n]|=i<<a&67108863,this.words[n+1]|=i>>>26-a&4194303,(a+=24)>=26&&(a-=26,n++);r+6!==e&&(i=s(t,e,r+6),this.words[n]|=i<<a&67108863,this.words[n+1]|=i>>>26-a&4194303),this.strip()},a.prototype._parseBase=function(t,e,r){this.words=[0],this.length=1;for(var n=0,i=1;i<=67108863;i*=e)n++;n--,i=i/e|0;for(var a=t.length-r,o=a%n,s=Math.min(a,a-o)+r,c=0,u=r;u<s;u+=n)c=l(t,u,u+n,e),this.imuln(i),this.words[0]+c<67108864?this.words[0]+=c:this._iaddn(c);if(0!==o){var f=1;for(c=l(t,u,t.length,e),u=0;u<o;u++)f*=e;this.imuln(f),this.words[0]+c<67108864?this.words[0]+=c:this._iaddn(c)}},a.prototype.copy=function(t){t.words=new Array(this.length);for(var e=0;e<this.length;e++)t.words[e]=this.words[e];t.length=this.length,t.negative=this.negative,t.red=this.red},a.prototype.clone=function(){var t=new a(null);return this.copy(t),t},a.prototype._expand=function(t){for(;this.length<t;)this.words[this.length++]=0;return this},a.prototype.strip=function(){for(;this.length>1&&0===this.words[this.length-1];)this.length--;return this._normSign()},a.prototype._normSign=function(){return 1===this.length&&0===this.words[0]&&(this.negative=0),this},a.prototype.inspect=function(){return(this.red?"<BN-R: ":"<BN: ")+this.toString(16)+">"};var c=["","0","00","000","0000","00000","000000","0000000","00000000","000000000","0000000000","00000000000","000000000000","0000000000000","00000000000000","000000000000000","0000000000000000","00000000000000000","000000000000000000","0000000000000000000","00000000000000000000","000000000000000000000","0000000000000000000000","00000000000000000000000","000000000000000000000000","0000000000000000000000000"],u=[0,0,25,16,12,11,10,9,8,8,7,7,7,7,6,6,6,6,6,6,6,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5,5],f=[0,0,33554432,43046721,16777216,48828125,60466176,40353607,16777216,43046721,1e7,19487171,35831808,62748517,7529536,11390625,16777216,24137569,34012224,47045881,64e6,4084101,5153632,6436343,7962624,9765625,11881376,14348907,17210368,20511149,243e5,28629151,33554432,39135393,45435424,52521875,60466176];function h(t,e,r){r.negative=e.negative^t.negative;var n=t.length+e.length|0;r.length=n,n=n-1|0;var i=0|t.words[0],a=0|e.words[0],o=i*a,s=67108863&o,l=o/67108864|0;r.words[0]=s;for(var c=1;c<n;c++){for(var u=l>>>26,f=67108863&l,h=Math.min(c,e.length-1),p=Math.max(0,c-t.length+1);p<=h;p++){var d=c-p|0;u+=(o=(i=0|t.words[d])*(a=0|e.words[p])+f)/67108864|0,f=67108863&o}r.words[c]=0|f,l=0|u}return 0!==l?r.words[c]=0|l:r.length--,r.strip()}a.prototype.toString=function(t,e){var r;if(e=0|e||1,16===(t=t||10)||"hex"===t){r="";for(var i=0,a=0,o=0;o<this.length;o++){var s=this.words[o],l=(16777215&(s<<i|a)).toString(16);r=0!==(a=s>>>24-i&16777215)||o!==this.length-1?c[6-l.length]+l+r:l+r,(i+=2)>=26&&(i-=26,o--)}for(0!==a&&(r=a.toString(16)+r);r.length%e!=0;)r="0"+r;return 0!==this.negative&&(r="-"+r),r}if(t===(0|t)&&t>=2&&t<=36){var h=u[t],p=f[t];r="";var d=this.clone();for(d.negative=0;!d.isZero();){var g=d.modn(p).toString(t);r=(d=d.idivn(p)).isZero()?g+r:c[h-g.length]+g+r}for(this.isZero()&&(r="0"+r);r.length%e!=0;)r="0"+r;return 0!==this.negative&&(r="-"+r),r}n(!1,"Base should be between 2 and 36")},a.prototype.toNumber=function(){var t=this.words[0];return 2===this.length?t+=67108864*this.words[1]:3===this.length&&1===this.words[2]?t+=4503599627370496+67108864*this.words[1]:this.length>2&&n(!1,"Number can only safely store up to 53 bits"),0!==this.negative?-t:t},a.prototype.toJSON=function(){return this.toString(16)},a.prototype.toBuffer=function(t,e){return n("undefined"!=typeof o),this.toArrayLike(o,t,e)},a.prototype.toArray=function(t,e){return this.toArrayLike(Array,t,e)},a.prototype.toArrayLike=function(t,e,r){var i=this.byteLength(),a=r||Math.max(1,i);n(i<=a,"byte array longer than desired length"),n(a>0,"Requested array length <= 0"),this.strip();var o,s,l="le"===e,c=new t(a),u=this.clone();if(l){for(s=0;!u.isZero();s++)o=u.andln(255),u.iushrn(8),c[s]=o;for(;s<a;s++)c[s]=0}else{for(s=0;s<a-i;s++)c[s]=0;for(s=0;!u.isZero();s++)o=u.andln(255),u.iushrn(8),c[a-s-1]=o}return c},Math.clz32?a.prototype._countBits=function(t){return 32-Math.clz32(t)}:a.prototype._countBits=function(t){var e=t,r=0;return e>=4096&&(r+=13,e>>>=13),e>=64&&(r+=7,e>>>=7),e>=8&&(r+=4,e>>>=4),e>=2&&(r+=2,e>>>=2),r+e},a.prototype._zeroBits=function(t){if(0===t)return 26;var e=t,r=0;return 0==(8191&e)&&(r+=13,e>>>=13),0==(127&e)&&(r+=7,e>>>=7),0==(15&e)&&(r+=4,e>>>=4),0==(3&e)&&(r+=2,e>>>=2),0==(1&e)&&r++,r},a.prototype.bitLength=function(){var t=this.words[this.length-1],e=this._countBits(t);return 26*(this.length-1)+e},a.prototype.zeroBits=function(){if(this.isZero())return 0;for(var t=0,e=0;e<this.length;e++){var r=this._zeroBits(this.words[e]);if(t+=r,26!==r)break}return t},a.prototype.byteLength=function(){return Math.ceil(this.bitLength()/8)},a.prototype.toTwos=function(t){return 0!==this.negative?this.abs().inotn(t).iaddn(1):this.clone()},a.prototype.fromTwos=function(t){return this.testn(t-1)?this.notn(t).iaddn(1).ineg():this.clone()},a.prototype.isNeg=function(){return 0!==this.negative},a.prototype.neg=function(){return this.clone().ineg()},a.prototype.ineg=function(){return this.isZero()||(this.negative^=1),this},a.prototype.iuor=function(t){for(;this.length<t.length;)this.words[this.length++]=0;for(var e=0;e<t.length;e++)this.words[e]=this.words[e]|t.words[e];return this.strip()},a.prototype.ior=function(t){return n(0==(this.negative|t.negative)),this.iuor(t)},a.prototype.or=function(t){return this.length>t.length?this.clone().ior(t):t.clone().ior(this)},a.prototype.uor=function(t){return this.length>t.length?this.clone().iuor(t):t.clone().iuor(this)},a.prototype.iuand=function(t){var e;e=this.length>t.length?t:this;for(var r=0;r<e.length;r++)this.words[r]=this.words[r]&t.words[r];return this.length=e.length,this.strip()},a.prototype.iand=function(t){return n(0==(this.negative|t.negative)),this.iuand(t)},a.prototype.and=function(t){return this.length>t.length?this.clone().iand(t):t.clone().iand(this)},a.prototype.uand=function(t){return this.length>t.length?this.clone().iuand(t):t.clone().iuand(this)},a.prototype.iuxor=function(t){var e,r;this.length>t.length?(e=this,r=t):(e=t,r=this);for(var n=0;n<r.length;n++)this.words[n]=e.words[n]^r.words[n];if(this!==e)for(;n<e.length;n++)this.words[n]=e.words[n];return this.length=e.length,this.strip()},a.prototype.ixor=function(t){return n(0==(this.negative|t.negative)),this.iuxor(t)},a.prototype.xor=function(t){return this.length>t.length?this.clone().ixor(t):t.clone().ixor(this)},a.prototype.uxor=function(t){return this.length>t.length?this.clone().iuxor(t):t.clone().iuxor(this)},a.prototype.inotn=function(t){n("number"==typeof t&&t>=0);var e=0|Math.ceil(t/26),r=t%26;this._expand(e),r>0&&e--;for(var i=0;i<e;i++)this.words[i]=67108863&~this.words[i];return r>0&&(this.words[i]=~this.words[i]&67108863>>26-r),this.strip()},a.prototype.notn=function(t){return this.clone().inotn(t)},a.prototype.setn=function(t,e){n("number"==typeof t&&t>=0);var r=t/26|0,i=t%26;return this._expand(r+1),this.words[r]=e?this.words[r]|1<<i:this.words[r]&~(1<<i),this.strip()},a.prototype.iadd=function(t){var e,r,n;if(0!==this.negative&&0===t.negative)return this.negative=0,e=this.isub(t),this.negative^=1,this._normSign();if(0===this.negative&&0!==t.negative)return t.negative=0,e=this.isub(t),t.negative=1,e._normSign();this.length>t.length?(r=this,n=t):(r=t,n=this);for(var i=0,a=0;a<n.length;a++)e=(0|r.words[a])+(0|n.words[a])+i,this.words[a]=67108863&e,i=e>>>26;for(;0!==i&&a<r.length;a++)e=(0|r.words[a])+i,this.words[a]=67108863&e,i=e>>>26;if(this.length=r.length,0!==i)this.words[this.length]=i,this.length++;else if(r!==this)for(;a<r.length;a++)this.words[a]=r.words[a];return this},a.prototype.add=function(t){var e;return 0!==t.negative&&0===this.negative?(t.negative=0,e=this.sub(t),t.negative^=1,e):0===t.negative&&0!==this.negative?(this.negative=0,e=t.sub(this),this.negative=1,e):this.length>t.length?this.clone().iadd(t):t.clone().iadd(this)},a.prototype.isub=function(t){if(0!==t.negative){t.negative=0;var e=this.iadd(t);return t.negative=1,e._normSign()}if(0!==this.negative)return this.negative=0,this.iadd(t),this.negative=1,this._normSign();var r,n,i=this.cmp(t);if(0===i)return this.negative=0,this.length=1,this.words[0]=0,this;i>0?(r=this,n=t):(r=t,n=this);for(var a=0,o=0;o<n.length;o++)a=(e=(0|r.words[o])-(0|n.words[o])+a)>>26,this.words[o]=67108863&e;for(;0!==a&&o<r.length;o++)a=(e=(0|r.words[o])+a)>>26,this.words[o]=67108863&e;if(0===a&&o<r.length&&r!==this)for(;o<r.length;o++)this.words[o]=r.words[o];return this.length=Math.max(this.length,o),r!==this&&(this.negative=1),this.strip()},a.prototype.sub=function(t){return this.clone().isub(t)};var p=function(t,e,r){var n,i,a,o=t.words,s=e.words,l=r.words,c=0,u=0|o[0],f=8191&u,h=u>>>13,p=0|o[1],d=8191&p,g=p>>>13,m=0|o[2],v=8191&m,y=m>>>13,x=0|o[3],b=8191&x,_=x>>>13,w=0|o[4],T=8191&w,k=w>>>13,M=0|o[5],A=8191&M,S=M>>>13,E=0|o[6],C=8191&E,L=E>>>13,I=0|o[7],P=8191&I,z=I>>>13,O=0|o[8],D=8191&O,R=O>>>13,F=0|o[9],B=8191&F,N=F>>>13,j=0|s[0],U=8191&j,V=j>>>13,q=0|s[1],H=8191&q,G=q>>>13,Y=0|s[2],W=8191&Y,X=Y>>>13,Z=0|s[3],J=8191&Z,K=Z>>>13,Q=0|s[4],$=8191&Q,tt=Q>>>13,et=0|s[5],rt=8191&et,nt=et>>>13,it=0|s[6],at=8191&it,ot=it>>>13,st=0|s[7],lt=8191&st,ct=st>>>13,ut=0|s[8],ft=8191&ut,ht=ut>>>13,pt=0|s[9],dt=8191&pt,gt=pt>>>13;r.negative=t.negative^e.negative,r.length=19;var mt=(c+(n=Math.imul(f,U))|0)+((8191&(i=(i=Math.imul(f,V))+Math.imul(h,U)|0))<<13)|0;c=((a=Math.imul(h,V))+(i>>>13)|0)+(mt>>>26)|0,mt&=67108863,n=Math.imul(d,U),i=(i=Math.imul(d,V))+Math.imul(g,U)|0,a=Math.imul(g,V);var vt=(c+(n=n+Math.imul(f,H)|0)|0)+((8191&(i=(i=i+Math.imul(f,G)|0)+Math.imul(h,H)|0))<<13)|0;c=((a=a+Math.imul(h,G)|0)+(i>>>13)|0)+(vt>>>26)|0,vt&=67108863,n=Math.imul(v,U),i=(i=Math.imul(v,V))+Math.imul(y,U)|0,a=Math.imul(y,V),n=n+Math.imul(d,H)|0,i=(i=i+Math.imul(d,G)|0)+Math.imul(g,H)|0,a=a+Math.imul(g,G)|0;var yt=(c+(n=n+Math.imul(f,W)|0)|0)+((8191&(i=(i=i+Math.imul(f,X)|0)+Math.imul(h,W)|0))<<13)|0;c=((a=a+Math.imul(h,X)|0)+(i>>>13)|0)+(yt>>>26)|0,yt&=67108863,n=Math.imul(b,U),i=(i=Math.imul(b,V))+Math.imul(_,U)|0,a=Math.imul(_,V),n=n+Math.imul(v,H)|0,i=(i=i+Math.imul(v,G)|0)+Math.imul(y,H)|0,a=a+Math.imul(y,G)|0,n=n+Math.imul(d,W)|0,i=(i=i+Math.imul(d,X)|0)+Math.imul(g,W)|0,a=a+Math.imul(g,X)|0;var xt=(c+(n=n+Math.imul(f,J)|0)|0)+((8191&(i=(i=i+Math.imul(f,K)|0)+Math.imul(h,J)|0))<<13)|0;c=((a=a+Math.imul(h,K)|0)+(i>>>13)|0)+(xt>>>26)|0,xt&=67108863,n=Math.imul(T,U),i=(i=Math.imul(T,V))+Math.imul(k,U)|0,a=Math.imul(k,V),n=n+Math.imul(b,H)|0,i=(i=i+Math.imul(b,G)|0)+Math.imul(_,H)|0,a=a+Math.imul(_,G)|0,n=n+Math.imul(v,W)|0,i=(i=i+Math.imul(v,X)|0)+Math.imul(y,W)|0,a=a+Math.imul(y,X)|0,n=n+Math.imul(d,J)|0,i=(i=i+Math.imul(d,K)|0)+Math.imul(g,J)|0,a=a+Math.imul(g,K)|0;var bt=(c+(n=n+Math.imul(f,$)|0)|0)+((8191&(i=(i=i+Math.imul(f,tt)|0)+Math.imul(h,$)|0))<<13)|0;c=((a=a+Math.imul(h,tt)|0)+(i>>>13)|0)+(bt>>>26)|0,bt&=67108863,n=Math.imul(A,U),i=(i=Math.imul(A,V))+Math.imul(S,U)|0,a=Math.imul(S,V),n=n+Math.imul(T,H)|0,i=(i=i+Math.imul(T,G)|0)+Math.imul(k,H)|0,a=a+Math.imul(k,G)|0,n=n+Math.imul(b,W)|0,i=(i=i+Math.imul(b,X)|0)+Math.imul(_,W)|0,a=a+Math.imul(_,X)|0,n=n+Math.imul(v,J)|0,i=(i=i+Math.imul(v,K)|0)+Math.imul(y,J)|0,a=a+Math.imul(y,K)|0,n=n+Math.imul(d,$)|0,i=(i=i+Math.imul(d,tt)|0)+Math.imul(g,$)|0,a=a+Math.imul(g,tt)|0;var _t=(c+(n=n+Math.imul(f,rt)|0)|0)+((8191&(i=(i=i+Math.imul(f,nt)|0)+Math.imul(h,rt)|0))<<13)|0;c=((a=a+Math.imul(h,nt)|0)+(i>>>13)|0)+(_t>>>26)|0,_t&=67108863,n=Math.imul(C,U),i=(i=Math.imul(C,V))+Math.imul(L,U)|0,a=Math.imul(L,V),n=n+Math.imul(A,H)|0,i=(i=i+Math.imul(A,G)|0)+Math.imul(S,H)|0,a=a+Math.imul(S,G)|0,n=n+Math.imul(T,W)|0,i=(i=i+Math.imul(T,X)|0)+Math.imul(k,W)|0,a=a+Math.imul(k,X)|0,n=n+Math.imul(b,J)|0,i=(i=i+Math.imul(b,K)|0)+Math.imul(_,J)|0,a=a+Math.imul(_,K)|0,n=n+Math.imul(v,$)|0,i=(i=i+Math.imul(v,tt)|0)+Math.imul(y,$)|0,a=a+Math.imul(y,tt)|0,n=n+Math.imul(d,rt)|0,i=(i=i+Math.imul(d,nt)|0)+Math.imul(g,rt)|0,a=a+Math.imul(g,nt)|0;var wt=(c+(n=n+Math.imul(f,at)|0)|0)+((8191&(i=(i=i+Math.imul(f,ot)|0)+Math.imul(h,at)|0))<<13)|0;c=((a=a+Math.imul(h,ot)|0)+(i>>>13)|0)+(wt>>>26)|0,wt&=67108863,n=Math.imul(P,U),i=(i=Math.imul(P,V))+Math.imul(z,U)|0,a=Math.imul(z,V),n=n+Math.imul(C,H)|0,i=(i=i+Math.imul(C,G)|0)+Math.imul(L,H)|0,a=a+Math.imul(L,G)|0,n=n+Math.imul(A,W)|0,i=(i=i+Math.imul(A,X)|0)+Math.imul(S,W)|0,a=a+Math.imul(S,X)|0,n=n+Math.imul(T,J)|0,i=(i=i+Math.imul(T,K)|0)+Math.imul(k,J)|0,a=a+Math.imul(k,K)|0,n=n+Math.imul(b,$)|0,i=(i=i+Math.imul(b,tt)|0)+Math.imul(_,$)|0,a=a+Math.imul(_,tt)|0,n=n+Math.imul(v,rt)|0,i=(i=i+Math.imul(v,nt)|0)+Math.imul(y,rt)|0,a=a+Math.imul(y,nt)|0,n=n+Math.imul(d,at)|0,i=(i=i+Math.imul(d,ot)|0)+Math.imul(g,at)|0,a=a+Math.imul(g,ot)|0;var Tt=(c+(n=n+Math.imul(f,lt)|0)|0)+((8191&(i=(i=i+Math.imul(f,ct)|0)+Math.imul(h,lt)|0))<<13)|0;c=((a=a+Math.imul(h,ct)|0)+(i>>>13)|0)+(Tt>>>26)|0,Tt&=67108863,n=Math.imul(D,U),i=(i=Math.imul(D,V))+Math.imul(R,U)|0,a=Math.imul(R,V),n=n+Math.imul(P,H)|0,i=(i=i+Math.imul(P,G)|0)+Math.imul(z,H)|0,a=a+Math.imul(z,G)|0,n=n+Math.imul(C,W)|0,i=(i=i+Math.imul(C,X)|0)+Math.imul(L,W)|0,a=a+Math.imul(L,X)|0,n=n+Math.imul(A,J)|0,i=(i=i+Math.imul(A,K)|0)+Math.imul(S,J)|0,a=a+Math.imul(S,K)|0,n=n+Math.imul(T,$)|0,i=(i=i+Math.imul(T,tt)|0)+Math.imul(k,$)|0,a=a+Math.imul(k,tt)|0,n=n+Math.imul(b,rt)|0,i=(i=i+Math.imul(b,nt)|0)+Math.imul(_,rt)|0,a=a+Math.imul(_,nt)|0,n=n+Math.imul(v,at)|0,i=(i=i+Math.imul(v,ot)|0)+Math.imul(y,at)|0,a=a+Math.imul(y,ot)|0,n=n+Math.imul(d,lt)|0,i=(i=i+Math.imul(d,ct)|0)+Math.imul(g,lt)|0,a=a+Math.imul(g,ct)|0;var kt=(c+(n=n+Math.imul(f,ft)|0)|0)+((8191&(i=(i=i+Math.imul(f,ht)|0)+Math.imul(h,ft)|0))<<13)|0;c=((a=a+Math.imul(h,ht)|0)+(i>>>13)|0)+(kt>>>26)|0,kt&=67108863,n=Math.imul(B,U),i=(i=Math.imul(B,V))+Math.imul(N,U)|0,a=Math.imul(N,V),n=n+Math.imul(D,H)|0,i=(i=i+Math.imul(D,G)|0)+Math.imul(R,H)|0,a=a+Math.imul(R,G)|0,n=n+Math.imul(P,W)|0,i=(i=i+Math.imul(P,X)|0)+Math.imul(z,W)|0,a=a+Math.imul(z,X)|0,n=n+Math.imul(C,J)|0,i=(i=i+Math.imul(C,K)|0)+Math.imul(L,J)|0,a=a+Math.imul(L,K)|0,n=n+Math.imul(A,$)|0,i=(i=i+Math.imul(A,tt)|0)+Math.imul(S,$)|0,a=a+Math.imul(S,tt)|0,n=n+Math.imul(T,rt)|0,i=(i=i+Math.imul(T,nt)|0)+Math.imul(k,rt)|0,a=a+Math.imul(k,nt)|0,n=n+Math.imul(b,at)|0,i=(i=i+Math.imul(b,ot)|0)+Math.imul(_,at)|0,a=a+Math.imul(_,ot)|0,n=n+Math.imul(v,lt)|0,i=(i=i+Math.imul(v,ct)|0)+Math.imul(y,lt)|0,a=a+Math.imul(y,ct)|0,n=n+Math.imul(d,ft)|0,i=(i=i+Math.imul(d,ht)|0)+Math.imul(g,ft)|0,a=a+Math.imul(g,ht)|0;var Mt=(c+(n=n+Math.imul(f,dt)|0)|0)+((8191&(i=(i=i+Math.imul(f,gt)|0)+Math.imul(h,dt)|0))<<13)|0;c=((a=a+Math.imul(h,gt)|0)+(i>>>13)|0)+(Mt>>>26)|0,Mt&=67108863,n=Math.imul(B,H),i=(i=Math.imul(B,G))+Math.imul(N,H)|0,a=Math.imul(N,G),n=n+Math.imul(D,W)|0,i=(i=i+Math.imul(D,X)|0)+Math.imul(R,W)|0,a=a+Math.imul(R,X)|0,n=n+Math.imul(P,J)|0,i=(i=i+Math.imul(P,K)|0)+Math.imul(z,J)|0,a=a+Math.imul(z,K)|0,n=n+Math.imul(C,$)|0,i=(i=i+Math.imul(C,tt)|0)+Math.imul(L,$)|0,a=a+Math.imul(L,tt)|0,n=n+Math.imul(A,rt)|0,i=(i=i+Math.imul(A,nt)|0)+Math.imul(S,rt)|0,a=a+Math.imul(S,nt)|0,n=n+Math.imul(T,at)|0,i=(i=i+Math.imul(T,ot)|0)+Math.imul(k,at)|0,a=a+Math.imul(k,ot)|0,n=n+Math.imul(b,lt)|0,i=(i=i+Math.imul(b,ct)|0)+Math.imul(_,lt)|0,a=a+Math.imul(_,ct)|0,n=n+Math.imul(v,ft)|0,i=(i=i+Math.imul(v,ht)|0)+Math.imul(y,ft)|0,a=a+Math.imul(y,ht)|0;var At=(c+(n=n+Math.imul(d,dt)|0)|0)+((8191&(i=(i=i+Math.imul(d,gt)|0)+Math.imul(g,dt)|0))<<13)|0;c=((a=a+Math.imul(g,gt)|0)+(i>>>13)|0)+(At>>>26)|0,At&=67108863,n=Math.imul(B,W),i=(i=Math.imul(B,X))+Math.imul(N,W)|0,a=Math.imul(N,X),n=n+Math.imul(D,J)|0,i=(i=i+Math.imul(D,K)|0)+Math.imul(R,J)|0,a=a+Math.imul(R,K)|0,n=n+Math.imul(P,$)|0,i=(i=i+Math.imul(P,tt)|0)+Math.imul(z,$)|0,a=a+Math.imul(z,tt)|0,n=n+Math.imul(C,rt)|0,i=(i=i+Math.imul(C,nt)|0)+Math.imul(L,rt)|0,a=a+Math.imul(L,nt)|0,n=n+Math.imul(A,at)|0,i=(i=i+Math.imul(A,ot)|0)+Math.imul(S,at)|0,a=a+Math.imul(S,ot)|0,n=n+Math.imul(T,lt)|0,i=(i=i+Math.imul(T,ct)|0)+Math.imul(k,lt)|0,a=a+Math.imul(k,ct)|0,n=n+Math.imul(b,ft)|0,i=(i=i+Math.imul(b,ht)|0)+Math.imul(_,ft)|0,a=a+Math.imul(_,ht)|0;var St=(c+(n=n+Math.imul(v,dt)|0)|0)+((8191&(i=(i=i+Math.imul(v,gt)|0)+Math.imul(y,dt)|0))<<13)|0;c=((a=a+Math.imul(y,gt)|0)+(i>>>13)|0)+(St>>>26)|0,St&=67108863,n=Math.imul(B,J),i=(i=Math.imul(B,K))+Math.imul(N,J)|0,a=Math.imul(N,K),n=n+Math.imul(D,$)|0,i=(i=i+Math.imul(D,tt)|0)+Math.imul(R,$)|0,a=a+Math.imul(R,tt)|0,n=n+Math.imul(P,rt)|0,i=(i=i+Math.imul(P,nt)|0)+Math.imul(z,rt)|0,a=a+Math.imul(z,nt)|0,n=n+Math.imul(C,at)|0,i=(i=i+Math.imul(C,ot)|0)+Math.imul(L,at)|0,a=a+Math.imul(L,ot)|0,n=n+Math.imul(A,lt)|0,i=(i=i+Math.imul(A,ct)|0)+Math.imul(S,lt)|0,a=a+Math.imul(S,ct)|0,n=n+Math.imul(T,ft)|0,i=(i=i+Math.imul(T,ht)|0)+Math.imul(k,ft)|0,a=a+Math.imul(k,ht)|0;var Et=(c+(n=n+Math.imul(b,dt)|0)|0)+((8191&(i=(i=i+Math.imul(b,gt)|0)+Math.imul(_,dt)|0))<<13)|0;c=((a=a+Math.imul(_,gt)|0)+(i>>>13)|0)+(Et>>>26)|0,Et&=67108863,n=Math.imul(B,$),i=(i=Math.imul(B,tt))+Math.imul(N,$)|0,a=Math.imul(N,tt),n=n+Math.imul(D,rt)|0,i=(i=i+Math.imul(D,nt)|0)+Math.imul(R,rt)|0,a=a+Math.imul(R,nt)|0,n=n+Math.imul(P,at)|0,i=(i=i+Math.imul(P,ot)|0)+Math.imul(z,at)|0,a=a+Math.imul(z,ot)|0,n=n+Math.imul(C,lt)|0,i=(i=i+Math.imul(C,ct)|0)+Math.imul(L,lt)|0,a=a+Math.imul(L,ct)|0,n=n+Math.imul(A,ft)|0,i=(i=i+Math.imul(A,ht)|0)+Math.imul(S,ft)|0,a=a+Math.imul(S,ht)|0;var Ct=(c+(n=n+Math.imul(T,dt)|0)|0)+((8191&(i=(i=i+Math.imul(T,gt)|0)+Math.imul(k,dt)|0))<<13)|0;c=((a=a+Math.imul(k,gt)|0)+(i>>>13)|0)+(Ct>>>26)|0,Ct&=67108863,n=Math.imul(B,rt),i=(i=Math.imul(B,nt))+Math.imul(N,rt)|0,a=Math.imul(N,nt),n=n+Math.imul(D,at)|0,i=(i=i+Math.imul(D,ot)|0)+Math.imul(R,at)|0,a=a+Math.imul(R,ot)|0,n=n+Math.imul(P,lt)|0,i=(i=i+Math.imul(P,ct)|0)+Math.imul(z,lt)|0,a=a+Math.imul(z,ct)|0,n=n+Math.imul(C,ft)|0,i=(i=i+Math.imul(C,ht)|0)+Math.imul(L,ft)|0,a=a+Math.imul(L,ht)|0;var Lt=(c+(n=n+Math.imul(A,dt)|0)|0)+((8191&(i=(i=i+Math.imul(A,gt)|0)+Math.imul(S,dt)|0))<<13)|0;c=((a=a+Math.imul(S,gt)|0)+(i>>>13)|0)+(Lt>>>26)|0,Lt&=67108863,n=Math.imul(B,at),i=(i=Math.imul(B,ot))+Math.imul(N,at)|0,a=Math.imul(N,ot),n=n+Math.imul(D,lt)|0,i=(i=i+Math.imul(D,ct)|0)+Math.imul(R,lt)|0,a=a+Math.imul(R,ct)|0,n=n+Math.imul(P,ft)|0,i=(i=i+Math.imul(P,ht)|0)+Math.imul(z,ft)|0,a=a+Math.imul(z,ht)|0;var It=(c+(n=n+Math.imul(C,dt)|0)|0)+((8191&(i=(i=i+Math.imul(C,gt)|0)+Math.imul(L,dt)|0))<<13)|0;c=((a=a+Math.imul(L,gt)|0)+(i>>>13)|0)+(It>>>26)|0,It&=67108863,n=Math.imul(B,lt),i=(i=Math.imul(B,ct))+Math.imul(N,lt)|0,a=Math.imul(N,ct),n=n+Math.imul(D,ft)|0,i=(i=i+Math.imul(D,ht)|0)+Math.imul(R,ft)|0,a=a+Math.imul(R,ht)|0;var Pt=(c+(n=n+Math.imul(P,dt)|0)|0)+((8191&(i=(i=i+Math.imul(P,gt)|0)+Math.imul(z,dt)|0))<<13)|0;c=((a=a+Math.imul(z,gt)|0)+(i>>>13)|0)+(Pt>>>26)|0,Pt&=67108863,n=Math.imul(B,ft),i=(i=Math.imul(B,ht))+Math.imul(N,ft)|0,a=Math.imul(N,ht);var zt=(c+(n=n+Math.imul(D,dt)|0)|0)+((8191&(i=(i=i+Math.imul(D,gt)|0)+Math.imul(R,dt)|0))<<13)|0;c=((a=a+Math.imul(R,gt)|0)+(i>>>13)|0)+(zt>>>26)|0,zt&=67108863;var Ot=(c+(n=Math.imul(B,dt))|0)+((8191&(i=(i=Math.imul(B,gt))+Math.imul(N,dt)|0))<<13)|0;return c=((a=Math.imul(N,gt))+(i>>>13)|0)+(Ot>>>26)|0,Ot&=67108863,l[0]=mt,l[1]=vt,l[2]=yt,l[3]=xt,l[4]=bt,l[5]=_t,l[6]=wt,l[7]=Tt,l[8]=kt,l[9]=Mt,l[10]=At,l[11]=St,l[12]=Et,l[13]=Ct,l[14]=Lt,l[15]=It,l[16]=Pt,l[17]=zt,l[18]=Ot,0!==c&&(l[19]=c,r.length++),r};function d(t,e,r){return(new g).mulp(t,e,r)}function g(t,e){this.x=t,this.y=e}Math.imul||(p=h),a.prototype.mulTo=function(t,e){var r=this.length+t.length;return 10===this.length&&10===t.length?p(this,t,e):r<63?h(this,t,e):r<1024?function(t,e,r){r.negative=e.negative^t.negative,r.length=t.length+e.length;for(var n=0,i=0,a=0;a<r.length-1;a++){var o=i;i=0;for(var s=67108863&n,l=Math.min(a,e.length-1),c=Math.max(0,a-t.length+1);c<=l;c++){var u=a-c,f=(0|t.words[u])*(0|e.words[c]),h=67108863&f;s=67108863&(h=h+s|0),i+=(o=(o=o+(f/67108864|0)|0)+(h>>>26)|0)>>>26,o&=67108863}r.words[a]=s,n=o,o=i}return 0!==n?r.words[a]=n:r.length--,r.strip()}(this,t,e):d(this,t,e)},g.prototype.makeRBT=function(t){for(var e=new Array(t),r=a.prototype._countBits(t)-1,n=0;n<t;n++)e[n]=this.revBin(n,r,t);return e},g.prototype.revBin=function(t,e,r){if(0===t||t===r-1)return t;for(var n=0,i=0;i<e;i++)n|=(1&t)<<e-i-1,t>>=1;return n},g.prototype.permute=function(t,e,r,n,i,a){for(var o=0;o<a;o++)n[o]=e[t[o]],i[o]=r[t[o]]},g.prototype.transform=function(t,e,r,n,i,a){this.permute(a,t,e,r,n,i);for(var o=1;o<i;o<<=1)for(var s=o<<1,l=Math.cos(2*Math.PI/s),c=Math.sin(2*Math.PI/s),u=0;u<i;u+=s)for(var f=l,h=c,p=0;p<o;p++){var d=r[u+p],g=n[u+p],m=r[u+p+o],v=n[u+p+o],y=f*m-h*v;v=f*v+h*m,m=y,r[u+p]=d+m,n[u+p]=g+v,r[u+p+o]=d-m,n[u+p+o]=g-v,p!==s&&(y=l*f-c*h,h=l*h+c*f,f=y)}},g.prototype.guessLen13b=function(t,e){var r=1|Math.max(e,t),n=1&r,i=0;for(r=r/2|0;r;r>>>=1)i++;return 1<<i+1+n},g.prototype.conjugate=function(t,e,r){if(!(r<=1))for(var n=0;n<r/2;n++){var i=t[n];t[n]=t[r-n-1],t[r-n-1]=i,i=e[n],e[n]=-e[r-n-1],e[r-n-1]=-i}},g.prototype.normalize13b=function(t,e){for(var r=0,n=0;n<e/2;n++){var i=8192*Math.round(t[2*n+1]/e)+Math.round(t[2*n]/e)+r;t[n]=67108863&i,r=i<67108864?0:i/67108864|0}return t},g.prototype.convert13b=function(t,e,r,i){for(var a=0,o=0;o<e;o++)a+=0|t[o],r[2*o]=8191&a,a>>>=13,r[2*o+1]=8191&a,a>>>=13;for(o=2*e;o<i;++o)r[o]=0;n(0===a),n(0==(-8192&a))},g.prototype.stub=function(t){for(var e=new Array(t),r=0;r<t;r++)e[r]=0;return e},g.prototype.mulp=function(t,e,r){var n=2*this.guessLen13b(t.length,e.length),i=this.makeRBT(n),a=this.stub(n),o=new Array(n),s=new Array(n),l=new Array(n),c=new Array(n),u=new Array(n),f=new Array(n),h=r.words;h.length=n,this.convert13b(t.words,t.length,o,n),this.convert13b(e.words,e.length,c,n),this.transform(o,a,s,l,n,i),this.transform(c,a,u,f,n,i);for(var p=0;p<n;p++){var d=s[p]*u[p]-l[p]*f[p];l[p]=s[p]*f[p]+l[p]*u[p],s[p]=d}return this.conjugate(s,l,n),this.transform(s,l,h,a,n,i),this.conjugate(h,a,n),this.normalize13b(h,n),r.negative=t.negative^e.negative,r.length=t.length+e.length,r.strip()},a.prototype.mul=function(t){var e=new a(null);return e.words=new Array(this.length+t.length),this.mulTo(t,e)},a.prototype.mulf=function(t){var e=new a(null);return e.words=new Array(this.length+t.length),d(this,t,e)},a.prototype.imul=function(t){return this.clone().mulTo(t,this)},a.prototype.imuln=function(t){n("number"==typeof t),n(t<67108864);for(var e=0,r=0;r<this.length;r++){var i=(0|this.words[r])*t,a=(67108863&i)+(67108863&e);e>>=26,e+=i/67108864|0,e+=a>>>26,this.words[r]=67108863&a}return 0!==e&&(this.words[r]=e,this.length++),this},a.prototype.muln=function(t){return this.clone().imuln(t)},a.prototype.sqr=function(){return this.mul(this)},a.prototype.isqr=function(){return this.imul(this.clone())},a.prototype.pow=function(t){var e=function(t){for(var e=new Array(t.bitLength()),r=0;r<e.length;r++){var n=r/26|0,i=r%26;e[r]=(t.words[n]&1<<i)>>>i}return e}(t);if(0===e.length)return new a(1);for(var r=this,n=0;n<e.length&&0===e[n];n++,r=r.sqr());if(++n<e.length)for(var i=r.sqr();n<e.length;n++,i=i.sqr())0!==e[n]&&(r=r.mul(i));return r},a.prototype.iushln=function(t){n("number"==typeof t&&t>=0);var e,r=t%26,i=(t-r)/26,a=67108863>>>26-r<<26-r;if(0!==r){var o=0;for(e=0;e<this.length;e++){var s=this.words[e]&a,l=(0|this.words[e])-s<<r;this.words[e]=l|o,o=s>>>26-r}o&&(this.words[e]=o,this.length++)}if(0!==i){for(e=this.length-1;e>=0;e--)this.words[e+i]=this.words[e];for(e=0;e<i;e++)this.words[e]=0;this.length+=i}return this.strip()},a.prototype.ishln=function(t){return n(0===this.negative),this.iushln(t)},a.prototype.iushrn=function(t,e,r){var i;n("number"==typeof t&&t>=0),i=e?(e-e%26)/26:0;var a=t%26,o=Math.min((t-a)/26,this.length),s=67108863^67108863>>>a<<a,l=r;if(i-=o,i=Math.max(0,i),l){for(var c=0;c<o;c++)l.words[c]=this.words[c];l.length=o}if(0===o);else if(this.length>o)for(this.length-=o,c=0;c<this.length;c++)this.words[c]=this.words[c+o];else this.words[0]=0,this.length=1;var u=0;for(c=this.length-1;c>=0&&(0!==u||c>=i);c--){var f=0|this.words[c];this.words[c]=u<<26-a|f>>>a,u=f&s}return l&&0!==u&&(l.words[l.length++]=u),0===this.length&&(this.words[0]=0,this.length=1),this.strip()},a.prototype.ishrn=function(t,e,r){return n(0===this.negative),this.iushrn(t,e,r)},a.prototype.shln=function(t){return this.clone().ishln(t)},a.prototype.ushln=function(t){return this.clone().iushln(t)},a.prototype.shrn=function(t){return this.clone().ishrn(t)},a.prototype.ushrn=function(t){return this.clone().iushrn(t)},a.prototype.testn=function(t){n("number"==typeof t&&t>=0);var e=t%26,r=(t-e)/26,i=1<<e;return!(this.length<=r)&&!!(this.words[r]&i)},a.prototype.imaskn=function(t){n("number"==typeof t&&t>=0);var e=t%26,r=(t-e)/26;if(n(0===this.negative,"imaskn works only with positive numbers"),this.length<=r)return this;if(0!==e&&r++,this.length=Math.min(r,this.length),0!==e){var i=67108863^67108863>>>e<<e;this.words[this.length-1]&=i}return this.strip()},a.prototype.maskn=function(t){return this.clone().imaskn(t)},a.prototype.iaddn=function(t){return n("number"==typeof t),n(t<67108864),t<0?this.isubn(-t):0!==this.negative?1===this.length&&(0|this.words[0])<t?(this.words[0]=t-(0|this.words[0]),this.negative=0,this):(this.negative=0,this.isubn(t),this.negative=1,this):this._iaddn(t)},a.prototype._iaddn=function(t){this.words[0]+=t;for(var e=0;e<this.length&&this.words[e]>=67108864;e++)this.words[e]-=67108864,e===this.length-1?this.words[e+1]=1:this.words[e+1]++;return this.length=Math.max(this.length,e+1),this},a.prototype.isubn=function(t){if(n("number"==typeof t),n(t<67108864),t<0)return this.iaddn(-t);if(0!==this.negative)return this.negative=0,this.iaddn(t),this.negative=1,this;if(this.words[0]-=t,1===this.length&&this.words[0]<0)this.words[0]=-this.words[0],this.negative=1;else for(var e=0;e<this.length&&this.words[e]<0;e++)this.words[e]+=67108864,this.words[e+1]-=1;return this.strip()},a.prototype.addn=function(t){return this.clone().iaddn(t)},a.prototype.subn=function(t){return this.clone().isubn(t)},a.prototype.iabs=function(){return this.negative=0,this},a.prototype.abs=function(){return this.clone().iabs()},a.prototype._ishlnsubmul=function(t,e,r){var i,a,o=t.length+r;this._expand(o);var s=0;for(i=0;i<t.length;i++){a=(0|this.words[i+r])+s;var l=(0|t.words[i])*e;s=((a-=67108863&l)>>26)-(l/67108864|0),this.words[i+r]=67108863&a}for(;i<this.length-r;i++)s=(a=(0|this.words[i+r])+s)>>26,this.words[i+r]=67108863&a;if(0===s)return this.strip();for(n(-1===s),s=0,i=0;i<this.length;i++)s=(a=-(0|this.words[i])+s)>>26,this.words[i]=67108863&a;return this.negative=1,this.strip()},a.prototype._wordDiv=function(t,e){var r=(this.length,t.length),n=this.clone(),i=t,o=0|i.words[i.length-1];0!==(r=26-this._countBits(o))&&(i=i.ushln(r),n.iushln(r),o=0|i.words[i.length-1]);var s,l=n.length-i.length;if("mod"!==e){(s=new a(null)).length=l+1,s.words=new Array(s.length);for(var c=0;c<s.length;c++)s.words[c]=0}var u=n.clone()._ishlnsubmul(i,1,l);0===u.negative&&(n=u,s&&(s.words[l]=1));for(var f=l-1;f>=0;f--){var h=67108864*(0|n.words[i.length+f])+(0|n.words[i.length+f-1]);for(h=Math.min(h/o|0,67108863),n._ishlnsubmul(i,h,f);0!==n.negative;)h--,n.negative=0,n._ishlnsubmul(i,1,f),n.isZero()||(n.negative^=1);s&&(s.words[f]=h)}return s&&s.strip(),n.strip(),"div"!==e&&0!==r&&n.iushrn(r),{div:s||null,mod:n}},a.prototype.divmod=function(t,e,r){return n(!t.isZero()),this.isZero()?{div:new a(0),mod:new a(0)}:0!==this.negative&&0===t.negative?(s=this.neg().divmod(t,e),"mod"!==e&&(i=s.div.neg()),"div"!==e&&(o=s.mod.neg(),r&&0!==o.negative&&o.iadd(t)),{div:i,mod:o}):0===this.negative&&0!==t.negative?(s=this.divmod(t.neg(),e),"mod"!==e&&(i=s.div.neg()),{div:i,mod:s.mod}):0!=(this.negative&t.negative)?(s=this.neg().divmod(t.neg(),e),"div"!==e&&(o=s.mod.neg(),r&&0!==o.negative&&o.isub(t)),{div:s.div,mod:o}):t.length>this.length||this.cmp(t)<0?{div:new a(0),mod:this}:1===t.length?"div"===e?{div:this.divn(t.words[0]),mod:null}:"mod"===e?{div:null,mod:new a(this.modn(t.words[0]))}:{div:this.divn(t.words[0]),mod:new a(this.modn(t.words[0]))}:this._wordDiv(t,e);var i,o,s},a.prototype.div=function(t){return this.divmod(t,"div",!1).div},a.prototype.mod=function(t){return this.divmod(t,"mod",!1).mod},a.prototype.umod=function(t){return this.divmod(t,"mod",!0).mod},a.prototype.divRound=function(t){var e=this.divmod(t);if(e.mod.isZero())return e.div;var r=0!==e.div.negative?e.mod.isub(t):e.mod,n=t.ushrn(1),i=t.andln(1),a=r.cmp(n);return a<0||1===i&&0===a?e.div:0!==e.div.negative?e.div.isubn(1):e.div.iaddn(1)},a.prototype.modn=function(t){n(t<=67108863);for(var e=(1<<26)%t,r=0,i=this.length-1;i>=0;i--)r=(e*r+(0|this.words[i]))%t;return r},a.prototype.idivn=function(t){n(t<=67108863);for(var e=0,r=this.length-1;r>=0;r--){var i=(0|this.words[r])+67108864*e;this.words[r]=i/t|0,e=i%t}return this.strip()},a.prototype.divn=function(t){return this.clone().idivn(t)},a.prototype.egcd=function(t){n(0===t.negative),n(!t.isZero());var e=this,r=t.clone();e=0!==e.negative?e.umod(t):e.clone();for(var i=new a(1),o=new a(0),s=new a(0),l=new a(1),c=0;e.isEven()&&r.isEven();)e.iushrn(1),r.iushrn(1),++c;for(var u=r.clone(),f=e.clone();!e.isZero();){for(var h=0,p=1;0==(e.words[0]&p)&&h<26;++h,p<<=1);if(h>0)for(e.iushrn(h);h-- >0;)(i.isOdd()||o.isOdd())&&(i.iadd(u),o.isub(f)),i.iushrn(1),o.iushrn(1);for(var d=0,g=1;0==(r.words[0]&g)&&d<26;++d,g<<=1);if(d>0)for(r.iushrn(d);d-- >0;)(s.isOdd()||l.isOdd())&&(s.iadd(u),l.isub(f)),s.iushrn(1),l.iushrn(1);e.cmp(r)>=0?(e.isub(r),i.isub(s),o.isub(l)):(r.isub(e),s.isub(i),l.isub(o))}return{a:s,b:l,gcd:r.iushln(c)}},a.prototype._invmp=function(t){n(0===t.negative),n(!t.isZero());var e=this,r=t.clone();e=0!==e.negative?e.umod(t):e.clone();for(var i,o=new a(1),s=new a(0),l=r.clone();e.cmpn(1)>0&&r.cmpn(1)>0;){for(var c=0,u=1;0==(e.words[0]&u)&&c<26;++c,u<<=1);if(c>0)for(e.iushrn(c);c-- >0;)o.isOdd()&&o.iadd(l),o.iushrn(1);for(var f=0,h=1;0==(r.words[0]&h)&&f<26;++f,h<<=1);if(f>0)for(r.iushrn(f);f-- >0;)s.isOdd()&&s.iadd(l),s.iushrn(1);e.cmp(r)>=0?(e.isub(r),o.isub(s)):(r.isub(e),s.isub(o))}return(i=0===e.cmpn(1)?o:s).cmpn(0)<0&&i.iadd(t),i},a.prototype.gcd=function(t){if(this.isZero())return t.abs();if(t.isZero())return this.abs();var e=this.clone(),r=t.clone();e.negative=0,r.negative=0;for(var n=0;e.isEven()&&r.isEven();n++)e.iushrn(1),r.iushrn(1);for(;;){for(;e.isEven();)e.iushrn(1);for(;r.isEven();)r.iushrn(1);var i=e.cmp(r);if(i<0){var a=e;e=r,r=a}else if(0===i||0===r.cmpn(1))break;e.isub(r)}return r.iushln(n)},a.prototype.invm=function(t){return this.egcd(t).a.umod(t)},a.prototype.isEven=function(){return 0==(1&this.words[0])},a.prototype.isOdd=function(){return 1==(1&this.words[0])},a.prototype.andln=function(t){return this.words[0]&t},a.prototype.bincn=function(t){n("number"==typeof t);var e=t%26,r=(t-e)/26,i=1<<e;if(this.length<=r)return this._expand(r+1),this.words[r]|=i,this;for(var a=i,o=r;0!==a&&o<this.length;o++){var s=0|this.words[o];a=(s+=a)>>>26,s&=67108863,this.words[o]=s}return 0!==a&&(this.words[o]=a,this.length++),this},a.prototype.isZero=function(){return 1===this.length&&0===this.words[0]},a.prototype.cmpn=function(t){var e,r=t<0;if(0!==this.negative&&!r)return-1;if(0===this.negative&&r)return 1;if(this.strip(),this.length>1)e=1;else{r&&(t=-t),n(t<=67108863,"Number is too big");var i=0|this.words[0];e=i===t?0:i<t?-1:1}return 0!==this.negative?0|-e:e},a.prototype.cmp=function(t){if(0!==this.negative&&0===t.negative)return-1;if(0===this.negative&&0!==t.negative)return 1;var e=this.ucmp(t);return 0!==this.negative?0|-e:e},a.prototype.ucmp=function(t){if(this.length>t.length)return 1;if(this.length<t.length)return-1;for(var e=0,r=this.length-1;r>=0;r--){var n=0|this.words[r],i=0|t.words[r];if(n!==i){n<i?e=-1:n>i&&(e=1);break}}return e},a.prototype.gtn=function(t){return 1===this.cmpn(t)},a.prototype.gt=function(t){return 1===this.cmp(t)},a.prototype.gten=function(t){return this.cmpn(t)>=0},a.prototype.gte=function(t){return this.cmp(t)>=0},a.prototype.ltn=function(t){return-1===this.cmpn(t)},a.prototype.lt=function(t){return-1===this.cmp(t)},a.prototype.lten=function(t){return this.cmpn(t)<=0},a.prototype.lte=function(t){return this.cmp(t)<=0},a.prototype.eqn=function(t){return 0===this.cmpn(t)},a.prototype.eq=function(t){return 0===this.cmp(t)},a.red=function(t){return new w(t)},a.prototype.toRed=function(t){return n(!this.red,"Already a number in reduction context"),n(0===this.negative,"red works only with positives"),t.convertTo(this)._forceRed(t)},a.prototype.fromRed=function(){return n(this.red,"fromRed works only with numbers in reduction context"),this.red.convertFrom(this)},a.prototype._forceRed=function(t){return this.red=t,this},a.prototype.forceRed=function(t){return n(!this.red,"Already a number in reduction context"),this._forceRed(t)},a.prototype.redAdd=function(t){return n(this.red,"redAdd works only with red numbers"),this.red.add(this,t)},a.prototype.redIAdd=function(t){return n(this.red,"redIAdd works only with red numbers"),this.red.iadd(this,t)},a.prototype.redSub=function(t){return n(this.red,"redSub works only with red numbers"),this.red.sub(this,t)},a.prototype.redISub=function(t){return n(this.red,"redISub works only with red numbers"),this.red.isub(this,t)},a.prototype.redShl=function(t){return n(this.red,"redShl works only with red numbers"),this.red.shl(this,t)},a.prototype.redMul=function(t){return n(this.red,"redMul works only with red numbers"),this.red._verify2(this,t),this.red.mul(this,t)},a.prototype.redIMul=function(t){return n(this.red,"redMul works only with red numbers"),this.red._verify2(this,t),this.red.imul(this,t)},a.prototype.redSqr=function(){return n(this.red,"redSqr works only with red numbers"),this.red._verify1(this),this.red.sqr(this)},a.prototype.redISqr=function(){return n(this.red,"redISqr works only with red numbers"),this.red._verify1(this),this.red.isqr(this)},a.prototype.redSqrt=function(){return n(this.red,"redSqrt works only with red numbers"),this.red._verify1(this),this.red.sqrt(this)},a.prototype.redInvm=function(){return n(this.red,"redInvm works only with red numbers"),this.red._verify1(this),this.red.invm(this)},a.prototype.redNeg=function(){return n(this.red,"redNeg works only with red numbers"),this.red._verify1(this),this.red.neg(this)},a.prototype.redPow=function(t){return n(this.red&&!t.red,"redPow(normalNum)"),this.red._verify1(this),this.red.pow(this,t)};var m={k256:null,p224:null,p192:null,p25519:null};function v(t,e){this.name=t,this.p=new a(e,16),this.n=this.p.bitLength(),this.k=new a(1).iushln(this.n).isub(this.p),this.tmp=this._tmp()}function y(){v.call(this,"k256","ffffffff ffffffff ffffffff ffffffff ffffffff ffffffff fffffffe fffffc2f")}function x(){v.call(this,"p224","ffffffff ffffffff ffffffff ffffffff 00000000 00000000 00000001")}function b(){v.call(this,"p192","ffffffff ffffffff ffffffff fffffffe ffffffff ffffffff")}function _(){v.call(this,"25519","7fffffffffffffff ffffffffffffffff ffffffffffffffff ffffffffffffffed")}function w(t){if("string"==typeof t){var e=a._prime(t);this.m=e.p,this.prime=e}else n(t.gtn(1),"modulus must be greater than 1"),this.m=t,this.prime=null}function T(t){w.call(this,t),this.shift=this.m.bitLength(),this.shift%26!=0&&(this.shift+=26-this.shift%26),this.r=new a(1).iushln(this.shift),this.r2=this.imod(this.r.sqr()),this.rinv=this.r._invmp(this.m),this.minv=this.rinv.mul(this.r).isubn(1).div(this.m),this.minv=this.minv.umod(this.r),this.minv=this.r.sub(this.minv)}v.prototype._tmp=function(){var t=new a(null);return t.words=new Array(Math.ceil(this.n/13)),t},v.prototype.ireduce=function(t){var e,r=t;do{this.split(r,this.tmp),e=(r=(r=this.imulK(r)).iadd(this.tmp)).bitLength()}while(e>this.n);var n=e<this.n?-1:r.ucmp(this.p);return 0===n?(r.words[0]=0,r.length=1):n>0?r.isub(this.p):r.strip(),r},v.prototype.split=function(t,e){t.iushrn(this.n,0,e)},v.prototype.imulK=function(t){return t.imul(this.k)},i(y,v),y.prototype.split=function(t,e){for(var r=Math.min(t.length,9),n=0;n<r;n++)e.words[n]=t.words[n];if(e.length=r,t.length<=9)return t.words[0]=0,void(t.length=1);var i=t.words[9];for(e.words[e.length++]=4194303&i,n=10;n<t.length;n++){var a=0|t.words[n];t.words[n-10]=(4194303&a)<<4|i>>>22,i=a}i>>>=22,t.words[n-10]=i,0===i&&t.length>10?t.length-=10:t.length-=9},y.prototype.imulK=function(t){t.words[t.length]=0,t.words[t.length+1]=0,t.length+=2;for(var e=0,r=0;r<t.length;r++){var n=0|t.words[r];e+=977*n,t.words[r]=67108863&e,e=64*n+(e/67108864|0)}return 0===t.words[t.length-1]&&(t.length--,0===t.words[t.length-1]&&t.length--),t},i(x,v),i(b,v),i(_,v),_.prototype.imulK=function(t){for(var e=0,r=0;r<t.length;r++){var n=19*(0|t.words[r])+e,i=67108863&n;n>>>=26,t.words[r]=i,e=n}return 0!==e&&(t.words[t.length++]=e),t},a._prime=function(t){if(m[t])return m[t];var e;if("k256"===t)e=new y;else if("p224"===t)e=new x;else if("p192"===t)e=new b;else{if("p25519"!==t)throw new Error("Unknown prime "+t);e=new _}return m[t]=e,e},w.prototype._verify1=function(t){n(0===t.negative,"red works only with positives"),n(t.red,"red works only with red numbers")},w.prototype._verify2=function(t,e){n(0==(t.negative|e.negative),"red works only with positives"),n(t.red&&t.red===e.red,"red works only with red numbers")},w.prototype.imod=function(t){return this.prime?this.prime.ireduce(t)._forceRed(this):t.umod(this.m)._forceRed(this)},w.prototype.neg=function(t){return t.isZero()?t.clone():this.m.sub(t)._forceRed(this)},w.prototype.add=function(t,e){this._verify2(t,e);var r=t.add(e);return r.cmp(this.m)>=0&&r.isub(this.m),r._forceRed(this)},w.prototype.iadd=function(t,e){this._verify2(t,e);var r=t.iadd(e);return r.cmp(this.m)>=0&&r.isub(this.m),r},w.prototype.sub=function(t,e){this._verify2(t,e);var r=t.sub(e);return r.cmpn(0)<0&&r.iadd(this.m),r._forceRed(this)},w.prototype.isub=function(t,e){this._verify2(t,e);var r=t.isub(e);return r.cmpn(0)<0&&r.iadd(this.m),r},w.prototype.shl=function(t,e){return this._verify1(t),this.imod(t.ushln(e))},w.prototype.imul=function(t,e){return this._verify2(t,e),this.imod(t.imul(e))},w.prototype.mul=function(t,e){return this._verify2(t,e),this.imod(t.mul(e))},w.prototype.isqr=function(t){return this.imul(t,t.clone())},w.prototype.sqr=function(t){return this.mul(t,t)},w.prototype.sqrt=function(t){if(t.isZero())return t.clone();var e=this.m.andln(3);if(n(e%2==1),3===e){var r=this.m.add(new a(1)).iushrn(2);return this.pow(t,r)}for(var i=this.m.subn(1),o=0;!i.isZero()&&0===i.andln(1);)o++,i.iushrn(1);n(!i.isZero());var s=new a(1).toRed(this),l=s.redNeg(),c=this.m.subn(1).iushrn(1),u=this.m.bitLength();for(u=new a(2*u*u).toRed(this);0!==this.pow(u,c).cmp(l);)u.redIAdd(l);for(var f=this.pow(u,i),h=this.pow(t,i.addn(1).iushrn(1)),p=this.pow(t,i),d=o;0!==p.cmp(s);){for(var g=p,m=0;0!==g.cmp(s);m++)g=g.redSqr();n(m<d);var v=this.pow(f,new a(1).iushln(d-m-1));h=h.redMul(v),f=v.redSqr(),p=p.redMul(f),d=m}return h},w.prototype.invm=function(t){var e=t._invmp(this.m);return 0!==e.negative?(e.negative=0,this.imod(e).redNeg()):this.imod(e)},w.prototype.pow=function(t,e){if(e.isZero())return new a(1).toRed(this);if(0===e.cmpn(1))return t.clone();var r=new Array(16);r[0]=new a(1).toRed(this),r[1]=t;for(var n=2;n<r.length;n++)r[n]=this.mul(r[n-1],t);var i=r[0],o=0,s=0,l=e.bitLength()%26;for(0===l&&(l=26),n=e.length-1;n>=0;n--){for(var c=e.words[n],u=l-1;u>=0;u--){var f=c>>u&1;i!==r[0]&&(i=this.sqr(i)),0!==f||0!==o?(o<<=1,o|=f,(4===++s||0===n&&0===u)&&(i=this.mul(i,r[o]),s=0,o=0)):s=0}l=26}return i},w.prototype.convertTo=function(t){var e=t.umod(this.m);return e===t?e.clone():e},w.prototype.convertFrom=function(t){var e=t.clone();return e.red=null,e},a.mont=function(t){return new T(t)},i(T,w),T.prototype.convertTo=function(t){return this.imod(t.ushln(this.shift))},T.prototype.convertFrom=function(t){var e=this.imod(t.mul(this.rinv));return e.red=null,e},T.prototype.imul=function(t,e){if(t.isZero()||e.isZero())return t.words[0]=0,t.length=1,t;var r=t.imul(e),n=r.maskn(this.shift).mul(this.minv).imaskn(this.shift).mul(this.m),i=r.isub(n).iushrn(this.shift),a=i;return i.cmp(this.m)>=0?a=i.isub(this.m):i.cmpn(0)<0&&(a=i.iadd(this.m)),a._forceRed(this)},T.prototype.mul=function(t,e){if(t.isZero()||e.isZero())return new a(0)._forceRed(this);var r=t.mul(e),n=r.maskn(this.shift).mul(this.minv).imaskn(this.shift).mul(this.m),i=r.isub(n).iushrn(this.shift),o=i;return i.cmp(this.m)>=0?o=i.isub(this.m):i.cmpn(0)<0&&(o=i.iadd(this.m)),o._forceRed(this)},T.prototype.invm=function(t){return this.imod(t._invmp(this.m).mul(this.r2))._forceRed(this)}}("undefined"==typeof e||e,this)},{buffer:108}],100:[function(t,e,r){"use strict";e.exports=function(t){var e,r,n,i=t.length,a=0;for(e=0;e<i;++e)a+=t[e].length;var o=new Array(a),s=0;for(e=0;e<i;++e){var l=t[e],c=l.length;for(r=0;r<c;++r){var u=o[s++]=new Array(c-1),f=0;for(n=0;n<c;++n)n!==r&&(u[f++]=l[n]);if(1&r){var h=u[1];u[1]=u[0],u[0]=h}}}return o}},{}],101:[function(t,e,r){"use strict";e.exports=function(t,e,r){switch(arguments.length){case 1:return f(t);case 2:return"function"==typeof e?c(t,t,e,!0):h(t,e);case 3:return c(t,e,r,!1);default:throw new Error("box-intersect: Invalid arguments")}};var n,i=t("typedarray-pool"),a=t("./lib/sweep"),o=t("./lib/intersect");function s(t,e){for(var r=0;r<t;++r)if(!(e[r]<=e[r+t]))return!0;return!1}function l(t,e,r,n){for(var i=0,a=0,o=0,l=t.length;o<l;++o){var c=t[o];if(!s(e,c)){for(var u=0;u<2*e;++u)r[i++]=c[u];n[a++]=o}}return a}function c(t,e,r,n){var s=t.length,c=e.length;if(!(s<=0||c<=0)){var u=t[0].length>>>1;if(!(u<=0)){var f,h=i.mallocDouble(2*u*s),p=i.mallocInt32(s);if((s=l(t,u,h,p))>0){if(1===u&&n)a.init(s),f=a.sweepComplete(u,r,0,s,h,p,0,s,h,p);else{var d=i.mallocDouble(2*u*c),g=i.mallocInt32(c);(c=l(e,u,d,g))>0&&(a.init(s+c),f=1===u?a.sweepBipartite(u,r,0,s,h,p,0,c,d,g):o(u,r,n,s,h,p,c,d,g),i.free(d),i.free(g))}i.free(h),i.free(p)}return f}}}function u(t,e){n.push([t,e])}function f(t){return n=[],c(t,t,u,!0),n}function h(t,e){return n=[],c(t,e,u,!1),n}},{"./lib/intersect":103,"./lib/sweep":107,"typedarray-pool":595}],102:[function(t,e,r){"use strict";var n=["d","ax","vv","rs","re","rb","ri","bs","be","bb","bi"];function i(t){var e="bruteForce"+(t?"Full":"Partial"),r=[],i=n.slice();t||i.splice(3,0,"fp");var a=["function "+e+"("+i.join()+"){"];function o(e,i){var o=function(t,e,r){var i="bruteForce"+(t?"Red":"Blue")+(e?"Flip":"")+(r?"Full":""),a=["function ",i,"(",n.join(),"){","var ","es","=2*","d",";"],o="for(var i=rs,rp=es*rs;i<re;++i,rp+=es){var x0=rb[ax+rp],x1=rb[ax+rp+d],xi=ri[i];",s="for(var j=bs,bp=es*bs;j<be;++j,bp+=es){var y0=bb[ax+bp],"+(r?"y1=bb[ax+bp+d],":"")+"yi=bi[j];";return t?a.push(o,"Q",":",s):a.push(s,"Q",":",o),r?a.push("if(y1<x0||x1<y0)continue;"):e?a.push("if(y0<=x0||x1<y0)continue;"):a.push("if(y0<x0||x1<y0)continue;"),a.push("for(var k=ax+1;k<d;++k){var r0=rb[k+rp],r1=rb[k+d+rp],b0=bb[k+bp],b1=bb[k+d+bp];if(r1<b0||b1<r0)continue Q;}var rv=vv("),e?a.push("yi,xi"):a.push("xi,yi"),a.push(");if(rv!==void 0)return rv;}}}"),{name:i,code:a.join("")}}(e,i,t);r.push(o.code),a.push("return "+o.name+"("+n.join()+");")}a.push("if(re-rs>be-bs){"),t?(o(!0,!1),a.push("}else{"),o(!1,!1)):(a.push("if(fp){"),o(!0,!0),a.push("}else{"),o(!0,!1),a.push("}}else{if(fp){"),o(!1,!0),a.push("}else{"),o(!1,!1),a.push("}")),a.push("}}return "+e);var s=r.join("")+a.join("");return new Function(s)()}r.partial=i(!1),r.full=i(!0)},{}],103:[function(t,e,r){"use strict";e.exports=function(t,e,r,a,u,w,T,k,M){!function(t,e){var r=8*i.log2(e+1)*(t+1)|0,a=i.nextPow2(6*r);v.length<a&&(n.free(v),v=n.mallocInt32(a));var o=i.nextPow2(2*r);y.length<o&&(n.free(y),y=n.mallocDouble(o))}(t,a+T);var A,S=0,E=2*t;x(S++,0,0,a,0,T,r?16:0,-1/0,1/0),r||x(S++,0,0,T,0,a,1,-1/0,1/0);for(;S>0;){var C=6*(S-=1),L=v[C],I=v[C+1],P=v[C+2],z=v[C+3],O=v[C+4],D=v[C+5],R=2*S,F=y[R],B=y[R+1],N=1&D,j=!!(16&D),U=u,V=w,q=k,H=M;if(N&&(U=k,V=M,q=u,H=w),!(2&D&&(P=p(t,L,I,P,U,V,B),I>=P)||4&D&&(I=d(t,L,I,P,U,V,F))>=P)){var G=P-I,Y=O-z;if(j){if(t*G*(G+Y)<1<<22){if(void 0!==(A=l.scanComplete(t,L,e,I,P,U,V,z,O,q,H)))return A;continue}}else{if(t*Math.min(G,Y)<128){if(void 0!==(A=o(t,L,e,N,I,P,U,V,z,O,q,H)))return A;continue}if(t*G*Y<1<<22){if(void 0!==(A=l.scanBipartite(t,L,e,N,I,P,U,V,z,O,q,H)))return A;continue}}var W=f(t,L,I,P,U,V,F,B);if(I<W)if(t*(W-I)<128){if(void 0!==(A=s(t,L+1,e,I,W,U,V,z,O,q,H)))return A}else if(L===t-2){if(void 0!==(A=N?l.sweepBipartite(t,e,z,O,q,H,I,W,U,V):l.sweepBipartite(t,e,I,W,U,V,z,O,q,H)))return A}else x(S++,L+1,I,W,z,O,N,-1/0,1/0),x(S++,L+1,z,O,I,W,1^N,-1/0,1/0);if(W<P){var X=c(t,L,z,O,q,H),Z=q[E*X+L],J=h(t,L,X,O,q,H,Z);if(J<O&&x(S++,L,W,P,J,O,(4|N)+(j?16:0),Z,B),z<X&&x(S++,L,W,P,z,X,(2|N)+(j?16:0),F,Z),X+1===J){if(void 0!==(A=j?_(t,L,e,W,P,U,V,X,q,H[X]):b(t,L,e,N,W,P,U,V,X,q,H[X])))return A}else if(X<J){var K;if(j){if(K=g(t,L,W,P,U,V,Z),W<K){var Q=h(t,L,W,K,U,V,Z);if(L===t-2){if(W<Q&&void 0!==(A=l.sweepComplete(t,e,W,Q,U,V,X,J,q,H)))return A;if(Q<K&&void 0!==(A=l.sweepBipartite(t,e,Q,K,U,V,X,J,q,H)))return A}else W<Q&&x(S++,L+1,W,Q,X,J,16,-1/0,1/0),Q<K&&(x(S++,L+1,Q,K,X,J,0,-1/0,1/0),x(S++,L+1,X,J,Q,K,1,-1/0,1/0))}}else K=N?m(t,L,W,P,U,V,Z):g(t,L,W,P,U,V,Z),W<K&&(L===t-2?A=N?l.sweepBipartite(t,e,X,J,q,H,W,K,U,V):l.sweepBipartite(t,e,W,K,U,V,X,J,q,H):(x(S++,L+1,W,K,X,J,N,-1/0,1/0),x(S++,L+1,X,J,W,K,1^N,-1/0,1/0)))}}}}};var n=t("typedarray-pool"),i=t("bit-twiddle"),a=t("./brute"),o=a.partial,s=a.full,l=t("./sweep"),c=t("./median"),u=t("./partition"),f=u("!(lo>=p0)&&!(p1>=hi)",["p0","p1"]),h=u("lo===p0",["p0"]),p=u("lo<p0",["p0"]),d=u("hi<=p0",["p0"]),g=u("lo<=p0&&p0<=hi",["p0"]),m=u("lo<p0&&p0<=hi",["p0"]),v=n.mallocInt32(1024),y=n.mallocDouble(1024);function x(t,e,r,n,i,a,o,s,l){var c=6*t;v[c]=e,v[c+1]=r,v[c+2]=n,v[c+3]=i,v[c+4]=a,v[c+5]=o;var u=2*t;y[u]=s,y[u+1]=l}function b(t,e,r,n,i,a,o,s,l,c,u){var f=2*t,h=l*f,p=c[h+e];t:for(var d=i,g=i*f;d<a;++d,g+=f){var m=o[g+e],v=o[g+e+t];if(!(p<m||v<p)&&(!n||p!==m)){for(var y,x=s[d],b=e+1;b<t;++b){m=o[g+b],v=o[g+b+t];var _=c[h+b],w=c[h+b+t];if(v<_||w<m)continue t}if(void 0!==(y=n?r(u,x):r(x,u)))return y}}}function _(t,e,r,n,i,a,o,s,l,c){var u=2*t,f=s*u,h=l[f+e];t:for(var p=n,d=n*u;p<i;++p,d+=u){var g=o[p];if(g!==c){var m=a[d+e],v=a[d+e+t];if(!(h<m||v<h)){for(var y=e+1;y<t;++y){m=a[d+y],v=a[d+y+t];var x=l[f+y],b=l[f+y+t];if(v<x||b<m)continue t}var _=r(g,c);if(void 0!==_)return _}}}}},{"./brute":102,"./median":104,"./partition":105,"./sweep":107,"bit-twiddle":97,"typedarray-pool":595}],104:[function(t,e,r){"use strict";e.exports=function(t,e,r,a,o,s){if(a<=r+1)return r;var l=r,c=a,u=a+r>>>1,f=2*t,h=u,p=o[f*u+e];for(;l<c;){if(c-l<8){i(t,e,l,c,o,s),p=o[f*u+e];break}var d=c-l,g=Math.random()*d+l|0,m=o[f*g+e],v=Math.random()*d+l|0,y=o[f*v+e],x=Math.random()*d+l|0,b=o[f*x+e];m<=y?b>=y?(h=v,p=y):m>=b?(h=g,p=m):(h=x,p=b):y>=b?(h=v,p=y):b>=m?(h=g,p=m):(h=x,p=b);for(var _=f*(c-1),w=f*h,T=0;T<f;++T,++_,++w){var k=o[_];o[_]=o[w],o[w]=k}var M=s[c-1];s[c-1]=s[h],s[h]=M,h=n(t,e,l,c-1,o,s,p);for(_=f*(c-1),w=f*h,T=0;T<f;++T,++_,++w){k=o[_];o[_]=o[w],o[w]=k}M=s[c-1];if(s[c-1]=s[h],s[h]=M,u<h){for(c=h-1;l<c&&o[f*(c-1)+e]===p;)c-=1;c+=1}else{if(!(h<u))break;for(l=h+1;l<c&&o[f*l+e]===p;)l+=1}}return n(t,e,r,u,o,s,o[f*u+e])};var n=t("./partition")("lo<p0",["p0"]);function i(t,e,r,n,i,a){for(var o=2*t,s=o*(r+1)+e,l=r+1;l<n;++l,s+=o)for(var c=i[s],u=l,f=o*(l-1);u>r&&i[f+e]>c;--u,f-=o){for(var h=f,p=f+o,d=0;d<o;++d,++h,++p){var g=i[h];i[h]=i[p],i[p]=g}var m=a[u];a[u]=a[u-1],a[u-1]=m}}},{"./partition":105}],105:[function(t,e,r){"use strict";e.exports=function(t,e){var r="abcdef".split("").concat(e),n=[];t.indexOf("lo")>=0&&n.push("lo=e[k+n]");t.indexOf("hi")>=0&&n.push("hi=e[k+o]");return r.push("for(var j=2*a,k=j*c,l=k,m=c,n=b,o=a+b,p=c;d>p;++p,k+=j){var _;if($)if(m===p)m+=1,l+=j;else{for(var s=0;j>s;++s){var t=e[k+s];e[k+s]=e[l],e[l++]=t}var u=f[p];f[p]=f[m],f[m++]=u}}return m".replace("_",n.join()).replace("$",t)),Function.apply(void 0,r)}},{}],106:[function(t,e,r){"use strict";e.exports=function(t,e){e<=128?n(0,e-1,t):function t(e,r,u){var f=(r-e+1)/6|0,h=e+f,p=r-f,d=e+r>>1,g=d-f,m=d+f,v=h,y=g,x=d,b=m,_=p,w=e+1,T=r-1,k=0;l(v,y,u)&&(k=v,v=y,y=k);l(b,_,u)&&(k=b,b=_,_=k);l(v,x,u)&&(k=v,v=x,x=k);l(y,x,u)&&(k=y,y=x,x=k);l(v,b,u)&&(k=v,v=b,b=k);l(x,b,u)&&(k=x,x=b,b=k);l(y,_,u)&&(k=y,y=_,_=k);l(y,x,u)&&(k=y,y=x,x=k);l(b,_,u)&&(k=b,b=_,_=k);for(var M=u[2*y],A=u[2*y+1],S=u[2*b],E=u[2*b+1],C=2*v,L=2*x,I=2*_,P=2*h,z=2*d,O=2*p,D=0;D<2;++D){var R=u[C+D],F=u[L+D],B=u[I+D];u[P+D]=R,u[z+D]=F,u[O+D]=B}a(g,e,u),a(m,r,u);for(var N=w;N<=T;++N)if(c(N,M,A,u))N!==w&&i(N,w,u),++w;else if(!c(N,S,E,u))for(;;){if(c(T,S,E,u)){c(T,M,A,u)?(o(N,w,T,u),++w,--T):(i(N,T,u),--T);break}if(--T<N)break}s(e,w-1,M,A,u),s(r,T+1,S,E,u),w-2-e<=32?n(e,w-2,u):t(e,w-2,u);r-(T+2)<=32?n(T+2,r,u):t(T+2,r,u);T-w<=32?n(w,T,u):t(w,T,u)}(0,e-1,t)};function n(t,e,r){for(var n=2*(t+1),i=t+1;i<=e;++i){for(var a=r[n++],o=r[n++],s=i,l=n-2;s-- >t;){var c=r[l-2],u=r[l-1];if(c<a)break;if(c===a&&u<o)break;r[l]=c,r[l+1]=u,l-=2}r[l]=a,r[l+1]=o}}function i(t,e,r){e*=2;var n=r[t*=2],i=r[t+1];r[t]=r[e],r[t+1]=r[e+1],r[e]=n,r[e+1]=i}function a(t,e,r){e*=2,r[t*=2]=r[e],r[t+1]=r[e+1]}function o(t,e,r,n){e*=2,r*=2;var i=n[t*=2],a=n[t+1];n[t]=n[e],n[t+1]=n[e+1],n[e]=n[r],n[e+1]=n[r+1],n[r]=i,n[r+1]=a}function s(t,e,r,n,i){e*=2,i[t*=2]=i[e],i[e]=r,i[t+1]=i[e+1],i[e+1]=n}function l(t,e,r){e*=2;var n=r[t*=2],i=r[e];return!(n<i)&&(n!==i||r[t+1]>r[e+1])}function c(t,e,r,n){var i=n[t*=2];return i<e||i===e&&n[t+1]<r}},{}],107:[function(t,e,r){"use strict";e.exports={init:function(t){var e=i.nextPow2(t);o.length<e&&(n.free(o),o=n.mallocInt32(e));s.length<e&&(n.free(s),s=n.mallocInt32(e));l.length<e&&(n.free(l),l=n.mallocInt32(e));c.length<e&&(n.free(c),c=n.mallocInt32(e));u.length<e&&(n.free(u),u=n.mallocInt32(e));f.length<e&&(n.free(f),f=n.mallocInt32(e));var r=8*e;h.length<r&&(n.free(h),h=n.mallocDouble(r))},sweepBipartite:function(t,e,r,n,i,u,f,g,m,v){for(var y=0,x=2*t,b=t-1,_=x-1,w=r;w<n;++w){var T=u[w],k=x*w;h[y++]=i[k+b],h[y++]=-(T+1),h[y++]=i[k+_],h[y++]=T}for(w=f;w<g;++w){T=v[w]+(1<<28);var M=x*w;h[y++]=m[M+b],h[y++]=-T,h[y++]=m[M+_],h[y++]=T}var A=y>>>1;a(h,A);var S=0,E=0;for(w=0;w<A;++w){var C=0|h[2*w+1];if(C>=1<<28)p(l,c,E--,C=C-(1<<28)|0);else if(C>=0)p(o,s,S--,C);else if(C<=-(1<<28)){C=-C-(1<<28)|0;for(var L=0;L<S;++L){if(void 0!==(I=e(o[L],C)))return I}d(l,c,E++,C)}else{C=-C-1|0;for(L=0;L<E;++L){var I;if(void 0!==(I=e(C,l[L])))return I}d(o,s,S++,C)}}},sweepComplete:function(t,e,r,n,i,g,m,v,y,x){for(var b=0,_=2*t,w=t-1,T=_-1,k=r;k<n;++k){var M=g[k]+1<<1,A=_*k;h[b++]=i[A+w],h[b++]=-M,h[b++]=i[A+T],h[b++]=M}for(k=m;k<v;++k){M=x[k]+1<<1;var S=_*k;h[b++]=y[S+w],h[b++]=1|-M,h[b++]=y[S+T],h[b++]=1|M}var E=b>>>1;a(h,E);var C=0,L=0,I=0;for(k=0;k<E;++k){var P=0|h[2*k+1],z=1&P;if(k<E-1&&P>>1==h[2*k+3]>>1&&(z=2,k+=1),P<0){for(var O=-(P>>1)-1,D=0;D<I;++D){if(void 0!==(R=e(u[D],O)))return R}if(0!==z)for(D=0;D<C;++D){if(void 0!==(R=e(o[D],O)))return R}if(1!==z)for(D=0;D<L;++D){var R;if(void 0!==(R=e(l[D],O)))return R}0===z?d(o,s,C++,O):1===z?d(l,c,L++,O):2===z&&d(u,f,I++,O)}else{O=(P>>1)-1;0===z?p(o,s,C--,O):1===z?p(l,c,L--,O):2===z&&p(u,f,I--,O)}}},scanBipartite:function(t,e,r,n,i,l,c,u,f,g,m,v){var y=0,x=2*t,b=e,_=e+t,w=1,T=1;n?T=1<<28:w=1<<28;for(var k=i;k<l;++k){var M=k+w,A=x*k;h[y++]=c[A+b],h[y++]=-M,h[y++]=c[A+_],h[y++]=M}for(k=f;k<g;++k){M=k+T;var S=x*k;h[y++]=m[S+b],h[y++]=-M}var E=y>>>1;a(h,E);var C=0;for(k=0;k<E;++k){var L=0|h[2*k+1];if(L<0){var I=!1;if((M=-L)>=1<<28?(I=!n,M-=1<<28):(I=!!n,M-=1),I)d(o,s,C++,M);else{var P=v[M],z=x*M,O=m[z+e+1],D=m[z+e+1+t];t:for(var R=0;R<C;++R){var F=o[R],B=x*F;if(!(D<c[B+e+1]||c[B+e+1+t]<O)){for(var N=e+2;N<t;++N)if(m[z+N+t]<c[B+N]||c[B+N+t]<m[z+N])continue t;var j,U=u[F];if(void 0!==(j=n?r(P,U):r(U,P)))return j}}}}else p(o,s,C--,L-w)}},scanComplete:function(t,e,r,n,i,s,l,c,u,f,p){for(var d=0,g=2*t,m=e,v=e+t,y=n;y<i;++y){var x=y+(1<<28),b=g*y;h[d++]=s[b+m],h[d++]=-x,h[d++]=s[b+v],h[d++]=x}for(y=c;y<u;++y){x=y+1;var _=g*y;h[d++]=f[_+m],h[d++]=-x}var w=d>>>1;a(h,w);var T=0;for(y=0;y<w;++y){var k=0|h[2*y+1];if(k<0){if((x=-k)>=1<<28)o[T++]=x-(1<<28);else{var M=p[x-=1],A=g*x,S=f[A+e+1],E=f[A+e+1+t];t:for(var C=0;C<T;++C){var L=o[C],I=l[L];if(I===M)break;var P=g*L;if(!(E<s[P+e+1]||s[P+e+1+t]<S)){for(var z=e+2;z<t;++z)if(f[A+z+t]<s[P+z]||s[P+z+t]<f[A+z])continue t;var O=r(I,M);if(void 0!==O)return O}}}}else{for(x=k-(1<<28),C=T-1;C>=0;--C)if(o[C]===x){for(z=C+1;z<T;++z)o[z-1]=o[z];break}--T}}}};var n=t("typedarray-pool"),i=t("bit-twiddle"),a=t("./sort"),o=n.mallocInt32(1024),s=n.mallocInt32(1024),l=n.mallocInt32(1024),c=n.mallocInt32(1024),u=n.mallocInt32(1024),f=n.mallocInt32(1024),h=n.mallocDouble(8192);function p(t,e,r,n){var i=e[n],a=t[r-1];t[i]=a,e[a]=i}function d(t,e,r,n){t[r]=n,e[n]=r}},{"./sort":106,"bit-twiddle":97,"typedarray-pool":595}],108:[function(t,e,r){},{}],109:[function(t,e,r){arguments[4][108][0].apply(r,arguments)},{dup:108}],110:[function(t,e,r){"use strict";var n,i="object"==typeof Reflect?Reflect:null,a=i&&"function"==typeof i.apply?i.apply:function(t,e,r){return Function.prototype.apply.call(t,e,r)};n=i&&"function"==typeof i.ownKeys?i.ownKeys:Object.getOwnPropertySymbols?function(t){return Object.getOwnPropertyNames(t).concat(Object.getOwnPropertySymbols(t))}:function(t){return Object.getOwnPropertyNames(t)};var o=Number.isNaN||function(t){return t!=t};function s(){s.init.call(this)}e.exports=s,e.exports.once=function(t,e){return new Promise((function(r,n){function i(){void 0!==a&&t.removeListener("error",a),r([].slice.call(arguments))}var a;"error"!==e&&(a=function(r){t.removeListener(e,i),n(r)},t.once("error",a)),t.once(e,i)}))},s.EventEmitter=s,s.prototype._events=void 0,s.prototype._eventsCount=0,s.prototype._maxListeners=void 0;var l=10;function c(t){if("function"!=typeof t)throw new TypeError('The "listener" argument must be of type Function. Received type '+typeof t)}function u(t){return void 0===t._maxListeners?s.defaultMaxListeners:t._maxListeners}function f(t,e,r,n){var i,a,o,s;if(c(r),void 0===(a=t._events)?(a=t._events=Object.create(null),t._eventsCount=0):(void 0!==a.newListener&&(t.emit("newListener",e,r.listener?r.listener:r),a=t._events),o=a[e]),void 0===o)o=a[e]=r,++t._eventsCount;else if("function"==typeof o?o=a[e]=n?[r,o]:[o,r]:n?o.unshift(r):o.push(r),(i=u(t))>0&&o.length>i&&!o.warned){o.warned=!0;var l=new Error("Possible EventEmitter memory leak detected. "+o.length+" "+String(e)+" listeners added. Use emitter.setMaxListeners() to increase limit");l.name="MaxListenersExceededWarning",l.emitter=t,l.type=e,l.count=o.length,s=l,console&&console.warn&&console.warn(s)}return t}function h(){if(!this.fired)return this.target.removeListener(this.type,this.wrapFn),this.fired=!0,0===arguments.length?this.listener.call(this.target):this.listener.apply(this.target,arguments)}function p(t,e,r){var n={fired:!1,wrapFn:void 0,target:t,type:e,listener:r},i=h.bind(n);return i.listener=r,n.wrapFn=i,i}function d(t,e,r){var n=t._events;if(void 0===n)return[];var i=n[e];return void 0===i?[]:"function"==typeof i?r?[i.listener||i]:[i]:r?function(t){for(var e=new Array(t.length),r=0;r<e.length;++r)e[r]=t[r].listener||t[r];return e}(i):m(i,i.length)}function g(t){var e=this._events;if(void 0!==e){var r=e[t];if("function"==typeof r)return 1;if(void 0!==r)return r.length}return 0}function m(t,e){for(var r=new Array(e),n=0;n<e;++n)r[n]=t[n];return r}Object.defineProperty(s,"defaultMaxListeners",{enumerable:!0,get:function(){return l},set:function(t){if("number"!=typeof t||t<0||o(t))throw new RangeError('The value of "defaultMaxListeners" is out of range. It must be a non-negative number. Received '+t+".");l=t}}),s.init=function(){void 0!==this._events&&this._events!==Object.getPrototypeOf(this)._events||(this._events=Object.create(null),this._eventsCount=0),this._maxListeners=this._maxListeners||void 0},s.prototype.setMaxListeners=function(t){if("number"!=typeof t||t<0||o(t))throw new RangeError('The value of "n" is out of range. It must be a non-negative number. Received '+t+".");return this._maxListeners=t,this},s.prototype.getMaxListeners=function(){return u(this)},s.prototype.emit=function(t){for(var e=[],r=1;r<arguments.length;r++)e.push(arguments[r]);var n="error"===t,i=this._events;if(void 0!==i)n=n&&void 0===i.error;else if(!n)return!1;if(n){var o;if(e.length>0&&(o=e[0]),o instanceof Error)throw o;var s=new Error("Unhandled error."+(o?" ("+o.message+")":""));throw s.context=o,s}var l=i[t];if(void 0===l)return!1;if("function"==typeof l)a(l,this,e);else{var c=l.length,u=m(l,c);for(r=0;r<c;++r)a(u[r],this,e)}return!0},s.prototype.addListener=function(t,e){return f(this,t,e,!1)},s.prototype.on=s.prototype.addListener,s.prototype.prependListener=function(t,e){return f(this,t,e,!0)},s.prototype.once=function(t,e){return c(e),this.on(t,p(this,t,e)),this},s.prototype.prependOnceListener=function(t,e){return c(e),this.prependListener(t,p(this,t,e)),this},s.prototype.removeListener=function(t,e){var r,n,i,a,o;if(c(e),void 0===(n=this._events))return this;if(void 0===(r=n[t]))return this;if(r===e||r.listener===e)0==--this._eventsCount?this._events=Object.create(null):(delete n[t],n.removeListener&&this.emit("removeListener",t,r.listener||e));else if("function"!=typeof r){for(i=-1,a=r.length-1;a>=0;a--)if(r[a]===e||r[a].listener===e){o=r[a].listener,i=a;break}if(i<0)return this;0===i?r.shift():function(t,e){for(;e+1<t.length;e++)t[e]=t[e+1];t.pop()}(r,i),1===r.length&&(n[t]=r[0]),void 0!==n.removeListener&&this.emit("removeListener",t,o||e)}return this},s.prototype.off=s.prototype.removeListener,s.prototype.removeAllListeners=function(t){var e,r,n;if(void 0===(r=this._events))return this;if(void 0===r.removeListener)return 0===arguments.length?(this._events=Object.create(null),this._eventsCount=0):void 0!==r[t]&&(0==--this._eventsCount?this._events=Object.create(null):delete r[t]),this;if(0===arguments.length){var i,a=Object.keys(r);for(n=0;n<a.length;++n)"removeListener"!==(i=a[n])&&this.removeAllListeners(i);return this.removeAllListeners("removeListener"),this._events=Object.create(null),this._eventsCount=0,this}if("function"==typeof(e=r[t]))this.removeListener(t,e);else if(void 0!==e)for(n=e.length-1;n>=0;n--)this.removeListener(t,e[n]);return this},s.prototype.listeners=function(t){return d(this,t,!0)},s.prototype.rawListeners=function(t){return d(this,t,!1)},s.listenerCount=function(t,e){return"function"==typeof t.listenerCount?t.listenerCount(e):g.call(t,e)},s.prototype.listenerCount=g,s.prototype.eventNames=function(){return this._eventsCount>0?n(this._events):[]}},{}],111:[function(t,e,r){(function(e){(function(){
/*!
 * The buffer module from node.js, for the browser.
 *
 * @author   Feross Aboukhadijeh <https://feross.org>
 * @license  MIT
 */
"use strict";var e=t("base64-js"),n=t("ieee754");r.Buffer=a,r.SlowBuffer=function(t){+t!=t&&(t=0);return a.alloc(+t)},r.INSPECT_MAX_BYTES=50;function i(t){if(t>2147483647)throw new RangeError('The value "'+t+'" is invalid for option "size"');var e=new Uint8Array(t);return e.__proto__=a.prototype,e}function a(t,e,r){if("number"==typeof t){if("string"==typeof e)throw new TypeError('The "string" argument must be of type string. Received type number');return l(t)}return o(t,e,r)}function o(t,e,r){if("string"==typeof t)return function(t,e){"string"==typeof e&&""!==e||(e="utf8");if(!a.isEncoding(e))throw new TypeError("Unknown encoding: "+e);var r=0|f(t,e),n=i(r),o=n.write(t,e);o!==r&&(n=n.slice(0,o));return n}(t,e);if(ArrayBuffer.isView(t))return c(t);if(null==t)throw TypeError("The first argument must be one of type string, Buffer, ArrayBuffer, Array, or Array-like Object. Received type "+typeof t);if(B(t,ArrayBuffer)||t&&B(t.buffer,ArrayBuffer))return function(t,e,r){if(e<0||t.byteLength<e)throw new RangeError('"offset" is outside of buffer bounds');if(t.byteLength<e+(r||0))throw new RangeError('"length" is outside of buffer bounds');var n;n=void 0===e&&void 0===r?new Uint8Array(t):void 0===r?new Uint8Array(t,e):new Uint8Array(t,e,r);return n.__proto__=a.prototype,n}(t,e,r);if("number"==typeof t)throw new TypeError('The "value" argument must not be of type number. Received type number');var n=t.valueOf&&t.valueOf();if(null!=n&&n!==t)return a.from(n,e,r);var o=function(t){if(a.isBuffer(t)){var e=0|u(t.length),r=i(e);return 0===r.length||t.copy(r,0,0,e),r}if(void 0!==t.length)return"number"!=typeof t.length||N(t.length)?i(0):c(t);if("Buffer"===t.type&&Array.isArray(t.data))return c(t.data)}(t);if(o)return o;if("undefined"!=typeof Symbol&&null!=Symbol.toPrimitive&&"function"==typeof t[Symbol.toPrimitive])return a.from(t[Symbol.toPrimitive]("string"),e,r);throw new TypeError("The first argument must be one of type string, Buffer, ArrayBuffer, Array, or Array-like Object. Received type "+typeof t)}function s(t){if("number"!=typeof t)throw new TypeError('"size" argument must be of type number');if(t<0)throw new RangeError('The value "'+t+'" is invalid for option "size"')}function l(t){return s(t),i(t<0?0:0|u(t))}function c(t){for(var e=t.length<0?0:0|u(t.length),r=i(e),n=0;n<e;n+=1)r[n]=255&t[n];return r}function u(t){if(t>=2147483647)throw new RangeError("Attempt to allocate Buffer larger than maximum size: 0x"+2147483647..toString(16)+" bytes");return 0|t}function f(t,e){if(a.isBuffer(t))return t.length;if(ArrayBuffer.isView(t)||B(t,ArrayBuffer))return t.byteLength;if("string"!=typeof t)throw new TypeError('The "string" argument must be one of type string, Buffer, or ArrayBuffer. Received type '+typeof t);var r=t.length,n=arguments.length>2&&!0===arguments[2];if(!n&&0===r)return 0;for(var i=!1;;)switch(e){case"ascii":case"latin1":case"binary":return r;case"utf8":case"utf-8":return D(t).length;case"ucs2":case"ucs-2":case"utf16le":case"utf-16le":return 2*r;case"hex":return r>>>1;case"base64":return R(t).length;default:if(i)return n?-1:D(t).length;e=(""+e).toLowerCase(),i=!0}}function h(t,e,r){var n=!1;if((void 0===e||e<0)&&(e=0),e>this.length)return"";if((void 0===r||r>this.length)&&(r=this.length),r<=0)return"";if((r>>>=0)<=(e>>>=0))return"";for(t||(t="utf8");;)switch(t){case"hex":return A(this,e,r);case"utf8":case"utf-8":return T(this,e,r);case"ascii":return k(this,e,r);case"latin1":case"binary":return M(this,e,r);case"base64":return w(this,e,r);case"ucs2":case"ucs-2":case"utf16le":case"utf-16le":return S(this,e,r);default:if(n)throw new TypeError("Unknown encoding: "+t);t=(t+"").toLowerCase(),n=!0}}function p(t,e,r){var n=t[e];t[e]=t[r],t[r]=n}function d(t,e,r,n,i){if(0===t.length)return-1;if("string"==typeof r?(n=r,r=0):r>2147483647?r=2147483647:r<-2147483648&&(r=-2147483648),N(r=+r)&&(r=i?0:t.length-1),r<0&&(r=t.length+r),r>=t.length){if(i)return-1;r=t.length-1}else if(r<0){if(!i)return-1;r=0}if("string"==typeof e&&(e=a.from(e,n)),a.isBuffer(e))return 0===e.length?-1:g(t,e,r,n,i);if("number"==typeof e)return e&=255,"function"==typeof Uint8Array.prototype.indexOf?i?Uint8Array.prototype.indexOf.call(t,e,r):Uint8Array.prototype.lastIndexOf.call(t,e,r):g(t,[e],r,n,i);throw new TypeError("val must be string, number or Buffer")}function g(t,e,r,n,i){var a,o=1,s=t.length,l=e.length;if(void 0!==n&&("ucs2"===(n=String(n).toLowerCase())||"ucs-2"===n||"utf16le"===n||"utf-16le"===n)){if(t.length<2||e.length<2)return-1;o=2,s/=2,l/=2,r/=2}function c(t,e){return 1===o?t[e]:t.readUInt16BE(e*o)}if(i){var u=-1;for(a=r;a<s;a++)if(c(t,a)===c(e,-1===u?0:a-u)){if(-1===u&&(u=a),a-u+1===l)return u*o}else-1!==u&&(a-=a-u),u=-1}else for(r+l>s&&(r=s-l),a=r;a>=0;a--){for(var f=!0,h=0;h<l;h++)if(c(t,a+h)!==c(e,h)){f=!1;break}if(f)return a}return-1}function m(t,e,r,n){r=Number(r)||0;var i=t.length-r;n?(n=Number(n))>i&&(n=i):n=i;var a=e.length;n>a/2&&(n=a/2);for(var o=0;o<n;++o){var s=parseInt(e.substr(2*o,2),16);if(N(s))return o;t[r+o]=s}return o}function v(t,e,r,n){return F(D(e,t.length-r),t,r,n)}function y(t,e,r,n){return F(function(t){for(var e=[],r=0;r<t.length;++r)e.push(255&t.charCodeAt(r));return e}(e),t,r,n)}function x(t,e,r,n){return y(t,e,r,n)}function b(t,e,r,n){return F(R(e),t,r,n)}function _(t,e,r,n){return F(function(t,e){for(var r,n,i,a=[],o=0;o<t.length&&!((e-=2)<0);++o)r=t.charCodeAt(o),n=r>>8,i=r%256,a.push(i),a.push(n);return a}(e,t.length-r),t,r,n)}function w(t,r,n){return 0===r&&n===t.length?e.fromByteArray(t):e.fromByteArray(t.slice(r,n))}function T(t,e,r){r=Math.min(t.length,r);for(var n=[],i=e;i<r;){var a,o,s,l,c=t[i],u=null,f=c>239?4:c>223?3:c>191?2:1;if(i+f<=r)switch(f){case 1:c<128&&(u=c);break;case 2:128==(192&(a=t[i+1]))&&(l=(31&c)<<6|63&a)>127&&(u=l);break;case 3:a=t[i+1],o=t[i+2],128==(192&a)&&128==(192&o)&&(l=(15&c)<<12|(63&a)<<6|63&o)>2047&&(l<55296||l>57343)&&(u=l);break;case 4:a=t[i+1],o=t[i+2],s=t[i+3],128==(192&a)&&128==(192&o)&&128==(192&s)&&(l=(15&c)<<18|(63&a)<<12|(63&o)<<6|63&s)>65535&&l<1114112&&(u=l)}null===u?(u=65533,f=1):u>65535&&(u-=65536,n.push(u>>>10&1023|55296),u=56320|1023&u),n.push(u),i+=f}return function(t){var e=t.length;if(e<=4096)return String.fromCharCode.apply(String,t);var r="",n=0;for(;n<e;)r+=String.fromCharCode.apply(String,t.slice(n,n+=4096));return r}(n)}r.kMaxLength=2147483647,a.TYPED_ARRAY_SUPPORT=function(){try{var t=new Uint8Array(1);return t.__proto__={__proto__:Uint8Array.prototype,foo:function(){return 42}},42===t.foo()}catch(t){return!1}}(),a.TYPED_ARRAY_SUPPORT||"undefined"==typeof console||"function"!=typeof console.error||console.error("This browser lacks typed array (Uint8Array) support which is required by `buffer` v5.x. Use `buffer` v4.x if you require old browser support."),Object.defineProperty(a.prototype,"parent",{enumerable:!0,get:function(){if(a.isBuffer(this))return this.buffer}}),Object.defineProperty(a.prototype,"offset",{enumerable:!0,get:function(){if(a.isBuffer(this))return this.byteOffset}}),"undefined"!=typeof Symbol&&null!=Symbol.species&&a[Symbol.species]===a&&Object.defineProperty(a,Symbol.species,{value:null,configurable:!0,enumerable:!1,writable:!1}),a.poolSize=8192,a.from=function(t,e,r){return o(t,e,r)},a.prototype.__proto__=Uint8Array.prototype,a.__proto__=Uint8Array,a.alloc=function(t,e,r){return function(t,e,r){return s(t),t<=0?i(t):void 0!==e?"string"==typeof r?i(t).fill(e,r):i(t).fill(e):i(t)}(t,e,r)},a.allocUnsafe=function(t){return l(t)},a.allocUnsafeSlow=function(t){return l(t)},a.isBuffer=function(t){return null!=t&&!0===t._isBuffer&&t!==a.prototype},a.compare=function(t,e){if(B(t,Uint8Array)&&(t=a.from(t,t.offset,t.byteLength)),B(e,Uint8Array)&&(e=a.from(e,e.offset,e.byteLength)),!a.isBuffer(t)||!a.isBuffer(e))throw new TypeError('The "buf1", "buf2" arguments must be one of type Buffer or Uint8Array');if(t===e)return 0;for(var r=t.length,n=e.length,i=0,o=Math.min(r,n);i<o;++i)if(t[i]!==e[i]){r=t[i],n=e[i];break}return r<n?-1:n<r?1:0},a.isEncoding=function(t){switch(String(t).toLowerCase()){case"hex":case"utf8":case"utf-8":case"ascii":case"latin1":case"binary":case"base64":case"ucs2":case"ucs-2":case"utf16le":case"utf-16le":return!0;default:return!1}},a.concat=function(t,e){if(!Array.isArray(t))throw new TypeError('"list" argument must be an Array of Buffers');if(0===t.length)return a.alloc(0);var r;if(void 0===e)for(e=0,r=0;r<t.length;++r)e+=t[r].length;var n=a.allocUnsafe(e),i=0;for(r=0;r<t.length;++r){var o=t[r];if(B(o,Uint8Array)&&(o=a.from(o)),!a.isBuffer(o))throw new TypeError('"list" argument must be an Array of Buffers');o.copy(n,i),i+=o.length}return n},a.byteLength=f,a.prototype._isBuffer=!0,a.prototype.swap16=function(){var t=this.length;if(t%2!=0)throw new RangeError("Buffer size must be a multiple of 16-bits");for(var e=0;e<t;e+=2)p(this,e,e+1);return this},a.prototype.swap32=function(){var t=this.length;if(t%4!=0)throw new RangeError("Buffer size must be a multiple of 32-bits");for(var e=0;e<t;e+=4)p(this,e,e+3),p(this,e+1,e+2);return this},a.prototype.swap64=function(){var t=this.length;if(t%8!=0)throw new RangeError("Buffer size must be a multiple of 64-bits");for(var e=0;e<t;e+=8)p(this,e,e+7),p(this,e+1,e+6),p(this,e+2,e+5),p(this,e+3,e+4);return this},a.prototype.toString=function(){var t=this.length;return 0===t?"":0===arguments.length?T(this,0,t):h.apply(this,arguments)},a.prototype.toLocaleString=a.prototype.toString,a.prototype.equals=function(t){if(!a.isBuffer(t))throw new TypeError("Argument must be a Buffer");return this===t||0===a.compare(this,t)},a.prototype.inspect=function(){var t="",e=r.INSPECT_MAX_BYTES;return t=this.toString("hex",0,e).replace(/(.{2})/g,"$1 ").trim(),this.length>e&&(t+=" ... "),"<Buffer "+t+">"},a.prototype.compare=function(t,e,r,n,i){if(B(t,Uint8Array)&&(t=a.from(t,t.offset,t.byteLength)),!a.isBuffer(t))throw new TypeError('The "target" argument must be one of type Buffer or Uint8Array. Received type '+typeof t);if(void 0===e&&(e=0),void 0===r&&(r=t?t.length:0),void 0===n&&(n=0),void 0===i&&(i=this.length),e<0||r>t.length||n<0||i>this.length)throw new RangeError("out of range index");if(n>=i&&e>=r)return 0;if(n>=i)return-1;if(e>=r)return 1;if(this===t)return 0;for(var o=(i>>>=0)-(n>>>=0),s=(r>>>=0)-(e>>>=0),l=Math.min(o,s),c=this.slice(n,i),u=t.slice(e,r),f=0;f<l;++f)if(c[f]!==u[f]){o=c[f],s=u[f];break}return o<s?-1:s<o?1:0},a.prototype.includes=function(t,e,r){return-1!==this.indexOf(t,e,r)},a.prototype.indexOf=function(t,e,r){return d(this,t,e,r,!0)},a.prototype.lastIndexOf=function(t,e,r){return d(this,t,e,r,!1)},a.prototype.write=function(t,e,r,n){if(void 0===e)n="utf8",r=this.length,e=0;else if(void 0===r&&"string"==typeof e)n=e,r=this.length,e=0;else{if(!isFinite(e))throw new Error("Buffer.write(string, encoding, offset[, length]) is no longer supported");e>>>=0,isFinite(r)?(r>>>=0,void 0===n&&(n="utf8")):(n=r,r=void 0)}var i=this.length-e;if((void 0===r||r>i)&&(r=i),t.length>0&&(r<0||e<0)||e>this.length)throw new RangeError("Attempt to write outside buffer bounds");n||(n="utf8");for(var a=!1;;)switch(n){case"hex":return m(this,t,e,r);case"utf8":case"utf-8":return v(this,t,e,r);case"ascii":return y(this,t,e,r);case"latin1":case"binary":return x(this,t,e,r);case"base64":return b(this,t,e,r);case"ucs2":case"ucs-2":case"utf16le":case"utf-16le":return _(this,t,e,r);default:if(a)throw new TypeError("Unknown encoding: "+n);n=(""+n).toLowerCase(),a=!0}},a.prototype.toJSON=function(){return{type:"Buffer",data:Array.prototype.slice.call(this._arr||this,0)}};function k(t,e,r){var n="";r=Math.min(t.length,r);for(var i=e;i<r;++i)n+=String.fromCharCode(127&t[i]);return n}function M(t,e,r){var n="";r=Math.min(t.length,r);for(var i=e;i<r;++i)n+=String.fromCharCode(t[i]);return n}function A(t,e,r){var n=t.length;(!e||e<0)&&(e=0),(!r||r<0||r>n)&&(r=n);for(var i="",a=e;a<r;++a)i+=O(t[a]);return i}function S(t,e,r){for(var n=t.slice(e,r),i="",a=0;a<n.length;a+=2)i+=String.fromCharCode(n[a]+256*n[a+1]);return i}function E(t,e,r){if(t%1!=0||t<0)throw new RangeError("offset is not uint");if(t+e>r)throw new RangeError("Trying to access beyond buffer length")}function C(t,e,r,n,i,o){if(!a.isBuffer(t))throw new TypeError('"buffer" argument must be a Buffer instance');if(e>i||e<o)throw new RangeError('"value" argument is out of bounds');if(r+n>t.length)throw new RangeError("Index out of range")}function L(t,e,r,n,i,a){if(r+n>t.length)throw new RangeError("Index out of range");if(r<0)throw new RangeError("Index out of range")}function I(t,e,r,i,a){return e=+e,r>>>=0,a||L(t,0,r,4),n.write(t,e,r,i,23,4),r+4}function P(t,e,r,i,a){return e=+e,r>>>=0,a||L(t,0,r,8),n.write(t,e,r,i,52,8),r+8}a.prototype.slice=function(t,e){var r=this.length;(t=~~t)<0?(t+=r)<0&&(t=0):t>r&&(t=r),(e=void 0===e?r:~~e)<0?(e+=r)<0&&(e=0):e>r&&(e=r),e<t&&(e=t);var n=this.subarray(t,e);return n.__proto__=a.prototype,n},a.prototype.readUIntLE=function(t,e,r){t>>>=0,e>>>=0,r||E(t,e,this.length);for(var n=this[t],i=1,a=0;++a<e&&(i*=256);)n+=this[t+a]*i;return n},a.prototype.readUIntBE=function(t,e,r){t>>>=0,e>>>=0,r||E(t,e,this.length);for(var n=this[t+--e],i=1;e>0&&(i*=256);)n+=this[t+--e]*i;return n},a.prototype.readUInt8=function(t,e){return t>>>=0,e||E(t,1,this.length),this[t]},a.prototype.readUInt16LE=function(t,e){return t>>>=0,e||E(t,2,this.length),this[t]|this[t+1]<<8},a.prototype.readUInt16BE=function(t,e){return t>>>=0,e||E(t,2,this.length),this[t]<<8|this[t+1]},a.prototype.readUInt32LE=function(t,e){return t>>>=0,e||E(t,4,this.length),(this[t]|this[t+1]<<8|this[t+2]<<16)+16777216*this[t+3]},a.prototype.readUInt32BE=function(t,e){return t>>>=0,e||E(t,4,this.length),16777216*this[t]+(this[t+1]<<16|this[t+2]<<8|this[t+3])},a.prototype.readIntLE=function(t,e,r){t>>>=0,e>>>=0,r||E(t,e,this.length);for(var n=this[t],i=1,a=0;++a<e&&(i*=256);)n+=this[t+a]*i;return n>=(i*=128)&&(n-=Math.pow(2,8*e)),n},a.prototype.readIntBE=function(t,e,r){t>>>=0,e>>>=0,r||E(t,e,this.length);for(var n=e,i=1,a=this[t+--n];n>0&&(i*=256);)a+=this[t+--n]*i;return a>=(i*=128)&&(a-=Math.pow(2,8*e)),a},a.prototype.readInt8=function(t,e){return t>>>=0,e||E(t,1,this.length),128&this[t]?-1*(255-this[t]+1):this[t]},a.prototype.readInt16LE=function(t,e){t>>>=0,e||E(t,2,this.length);var r=this[t]|this[t+1]<<8;return 32768&r?4294901760|r:r},a.prototype.readInt16BE=function(t,e){t>>>=0,e||E(t,2,this.length);var r=this[t+1]|this[t]<<8;return 32768&r?4294901760|r:r},a.prototype.readInt32LE=function(t,e){return t>>>=0,e||E(t,4,this.length),this[t]|this[t+1]<<8|this[t+2]<<16|this[t+3]<<24},a.prototype.readInt32BE=function(t,e){return t>>>=0,e||E(t,4,this.length),this[t]<<24|this[t+1]<<16|this[t+2]<<8|this[t+3]},a.prototype.readFloatLE=function(t,e){return t>>>=0,e||E(t,4,this.length),n.read(this,t,!0,23,4)},a.prototype.readFloatBE=function(t,e){return t>>>=0,e||E(t,4,this.length),n.read(this,t,!1,23,4)},a.prototype.readDoubleLE=function(t,e){return t>>>=0,e||E(t,8,this.length),n.read(this,t,!0,52,8)},a.prototype.readDoubleBE=function(t,e){return t>>>=0,e||E(t,8,this.length),n.read(this,t,!1,52,8)},a.prototype.writeUIntLE=function(t,e,r,n){(t=+t,e>>>=0,r>>>=0,n)||C(this,t,e,r,Math.pow(2,8*r)-1,0);var i=1,a=0;for(this[e]=255&t;++a<r&&(i*=256);)this[e+a]=t/i&255;return e+r},a.prototype.writeUIntBE=function(t,e,r,n){(t=+t,e>>>=0,r>>>=0,n)||C(this,t,e,r,Math.pow(2,8*r)-1,0);var i=r-1,a=1;for(this[e+i]=255&t;--i>=0&&(a*=256);)this[e+i]=t/a&255;return e+r},a.prototype.writeUInt8=function(t,e,r){return t=+t,e>>>=0,r||C(this,t,e,1,255,0),this[e]=255&t,e+1},a.prototype.writeUInt16LE=function(t,e,r){return t=+t,e>>>=0,r||C(this,t,e,2,65535,0),this[e]=255&t,this[e+1]=t>>>8,e+2},a.prototype.writeUInt16BE=function(t,e,r){return t=+t,e>>>=0,r||C(this,t,e,2,65535,0),this[e]=t>>>8,this[e+1]=255&t,e+2},a.prototype.writeUInt32LE=function(t,e,r){return t=+t,e>>>=0,r||C(this,t,e,4,4294967295,0),this[e+3]=t>>>24,this[e+2]=t>>>16,this[e+1]=t>>>8,this[e]=255&t,e+4},a.prototype.writeUInt32BE=function(t,e,r){return t=+t,e>>>=0,r||C(this,t,e,4,4294967295,0),this[e]=t>>>24,this[e+1]=t>>>16,this[e+2]=t>>>8,this[e+3]=255&t,e+4},a.prototype.writeIntLE=function(t,e,r,n){if(t=+t,e>>>=0,!n){var i=Math.pow(2,8*r-1);C(this,t,e,r,i-1,-i)}var a=0,o=1,s=0;for(this[e]=255&t;++a<r&&(o*=256);)t<0&&0===s&&0!==this[e+a-1]&&(s=1),this[e+a]=(t/o>>0)-s&255;return e+r},a.prototype.writeIntBE=function(t,e,r,n){if(t=+t,e>>>=0,!n){var i=Math.pow(2,8*r-1);C(this,t,e,r,i-1,-i)}var a=r-1,o=1,s=0;for(this[e+a]=255&t;--a>=0&&(o*=256);)t<0&&0===s&&0!==this[e+a+1]&&(s=1),this[e+a]=(t/o>>0)-s&255;return e+r},a.prototype.writeInt8=function(t,e,r){return t=+t,e>>>=0,r||C(this,t,e,1,127,-128),t<0&&(t=255+t+1),this[e]=255&t,e+1},a.prototype.writeInt16LE=function(t,e,r){return t=+t,e>>>=0,r||C(this,t,e,2,32767,-32768),this[e]=255&t,this[e+1]=t>>>8,e+2},a.prototype.writeInt16BE=function(t,e,r){return t=+t,e>>>=0,r||C(this,t,e,2,32767,-32768),this[e]=t>>>8,this[e+1]=255&t,e+2},a.prototype.writeInt32LE=function(t,e,r){return t=+t,e>>>=0,r||C(this,t,e,4,2147483647,-2147483648),this[e]=255&t,this[e+1]=t>>>8,this[e+2]=t>>>16,this[e+3]=t>>>24,e+4},a.prototype.writeInt32BE=function(t,e,r){return t=+t,e>>>=0,r||C(this,t,e,4,2147483647,-2147483648),t<0&&(t=4294967295+t+1),this[e]=t>>>24,this[e+1]=t>>>16,this[e+2]=t>>>8,this[e+3]=255&t,e+4},a.prototype.writeFloatLE=function(t,e,r){return I(this,t,e,!0,r)},a.prototype.writeFloatBE=function(t,e,r){return I(this,t,e,!1,r)},a.prototype.writeDoubleLE=function(t,e,r){return P(this,t,e,!0,r)},a.prototype.writeDoubleBE=function(t,e,r){return P(this,t,e,!1,r)},a.prototype.copy=function(t,e,r,n){if(!a.isBuffer(t))throw new TypeError("argument should be a Buffer");if(r||(r=0),n||0===n||(n=this.length),e>=t.length&&(e=t.length),e||(e=0),n>0&&n<r&&(n=r),n===r)return 0;if(0===t.length||0===this.length)return 0;if(e<0)throw new RangeError("targetStart out of bounds");if(r<0||r>=this.length)throw new RangeError("Index out of range");if(n<0)throw new RangeError("sourceEnd out of bounds");n>this.length&&(n=this.length),t.length-e<n-r&&(n=t.length-e+r);var i=n-r;if(this===t&&"function"==typeof Uint8Array.prototype.copyWithin)this.copyWithin(e,r,n);else if(this===t&&r<e&&e<n)for(var o=i-1;o>=0;--o)t[o+e]=this[o+r];else Uint8Array.prototype.set.call(t,this.subarray(r,n),e);return i},a.prototype.fill=function(t,e,r,n){if("string"==typeof t){if("string"==typeof e?(n=e,e=0,r=this.length):"string"==typeof r&&(n=r,r=this.length),void 0!==n&&"string"!=typeof n)throw new TypeError("encoding must be a string");if("string"==typeof n&&!a.isEncoding(n))throw new TypeError("Unknown encoding: "+n);if(1===t.length){var i=t.charCodeAt(0);("utf8"===n&&i<128||"latin1"===n)&&(t=i)}}else"number"==typeof t&&(t&=255);if(e<0||this.length<e||this.length<r)throw new RangeError("Out of range index");if(r<=e)return this;var o;if(e>>>=0,r=void 0===r?this.length:r>>>0,t||(t=0),"number"==typeof t)for(o=e;o<r;++o)this[o]=t;else{var s=a.isBuffer(t)?t:a.from(t,n),l=s.length;if(0===l)throw new TypeError('The value "'+t+'" is invalid for argument "value"');for(o=0;o<r-e;++o)this[o+e]=s[o%l]}return this};var z=/[^+/0-9A-Za-z-_]/g;function O(t){return t<16?"0"+t.toString(16):t.toString(16)}function D(t,e){var r;e=e||1/0;for(var n=t.length,i=null,a=[],o=0;o<n;++o){if((r=t.charCodeAt(o))>55295&&r<57344){if(!i){if(r>56319){(e-=3)>-1&&a.push(239,191,189);continue}if(o+1===n){(e-=3)>-1&&a.push(239,191,189);continue}i=r;continue}if(r<56320){(e-=3)>-1&&a.push(239,191,189),i=r;continue}r=65536+(i-55296<<10|r-56320)}else i&&(e-=3)>-1&&a.push(239,191,189);if(i=null,r<128){if((e-=1)<0)break;a.push(r)}else if(r<2048){if((e-=2)<0)break;a.push(r>>6|192,63&r|128)}else if(r<65536){if((e-=3)<0)break;a.push(r>>12|224,r>>6&63|128,63&r|128)}else{if(!(r<1114112))throw new Error("Invalid code point");if((e-=4)<0)break;a.push(r>>18|240,r>>12&63|128,r>>6&63|128,63&r|128)}}return a}function R(t){return e.toByteArray(function(t){if((t=(t=t.split("=")[0]).trim().replace(z,"")).length<2)return"";for(;t.length%4!=0;)t+="=";return t}(t))}function F(t,e,r,n){for(var i=0;i<n&&!(i+r>=e.length||i>=t.length);++i)e[i+r]=t[i];return i}function B(t,e){return t instanceof e||null!=t&&null!=t.constructor&&null!=t.constructor.name&&t.constructor.name===e.name}function N(t){return t!=t}}).call(this)}).call(this,t("buffer").Buffer)},{"base64-js":79,buffer:111,ieee754:442}],112:[function(t,e,r){"use strict";var n=t("./lib/monotone"),i=t("./lib/triangulation"),a=t("./lib/delaunay"),o=t("./lib/filter");function s(t){return[Math.min(t[0],t[1]),Math.max(t[0],t[1])]}function l(t,e){return t[0]-e[0]||t[1]-e[1]}function c(t,e,r){return e in t?t[e]:r}e.exports=function(t,e,r){Array.isArray(e)?(r=r||{},e=e||[]):(r=e||{},e=[]);var u=!!c(r,"delaunay",!0),f=!!c(r,"interior",!0),h=!!c(r,"exterior",!0),p=!!c(r,"infinity",!1);if(!f&&!h||0===t.length)return[];var d=n(t,e);if(u||f!==h||p){for(var g=i(t.length,function(t){return t.map(s).sort(l)}(e)),m=0;m<d.length;++m){var v=d[m];g.addTriangle(v[0],v[1],v[2])}return u&&a(t,g),h?f?p?o(g,0,p):g.cells():o(g,1,p):o(g,-1)}return d}},{"./lib/delaunay":113,"./lib/filter":114,"./lib/monotone":115,"./lib/triangulation":116}],113:[function(t,e,r){"use strict";var n=t("robust-in-sphere")[4];t("binary-search-bounds");function i(t,e,r,i,a,o){var s=e.opposite(i,a);if(!(s<0)){if(a<i){var l=i;i=a,a=l,l=o,o=s,s=l}e.isConstraint(i,a)||n(t[i],t[a],t[o],t[s])<0&&r.push(i,a)}}e.exports=function(t,e){for(var r=[],a=t.length,o=e.stars,s=0;s<a;++s)for(var l=o[s],c=1;c<l.length;c+=2){if(!((p=l[c])<s)&&!e.isConstraint(s,p)){for(var u=l[c-1],f=-1,h=1;h<l.length;h+=2)if(l[h-1]===p){f=l[h];break}f<0||n(t[s],t[p],t[u],t[f])<0&&r.push(s,p)}}for(;r.length>0;){for(var p=r.pop(),d=(s=r.pop(),u=-1,f=-1,l=o[s],1);d<l.length;d+=2){var g=l[d-1],m=l[d];g===p?f=m:m===p&&(u=g)}u<0||f<0||(n(t[s],t[p],t[u],t[f])>=0||(e.flip(s,p),i(t,e,r,u,s,f),i(t,e,r,s,f,u),i(t,e,r,f,p,u),i(t,e,r,p,u,f)))}}},{"binary-search-bounds":96,"robust-in-sphere":546}],114:[function(t,e,r){"use strict";var n,i=t("binary-search-bounds");function a(t,e,r,n,i,a,o){this.cells=t,this.neighbor=e,this.flags=n,this.constraint=r,this.active=i,this.next=a,this.boundary=o}function o(t,e){return t[0]-e[0]||t[1]-e[1]||t[2]-e[2]}e.exports=function(t,e,r){var n=function(t,e){for(var r=t.cells(),n=r.length,i=0;i<n;++i){var s=(v=r[i])[0],l=v[1],c=v[2];l<c?l<s&&(v[0]=l,v[1]=c,v[2]=s):c<s&&(v[0]=c,v[1]=s,v[2]=l)}r.sort(o);var u=new Array(n);for(i=0;i<u.length;++i)u[i]=0;var f=[],h=[],p=new Array(3*n),d=new Array(3*n),g=null;e&&(g=[]);var m=new a(r,p,d,u,f,h,g);for(i=0;i<n;++i)for(var v=r[i],y=0;y<3;++y){s=v[y],l=v[(y+1)%3];var x=p[3*i+y]=m.locate(l,s,t.opposite(l,s)),b=d[3*i+y]=t.isConstraint(s,l);x<0&&(b?h.push(i):(f.push(i),u[i]=1),e&&g.push([l,s,-1]))}return m}(t,r);if(0===e)return r?n.cells.concat(n.boundary):n.cells;var i=1,s=n.active,l=n.next,c=n.flags,u=n.cells,f=n.constraint,h=n.neighbor;for(;s.length>0||l.length>0;){for(;s.length>0;){var p=s.pop();if(c[p]!==-i){c[p]=i;u[p];for(var d=0;d<3;++d){var g=h[3*p+d];g>=0&&0===c[g]&&(f[3*p+d]?l.push(g):(s.push(g),c[g]=i))}}}var m=l;l=s,s=m,l.length=0,i=-i}var v=function(t,e,r){for(var n=0,i=0;i<t.length;++i)e[i]===r&&(t[n++]=t[i]);return t.length=n,t}(u,c,e);if(r)return v.concat(n.boundary);return v},a.prototype.locate=(n=[0,0,0],function(t,e,r){var a=t,s=e,l=r;return e<r?e<t&&(a=e,s=r,l=t):r<t&&(a=r,s=t,l=e),a<0?-1:(n[0]=a,n[1]=s,n[2]=l,i.eq(this.cells,n,o))})},{"binary-search-bounds":96}],115:[function(t,e,r){"use strict";var n=t("binary-search-bounds"),i=t("robust-orientation")[3];function a(t,e,r,n,i){this.a=t,this.b=e,this.idx=r,this.lowerIds=n,this.upperIds=i}function o(t,e,r,n){this.a=t,this.b=e,this.type=r,this.idx=n}function s(t,e){var r=t.a[0]-e.a[0]||t.a[1]-e.a[1]||t.type-e.type;return r||(0!==t.type&&(r=i(t.a,t.b,e.b))?r:t.idx-e.idx)}function l(t,e){return i(t.a,t.b,e)}function c(t,e,r,a,o){for(var s=n.lt(e,a,l),c=n.gt(e,a,l),u=s;u<c;++u){for(var f=e[u],h=f.lowerIds,p=h.length;p>1&&i(r[h[p-2]],r[h[p-1]],a)>0;)t.push([h[p-1],h[p-2],o]),p-=1;h.length=p,h.push(o);var d=f.upperIds;for(p=d.length;p>1&&i(r[d[p-2]],r[d[p-1]],a)<0;)t.push([d[p-2],d[p-1],o]),p-=1;d.length=p,d.push(o)}}function u(t,e){var r;return(r=t.a[0]<e.a[0]?i(t.a,t.b,e.a):i(e.b,e.a,t.a))?r:(r=e.b[0]<t.b[0]?i(t.a,t.b,e.b):i(e.b,e.a,t.b))||t.idx-e.idx}function f(t,e,r){var i=n.le(t,r,u),o=t[i],s=o.upperIds,l=s[s.length-1];o.upperIds=[l],t.splice(i+1,0,new a(r.a,r.b,r.idx,[l],s))}function h(t,e,r){var i=r.a;r.a=r.b,r.b=i;var a=n.eq(t,r,u),o=t[a];t[a-1].upperIds=o.upperIds,t.splice(a,1)}e.exports=function(t,e){for(var r=t.length,n=e.length,i=[],l=0;l<r;++l)i.push(new o(t[l],null,0,l));for(l=0;l<n;++l){var u=e[l],p=t[u[0]],d=t[u[1]];p[0]<d[0]?i.push(new o(p,d,2,l),new o(d,p,1,l)):p[0]>d[0]&&i.push(new o(d,p,2,l),new o(p,d,1,l))}i.sort(s);for(var g=i[0].a[0]-(1+Math.abs(i[0].a[0]))*Math.pow(2,-52),m=[new a([g,1],[g,0],-1,[],[],[],[])],v=[],y=(l=0,i.length);l<y;++l){var x=i[l],b=x.type;0===b?c(v,m,t,x.a,x.idx):2===b?f(m,t,x):h(m,t,x)}return v}},{"binary-search-bounds":96,"robust-orientation":548}],116:[function(t,e,r){"use strict";var n=t("binary-search-bounds");function i(t,e){this.stars=t,this.edges=e}e.exports=function(t,e){for(var r=new Array(t),n=0;n<t;++n)r[n]=[];return new i(r,e)};var a=i.prototype;function o(t,e,r){for(var n=1,i=t.length;n<i;n+=2)if(t[n-1]===e&&t[n]===r)return t[n-1]=t[i-2],t[n]=t[i-1],void(t.length=i-2)}a.isConstraint=function(){var t=[0,0];function e(t,e){return t[0]-e[0]||t[1]-e[1]}return function(r,i){return t[0]=Math.min(r,i),t[1]=Math.max(r,i),n.eq(this.edges,t,e)>=0}}(),a.removeTriangle=function(t,e,r){var n=this.stars;o(n[t],e,r),o(n[e],r,t),o(n[r],t,e)},a.addTriangle=function(t,e,r){var n=this.stars;n[t].push(e,r),n[e].push(r,t),n[r].push(t,e)},a.opposite=function(t,e){for(var r=this.stars[e],n=1,i=r.length;n<i;n+=2)if(r[n]===t)return r[n-1];return-1},a.flip=function(t,e){var r=this.opposite(t,e),n=this.opposite(e,t);this.removeTriangle(t,e,r),this.removeTriangle(e,t,n),this.addTriangle(t,n,r),this.addTriangle(e,r,n)},a.edges=function(){for(var t=this.stars,e=[],r=0,n=t.length;r<n;++r)for(var i=t[r],a=0,o=i.length;a<o;a+=2)e.push([i[a],i[a+1]]);return e},a.cells=function(){for(var t=this.stars,e=[],r=0,n=t.length;r<n;++r)for(var i=t[r],a=0,o=i.length;a<o;a+=2){var s=i[a],l=i[a+1];r<Math.min(s,l)&&e.push([r,s,l])}return e}},{"binary-search-bounds":96}],117:[function(t,e,r){"use strict";e.exports=function(t){for(var e=1,r=1;r<t.length;++r)for(var n=0;n<r;++n)if(t[r]<t[n])e=-e;else if(t[n]===t[r])return 0;return e}},{}],118:[function(t,e,r){"use strict";var n=t("dup"),i=t("robust-linear-solve");function a(t,e){for(var r=0,n=t.length,i=0;i<n;++i)r+=t[i]*e[i];return r}function o(t){var e=t.length;if(0===e)return[];t[0].length;var r=n([t.length+1,t.length+1],1),o=n([t.length+1],1);r[e][e]=0;for(var s=0;s<e;++s){for(var l=0;l<=s;++l)r[l][s]=r[s][l]=2*a(t[s],t[l]);o[s]=a(t[s],t[s])}var c=i(r,o),u=0,f=c[e+1];for(s=0;s<f.length;++s)u+=f[s];var h=new Array(e);for(s=0;s<e;++s){f=c[s];var p=0;for(l=0;l<f.length;++l)p+=f[l];h[s]=p/u}return h}function s(t){if(0===t.length)return[];for(var e=t[0].length,r=n([e]),i=o(t),a=0;a<t.length;++a)for(var s=0;s<e;++s)r[s]+=t[a][s]*i[a];return r}s.barycenetric=o,e.exports=s},{dup:176,"robust-linear-solve":547}],119:[function(t,e,r){e.exports=function(t){for(var e=n(t),r=0,i=0;i<t.length;++i)for(var a=t[i],o=0;o<e.length;++o)r+=Math.pow(a[o]-e[o],2);return Math.sqrt(r/t.length)};var n=t("circumcenter")},{circumcenter:118}],120:[function(t,e,r){e.exports=function(t,e,r){return e<r?t<e?e:t>r?r:t:t<r?r:t>e?e:t}},{}],121:[function(t,e,r){"use strict";e.exports=function(t,e,r){var n;if(r){n=e;for(var i=new Array(e.length),a=0;a<e.length;++a){var o=e[a];i[a]=[o[0],o[1],r[a]]}e=i}var s=function(t,e,r){var n=d(t,[],p(t));return v(e,n,r),!!n}(t,e,!!r);for(;y(t,e,!!r);)s=!0;if(r&&s){n.length=0,r.length=0;for(a=0;a<e.length;++a){o=e[a];n.push([o[0],o[1]]),r.push(o[2])}}return s};var n=t("union-find"),i=t("box-intersect"),a=t("robust-segment-intersect"),o=t("big-rat"),s=t("big-rat/cmp"),l=t("big-rat/to-float"),c=t("rat-vec"),u=t("nextafter"),f=t("./lib/rat-seg-intersect");function h(t){var e=l(t);return[u(e,-1/0),u(e,1/0)]}function p(t){for(var e=new Array(t.length),r=0;r<t.length;++r){var n=t[r];e[r]=[u(n[0],-1/0),u(n[1],-1/0),u(n[0],1/0),u(n[1],1/0)]}return e}function d(t,e,r){for(var a=e.length,o=new n(a),s=[],l=0;l<e.length;++l){var c=e[l],f=h(c[0]),p=h(c[1]);s.push([u(f[0],-1/0),u(p[0],-1/0),u(f[1],1/0),u(p[1],1/0)])}i(s,(function(t,e){o.link(t,e)}));var d=!0,g=new Array(a);for(l=0;l<a;++l){(v=o.find(l))!==l&&(d=!1,t[v]=[Math.min(t[l][0],t[v][0]),Math.min(t[l][1],t[v][1])])}if(d)return null;var m=0;for(l=0;l<a;++l){var v;(v=o.find(l))===l?(g[l]=m,t[m++]=t[l]):g[l]=-1}t.length=m;for(l=0;l<a;++l)g[l]<0&&(g[l]=g[o.find(l)]);return g}function g(t,e){return t[0]-e[0]||t[1]-e[1]}function m(t,e){var r=t[0]-e[0]||t[1]-e[1];return r||(t[2]<e[2]?-1:t[2]>e[2]?1:0)}function v(t,e,r){if(0!==t.length){if(e)for(var n=0;n<t.length;++n){var i=e[(o=t[n])[0]],a=e[o[1]];o[0]=Math.min(i,a),o[1]=Math.max(i,a)}else for(n=0;n<t.length;++n){var o;i=(o=t[n])[0],a=o[1];o[0]=Math.min(i,a),o[1]=Math.max(i,a)}r?t.sort(m):t.sort(g);var s=1;for(n=1;n<t.length;++n){var l=t[n-1],c=t[n];(c[0]!==l[0]||c[1]!==l[1]||r&&c[2]!==l[2])&&(t[s++]=c)}t.length=s}}function y(t,e,r){var n=function(t,e){for(var r=new Array(e.length),n=0;n<e.length;++n){var i=e[n],a=t[i[0]],o=t[i[1]];r[n]=[u(Math.min(a[0],o[0]),-1/0),u(Math.min(a[1],o[1]),-1/0),u(Math.max(a[0],o[0]),1/0),u(Math.max(a[1],o[1]),1/0)]}return r}(t,e),h=function(t,e,r){var n=[];return i(r,(function(r,i){var o=e[r],s=e[i];if(o[0]!==s[0]&&o[0]!==s[1]&&o[1]!==s[0]&&o[1]!==s[1]){var l=t[o[0]],c=t[o[1]],u=t[s[0]],f=t[s[1]];a(l,c,u,f)&&n.push([r,i])}})),n}(t,e,n),g=p(t),m=function(t,e,r,n){var o=[];return i(r,n,(function(r,n){var i=e[r];if(i[0]!==n&&i[1]!==n){var s=t[n],l=t[i[0]],c=t[i[1]];a(l,c,s,s)&&o.push([r,n])}})),o}(t,e,n,g),y=d(t,function(t,e,r,n,i){var a,u,h=t.map((function(t){return[o(t[0]),o(t[1])]}));for(a=0;a<r.length;++a){var p=r[a];u=p[0];var d=p[1],g=e[u],m=e[d],v=f(c(t[g[0]]),c(t[g[1]]),c(t[m[0]]),c(t[m[1]]));if(v){var y=t.length;t.push([l(v[0]),l(v[1])]),h.push(v),n.push([u,y],[d,y])}}for(n.sort((function(t,e){if(t[0]!==e[0])return t[0]-e[0];var r=h[t[1]],n=h[e[1]];return s(r[0],n[0])||s(r[1],n[1])})),a=n.length-1;a>=0;--a){var x=e[u=(S=n[a])[0]],b=x[0],_=x[1],w=t[b],T=t[_];if((w[0]-T[0]||w[1]-T[1])<0){var k=b;b=_,_=k}x[0]=b;var M,A=x[1]=S[1];for(i&&(M=x[2]);a>0&&n[a-1][0]===u;){var S,E=(S=n[--a])[1];i?e.push([A,E,M]):e.push([A,E]),A=E}i?e.push([A,_,M]):e.push([A,_])}return h}(t,e,h,m,r));return v(e,y,r),!!y||(h.length>0||m.length>0)}},{"./lib/rat-seg-intersect":122,"big-rat":83,"big-rat/cmp":81,"big-rat/to-float":95,"box-intersect":101,nextafter:496,"rat-vec":530,"robust-segment-intersect":551,"union-find":596}],122:[function(t,e,r){"use strict";e.exports=function(t,e,r,n){var a=s(e,t),f=s(n,r),h=u(a,f);if(0===o(h))return null;var p=s(t,r),d=u(f,p),g=i(d,h),m=c(a,g);return l(t,m)};var n=t("big-rat/mul"),i=t("big-rat/div"),a=t("big-rat/sub"),o=t("big-rat/sign"),s=t("rat-vec/sub"),l=t("rat-vec/add"),c=t("rat-vec/muls");function u(t,e){return a(n(t[0],e[1]),n(t[1],e[0]))}},{"big-rat/div":82,"big-rat/mul":92,"big-rat/sign":93,"big-rat/sub":94,"rat-vec/add":529,"rat-vec/muls":531,"rat-vec/sub":532}],123:[function(t,e,r){"use strict";var n=t("clamp");function i(t,e){null==e&&(e=!0);var r=t[0],i=t[1],a=t[2],o=t[3];return null==o&&(o=e?1:255),e&&(r*=255,i*=255,a*=255,o*=255),16777216*(r=255&n(r,0,255))+((i=255&n(i,0,255))<<16)+((a=255&n(a,0,255))<<8)+(o=255&n(o,0,255))}e.exports=i,e.exports.to=i,e.exports.from=function(t,e){var r=(t=+t)>>>24,n=(16711680&t)>>>16,i=(65280&t)>>>8,a=255&t;return!1===e?[r,n,i,a]:[r/255,n/255,i/255,a/255]}},{clamp:120}],124:[function(t,e,r){"use strict";e.exports={aliceblue:[240,248,255],antiquewhite:[250,235,215],aqua:[0,255,255],aquamarine:[127,255,212],azure:[240,255,255],beige:[245,245,220],bisque:[255,228,196],black:[0,0,0],blanchedalmond:[255,235,205],blue:[0,0,255],blueviolet:[138,43,226],brown:[165,42,42],burlywood:[222,184,135],cadetblue:[95,158,160],chartreuse:[127,255,0],chocolate:[210,105,30],coral:[255,127,80],cornflowerblue:[100,149,237],cornsilk:[255,248,220],crimson:[220,20,60],cyan:[0,255,255],darkblue:[0,0,139],darkcyan:[0,139,139],darkgoldenrod:[184,134,11],darkgray:[169,169,169],darkgreen:[0,100,0],darkgrey:[169,169,169],darkkhaki:[189,183,107],darkmagenta:[139,0,139],darkolivegreen:[85,107,47],darkorange:[255,140,0],darkorchid:[153,50,204],darkred:[139,0,0],darksalmon:[233,150,122],darkseagreen:[143,188,143],darkslateblue:[72,61,139],darkslategray:[47,79,79],darkslategrey:[47,79,79],darkturquoise:[0,206,209],darkviolet:[148,0,211],deeppink:[255,20,147],deepskyblue:[0,191,255],dimgray:[105,105,105],dimgrey:[105,105,105],dodgerblue:[30,144,255],firebrick:[178,34,34],floralwhite:[255,250,240],forestgreen:[34,139,34],fuchsia:[255,0,255],gainsboro:[220,220,220],ghostwhite:[248,248,255],gold:[255,215,0],goldenrod:[218,165,32],gray:[128,128,128],green:[0,128,0],greenyellow:[173,255,47],grey:[128,128,128],honeydew:[240,255,240],hotpink:[255,105,180],indianred:[205,92,92],indigo:[75,0,130],ivory:[255,255,240],khaki:[240,230,140],lavender:[230,230,250],lavenderblush:[255,240,245],lawngreen:[124,252,0],lemonchiffon:[255,250,205],lightblue:[173,216,230],lightcoral:[240,128,128],lightcyan:[224,255,255],lightgoldenrodyellow:[250,250,210],lightgray:[211,211,211],lightgreen:[144,238,144],lightgrey:[211,211,211],lightpink:[255,182,193],lightsalmon:[255,160,122],lightseagreen:[32,178,170],lightskyblue:[135,206,250],lightslategray:[119,136,153],lightslategrey:[119,136,153],lightsteelblue:[176,196,222],lightyellow:[255,255,224],lime:[0,255,0],limegreen:[50,205,50],linen:[250,240,230],magenta:[255,0,255],maroon:[128,0,0],mediumaquamarine:[102,205,170],mediumblue:[0,0,205],mediumorchid:[186,85,211],mediumpurple:[147,112,219],mediumseagreen:[60,179,113],mediumslateblue:[123,104,238],mediumspringgreen:[0,250,154],mediumturquoise:[72,209,204],mediumvioletred:[199,21,133],midnightblue:[25,25,112],mintcream:[245,255,250],mistyrose:[255,228,225],moccasin:[255,228,181],navajowhite:[255,222,173],navy:[0,0,128],oldlace:[253,245,230],olive:[128,128,0],olivedrab:[107,142,35],orange:[255,165,0],orangered:[255,69,0],orchid:[218,112,214],palegoldenrod:[238,232,170],palegreen:[152,251,152],paleturquoise:[175,238,238],palevioletred:[219,112,147],papayawhip:[255,239,213],peachpuff:[255,218,185],peru:[205,133,63],pink:[255,192,203],plum:[221,160,221],powderblue:[176,224,230],purple:[128,0,128],rebeccapurple:[102,51,153],red:[255,0,0],rosybrown:[188,143,143],royalblue:[65,105,225],saddlebrown:[139,69,19],salmon:[250,128,114],sandybrown:[244,164,96],seagreen:[46,139,87],seashell:[255,245,238],sienna:[160,82,45],silver:[192,192,192],skyblue:[135,206,235],slateblue:[106,90,205],slategray:[112,128,144],slategrey:[112,128,144],snow:[255,250,250],springgreen:[0,255,127],steelblue:[70,130,180],tan:[210,180,140],teal:[0,128,128],thistle:[216,191,216],tomato:[255,99,71],turquoise:[64,224,208],violet:[238,130,238],wheat:[245,222,179],white:[255,255,255],whitesmoke:[245,245,245],yellow:[255,255,0],yellowgreen:[154,205,50]}},{}],125:[function(t,e,r){"use strict";var n=t("color-rgba"),i=t("clamp"),a=t("dtype");e.exports=function(t,e){"float"!==e&&e||(e="array"),"uint"===e&&(e="uint8"),"uint_clamped"===e&&(e="uint8_clamped");var r=new(a(e))(4),o="uint8"!==e&&"uint8_clamped"!==e;return t.length&&"string"!=typeof t||((t=n(t))[0]/=255,t[1]/=255,t[2]/=255),function(t){return t instanceof Uint8Array||t instanceof Uint8ClampedArray||!!(Array.isArray(t)&&(t[0]>1||0===t[0])&&(t[1]>1||0===t[1])&&(t[2]>1||0===t[2])&&(!t[3]||t[3]>1))}(t)?(r[0]=t[0],r[1]=t[1],r[2]=t[2],r[3]=null!=t[3]?t[3]:255,o&&(r[0]/=255,r[1]/=255,r[2]/=255,r[3]/=255),r):(o?(r[0]=t[0],r[1]=t[1],r[2]=t[2],r[3]=null!=t[3]?t[3]:1):(r[0]=i(Math.floor(255*t[0]),0,255),r[1]=i(Math.floor(255*t[1]),0,255),r[2]=i(Math.floor(255*t[2]),0,255),r[3]=null==t[3]?255:i(Math.floor(255*t[3]),0,255)),r)}},{clamp:120,"color-rgba":127,dtype:175}],126:[function(t,e,r){(function(r){(function(){"use strict";var n=t("color-name"),i=t("is-plain-obj"),a=t("defined");e.exports=function(t){var e,s,l=[],c=1;if("string"==typeof t)if(n[t])l=n[t].slice(),s="rgb";else if("transparent"===t)c=0,s="rgb",l=[0,0,0];else if(/^#[A-Fa-f0-9]+$/.test(t)){var u=(p=t.slice(1)).length;c=1,u<=4?(l=[parseInt(p[0]+p[0],16),parseInt(p[1]+p[1],16),parseInt(p[2]+p[2],16)],4===u&&(c=parseInt(p[3]+p[3],16)/255)):(l=[parseInt(p[0]+p[1],16),parseInt(p[2]+p[3],16),parseInt(p[4]+p[5],16)],8===u&&(c=parseInt(p[6]+p[7],16)/255)),l[0]||(l[0]=0),l[1]||(l[1]=0),l[2]||(l[2]=0),s="rgb"}else if(e=/^((?:rgb|hs[lvb]|hwb|cmyk?|xy[zy]|gray|lab|lchu?v?|[ly]uv|lms)a?)\s*\(([^\)]*)\)/.exec(t)){var f=e[1],h="rgb"===f,p=f.replace(/a$/,"");s=p;u="cmyk"===p?4:"gray"===p?1:3;l=e[2].trim().split(/\s*,\s*/).map((function(t,e){if(/%$/.test(t))return e===u?parseFloat(t)/100:"rgb"===p?255*parseFloat(t)/100:parseFloat(t);if("h"===p[e]){if(/deg$/.test(t))return parseFloat(t);if(void 0!==o[t])return o[t]}return parseFloat(t)})),f===p&&l.push(1),c=h||void 0===l[u]?1:l[u],l=l.slice(0,u)}else t.length>10&&/[0-9](?:\s|\/)/.test(t)&&(l=t.match(/([0-9]+)/g).map((function(t){return parseFloat(t)})),s=t.match(/([a-z])/gi).join("").toLowerCase());else if(isNaN(t))if(i(t)){var d=a(t.r,t.red,t.R,null);null!==d?(s="rgb",l=[d,a(t.g,t.green,t.G),a(t.b,t.blue,t.B)]):(s="hsl",l=[a(t.h,t.hue,t.H),a(t.s,t.saturation,t.S),a(t.l,t.lightness,t.L,t.b,t.brightness)]),c=a(t.a,t.alpha,t.opacity,1),null!=t.opacity&&(c/=100)}else(Array.isArray(t)||r.ArrayBuffer&&ArrayBuffer.isView&&ArrayBuffer.isView(t))&&(l=[t[0],t[1],t[2]],s="rgb",c=4===t.length?t[3]:1);else s="rgb",l=[t>>>16,(65280&t)>>>8,255&t];return{space:s,values:l,alpha:c}};var o={red:0,orange:60,yellow:120,green:180,blue:240,purple:300}}).call(this)}).call(this,"undefined"!=typeof global?global:"undefined"!=typeof self?self:"undefined"!=typeof window?window:{})},{"color-name":124,defined:170,"is-plain-obj":469}],127:[function(t,e,r){"use strict";var n=t("color-parse"),i=t("color-space/hsl"),a=t("clamp");e.exports=function(t){var e,r=n(t);return r.space?((e=Array(3))[0]=a(r.values[0],0,255),e[1]=a(r.values[1],0,255),e[2]=a(r.values[2],0,255),"h"===r.space[0]&&(e=i.rgb(e)),e.push(a(r.alpha,0,1)),e):[]}},{clamp:120,"color-parse":126,"color-space/hsl":128}],128:[function(t,e,r){"use strict";var n=t("./rgb");e.exports={name:"hsl",min:[0,0,0],max:[360,100,100],channel:["hue","saturation","lightness"],alias:["HSL"],rgb:function(t){var e,r,n,i,a,o=t[0]/360,s=t[1]/100,l=t[2]/100;if(0===s)return[a=255*l,a,a];e=2*l-(r=l<.5?l*(1+s):l+s-l*s),i=[0,0,0];for(var c=0;c<3;c++)(n=o+1/3*-(c-1))<0?n++:n>1&&n--,a=6*n<1?e+6*(r-e)*n:2*n<1?r:3*n<2?e+(r-e)*(2/3-n)*6:e,i[c]=255*a;return i}},n.hsl=function(t){var e,r,n=t[0]/255,i=t[1]/255,a=t[2]/255,o=Math.min(n,i,a),s=Math.max(n,i,a),l=s-o;return s===o?e=0:n===s?e=(i-a)/l:i===s?e=2+(a-n)/l:a===s&&(e=4+(n-i)/l),(e=Math.min(60*e,360))<0&&(e+=360),r=(o+s)/2,[e,100*(s===o?0:r<=.5?l/(s+o):l/(2-s-o)),100*r]}},{"./rgb":129}],129:[function(t,e,r){"use strict";e.exports={name:"rgb",min:[0,0,0],max:[255,255,255],channel:["red","green","blue"],alias:["RGB"]}},{}],130:[function(t,e,r){e.exports={jet:[{index:0,rgb:[0,0,131]},{index:.125,rgb:[0,60,170]},{index:.375,rgb:[5,255,255]},{index:.625,rgb:[255,255,0]},{index:.875,rgb:[250,0,0]},{index:1,rgb:[128,0,0]}],hsv:[{index:0,rgb:[255,0,0]},{index:.169,rgb:[253,255,2]},{index:.173,rgb:[247,255,2]},{index:.337,rgb:[0,252,4]},{index:.341,rgb:[0,252,10]},{index:.506,rgb:[1,249,255]},{index:.671,rgb:[2,0,253]},{index:.675,rgb:[8,0,253]},{index:.839,rgb:[255,0,251]},{index:.843,rgb:[255,0,245]},{index:1,rgb:[255,0,6]}],hot:[{index:0,rgb:[0,0,0]},{index:.3,rgb:[230,0,0]},{index:.6,rgb:[255,210,0]},{index:1,rgb:[255,255,255]}],cool:[{index:0,rgb:[0,255,255]},{index:1,rgb:[255,0,255]}],spring:[{index:0,rgb:[255,0,255]},{index:1,rgb:[255,255,0]}],summer:[{index:0,rgb:[0,128,102]},{index:1,rgb:[255,255,102]}],autumn:[{index:0,rgb:[255,0,0]},{index:1,rgb:[255,255,0]}],winter:[{index:0,rgb:[0,0,255]},{index:1,rgb:[0,255,128]}],bone:[{index:0,rgb:[0,0,0]},{index:.376,rgb:[84,84,116]},{index:.753,rgb:[169,200,200]},{index:1,rgb:[255,255,255]}],copper:[{index:0,rgb:[0,0,0]},{index:.804,rgb:[255,160,102]},{index:1,rgb:[255,199,127]}],greys:[{index:0,rgb:[0,0,0]},{index:1,rgb:[255,255,255]}],yignbu:[{index:0,rgb:[8,29,88]},{index:.125,rgb:[37,52,148]},{index:.25,rgb:[34,94,168]},{index:.375,rgb:[29,145,192]},{index:.5,rgb:[65,182,196]},{index:.625,rgb:[127,205,187]},{index:.75,rgb:[199,233,180]},{index:.875,rgb:[237,248,217]},{index:1,rgb:[255,255,217]}],greens:[{index:0,rgb:[0,68,27]},{index:.125,rgb:[0,109,44]},{index:.25,rgb:[35,139,69]},{index:.375,rgb:[65,171,93]},{index:.5,rgb:[116,196,118]},{index:.625,rgb:[161,217,155]},{index:.75,rgb:[199,233,192]},{index:.875,rgb:[229,245,224]},{index:1,rgb:[247,252,245]}],yiorrd:[{index:0,rgb:[128,0,38]},{index:.125,rgb:[189,0,38]},{index:.25,rgb:[227,26,28]},{index:.375,rgb:[252,78,42]},{index:.5,rgb:[253,141,60]},{index:.625,rgb:[254,178,76]},{index:.75,rgb:[254,217,118]},{index:.875,rgb:[255,237,160]},{index:1,rgb:[255,255,204]}],bluered:[{index:0,rgb:[0,0,255]},{index:1,rgb:[255,0,0]}],rdbu:[{index:0,rgb:[5,10,172]},{index:.35,rgb:[106,137,247]},{index:.5,rgb:[190,190,190]},{index:.6,rgb:[220,170,132]},{index:.7,rgb:[230,145,90]},{index:1,rgb:[178,10,28]}],picnic:[{index:0,rgb:[0,0,255]},{index:.1,rgb:[51,153,255]},{index:.2,rgb:[102,204,255]},{index:.3,rgb:[153,204,255]},{index:.4,rgb:[204,204,255]},{index:.5,rgb:[255,255,255]},{index:.6,rgb:[255,204,255]},{index:.7,rgb:[255,153,255]},{index:.8,rgb:[255,102,204]},{index:.9,rgb:[255,102,102]},{index:1,rgb:[255,0,0]}],rainbow:[{index:0,rgb:[150,0,90]},{index:.125,rgb:[0,0,200]},{index:.25,rgb:[0,25,255]},{index:.375,rgb:[0,152,255]},{index:.5,rgb:[44,255,150]},{index:.625,rgb:[151,255,0]},{index:.75,rgb:[255,234,0]},{index:.875,rgb:[255,111,0]},{index:1,rgb:[255,0,0]}],portland:[{index:0,rgb:[12,51,131]},{index:.25,rgb:[10,136,186]},{index:.5,rgb:[242,211,56]},{index:.75,rgb:[242,143,56]},{index:1,rgb:[217,30,30]}],blackbody:[{index:0,rgb:[0,0,0]},{index:.2,rgb:[230,0,0]},{index:.4,rgb:[230,210,0]},{index:.7,rgb:[255,255,255]},{index:1,rgb:[160,200,255]}],earth:[{index:0,rgb:[0,0,130]},{index:.1,rgb:[0,180,180]},{index:.2,rgb:[40,210,40]},{index:.4,rgb:[230,230,50]},{index:.6,rgb:[120,70,20]},{index:1,rgb:[255,255,255]}],electric:[{index:0,rgb:[0,0,0]},{index:.15,rgb:[30,0,100]},{index:.4,rgb:[120,0,100]},{index:.6,rgb:[160,90,0]},{index:.8,rgb:[230,200,0]},{index:1,rgb:[255,250,220]}],alpha:[{index:0,rgb:[255,255,255,0]},{index:1,rgb:[255,255,255,1]}],viridis:[{index:0,rgb:[68,1,84]},{index:.13,rgb:[71,44,122]},{index:.25,rgb:[59,81,139]},{index:.38,rgb:[44,113,142]},{index:.5,rgb:[33,144,141]},{index:.63,rgb:[39,173,129]},{index:.75,rgb:[92,200,99]},{index:.88,rgb:[170,220,50]},{index:1,rgb:[253,231,37]}],inferno:[{index:0,rgb:[0,0,4]},{index:.13,rgb:[31,12,72]},{index:.25,rgb:[85,15,109]},{index:.38,rgb:[136,34,106]},{index:.5,rgb:[186,54,85]},{index:.63,rgb:[227,89,51]},{index:.75,rgb:[249,140,10]},{index:.88,rgb:[249,201,50]},{index:1,rgb:[252,255,164]}],magma:[{index:0,rgb:[0,0,4]},{index:.13,rgb:[28,16,68]},{index:.25,rgb:[79,18,123]},{index:.38,rgb:[129,37,129]},{index:.5,rgb:[181,54,122]},{index:.63,rgb:[229,80,100]},{index:.75,rgb:[251,135,97]},{index:.88,rgb:[254,194,135]},{index:1,rgb:[252,253,191]}],plasma:[{index:0,rgb:[13,8,135]},{index:.13,rgb:[75,3,161]},{index:.25,rgb:[125,3,168]},{index:.38,rgb:[168,34,150]},{index:.5,rgb:[203,70,121]},{index:.63,rgb:[229,107,93]},{index:.75,rgb:[248,148,65]},{index:.88,rgb:[253,195,40]},{index:1,rgb:[240,249,33]}],warm:[{index:0,rgb:[125,0,179]},{index:.13,rgb:[172,0,187]},{index:.25,rgb:[219,0,170]},{index:.38,rgb:[255,0,130]},{index:.5,rgb:[255,63,74]},{index:.63,rgb:[255,123,0]},{index:.75,rgb:[234,176,0]},{index:.88,rgb:[190,228,0]},{index:1,rgb:[147,255,0]}],cool:[{index:0,rgb:[125,0,179]},{index:.13,rgb:[116,0,218]},{index:.25,rgb:[98,74,237]},{index:.38,rgb:[68,146,231]},{index:.5,rgb:[0,204,197]},{index:.63,rgb:[0,247,146]},{index:.75,rgb:[0,255,88]},{index:.88,rgb:[40,255,8]},{index:1,rgb:[147,255,0]}],"rainbow-soft":[{index:0,rgb:[125,0,179]},{index:.1,rgb:[199,0,180]},{index:.2,rgb:[255,0,121]},{index:.3,rgb:[255,108,0]},{index:.4,rgb:[222,194,0]},{index:.5,rgb:[150,255,0]},{index:.6,rgb:[0,255,55]},{index:.7,rgb:[0,246,150]},{index:.8,rgb:[50,167,222]},{index:.9,rgb:[103,51,235]},{index:1,rgb:[124,0,186]}],bathymetry:[{index:0,rgb:[40,26,44]},{index:.13,rgb:[59,49,90]},{index:.25,rgb:[64,76,139]},{index:.38,rgb:[63,110,151]},{index:.5,rgb:[72,142,158]},{index:.63,rgb:[85,174,163]},{index:.75,rgb:[120,206,163]},{index:.88,rgb:[187,230,172]},{index:1,rgb:[253,254,204]}],cdom:[{index:0,rgb:[47,15,62]},{index:.13,rgb:[87,23,86]},{index:.25,rgb:[130,28,99]},{index:.38,rgb:[171,41,96]},{index:.5,rgb:[206,67,86]},{index:.63,rgb:[230,106,84]},{index:.75,rgb:[242,149,103]},{index:.88,rgb:[249,193,135]},{index:1,rgb:[254,237,176]}],chlorophyll:[{index:0,rgb:[18,36,20]},{index:.13,rgb:[25,63,41]},{index:.25,rgb:[24,91,59]},{index:.38,rgb:[13,119,72]},{index:.5,rgb:[18,148,80]},{index:.63,rgb:[80,173,89]},{index:.75,rgb:[132,196,122]},{index:.88,rgb:[175,221,162]},{index:1,rgb:[215,249,208]}],density:[{index:0,rgb:[54,14,36]},{index:.13,rgb:[89,23,80]},{index:.25,rgb:[110,45,132]},{index:.38,rgb:[120,77,178]},{index:.5,rgb:[120,113,213]},{index:.63,rgb:[115,151,228]},{index:.75,rgb:[134,185,227]},{index:.88,rgb:[177,214,227]},{index:1,rgb:[230,241,241]}],"freesurface-blue":[{index:0,rgb:[30,4,110]},{index:.13,rgb:[47,14,176]},{index:.25,rgb:[41,45,236]},{index:.38,rgb:[25,99,212]},{index:.5,rgb:[68,131,200]},{index:.63,rgb:[114,156,197]},{index:.75,rgb:[157,181,203]},{index:.88,rgb:[200,208,216]},{index:1,rgb:[241,237,236]}],"freesurface-red":[{index:0,rgb:[60,9,18]},{index:.13,rgb:[100,17,27]},{index:.25,rgb:[142,20,29]},{index:.38,rgb:[177,43,27]},{index:.5,rgb:[192,87,63]},{index:.63,rgb:[205,125,105]},{index:.75,rgb:[216,162,148]},{index:.88,rgb:[227,199,193]},{index:1,rgb:[241,237,236]}],oxygen:[{index:0,rgb:[64,5,5]},{index:.13,rgb:[106,6,15]},{index:.25,rgb:[144,26,7]},{index:.38,rgb:[168,64,3]},{index:.5,rgb:[188,100,4]},{index:.63,rgb:[206,136,11]},{index:.75,rgb:[220,174,25]},{index:.88,rgb:[231,215,44]},{index:1,rgb:[248,254,105]}],par:[{index:0,rgb:[51,20,24]},{index:.13,rgb:[90,32,35]},{index:.25,rgb:[129,44,34]},{index:.38,rgb:[159,68,25]},{index:.5,rgb:[182,99,19]},{index:.63,rgb:[199,134,22]},{index:.75,rgb:[212,171,35]},{index:.88,rgb:[221,210,54]},{index:1,rgb:[225,253,75]}],phase:[{index:0,rgb:[145,105,18]},{index:.13,rgb:[184,71,38]},{index:.25,rgb:[186,58,115]},{index:.38,rgb:[160,71,185]},{index:.5,rgb:[110,97,218]},{index:.63,rgb:[50,123,164]},{index:.75,rgb:[31,131,110]},{index:.88,rgb:[77,129,34]},{index:1,rgb:[145,105,18]}],salinity:[{index:0,rgb:[42,24,108]},{index:.13,rgb:[33,50,162]},{index:.25,rgb:[15,90,145]},{index:.38,rgb:[40,118,137]},{index:.5,rgb:[59,146,135]},{index:.63,rgb:[79,175,126]},{index:.75,rgb:[120,203,104]},{index:.88,rgb:[193,221,100]},{index:1,rgb:[253,239,154]}],temperature:[{index:0,rgb:[4,35,51]},{index:.13,rgb:[23,51,122]},{index:.25,rgb:[85,59,157]},{index:.38,rgb:[129,79,143]},{index:.5,rgb:[175,95,130]},{index:.63,rgb:[222,112,101]},{index:.75,rgb:[249,146,66]},{index:.88,rgb:[249,196,65]},{index:1,rgb:[232,250,91]}],turbidity:[{index:0,rgb:[34,31,27]},{index:.13,rgb:[65,50,41]},{index:.25,rgb:[98,69,52]},{index:.38,rgb:[131,89,57]},{index:.5,rgb:[161,112,59]},{index:.63,rgb:[185,140,66]},{index:.75,rgb:[202,174,88]},{index:.88,rgb:[216,209,126]},{index:1,rgb:[233,246,171]}],"velocity-blue":[{index:0,rgb:[17,32,64]},{index:.13,rgb:[35,52,116]},{index:.25,rgb:[29,81,156]},{index:.38,rgb:[31,113,162]},{index:.5,rgb:[50,144,169]},{index:.63,rgb:[87,173,176]},{index:.75,rgb:[149,196,189]},{index:.88,rgb:[203,221,211]},{index:1,rgb:[254,251,230]}],"velocity-green":[{index:0,rgb:[23,35,19]},{index:.13,rgb:[24,64,38]},{index:.25,rgb:[11,95,45]},{index:.38,rgb:[39,123,35]},{index:.5,rgb:[95,146,12]},{index:.63,rgb:[152,165,18]},{index:.75,rgb:[201,186,69]},{index:.88,rgb:[233,216,137]},{index:1,rgb:[255,253,205]}],cubehelix:[{index:0,rgb:[0,0,0]},{index:.07,rgb:[22,5,59]},{index:.13,rgb:[60,4,105]},{index:.2,rgb:[109,1,135]},{index:.27,rgb:[161,0,147]},{index:.33,rgb:[210,2,142]},{index:.4,rgb:[251,11,123]},{index:.47,rgb:[255,29,97]},{index:.53,rgb:[255,54,69]},{index:.6,rgb:[255,85,46]},{index:.67,rgb:[255,120,34]},{index:.73,rgb:[255,157,37]},{index:.8,rgb:[241,191,57]},{index:.87,rgb:[224,220,93]},{index:.93,rgb:[218,241,142]},{index:1,rgb:[227,253,198]}]}},{}],131:[function(t,e,r){"use strict";var n=t("./colorScale"),i=t("lerp");function a(t){return[t[0]/255,t[1]/255,t[2]/255,t[3]]}function o(t){for(var e,r="#",n=0;n<3;++n)r+=("00"+(e=(e=t[n]).toString(16))).substr(e.length);return r}function s(t){return"rgba("+t.join(",")+")"}e.exports=function(t){var e,r,l,c,u,f,h,p,d,g;t||(t={});p=(t.nshades||72)-1,h=t.format||"hex",(f=t.colormap)||(f="jet");if("string"==typeof f){if(f=f.toLowerCase(),!n[f])throw Error(f+" not a supported colorscale");u=n[f]}else{if(!Array.isArray(f))throw Error("unsupported colormap option",f);u=f.slice()}if(u.length>p+1)throw new Error(f+" map requires nshades to be at least size "+u.length);d=Array.isArray(t.alpha)?2!==t.alpha.length?[1,1]:t.alpha.slice():"number"==typeof t.alpha?[t.alpha,t.alpha]:[1,1];e=u.map((function(t){return Math.round(t.index*p)})),d[0]=Math.min(Math.max(d[0],0),1),d[1]=Math.min(Math.max(d[1],0),1);var m=u.map((function(t,e){var r=u[e].index,n=u[e].rgb.slice();return 4===n.length&&n[3]>=0&&n[3]<=1||(n[3]=d[0]+(d[1]-d[0])*r),n})),v=[];for(g=0;g<e.length-1;++g){c=e[g+1]-e[g],r=m[g],l=m[g+1];for(var y=0;y<c;y++){var x=y/c;v.push([Math.round(i(r[0],l[0],x)),Math.round(i(r[1],l[1],x)),Math.round(i(r[2],l[2],x)),i(r[3],l[3],x)])}}v.push(u[u.length-1].rgb.concat(d[1])),"hex"===h?v=v.map(o):"rgbaString"===h?v=v.map(s):"float"===h&&(v=v.map(a));return v}},{"./colorScale":130,lerp:472}],132:[function(t,e,r){"use strict";e.exports=function(t,e,r,a){var o=n(e,r,a);if(0===o){var s=i(n(t,e,r)),c=i(n(t,e,a));if(s===c){if(0===s){var u=l(t,e,r),f=l(t,e,a);return u===f?0:u?1:-1}return 0}return 0===c?s>0||l(t,e,a)?-1:1:0===s?c>0||l(t,e,r)?1:-1:i(c-s)}var h=n(t,e,r);return h>0?o>0&&n(t,e,a)>0?1:-1:h<0?o>0||n(t,e,a)>0?1:-1:n(t,e,a)>0||l(t,e,r)?1:-1};var n=t("robust-orientation"),i=t("signum"),a=t("two-sum"),o=t("robust-product"),s=t("robust-sum");function l(t,e,r){var n=a(t[0],-e[0]),i=a(t[1],-e[1]),l=a(r[0],-e[0]),c=a(r[1],-e[1]),u=s(o(n,l),o(i,c));return u[u.length-1]>=0}},{"robust-orientation":548,"robust-product":549,"robust-sum":553,signum:554,"two-sum":583}],133:[function(t,e,r){e.exports=function(t,e){var r=t.length,a=t.length-e.length;if(a)return a;switch(r){case 0:return 0;case 1:return t[0]-e[0];case 2:return t[0]+t[1]-e[0]-e[1]||n(t[0],t[1])-n(e[0],e[1]);case 3:var o=t[0]+t[1],s=e[0]+e[1];if(a=o+t[2]-(s+e[2]))return a;var l=n(t[0],t[1]),c=n(e[0],e[1]);return n(l,t[2])-n(c,e[2])||n(l+t[2],o)-n(c+e[2],s);case 4:var u=t[0],f=t[1],h=t[2],p=t[3],d=e[0],g=e[1],m=e[2],v=e[3];return u+f+h+p-(d+g+m+v)||n(u,f,h,p)-n(d,g,m,v,d)||n(u+f,u+h,u+p,f+h,f+p,h+p)-n(d+g,d+m,d+v,g+m,g+v,m+v)||n(u+f+h,u+f+p,u+h+p,f+h+p)-n(d+g+m,d+g+v,d+m+v,g+m+v);default:for(var y=t.slice().sort(i),x=e.slice().sort(i),b=0;b<r;++b)if(a=y[b]-x[b])return a;return 0}};var n=Math.min;function i(t,e){return t-e}},{}],134:[function(t,e,r){"use strict";var n=t("compare-cell"),i=t("cell-orientation");e.exports=function(t,e){return n(t,e)||i(t)-i(e)}},{"cell-orientation":117,"compare-cell":133}],135:[function(t,e,r){"use strict";var n=t("./lib/ch1d"),i=t("./lib/ch2d"),a=t("./lib/chnd");e.exports=function(t){var e=t.length;if(0===e)return[];if(1===e)return[[0]];var r=t[0].length;if(0===r)return[];if(1===r)return n(t);if(2===r)return i(t);return a(t,r)}},{"./lib/ch1d":136,"./lib/ch2d":137,"./lib/chnd":138}],136:[function(t,e,r){"use strict";e.exports=function(t){for(var e=0,r=0,n=1;n<t.length;++n)t[n][0]<t[e][0]&&(e=n),t[n][0]>t[r][0]&&(r=n);return e<r?[[e],[r]]:e>r?[[r],[e]]:[[e]]}},{}],137:[function(t,e,r){"use strict";e.exports=function(t){var e=n(t),r=e.length;if(r<=2)return[];for(var i=new Array(r),a=e[r-1],o=0;o<r;++o){var s=e[o];i[o]=[a,s],a=s}return i};var n=t("monotone-convex-hull-2d")},{"monotone-convex-hull-2d":482}],138:[function(t,e,r){"use strict";e.exports=function(t,e){try{return n(t,!0)}catch(o){var r=i(t);if(r.length<=e)return[];var a=function(t,e){for(var r=t.length,n=new Array(r),i=0;i<e.length;++i)n[i]=t[e[i]];var a=e.length;for(i=0;i<r;++i)e.indexOf(i)<0&&(n[a++]=t[i]);return n}(t,r);return function(t,e){for(var r=t.length,n=e.length,i=0;i<r;++i)for(var a=t[i],o=0;o<a.length;++o){var s=a[o];if(s<n)a[o]=e[s];else{s-=n;for(var l=0;l<n;++l)s>=e[l]&&(s+=1);a[o]=s}}return t}(n(a,!0),r)}};var n=t("incremental-convex-hull"),i=t("affine-hull")},{"affine-hull":67,"incremental-convex-hull":459}],139:[function(t,e,r){e.exports={AFG:"afghan",ALA:"\\b\\wland",ALB:"albania",DZA:"algeria",ASM:"^(?=.*americ).*samoa",AND:"andorra",AGO:"angola",AIA:"anguill?a",ATA:"antarctica",ATG:"antigua",ARG:"argentin",ARM:"armenia",ABW:"^(?!.*bonaire).*\\baruba",AUS:"australia",AUT:"^(?!.*hungary).*austria|\\baustri.*\\bemp",AZE:"azerbaijan",BHS:"bahamas",BHR:"bahrain",BGD:"bangladesh|^(?=.*east).*paki?stan",BRB:"barbados",BLR:"belarus|byelo",BEL:"^(?!.*luxem).*belgium",BLZ:"belize|^(?=.*british).*honduras",BEN:"benin|dahome",BMU:"bermuda",BTN:"bhutan",BOL:"bolivia",BES:"^(?=.*bonaire).*eustatius|^(?=.*carib).*netherlands|\\bbes.?islands",BIH:"herzegovina|bosnia",BWA:"botswana|bechuana",BVT:"bouvet",BRA:"brazil",IOT:"british.?indian.?ocean",BRN:"brunei",BGR:"bulgaria",BFA:"burkina|\\bfaso|upper.?volta",BDI:"burundi",CPV:"verde",KHM:"cambodia|kampuchea|khmer",CMR:"cameroon",CAN:"canada",CYM:"cayman",CAF:"\\bcentral.african.republic",TCD:"\\bchad",CHL:"\\bchile",CHN:"^(?!.*\\bmac)(?!.*\\bhong)(?!.*\\btai)(?!.*\\brep).*china|^(?=.*peo)(?=.*rep).*china",CXR:"christmas",CCK:"\\bcocos|keeling",COL:"colombia",COM:"comoro",COG:"^(?!.*\\bdem)(?!.*\\bd[\\.]?r)(?!.*kinshasa)(?!.*zaire)(?!.*belg)(?!.*l.opoldville)(?!.*free).*\\bcongo",COK:"\\bcook",CRI:"costa.?rica",CIV:"ivoire|ivory",HRV:"croatia",CUB:"\\bcuba",CUW:"^(?!.*bonaire).*\\bcura(c|\xe7)ao",CYP:"cyprus",CSK:"czechoslovakia",CZE:"^(?=.*rep).*czech|czechia|bohemia",COD:"\\bdem.*congo|congo.*\\bdem|congo.*\\bd[\\.]?r|\\bd[\\.]?r.*congo|belgian.?congo|congo.?free.?state|kinshasa|zaire|l.opoldville|drc|droc|rdc",DNK:"denmark",DJI:"djibouti",DMA:"dominica(?!n)",DOM:"dominican.rep",ECU:"ecuador",EGY:"egypt",SLV:"el.?salvador",GNQ:"guine.*eq|eq.*guine|^(?=.*span).*guinea",ERI:"eritrea",EST:"estonia",ETH:"ethiopia|abyssinia",FLK:"falkland|malvinas",FRO:"faroe|faeroe",FJI:"fiji",FIN:"finland",FRA:"^(?!.*\\bdep)(?!.*martinique).*france|french.?republic|\\bgaul",GUF:"^(?=.*french).*guiana",PYF:"french.?polynesia|tahiti",ATF:"french.?southern",GAB:"gabon",GMB:"gambia",GEO:"^(?!.*south).*georgia",DDR:"german.?democratic.?republic|democratic.?republic.*germany|east.germany",DEU:"^(?!.*east).*germany|^(?=.*\\bfed.*\\brep).*german",GHA:"ghana|gold.?coast",GIB:"gibraltar",GRC:"greece|hellenic|hellas",GRL:"greenland",GRD:"grenada",GLP:"guadeloupe",GUM:"\\bguam",GTM:"guatemala",GGY:"guernsey",GIN:"^(?!.*eq)(?!.*span)(?!.*bissau)(?!.*portu)(?!.*new).*guinea",GNB:"bissau|^(?=.*portu).*guinea",GUY:"guyana|british.?guiana",HTI:"haiti",HMD:"heard.*mcdonald",VAT:"holy.?see|vatican|papal.?st",HND:"^(?!.*brit).*honduras",HKG:"hong.?kong",HUN:"^(?!.*austr).*hungary",ISL:"iceland",IND:"india(?!.*ocea)",IDN:"indonesia",IRN:"\\biran|persia",IRQ:"\\biraq|mesopotamia",IRL:"(^ireland)|(^republic.*ireland)",IMN:"^(?=.*isle).*\\bman",ISR:"israel",ITA:"italy",JAM:"jamaica",JPN:"japan",JEY:"jersey",JOR:"jordan",KAZ:"kazak",KEN:"kenya|british.?east.?africa|east.?africa.?prot",KIR:"kiribati",PRK:"^(?=.*democrat|people|north|d.*p.*.r).*\\bkorea|dprk|korea.*(d.*p.*r)",KWT:"kuwait",KGZ:"kyrgyz|kirghiz",LAO:"\\blaos?\\b",LVA:"latvia",LBN:"lebanon",LSO:"lesotho|basuto",LBR:"liberia",LBY:"libya",LIE:"liechtenstein",LTU:"lithuania",LUX:"^(?!.*belg).*luxem",MAC:"maca(o|u)",MDG:"madagascar|malagasy",MWI:"malawi|nyasa",MYS:"malaysia",MDV:"maldive",MLI:"\\bmali\\b",MLT:"\\bmalta",MHL:"marshall",MTQ:"martinique",MRT:"mauritania",MUS:"mauritius",MYT:"\\bmayotte",MEX:"\\bmexic",FSM:"fed.*micronesia|micronesia.*fed",MCO:"monaco",MNG:"mongolia",MNE:"^(?!.*serbia).*montenegro",MSR:"montserrat",MAR:"morocco|\\bmaroc",MOZ:"mozambique",MMR:"myanmar|burma",NAM:"namibia",NRU:"nauru",NPL:"nepal",NLD:"^(?!.*\\bant)(?!.*\\bcarib).*netherlands",ANT:"^(?=.*\\bant).*(nether|dutch)",NCL:"new.?caledonia",NZL:"new.?zealand",NIC:"nicaragua",NER:"\\bniger(?!ia)",NGA:"nigeria",NIU:"niue",NFK:"norfolk",MNP:"mariana",NOR:"norway",OMN:"\\boman|trucial",PAK:"^(?!.*east).*paki?stan",PLW:"palau",PSE:"palestin|\\bgaza|west.?bank",PAN:"panama",PNG:"papua|new.?guinea",PRY:"paraguay",PER:"peru",PHL:"philippines",PCN:"pitcairn",POL:"poland",PRT:"portugal",PRI:"puerto.?rico",QAT:"qatar",KOR:"^(?!.*d.*p.*r)(?!.*democrat)(?!.*people)(?!.*north).*\\bkorea(?!.*d.*p.*r)",MDA:"moldov|b(a|e)ssarabia",REU:"r(e|\xe9)union",ROU:"r(o|u|ou)mania",RUS:"\\brussia|soviet.?union|u\\.?s\\.?s\\.?r|socialist.?republics",RWA:"rwanda",BLM:"barth(e|\xe9)lemy",SHN:"helena",KNA:"kitts|\\bnevis",LCA:"\\blucia",MAF:"^(?=.*collectivity).*martin|^(?=.*france).*martin(?!ique)|^(?=.*french).*martin(?!ique)",SPM:"miquelon",VCT:"vincent",WSM:"^(?!.*amer).*samoa",SMR:"san.?marino",STP:"\\bs(a|\xe3)o.?tom(e|\xe9)",SAU:"\\bsa\\w*.?arabia",SEN:"senegal",SRB:"^(?!.*monte).*serbia",SYC:"seychell",SLE:"sierra",SGP:"singapore",SXM:"^(?!.*martin)(?!.*saba).*maarten",SVK:"^(?!.*cze).*slovak",SVN:"slovenia",SLB:"solomon",SOM:"somali",ZAF:"south.africa|s\\\\..?africa",SGS:"south.?georgia|sandwich",SSD:"\\bs\\w*.?sudan",ESP:"spain",LKA:"sri.?lanka|ceylon",SDN:"^(?!.*\\bs(?!u)).*sudan",SUR:"surinam|dutch.?guiana",SJM:"svalbard",SWZ:"swaziland",SWE:"sweden",CHE:"switz|swiss",SYR:"syria",TWN:"taiwan|taipei|formosa|^(?!.*peo)(?=.*rep).*china",TJK:"tajik",THA:"thailand|\\bsiam",MKD:"macedonia|fyrom",TLS:"^(?=.*leste).*timor|^(?=.*east).*timor",TGO:"togo",TKL:"tokelau",TON:"tonga",TTO:"trinidad|tobago",TUN:"tunisia",TUR:"turkey",TKM:"turkmen",TCA:"turks",TUV:"tuvalu",UGA:"uganda",UKR:"ukrain",ARE:"emirates|^u\\.?a\\.?e\\.?$|united.?arab.?em",GBR:"united.?kingdom|britain|^u\\.?k\\.?$",TZA:"tanzania",USA:"united.?states\\b(?!.*islands)|\\bu\\.?s\\.?a\\.?\\b|^\\s*u\\.?s\\.?\\b(?!.*islands)",UMI:"minor.?outlying.?is",URY:"uruguay",UZB:"uzbek",VUT:"vanuatu|new.?hebrides",VEN:"venezuela",VNM:"^(?!.*republic).*viet.?nam|^(?=.*socialist).*viet.?nam",VGB:"^(?=.*\\bu\\.?\\s?k).*virgin|^(?=.*brit).*virgin|^(?=.*kingdom).*virgin",VIR:"^(?=.*\\bu\\.?\\s?s).*virgin|^(?=.*states).*virgin",WLF:"futuna|wallis",ESH:"western.sahara",YEM:"^(?!.*arab)(?!.*north)(?!.*sana)(?!.*peo)(?!.*dem)(?!.*south)(?!.*aden)(?!.*\\bp\\.?d\\.?r).*yemen",YMD:"^(?=.*peo).*yemen|^(?!.*rep)(?=.*dem).*yemen|^(?=.*south).*yemen|^(?=.*aden).*yemen|^(?=.*\\bp\\.?d\\.?r).*yemen",YUG:"yugoslavia",ZMB:"zambia|northern.?rhodesia",EAZ:"zanzibar",ZWE:"zimbabwe|^(?!.*northern).*rhodesia"}},{}],140:[function(t,e,r){e.exports=["xx-small","x-small","small","medium","large","x-large","xx-large","larger","smaller"]},{}],141:[function(t,e,r){e.exports=["normal","condensed","semi-condensed","extra-condensed","ultra-condensed","expanded","semi-expanded","extra-expanded","ultra-expanded"]},{}],142:[function(t,e,r){e.exports=["normal","italic","oblique"]},{}],143:[function(t,e,r){e.exports=["normal","bold","bolder","lighter","100","200","300","400","500","600","700","800","900"]},{}],144:[function(t,e,r){"use strict";e.exports={parse:t("./parse"),stringify:t("./stringify")}},{"./parse":146,"./stringify":147}],145:[function(t,e,r){"use strict";var n=t("css-font-size-keywords");e.exports={isSize:function(t){return/^[\d\.]/.test(t)||-1!==t.indexOf("/")||-1!==n.indexOf(t)}}},{"css-font-size-keywords":140}],146:[function(t,e,r){"use strict";var n=t("unquote"),i=t("css-global-keywords"),a=t("css-system-font-keywords"),o=t("css-font-weight-keywords"),s=t("css-font-style-keywords"),l=t("css-font-stretch-keywords"),c=t("string-split-by"),u=t("./lib/util").isSize;e.exports=h;var f=h.cache={};function h(t){if("string"!=typeof t)throw new Error("Font argument must be a string.");if(f[t])return f[t];if(""===t)throw new Error("Cannot parse an empty string.");if(-1!==a.indexOf(t))return f[t]={system:t};for(var e,r={style:"normal",variant:"normal",weight:"normal",stretch:"normal",lineHeight:"normal",size:"1rem",family:["serif"]},h=c(t,/\s+/);e=h.shift();){if(-1!==i.indexOf(e))return["style","variant","weight","stretch"].forEach((function(t){r[t]=e})),f[t]=r;if(-1===s.indexOf(e))if("normal"!==e&&"small-caps"!==e)if(-1===l.indexOf(e)){if(-1===o.indexOf(e)){if(u(e)){var d=c(e,"/");if(r.size=d[0],null!=d[1]?r.lineHeight=p(d[1]):"/"===h[0]&&(h.shift(),r.lineHeight=p(h.shift())),!h.length)throw new Error("Missing required font-family.");return r.family=c(h.join(" "),/\s*,\s*/).map(n),f[t]=r}throw new Error("Unknown or unsupported font token: "+e)}r.weight=e}else r.stretch=e;else r.variant=e;else r.style=e}throw new Error("Missing required font-size.")}function p(t){var e=parseFloat(t);return e.toString()===t?e:t}},{"./lib/util":145,"css-font-stretch-keywords":141,"css-font-style-keywords":142,"css-font-weight-keywords":143,"css-global-keywords":148,"css-system-font-keywords":149,"string-split-by":568,unquote:598}],147:[function(t,e,r){"use strict";var n=t("pick-by-alias"),i=t("./lib/util").isSize,a=g(t("css-global-keywords")),o=g(t("css-system-font-keywords")),s=g(t("css-font-weight-keywords")),l=g(t("css-font-style-keywords")),c=g(t("css-font-stretch-keywords")),u={normal:1,"small-caps":1},f={serif:1,"sans-serif":1,monospace:1,cursive:1,fantasy:1,"system-ui":1},h="1rem",p="serif";function d(t,e){if(t&&!e[t]&&!a[t])throw Error("Unknown keyword `"+t+"`");return t}function g(t){for(var e={},r=0;r<t.length;r++)e[t[r]]=1;return e}e.exports=function(t){if((t=n(t,{style:"style fontstyle fontStyle font-style slope distinction",variant:"variant font-variant fontVariant fontvariant var capitalization",weight:"weight w font-weight fontWeight fontweight",stretch:"stretch font-stretch fontStretch fontstretch width",size:"size s font-size fontSize fontsize height em emSize",lineHeight:"lh line-height lineHeight lineheight leading",family:"font family fontFamily font-family fontfamily type typeface face",system:"system reserved default global"})).system)return t.system&&d(t.system,o),t.system;if(d(t.style,l),d(t.variant,u),d(t.weight,s),d(t.stretch,c),null==t.size&&(t.size=h),"number"==typeof t.size&&(t.size+="px"),!i)throw Error("Bad size value `"+t.size+"`");t.family||(t.family=p),Array.isArray(t.family)&&(t.family.length||(t.family=[p]),t.family=t.family.map((function(t){return f[t]?t:'"'+t+'"'})).join(", "));var e=[];return e.push(t.style),t.variant!==t.style&&e.push(t.variant),t.weight!==t.variant&&t.weight!==t.style&&e.push(t.weight),t.stretch!==t.weight&&t.stretch!==t.variant&&t.stretch!==t.style&&e.push(t.stretch),e.push(t.size+(null==t.lineHeight||"normal"===t.lineHeight||t.lineHeight+""=="1"?"":"/"+t.lineHeight)),e.push(t.family),e.filter(Boolean).join(" ")}},{"./lib/util":145,"css-font-stretch-keywords":141,"css-font-style-keywords":142,"css-font-weight-keywords":143,"css-global-keywords":148,"css-system-font-keywords":149,"pick-by-alias":511}],148:[function(t,e,r){e.exports=["inherit","initial","unset"]},{}],149:[function(t,e,r){e.exports=["caption","icon","menu","message-box","small-caption","status-bar"]},{}],150:[function(t,e,r){"use strict";e.exports=function(t,e,r,n,i,a){var o=i-1,s=i*i,l=o*o,c=(1+2*i)*l,u=i*l,f=s*(3-2*i),h=s*o;if(t.length){a||(a=new Array(t.length));for(var p=t.length-1;p>=0;--p)a[p]=c*t[p]+u*e[p]+f*r[p]+h*n[p];return a}return c*t+u*e+f*r+h*n},e.exports.derivative=function(t,e,r,n,i,a){var o=6*i*i-6*i,s=3*i*i-4*i+1,l=-6*i*i+6*i,c=3*i*i-2*i;if(t.length){a||(a=new Array(t.length));for(var u=t.length-1;u>=0;--u)a[u]=o*t[u]+s*e[u]+l*r[u]+c*n[u];return a}return o*t+s*e+l*r[u]+c*n}},{}],151:[function(t,e,r){"use strict";var n=t("./lib/thunk.js");function i(){this.argTypes=[],this.shimArgs=[],this.arrayArgs=[],this.arrayBlockIndices=[],this.scalarArgs=[],this.offsetArgs=[],this.offsetArgIndex=[],this.indexArgs=[],this.shapeArgs=[],this.funcName="",this.pre=null,this.body=null,this.post=null,this.debug=!1}e.exports=function(t){var e=new i;e.pre=t.pre,e.body=t.body,e.post=t.post;var r=t.args.slice(0);e.argTypes=r;for(var a=0;a<r.length;++a){var o=r[a];if("array"===o||"object"==typeof o&&o.blockIndices){if(e.argTypes[a]="array",e.arrayArgs.push(a),e.arrayBlockIndices.push(o.blockIndices?o.blockIndices:0),e.shimArgs.push("array"+a),a<e.pre.args.length&&e.pre.args[a].count>0)throw new Error("cwise: pre() block may not reference array args");if(a<e.post.args.length&&e.post.args[a].count>0)throw new Error("cwise: post() block may not reference array args")}else if("scalar"===o)e.scalarArgs.push(a),e.shimArgs.push("scalar"+a);else if("index"===o){if(e.indexArgs.push(a),a<e.pre.args.length&&e.pre.args[a].count>0)throw new Error("cwise: pre() block may not reference array index");if(a<e.body.args.length&&e.body.args[a].lvalue)throw new Error("cwise: body() block may not write to array index");if(a<e.post.args.length&&e.post.args[a].count>0)throw new Error("cwise: post() block may not reference array index")}else if("shape"===o){if(e.shapeArgs.push(a),a<e.pre.args.length&&e.pre.args[a].lvalue)throw new Error("cwise: pre() block may not write to array shape");if(a<e.body.args.length&&e.body.args[a].lvalue)throw new Error("cwise: body() block may not write to array shape");if(a<e.post.args.length&&e.post.args[a].lvalue)throw new Error("cwise: post() block may not write to array shape")}else{if("object"!=typeof o||!o.offset)throw new Error("cwise: Unknown argument type "+r[a]);e.argTypes[a]="offset",e.offsetArgs.push({array:o.array,offset:o.offset}),e.offsetArgIndex.push(a)}}if(e.arrayArgs.length<=0)throw new Error("cwise: No array arguments specified");if(e.pre.args.length>r.length)throw new Error("cwise: Too many arguments in pre() block");if(e.body.args.length>r.length)throw new Error("cwise: Too many arguments in body() block");if(e.post.args.length>r.length)throw new Error("cwise: Too many arguments in post() block");return e.debug=!!t.printCode||!!t.debug,e.funcName=t.funcName||"cwise",e.blockSize=t.blockSize||64,n(e)}},{"./lib/thunk.js":153}],152:[function(t,e,r){"use strict";var n=t("uniq");function i(t,e,r){var n,i,a=t.length,o=e.arrayArgs.length,s=e.indexArgs.length>0,l=[],c=[],u=0,f=0;for(n=0;n<a;++n)c.push(["i",n,"=0"].join(""));for(i=0;i<o;++i)for(n=0;n<a;++n)f=u,u=t[n],0===n?c.push(["d",i,"s",n,"=t",i,"p",u].join("")):c.push(["d",i,"s",n,"=(t",i,"p",u,"-s",f,"*t",i,"p",f,")"].join(""));for(c.length>0&&l.push("var "+c.join(",")),n=a-1;n>=0;--n)u=t[n],l.push(["for(i",n,"=0;i",n,"<s",u,";++i",n,"){"].join(""));for(l.push(r),n=0;n<a;++n){for(f=u,u=t[n],i=0;i<o;++i)l.push(["p",i,"+=d",i,"s",n].join(""));s&&(n>0&&l.push(["index[",f,"]-=s",f].join("")),l.push(["++index[",u,"]"].join(""))),l.push("}")}return l.join("\n")}function a(t,e,r){for(var n=t.body,i=[],a=[],o=0;o<t.args.length;++o){var s=t.args[o];if(!(s.count<=0)){var l=new RegExp(s.name,"g"),c="",u=e.arrayArgs.indexOf(o);switch(e.argTypes[o]){case"offset":var f=e.offsetArgIndex.indexOf(o);u=e.offsetArgs[f].array,c="+q"+f;case"array":c="p"+u+c;var h="l"+o,p="a"+u;if(0===e.arrayBlockIndices[u])1===s.count?"generic"===r[u]?s.lvalue?(i.push(["var ",h,"=",p,".get(",c,")"].join("")),n=n.replace(l,h),a.push([p,".set(",c,",",h,")"].join(""))):n=n.replace(l,[p,".get(",c,")"].join("")):n=n.replace(l,[p,"[",c,"]"].join("")):"generic"===r[u]?(i.push(["var ",h,"=",p,".get(",c,")"].join("")),n=n.replace(l,h),s.lvalue&&a.push([p,".set(",c,",",h,")"].join(""))):(i.push(["var ",h,"=",p,"[",c,"]"].join("")),n=n.replace(l,h),s.lvalue&&a.push([p,"[",c,"]=",h].join("")));else{for(var d=[s.name],g=[c],m=0;m<Math.abs(e.arrayBlockIndices[u]);m++)d.push("\\s*\\[([^\\]]+)\\]"),g.push("$"+(m+1)+"*t"+u+"b"+m);if(l=new RegExp(d.join(""),"g"),c=g.join("+"),"generic"===r[u])throw new Error("cwise: Generic arrays not supported in combination with blocks!");n=n.replace(l,[p,"[",c,"]"].join(""))}break;case"scalar":n=n.replace(l,"Y"+e.scalarArgs.indexOf(o));break;case"index":n=n.replace(l,"index");break;case"shape":n=n.replace(l,"shape")}}}return[i.join("\n"),n,a.join("\n")].join("\n").trim()}function o(t){for(var e=new Array(t.length),r=!0,n=0;n<t.length;++n){var i=t[n],a=i.match(/\d+/);a=a?a[0]:"",0===i.charAt(0)?e[n]="u"+i.charAt(1)+a:e[n]=i.charAt(0)+a,n>0&&(r=r&&e[n]===e[n-1])}return r?e[0]:e.join("")}e.exports=function(t,e){for(var r=e[1].length-Math.abs(t.arrayBlockIndices[0])|0,s=new Array(t.arrayArgs.length),l=new Array(t.arrayArgs.length),c=0;c<t.arrayArgs.length;++c)l[c]=e[2*c],s[c]=e[2*c+1];var u=[],f=[],h=[],p=[],d=[];for(c=0;c<t.arrayArgs.length;++c){t.arrayBlockIndices[c]<0?(h.push(0),p.push(r),u.push(r),f.push(r+t.arrayBlockIndices[c])):(h.push(t.arrayBlockIndices[c]),p.push(t.arrayBlockIndices[c]+r),u.push(0),f.push(t.arrayBlockIndices[c]));for(var g=[],m=0;m<s[c].length;m++)h[c]<=s[c][m]&&s[c][m]<p[c]&&g.push(s[c][m]-h[c]);d.push(g)}var v=["SS"],y=["'use strict'"],x=[];for(m=0;m<r;++m)x.push(["s",m,"=SS[",m,"]"].join(""));for(c=0;c<t.arrayArgs.length;++c){v.push("a"+c),v.push("t"+c),v.push("p"+c);for(m=0;m<r;++m)x.push(["t",c,"p",m,"=t",c,"[",h[c]+m,"]"].join(""));for(m=0;m<Math.abs(t.arrayBlockIndices[c]);++m)x.push(["t",c,"b",m,"=t",c,"[",u[c]+m,"]"].join(""))}for(c=0;c<t.scalarArgs.length;++c)v.push("Y"+c);if(t.shapeArgs.length>0&&x.push("shape=SS.slice(0)"),t.indexArgs.length>0){var b=new Array(r);for(c=0;c<r;++c)b[c]="0";x.push(["index=[",b.join(","),"]"].join(""))}for(c=0;c<t.offsetArgs.length;++c){var _=t.offsetArgs[c],w=[];for(m=0;m<_.offset.length;++m)0!==_.offset[m]&&(1===_.offset[m]?w.push(["t",_.array,"p",m].join("")):w.push([_.offset[m],"*t",_.array,"p",m].join("")));0===w.length?x.push("q"+c+"=0"):x.push(["q",c,"=",w.join("+")].join(""))}var T=n([].concat(t.pre.thisVars).concat(t.body.thisVars).concat(t.post.thisVars));for((x=x.concat(T)).length>0&&y.push("var "+x.join(",")),c=0;c<t.arrayArgs.length;++c)y.push("p"+c+"|=0");t.pre.body.length>3&&y.push(a(t.pre,t,l));var k=a(t.body,t,l),M=function(t){for(var e=0,r=t[0].length;e<r;){for(var n=1;n<t.length;++n)if(t[n][e]!==t[0][e])return e;++e}return e}(d);M<r?y.push(function(t,e,r,n){for(var a=e.length,o=r.arrayArgs.length,s=r.blockSize,l=r.indexArgs.length>0,c=[],u=0;u<o;++u)c.push(["var offset",u,"=p",u].join(""));for(u=t;u<a;++u)c.push(["for(var j"+u+"=SS[",e[u],"]|0;j",u,">0;){"].join("")),c.push(["if(j",u,"<",s,"){"].join("")),c.push(["s",e[u],"=j",u].join("")),c.push(["j",u,"=0"].join("")),c.push(["}else{s",e[u],"=",s].join("")),c.push(["j",u,"-=",s,"}"].join("")),l&&c.push(["index[",e[u],"]=j",u].join(""));for(u=0;u<o;++u){for(var f=["offset"+u],h=t;h<a;++h)f.push(["j",h,"*t",u,"p",e[h]].join(""));c.push(["p",u,"=(",f.join("+"),")"].join(""))}for(c.push(i(e,r,n)),u=t;u<a;++u)c.push("}");return c.join("\n")}(M,d[0],t,k)):y.push(i(d[0],t,k)),t.post.body.length>3&&y.push(a(t.post,t,l)),t.debug&&console.log("-----Generated cwise routine for ",e,":\n"+y.join("\n")+"\n----------");var A=[t.funcName||"unnamed","_cwise_loop_",s[0].join("s"),"m",M,o(l)].join("");return new Function(["function ",A,"(",v.join(","),"){",y.join("\n"),"} return ",A].join(""))()}},{uniq:597}],153:[function(t,e,r){"use strict";var n=t("./compile.js");e.exports=function(t){var e=["'use strict'","var CACHED={}"],r=[],i=t.funcName+"_cwise_thunk";e.push(["return function ",i,"(",t.shimArgs.join(","),"){"].join(""));for(var a=[],o=[],s=[["array",t.arrayArgs[0],".shape.slice(",Math.max(0,t.arrayBlockIndices[0]),t.arrayBlockIndices[0]<0?","+t.arrayBlockIndices[0]+")":")"].join("")],l=[],c=[],u=0;u<t.arrayArgs.length;++u){var f=t.arrayArgs[u];r.push(["t",f,"=array",f,".dtype,","r",f,"=array",f,".order"].join("")),a.push("t"+f),a.push("r"+f),o.push("t"+f),o.push("r"+f+".join()"),s.push("array"+f+".data"),s.push("array"+f+".stride"),s.push("array"+f+".offset|0"),u>0&&(l.push("array"+t.arrayArgs[0]+".shape.length===array"+f+".shape.length+"+(Math.abs(t.arrayBlockIndices[0])-Math.abs(t.arrayBlockIndices[u]))),c.push("array"+t.arrayArgs[0]+".shape[shapeIndex+"+Math.max(0,t.arrayBlockIndices[0])+"]===array"+f+".shape[shapeIndex+"+Math.max(0,t.arrayBlockIndices[u])+"]"))}for(t.arrayArgs.length>1&&(e.push("if (!("+l.join(" && ")+")) throw new Error('cwise: Arrays do not all have the same dimensionality!')"),e.push("for(var shapeIndex=array"+t.arrayArgs[0]+".shape.length-"+Math.abs(t.arrayBlockIndices[0])+"; shapeIndex--\x3e0;) {"),e.push("if (!("+c.join(" && ")+")) throw new Error('cwise: Arrays do not all have the same shape!')"),e.push("}")),u=0;u<t.scalarArgs.length;++u)s.push("scalar"+t.scalarArgs[u]);return r.push(["type=[",o.join(","),"].join()"].join("")),r.push("proc=CACHED[type]"),e.push("var "+r.join(",")),e.push(["if(!proc){","CACHED[type]=proc=compile([",a.join(","),"])}","return proc(",s.join(","),")}"].join("")),t.debug&&console.log("-----Generated thunk:\n"+e.join("\n")+"\n----------"),new Function("compile",e.join("\n"))(n.bind(void 0,t))}},{"./compile.js":152}],154:[function(t,e,r){"use strict";var n,i=t("type/value/is"),a=t("type/value/ensure"),o=t("type/plain-function/ensure"),s=t("es5-ext/object/copy"),l=t("es5-ext/object/normalize-options"),c=t("es5-ext/object/map"),u=Function.prototype.bind,f=Object.defineProperty,h=Object.prototype.hasOwnProperty;n=function(t,e,r){var n,i=a(e)&&o(e.value);return delete(n=s(e)).writable,delete n.value,n.get=function(){return!r.overwriteDefinition&&h.call(this,t)?i:(e.value=u.call(i,r.resolveContext?r.resolveContext(this):this),f(this,t,e),this[t])},n},e.exports=function(t){var e=l(arguments[1]);return i(e.resolveContext)&&o(e.resolveContext),c(t,(function(t,r){return n(r,t,e)}))}},{"es5-ext/object/copy":196,"es5-ext/object/map":204,"es5-ext/object/normalize-options":205,"type/plain-function/ensure":589,"type/value/ensure":593,"type/value/is":594}],155:[function(t,e,r){"use strict";var n=t("type/value/is"),i=t("type/plain-function/is"),a=t("es5-ext/object/assign"),o=t("es5-ext/object/normalize-options"),s=t("es5-ext/string/#/contains");(e.exports=function(t,e){var r,i,l,c,u;return arguments.length<2||"string"!=typeof t?(c=e,e=t,t=null):c=arguments[2],n(t)?(r=s.call(t,"c"),i=s.call(t,"e"),l=s.call(t,"w")):(r=l=!0,i=!1),u={value:e,configurable:r,enumerable:i,writable:l},c?a(o(c),u):u}).gs=function(t,e,r){var l,c,u,f;return"string"!=typeof t?(u=r,r=e,e=t,t=null):u=arguments[3],n(e)?i(e)?n(r)?i(r)||(u=r,r=void 0):r=void 0:(u=e,e=r=void 0):e=void 0,n(t)?(l=s.call(t,"c"),c=s.call(t,"e")):(l=!0,c=!1),f={get:e,set:r,configurable:l,enumerable:c},u?a(o(u),f):f}},{"es5-ext/object/assign":193,"es5-ext/object/normalize-options":205,"es5-ext/string/#/contains":212,"type/plain-function/is":590,"type/value/is":594}],156:[function(t,e,r){!function(t,n){n("object"==typeof r&&"undefined"!=typeof e?r:t.d3=t.d3||{})}(this,(function(t){"use strict";function e(t,e){return t<e?-1:t>e?1:t>=e?0:NaN}function r(t){var r;return 1===t.length&&(r=t,t=function(t,n){return e(r(t),n)}),{left:function(e,r,n,i){for(null==n&&(n=0),null==i&&(i=e.length);n<i;){var a=n+i>>>1;t(e[a],r)<0?n=a+1:i=a}return n},right:function(e,r,n,i){for(null==n&&(n=0),null==i&&(i=e.length);n<i;){var a=n+i>>>1;t(e[a],r)>0?i=a:n=a+1}return n}}}var n=r(e),i=n.right,a=n.left;function o(t,e){return[t,e]}function s(t){return null===t?NaN:+t}function l(t,e){var r,n,i=t.length,a=0,o=-1,l=0,c=0;if(null==e)for(;++o<i;)isNaN(r=s(t[o]))||(c+=(n=r-l)*(r-(l+=n/++a)));else for(;++o<i;)isNaN(r=s(e(t[o],o,t)))||(c+=(n=r-l)*(r-(l+=n/++a)));if(a>1)return c/(a-1)}function c(t,e){var r=l(t,e);return r?Math.sqrt(r):r}function u(t,e){var r,n,i,a=t.length,o=-1;if(null==e){for(;++o<a;)if(null!=(r=t[o])&&r>=r)for(n=i=r;++o<a;)null!=(r=t[o])&&(n>r&&(n=r),i<r&&(i=r))}else for(;++o<a;)if(null!=(r=e(t[o],o,t))&&r>=r)for(n=i=r;++o<a;)null!=(r=e(t[o],o,t))&&(n>r&&(n=r),i<r&&(i=r));return[n,i]}var f=Array.prototype,h=f.slice,p=f.map;function d(t){return function(){return t}}function g(t){return t}function m(t,e,r){t=+t,e=+e,r=(i=arguments.length)<2?(e=t,t=0,1):i<3?1:+r;for(var n=-1,i=0|Math.max(0,Math.ceil((e-t)/r)),a=new Array(i);++n<i;)a[n]=t+n*r;return a}var v=Math.sqrt(50),y=Math.sqrt(10),x=Math.sqrt(2);function b(t,e,r){var n=(e-t)/Math.max(0,r),i=Math.floor(Math.log(n)/Math.LN10),a=n/Math.pow(10,i);return i>=0?(a>=v?10:a>=y?5:a>=x?2:1)*Math.pow(10,i):-Math.pow(10,-i)/(a>=v?10:a>=y?5:a>=x?2:1)}function _(t,e,r){var n=Math.abs(e-t)/Math.max(0,r),i=Math.pow(10,Math.floor(Math.log(n)/Math.LN10)),a=n/i;return a>=v?i*=10:a>=y?i*=5:a>=x&&(i*=2),e<t?-i:i}function w(t){return Math.ceil(Math.log(t.length)/Math.LN2)+1}function T(t,e,r){if(null==r&&(r=s),n=t.length){if((e=+e)<=0||n<2)return+r(t[0],0,t);if(e>=1)return+r(t[n-1],n-1,t);var n,i=(n-1)*e,a=Math.floor(i),o=+r(t[a],a,t);return o+(+r(t[a+1],a+1,t)-o)*(i-a)}}function k(t,e){var r,n,i=t.length,a=-1;if(null==e){for(;++a<i;)if(null!=(r=t[a])&&r>=r)for(n=r;++a<i;)null!=(r=t[a])&&n>r&&(n=r)}else for(;++a<i;)if(null!=(r=e(t[a],a,t))&&r>=r)for(n=r;++a<i;)null!=(r=e(t[a],a,t))&&n>r&&(n=r);return n}function M(t){if(!(i=t.length))return[];for(var e=-1,r=k(t,A),n=new Array(r);++e<r;)for(var i,a=-1,o=n[e]=new Array(i);++a<i;)o[a]=t[a][e];return n}function A(t){return t.length}t.bisect=i,t.bisectRight=i,t.bisectLeft=a,t.ascending=e,t.bisector=r,t.cross=function(t,e,r){var n,i,a,s,l=t.length,c=e.length,u=new Array(l*c);for(null==r&&(r=o),n=a=0;n<l;++n)for(s=t[n],i=0;i<c;++i,++a)u[a]=r(s,e[i]);return u},t.descending=function(t,e){return e<t?-1:e>t?1:e>=t?0:NaN},t.deviation=c,t.extent=u,t.histogram=function(){var t=g,e=u,r=w;function n(n){var a,o,s=n.length,l=new Array(s);for(a=0;a<s;++a)l[a]=t(n[a],a,n);var c=e(l),u=c[0],f=c[1],h=r(l,u,f);Array.isArray(h)||(h=_(u,f,h),h=m(Math.ceil(u/h)*h,f,h));for(var p=h.length;h[0]<=u;)h.shift(),--p;for(;h[p-1]>f;)h.pop(),--p;var d,g=new Array(p+1);for(a=0;a<=p;++a)(d=g[a]=[]).x0=a>0?h[a-1]:u,d.x1=a<p?h[a]:f;for(a=0;a<s;++a)u<=(o=l[a])&&o<=f&&g[i(h,o,0,p)].push(n[a]);return g}return n.value=function(e){return arguments.length?(t="function"==typeof e?e:d(e),n):t},n.domain=function(t){return arguments.length?(e="function"==typeof t?t:d([t[0],t[1]]),n):e},n.thresholds=function(t){return arguments.length?(r="function"==typeof t?t:Array.isArray(t)?d(h.call(t)):d(t),n):r},n},t.thresholdFreedmanDiaconis=function(t,r,n){return t=p.call(t,s).sort(e),Math.ceil((n-r)/(2*(T(t,.75)-T(t,.25))*Math.pow(t.length,-1/3)))},t.thresholdScott=function(t,e,r){return Math.ceil((r-e)/(3.5*c(t)*Math.pow(t.length,-1/3)))},t.thresholdSturges=w,t.max=function(t,e){var r,n,i=t.length,a=-1;if(null==e){for(;++a<i;)if(null!=(r=t[a])&&r>=r)for(n=r;++a<i;)null!=(r=t[a])&&r>n&&(n=r)}else for(;++a<i;)if(null!=(r=e(t[a],a,t))&&r>=r)for(n=r;++a<i;)null!=(r=e(t[a],a,t))&&r>n&&(n=r);return n},t.mean=function(t,e){var r,n=t.length,i=n,a=-1,o=0;if(null==e)for(;++a<n;)isNaN(r=s(t[a]))?--i:o+=r;else for(;++a<n;)isNaN(r=s(e(t[a],a,t)))?--i:o+=r;if(i)return o/i},t.median=function(t,r){var n,i=t.length,a=-1,o=[];if(null==r)for(;++a<i;)isNaN(n=s(t[a]))||o.push(n);else for(;++a<i;)isNaN(n=s(r(t[a],a,t)))||o.push(n);return T(o.sort(e),.5)},t.merge=function(t){for(var e,r,n,i=t.length,a=-1,o=0;++a<i;)o+=t[a].length;for(r=new Array(o);--i>=0;)for(e=(n=t[i]).length;--e>=0;)r[--o]=n[e];return r},t.min=k,t.pairs=function(t,e){null==e&&(e=o);for(var r=0,n=t.length-1,i=t[0],a=new Array(n<0?0:n);r<n;)a[r]=e(i,i=t[++r]);return a},t.permute=function(t,e){for(var r=e.length,n=new Array(r);r--;)n[r]=t[e[r]];return n},t.quantile=T,t.range=m,t.scan=function(t,r){if(n=t.length){var n,i,a=0,o=0,s=t[o];for(null==r&&(r=e);++a<n;)(r(i=t[a],s)<0||0!==r(s,s))&&(s=i,o=a);return 0===r(s,s)?o:void 0}},t.shuffle=function(t,e,r){for(var n,i,a=(null==r?t.length:r)-(e=null==e?0:+e);a;)i=Math.random()*a--|0,n=t[a+e],t[a+e]=t[i+e],t[i+e]=n;return t},t.sum=function(t,e){var r,n=t.length,i=-1,a=0;if(null==e)for(;++i<n;)(r=+t[i])&&(a+=r);else for(;++i<n;)(r=+e(t[i],i,t))&&(a+=r);return a},t.ticks=function(t,e,r){var n,i,a,o,s=-1;if(r=+r,(t=+t)===(e=+e)&&r>0)return[t];if((n=e<t)&&(i=t,t=e,e=i),0===(o=b(t,e,r))||!isFinite(o))return[];if(o>0)for(t=Math.ceil(t/o),e=Math.floor(e/o),a=new Array(i=Math.ceil(e-t+1));++s<i;)a[s]=(t+s)*o;else for(t=Math.floor(t*o),e=Math.ceil(e*o),a=new Array(i=Math.ceil(t-e+1));++s<i;)a[s]=(t-s)/o;return n&&a.reverse(),a},t.tickIncrement=b,t.tickStep=_,t.transpose=M,t.variance=l,t.zip=function(){return M(arguments)},Object.defineProperty(t,"__esModule",{value:!0})}))},{}],157:[function(t,e,r){!function(t,n){n("object"==typeof r&&"undefined"!=typeof e?r:t.d3=t.d3||{})}(this,(function(t){"use strict";function e(){}function r(t,r){var n=new e;if(t instanceof e)t.each((function(t,e){n.set(e,t)}));else if(Array.isArray(t)){var i,a=-1,o=t.length;if(null==r)for(;++a<o;)n.set(a,t[a]);else for(;++a<o;)n.set(r(i=t[a],a,t),i)}else if(t)for(var s in t)n.set(s,t[s]);return n}function n(){return{}}function i(t,e,r){t[e]=r}function a(){return r()}function o(t,e,r){t.set(e,r)}function s(){}e.prototype=r.prototype={constructor:e,has:function(t){return"$"+t in this},get:function(t){return this["$"+t]},set:function(t,e){return this["$"+t]=e,this},remove:function(t){var e="$"+t;return e in this&&delete this[e]},clear:function(){for(var t in this)"$"===t[0]&&delete this[t]},keys:function(){var t=[];for(var e in this)"$"===e[0]&&t.push(e.slice(1));return t},values:function(){var t=[];for(var e in this)"$"===e[0]&&t.push(this[e]);return t},entries:function(){var t=[];for(var e in this)"$"===e[0]&&t.push({key:e.slice(1),value:this[e]});return t},size:function(){var t=0;for(var e in this)"$"===e[0]&&++t;return t},empty:function(){for(var t in this)if("$"===t[0])return!1;return!0},each:function(t){for(var e in this)"$"===e[0]&&t(this[e],e.slice(1),this)}};var l=r.prototype;function c(t,e){var r=new s;if(t instanceof s)t.each((function(t){r.add(t)}));else if(t){var n=-1,i=t.length;if(null==e)for(;++n<i;)r.add(t[n]);else for(;++n<i;)r.add(e(t[n],n,t))}return r}s.prototype=c.prototype={constructor:s,has:l.has,add:function(t){return this["$"+(t+="")]=t,this},remove:l.remove,clear:l.clear,values:l.keys,size:l.size,empty:l.empty,each:l.each},t.nest=function(){var t,e,s,l=[],c=[];function u(n,i,a,o){if(i>=l.length)return null!=t&&n.sort(t),null!=e?e(n):n;for(var s,c,f,h=-1,p=n.length,d=l[i++],g=r(),m=a();++h<p;)(f=g.get(s=d(c=n[h])+""))?f.push(c):g.set(s,[c]);return g.each((function(t,e){o(m,e,u(t,i,a,o))})),m}return s={object:function(t){return u(t,0,n,i)},map:function(t){return u(t,0,a,o)},entries:function(t){return function t(r,n){if(++n>l.length)return r;var i,a=c[n-1];return null!=e&&n>=l.length?i=r.entries():(i=[],r.each((function(e,r){i.push({key:r,values:t(e,n)})}))),null!=a?i.sort((function(t,e){return a(t.key,e.key)})):i}(u(t,0,a,o),0)},key:function(t){return l.push(t),s},sortKeys:function(t){return c[l.length-1]=t,s},sortValues:function(e){return t=e,s},rollup:function(t){return e=t,s}}},t.set=c,t.map=r,t.keys=function(t){var e=[];for(var r in t)e.push(r);return e},t.values=function(t){var e=[];for(var r in t)e.push(t[r]);return e},t.entries=function(t){var e=[];for(var r in t)e.push({key:r,value:t[r]});return e},Object.defineProperty(t,"__esModule",{value:!0})}))},{}],158:[function(t,e,r){!function(t,n){"object"==typeof r&&"undefined"!=typeof e?n(r):n((t=t||self).d3=t.d3||{})}(this,(function(t){"use strict";function e(t,e,r){t.prototype=e.prototype=r,r.constructor=t}function r(t,e){var r=Object.create(t.prototype);for(var n in e)r[n]=e[n];return r}function n(){}var i="\\s*([+-]?\\d+)\\s*",a="\\s*([+-]?\\d*\\.?\\d+(?:[eE][+-]?\\d+)?)\\s*",o="\\s*([+-]?\\d*\\.?\\d+(?:[eE][+-]?\\d+)?)%\\s*",s=/^#([0-9a-f]{3,8})$/,l=new RegExp("^rgb\\("+[i,i,i]+"\\)$"),c=new RegExp("^rgb\\("+[o,o,o]+"\\)$"),u=new RegExp("^rgba\\("+[i,i,i,a]+"\\)$"),f=new RegExp("^rgba\\("+[o,o,o,a]+"\\)$"),h=new RegExp("^hsl\\("+[a,o,o]+"\\)$"),p=new RegExp("^hsla\\("+[a,o,o,a]+"\\)$"),d={aliceblue:15792383,antiquewhite:16444375,aqua:65535,aquamarine:8388564,azure:15794175,beige:16119260,bisque:16770244,black:0,blanchedalmond:16772045,blue:255,blueviolet:9055202,brown:10824234,burlywood:14596231,cadetblue:6266528,chartreuse:8388352,chocolate:13789470,coral:16744272,cornflowerblue:6591981,cornsilk:16775388,crimson:14423100,cyan:65535,darkblue:139,darkcyan:35723,darkgoldenrod:12092939,darkgray:11119017,darkgreen:25600,darkgrey:11119017,darkkhaki:12433259,darkmagenta:9109643,darkolivegreen:5597999,darkorange:16747520,darkorchid:10040012,darkred:9109504,darksalmon:15308410,darkseagreen:9419919,darkslateblue:4734347,darkslategray:3100495,darkslategrey:3100495,darkturquoise:52945,darkviolet:9699539,deeppink:16716947,deepskyblue:49151,dimgray:6908265,dimgrey:6908265,dodgerblue:2003199,firebrick:11674146,floralwhite:16775920,forestgreen:2263842,fuchsia:16711935,gainsboro:14474460,ghostwhite:16316671,gold:16766720,goldenrod:14329120,gray:8421504,green:32768,greenyellow:11403055,grey:8421504,honeydew:15794160,hotpink:16738740,indianred:13458524,indigo:4915330,ivory:16777200,khaki:15787660,lavender:15132410,lavenderblush:16773365,lawngreen:8190976,lemonchiffon:16775885,lightblue:11393254,lightcoral:15761536,lightcyan:14745599,lightgoldenrodyellow:16448210,lightgray:13882323,lightgreen:9498256,lightgrey:13882323,lightpink:16758465,lightsalmon:16752762,lightseagreen:2142890,lightskyblue:8900346,lightslategray:7833753,lightslategrey:7833753,lightsteelblue:11584734,lightyellow:16777184,lime:65280,limegreen:3329330,linen:16445670,magenta:16711935,maroon:8388608,mediumaquamarine:6737322,mediumblue:205,mediumorchid:12211667,mediumpurple:9662683,mediumseagreen:3978097,mediumslateblue:8087790,mediumspringgreen:64154,mediumturquoise:4772300,mediumvioletred:13047173,midnightblue:1644912,mintcream:16121850,mistyrose:16770273,moccasin:16770229,navajowhite:16768685,navy:128,oldlace:16643558,olive:8421376,olivedrab:7048739,orange:16753920,orangered:16729344,orchid:14315734,palegoldenrod:15657130,palegreen:10025880,paleturquoise:11529966,palevioletred:14381203,papayawhip:16773077,peachpuff:16767673,peru:13468991,pink:16761035,plum:14524637,powderblue:11591910,purple:8388736,rebeccapurple:6697881,red:16711680,rosybrown:12357519,royalblue:4286945,saddlebrown:9127187,salmon:16416882,sandybrown:16032864,seagreen:3050327,seashell:16774638,sienna:10506797,silver:12632256,skyblue:8900331,slateblue:6970061,slategray:7372944,slategrey:7372944,snow:16775930,springgreen:65407,steelblue:4620980,tan:13808780,teal:32896,thistle:14204888,tomato:16737095,turquoise:4251856,violet:15631086,wheat:16113331,white:16777215,whitesmoke:16119285,yellow:16776960,yellowgreen:10145074};function g(){return this.rgb().formatHex()}function m(){return this.rgb().formatRgb()}function v(t){var e,r;return t=(t+"").trim().toLowerCase(),(e=s.exec(t))?(r=e[1].length,e=parseInt(e[1],16),6===r?y(e):3===r?new w(e>>8&15|e>>4&240,e>>4&15|240&e,(15&e)<<4|15&e,1):8===r?x(e>>24&255,e>>16&255,e>>8&255,(255&e)/255):4===r?x(e>>12&15|e>>8&240,e>>8&15|e>>4&240,e>>4&15|240&e,((15&e)<<4|15&e)/255):null):(e=l.exec(t))?new w(e[1],e[2],e[3],1):(e=c.exec(t))?new w(255*e[1]/100,255*e[2]/100,255*e[3]/100,1):(e=u.exec(t))?x(e[1],e[2],e[3],e[4]):(e=f.exec(t))?x(255*e[1]/100,255*e[2]/100,255*e[3]/100,e[4]):(e=h.exec(t))?A(e[1],e[2]/100,e[3]/100,1):(e=p.exec(t))?A(e[1],e[2]/100,e[3]/100,e[4]):d.hasOwnProperty(t)?y(d[t]):"transparent"===t?new w(NaN,NaN,NaN,0):null}function y(t){return new w(t>>16&255,t>>8&255,255&t,1)}function x(t,e,r,n){return n<=0&&(t=e=r=NaN),new w(t,e,r,n)}function b(t){return t instanceof n||(t=v(t)),t?new w((t=t.rgb()).r,t.g,t.b,t.opacity):new w}function _(t,e,r,n){return 1===arguments.length?b(t):new w(t,e,r,null==n?1:n)}function w(t,e,r,n){this.r=+t,this.g=+e,this.b=+r,this.opacity=+n}function T(){return"#"+M(this.r)+M(this.g)+M(this.b)}function k(){var t=this.opacity;return(1===(t=isNaN(t)?1:Math.max(0,Math.min(1,t)))?"rgb(":"rgba(")+Math.max(0,Math.min(255,Math.round(this.r)||0))+", "+Math.max(0,Math.min(255,Math.round(this.g)||0))+", "+Math.max(0,Math.min(255,Math.round(this.b)||0))+(1===t?")":", "+t+")")}function M(t){return((t=Math.max(0,Math.min(255,Math.round(t)||0)))<16?"0":"")+t.toString(16)}function A(t,e,r,n){return n<=0?t=e=r=NaN:r<=0||r>=1?t=e=NaN:e<=0&&(t=NaN),new C(t,e,r,n)}function S(t){if(t instanceof C)return new C(t.h,t.s,t.l,t.opacity);if(t instanceof n||(t=v(t)),!t)return new C;if(t instanceof C)return t;var e=(t=t.rgb()).r/255,r=t.g/255,i=t.b/255,a=Math.min(e,r,i),o=Math.max(e,r,i),s=NaN,l=o-a,c=(o+a)/2;return l?(s=e===o?(r-i)/l+6*(r<i):r===o?(i-e)/l+2:(e-r)/l+4,l/=c<.5?o+a:2-o-a,s*=60):l=c>0&&c<1?0:s,new C(s,l,c,t.opacity)}function E(t,e,r,n){return 1===arguments.length?S(t):new C(t,e,r,null==n?1:n)}function C(t,e,r,n){this.h=+t,this.s=+e,this.l=+r,this.opacity=+n}function L(t,e,r){return 255*(t<60?e+(r-e)*t/60:t<180?r:t<240?e+(r-e)*(240-t)/60:e)}e(n,v,{copy:function(t){return Object.assign(new this.constructor,this,t)},displayable:function(){return this.rgb().displayable()},hex:g,formatHex:g,formatHsl:function(){return S(this).formatHsl()},formatRgb:m,toString:m}),e(w,_,r(n,{brighter:function(t){return t=null==t?1/.7:Math.pow(1/.7,t),new w(this.r*t,this.g*t,this.b*t,this.opacity)},darker:function(t){return t=null==t?.7:Math.pow(.7,t),new w(this.r*t,this.g*t,this.b*t,this.opacity)},rgb:function(){return this},displayable:function(){return-.5<=this.r&&this.r<255.5&&-.5<=this.g&&this.g<255.5&&-.5<=this.b&&this.b<255.5&&0<=this.opacity&&this.opacity<=1},hex:T,formatHex:T,formatRgb:k,toString:k})),e(C,E,r(n,{brighter:function(t){return t=null==t?1/.7:Math.pow(1/.7,t),new C(this.h,this.s,this.l*t,this.opacity)},darker:function(t){return t=null==t?.7:Math.pow(.7,t),new C(this.h,this.s,this.l*t,this.opacity)},rgb:function(){var t=this.h%360+360*(this.h<0),e=isNaN(t)||isNaN(this.s)?0:this.s,r=this.l,n=r+(r<.5?r:1-r)*e,i=2*r-n;return new w(L(t>=240?t-240:t+120,i,n),L(t,i,n),L(t<120?t+240:t-120,i,n),this.opacity)},displayable:function(){return(0<=this.s&&this.s<=1||isNaN(this.s))&&0<=this.l&&this.l<=1&&0<=this.opacity&&this.opacity<=1},formatHsl:function(){var t=this.opacity;return(1===(t=isNaN(t)?1:Math.max(0,Math.min(1,t)))?"hsl(":"hsla(")+(this.h||0)+", "+100*(this.s||0)+"%, "+100*(this.l||0)+"%"+(1===t?")":", "+t+")")}}));var I=Math.PI/180,P=180/Math.PI,z=6/29,O=3*z*z;function D(t){if(t instanceof F)return new F(t.l,t.a,t.b,t.opacity);if(t instanceof H)return G(t);t instanceof w||(t=b(t));var e,r,n=U(t.r),i=U(t.g),a=U(t.b),o=B((.2225045*n+.7168786*i+.0606169*a)/1);return n===i&&i===a?e=r=o:(e=B((.4360747*n+.3850649*i+.1430804*a)/.96422),r=B((.0139322*n+.0971045*i+.7141733*a)/.82521)),new F(116*o-16,500*(e-o),200*(o-r),t.opacity)}function R(t,e,r,n){return 1===arguments.length?D(t):new F(t,e,r,null==n?1:n)}function F(t,e,r,n){this.l=+t,this.a=+e,this.b=+r,this.opacity=+n}function B(t){return t>.008856451679035631?Math.pow(t,1/3):t/O+4/29}function N(t){return t>z?t*t*t:O*(t-4/29)}function j(t){return 255*(t<=.0031308?12.92*t:1.055*Math.pow(t,1/2.4)-.055)}function U(t){return(t/=255)<=.04045?t/12.92:Math.pow((t+.055)/1.055,2.4)}function V(t){if(t instanceof H)return new H(t.h,t.c,t.l,t.opacity);if(t instanceof F||(t=D(t)),0===t.a&&0===t.b)return new H(NaN,0<t.l&&t.l<100?0:NaN,t.l,t.opacity);var e=Math.atan2(t.b,t.a)*P;return new H(e<0?e+360:e,Math.sqrt(t.a*t.a+t.b*t.b),t.l,t.opacity)}function q(t,e,r,n){return 1===arguments.length?V(t):new H(t,e,r,null==n?1:n)}function H(t,e,r,n){this.h=+t,this.c=+e,this.l=+r,this.opacity=+n}function G(t){if(isNaN(t.h))return new F(t.l,0,0,t.opacity);var e=t.h*I;return new F(t.l,Math.cos(e)*t.c,Math.sin(e)*t.c,t.opacity)}e(F,R,r(n,{brighter:function(t){return new F(this.l+18*(null==t?1:t),this.a,this.b,this.opacity)},darker:function(t){return new F(this.l-18*(null==t?1:t),this.a,this.b,this.opacity)},rgb:function(){var t=(this.l+16)/116,e=isNaN(this.a)?t:t+this.a/500,r=isNaN(this.b)?t:t-this.b/200;return new w(j(3.1338561*(e=.96422*N(e))-1.6168667*(t=1*N(t))-.4906146*(r=.82521*N(r))),j(-.9787684*e+1.9161415*t+.033454*r),j(.0719453*e-.2289914*t+1.4052427*r),this.opacity)}})),e(H,q,r(n,{brighter:function(t){return new H(this.h,this.c,this.l+18*(null==t?1:t),this.opacity)},darker:function(t){return new H(this.h,this.c,this.l-18*(null==t?1:t),this.opacity)},rgb:function(){return G(this).rgb()}}));var Y=-.14861,W=1.78277,X=-.29227,Z=-.90649,J=1.97294,K=J*Z,Q=J*W,$=W*X-Z*Y;function tt(t){if(t instanceof rt)return new rt(t.h,t.s,t.l,t.opacity);t instanceof w||(t=b(t));var e=t.r/255,r=t.g/255,n=t.b/255,i=($*n+K*e-Q*r)/($+K-Q),a=n-i,o=(J*(r-i)-X*a)/Z,s=Math.sqrt(o*o+a*a)/(J*i*(1-i)),l=s?Math.atan2(o,a)*P-120:NaN;return new rt(l<0?l+360:l,s,i,t.opacity)}function et(t,e,r,n){return 1===arguments.length?tt(t):new rt(t,e,r,null==n?1:n)}function rt(t,e,r,n){this.h=+t,this.s=+e,this.l=+r,this.opacity=+n}e(rt,et,r(n,{brighter:function(t){return t=null==t?1/.7:Math.pow(1/.7,t),new rt(this.h,this.s,this.l*t,this.opacity)},darker:function(t){return t=null==t?.7:Math.pow(.7,t),new rt(this.h,this.s,this.l*t,this.opacity)},rgb:function(){var t=isNaN(this.h)?0:(this.h+120)*I,e=+this.l,r=isNaN(this.s)?0:this.s*e*(1-e),n=Math.cos(t),i=Math.sin(t);return new w(255*(e+r*(Y*n+W*i)),255*(e+r*(X*n+Z*i)),255*(e+r*(J*n)),this.opacity)}})),t.color=v,t.cubehelix=et,t.gray=function(t,e){return new F(t,0,0,null==e?1:e)},t.hcl=q,t.hsl=E,t.lab=R,t.lch=function(t,e,r,n){return 1===arguments.length?V(t):new H(r,e,t,null==n?1:n)},t.rgb=_,Object.defineProperty(t,"__esModule",{value:!0})}))},{}],159:[function(t,e,r){!function(t,n){"object"==typeof r&&"undefined"!=typeof e?n(r):n((t=t||self).d3=t.d3||{})}(this,(function(t){"use strict";var e={value:function(){}};function r(){for(var t,e=0,r=arguments.length,i={};e<r;++e){if(!(t=arguments[e]+"")||t in i||/[\s.]/.test(t))throw new Error("illegal type: "+t);i[t]=[]}return new n(i)}function n(t){this._=t}function i(t,e){return t.trim().split(/^|\s+/).map((function(t){var r="",n=t.indexOf(".");if(n>=0&&(r=t.slice(n+1),t=t.slice(0,n)),t&&!e.hasOwnProperty(t))throw new Error("unknown type: "+t);return{type:t,name:r}}))}function a(t,e){for(var r,n=0,i=t.length;n<i;++n)if((r=t[n]).name===e)return r.value}function o(t,r,n){for(var i=0,a=t.length;i<a;++i)if(t[i].name===r){t[i]=e,t=t.slice(0,i).concat(t.slice(i+1));break}return null!=n&&t.push({name:r,value:n}),t}n.prototype=r.prototype={constructor:n,on:function(t,e){var r,n=this._,s=i(t+"",n),l=-1,c=s.length;if(!(arguments.length<2)){if(null!=e&&"function"!=typeof e)throw new Error("invalid callback: "+e);for(;++l<c;)if(r=(t=s[l]).type)n[r]=o(n[r],t.name,e);else if(null==e)for(r in n)n[r]=o(n[r],t.name,null);return this}for(;++l<c;)if((r=(t=s[l]).type)&&(r=a(n[r],t.name)))return r},copy:function(){var t={},e=this._;for(var r in e)t[r]=e[r].slice();return new n(t)},call:function(t,e){if((r=arguments.length-2)>0)for(var r,n,i=new Array(r),a=0;a<r;++a)i[a]=arguments[a+2];if(!this._.hasOwnProperty(t))throw new Error("unknown type: "+t);for(a=0,r=(n=this._[t]).length;a<r;++a)n[a].value.apply(e,i)},apply:function(t,e,r){if(!this._.hasOwnProperty(t))throw new Error("unknown type: "+t);for(var n=this._[t],i=0,a=n.length;i<a;++i)n[i].value.apply(e,r)}},t.dispatch=r,Object.defineProperty(t,"__esModule",{value:!0})}))},{}],160:[function(t,e,r){!function(n,i){"object"==typeof r&&"undefined"!=typeof e?i(r,t("d3-quadtree"),t("d3-collection"),t("d3-dispatch"),t("d3-timer")):i(n.d3=n.d3||{},n.d3,n.d3,n.d3,n.d3)}(this,(function(t,e,r,n,i){"use strict";function a(t){return function(){return t}}function o(){return 1e-6*(Math.random()-.5)}function s(t){return t.x+t.vx}function l(t){return t.y+t.vy}function c(t){return t.index}function u(t,e){var r=t.get(e);if(!r)throw new Error("missing: "+e);return r}function f(t){return t.x}function h(t){return t.y}var p=Math.PI*(3-Math.sqrt(5));t.forceCenter=function(t,e){var r;function n(){var n,i,a=r.length,o=0,s=0;for(n=0;n<a;++n)o+=(i=r[n]).x,s+=i.y;for(o=o/a-t,s=s/a-e,n=0;n<a;++n)(i=r[n]).x-=o,i.y-=s}return null==t&&(t=0),null==e&&(e=0),n.initialize=function(t){r=t},n.x=function(e){return arguments.length?(t=+e,n):t},n.y=function(t){return arguments.length?(e=+t,n):e},n},t.forceCollide=function(t){var r,n,i=1,c=1;function u(){for(var t,a,u,h,p,d,g,m=r.length,v=0;v<c;++v)for(a=e.quadtree(r,s,l).visitAfter(f),t=0;t<m;++t)u=r[t],d=n[u.index],g=d*d,h=u.x+u.vx,p=u.y+u.vy,a.visit(y);function y(t,e,r,n,a){var s=t.data,l=t.r,c=d+l;if(!s)return e>h+c||n<h-c||r>p+c||a<p-c;if(s.index>u.index){var f=h-s.x-s.vx,m=p-s.y-s.vy,v=f*f+m*m;v<c*c&&(0===f&&(v+=(f=o())*f),0===m&&(v+=(m=o())*m),v=(c-(v=Math.sqrt(v)))/v*i,u.vx+=(f*=v)*(c=(l*=l)/(g+l)),u.vy+=(m*=v)*c,s.vx-=f*(c=1-c),s.vy-=m*c)}}}function f(t){if(t.data)return t.r=n[t.data.index];for(var e=t.r=0;e<4;++e)t[e]&&t[e].r>t.r&&(t.r=t[e].r)}function h(){if(r){var e,i,a=r.length;for(n=new Array(a),e=0;e<a;++e)i=r[e],n[i.index]=+t(i,e,r)}}return"function"!=typeof t&&(t=a(null==t?1:+t)),u.initialize=function(t){r=t,h()},u.iterations=function(t){return arguments.length?(c=+t,u):c},u.strength=function(t){return arguments.length?(i=+t,u):i},u.radius=function(e){return arguments.length?(t="function"==typeof e?e:a(+e),h(),u):t},u},t.forceLink=function(t){var e,n,i,s,l,f=c,h=function(t){return 1/Math.min(s[t.source.index],s[t.target.index])},p=a(30),d=1;function g(r){for(var i=0,a=t.length;i<d;++i)for(var s,c,u,f,h,p,g,m=0;m<a;++m)c=(s=t[m]).source,f=(u=s.target).x+u.vx-c.x-c.vx||o(),h=u.y+u.vy-c.y-c.vy||o(),f*=p=((p=Math.sqrt(f*f+h*h))-n[m])/p*r*e[m],h*=p,u.vx-=f*(g=l[m]),u.vy-=h*g,c.vx+=f*(g=1-g),c.vy+=h*g}function m(){if(i){var a,o,c=i.length,h=t.length,p=r.map(i,f);for(a=0,s=new Array(c);a<h;++a)(o=t[a]).index=a,"object"!=typeof o.source&&(o.source=u(p,o.source)),"object"!=typeof o.target&&(o.target=u(p,o.target)),s[o.source.index]=(s[o.source.index]||0)+1,s[o.target.index]=(s[o.target.index]||0)+1;for(a=0,l=new Array(h);a<h;++a)o=t[a],l[a]=s[o.source.index]/(s[o.source.index]+s[o.target.index]);e=new Array(h),v(),n=new Array(h),y()}}function v(){if(i)for(var r=0,n=t.length;r<n;++r)e[r]=+h(t[r],r,t)}function y(){if(i)for(var e=0,r=t.length;e<r;++e)n[e]=+p(t[e],e,t)}return null==t&&(t=[]),g.initialize=function(t){i=t,m()},g.links=function(e){return arguments.length?(t=e,m(),g):t},g.id=function(t){return arguments.length?(f=t,g):f},g.iterations=function(t){return arguments.length?(d=+t,g):d},g.strength=function(t){return arguments.length?(h="function"==typeof t?t:a(+t),v(),g):h},g.distance=function(t){return arguments.length?(p="function"==typeof t?t:a(+t),y(),g):p},g},t.forceManyBody=function(){var t,r,n,i,s=a(-30),l=1,c=1/0,u=.81;function p(i){var a,o=t.length,s=e.quadtree(t,f,h).visitAfter(g);for(n=i,a=0;a<o;++a)r=t[a],s.visit(m)}function d(){if(t){var e,r,n=t.length;for(i=new Array(n),e=0;e<n;++e)r=t[e],i[r.index]=+s(r,e,t)}}function g(t){var e,r,n,a,o,s=0,l=0;if(t.length){for(n=a=o=0;o<4;++o)(e=t[o])&&(r=Math.abs(e.value))&&(s+=e.value,l+=r,n+=r*e.x,a+=r*e.y);t.x=n/l,t.y=a/l}else{(e=t).x=e.data.x,e.y=e.data.y;do{s+=i[e.data.index]}while(e=e.next)}t.value=s}function m(t,e,a,s){if(!t.value)return!0;var f=t.x-r.x,h=t.y-r.y,p=s-e,d=f*f+h*h;if(p*p/u<d)return d<c&&(0===f&&(d+=(f=o())*f),0===h&&(d+=(h=o())*h),d<l&&(d=Math.sqrt(l*d)),r.vx+=f*t.value*n/d,r.vy+=h*t.value*n/d),!0;if(!(t.length||d>=c)){(t.data!==r||t.next)&&(0===f&&(d+=(f=o())*f),0===h&&(d+=(h=o())*h),d<l&&(d=Math.sqrt(l*d)));do{t.data!==r&&(p=i[t.data.index]*n/d,r.vx+=f*p,r.vy+=h*p)}while(t=t.next)}}return p.initialize=function(e){t=e,d()},p.strength=function(t){return arguments.length?(s="function"==typeof t?t:a(+t),d(),p):s},p.distanceMin=function(t){return arguments.length?(l=t*t,p):Math.sqrt(l)},p.distanceMax=function(t){return arguments.length?(c=t*t,p):Math.sqrt(c)},p.theta=function(t){return arguments.length?(u=t*t,p):Math.sqrt(u)},p},t.forceRadial=function(t,e,r){var n,i,o,s=a(.1);function l(t){for(var a=0,s=n.length;a<s;++a){var l=n[a],c=l.x-e||1e-6,u=l.y-r||1e-6,f=Math.sqrt(c*c+u*u),h=(o[a]-f)*i[a]*t/f;l.vx+=c*h,l.vy+=u*h}}function c(){if(n){var e,r=n.length;for(i=new Array(r),o=new Array(r),e=0;e<r;++e)o[e]=+t(n[e],e,n),i[e]=isNaN(o[e])?0:+s(n[e],e,n)}}return"function"!=typeof t&&(t=a(+t)),null==e&&(e=0),null==r&&(r=0),l.initialize=function(t){n=t,c()},l.strength=function(t){return arguments.length?(s="function"==typeof t?t:a(+t),c(),l):s},l.radius=function(e){return arguments.length?(t="function"==typeof e?e:a(+e),c(),l):t},l.x=function(t){return arguments.length?(e=+t,l):e},l.y=function(t){return arguments.length?(r=+t,l):r},l},t.forceSimulation=function(t){var e,a=1,o=.001,s=1-Math.pow(o,1/300),l=0,c=.6,u=r.map(),f=i.timer(d),h=n.dispatch("tick","end");function d(){g(),h.call("tick",e),a<o&&(f.stop(),h.call("end",e))}function g(r){var n,i,o=t.length;void 0===r&&(r=1);for(var f=0;f<r;++f)for(a+=(l-a)*s,u.each((function(t){t(a)})),n=0;n<o;++n)null==(i=t[n]).fx?i.x+=i.vx*=c:(i.x=i.fx,i.vx=0),null==i.fy?i.y+=i.vy*=c:(i.y=i.fy,i.vy=0);return e}function m(){for(var e,r=0,n=t.length;r<n;++r){if((e=t[r]).index=r,null!=e.fx&&(e.x=e.fx),null!=e.fy&&(e.y=e.fy),isNaN(e.x)||isNaN(e.y)){var i=10*Math.sqrt(r),a=r*p;e.x=i*Math.cos(a),e.y=i*Math.sin(a)}(isNaN(e.vx)||isNaN(e.vy))&&(e.vx=e.vy=0)}}function v(e){return e.initialize&&e.initialize(t),e}return null==t&&(t=[]),m(),e={tick:g,restart:function(){return f.restart(d),e},stop:function(){return f.stop(),e},nodes:function(r){return arguments.length?(t=r,m(),u.each(v),e):t},alpha:function(t){return arguments.length?(a=+t,e):a},alphaMin:function(t){return arguments.length?(o=+t,e):o},alphaDecay:function(t){return arguments.length?(s=+t,e):+s},alphaTarget:function(t){return arguments.length?(l=+t,e):l},velocityDecay:function(t){return arguments.length?(c=1-t,e):1-c},force:function(t,r){return arguments.length>1?(null==r?u.remove(t):u.set(t,v(r)),e):u.get(t)},find:function(e,r,n){var i,a,o,s,l,c=0,u=t.length;for(null==n?n=1/0:n*=n,c=0;c<u;++c)(o=(i=e-(s=t[c]).x)*i+(a=r-s.y)*a)<n&&(l=s,n=o);return l},on:function(t,r){return arguments.length>1?(h.on(t,r),e):h.on(t)}}},t.forceX=function(t){var e,r,n,i=a(.1);function o(t){for(var i,a=0,o=e.length;a<o;++a)(i=e[a]).vx+=(n[a]-i.x)*r[a]*t}function s(){if(e){var a,o=e.length;for(r=new Array(o),n=new Array(o),a=0;a<o;++a)r[a]=isNaN(n[a]=+t(e[a],a,e))?0:+i(e[a],a,e)}}return"function"!=typeof t&&(t=a(null==t?0:+t)),o.initialize=function(t){e=t,s()},o.strength=function(t){return arguments.length?(i="function"==typeof t?t:a(+t),s(),o):i},o.x=function(e){return arguments.length?(t="function"==typeof e?e:a(+e),s(),o):t},o},t.forceY=function(t){var e,r,n,i=a(.1);function o(t){for(var i,a=0,o=e.length;a<o;++a)(i=e[a]).vy+=(n[a]-i.y)*r[a]*t}function s(){if(e){var a,o=e.length;for(r=new Array(o),n=new Array(o),a=0;a<o;++a)r[a]=isNaN(n[a]=+t(e[a],a,e))?0:+i(e[a],a,e)}}return"function"!=typeof t&&(t=a(null==t?0:+t)),o.initialize=function(t){e=t,s()},o.strength=function(t){return arguments.length?(i="function"==typeof t?t:a(+t),s(),o):i},o.y=function(e){return arguments.length?(t="function"==typeof e?e:a(+e),s(),o):t},o},Object.defineProperty(t,"__esModule",{value:!0})}))},{"d3-collection":157,"d3-dispatch":159,"d3-quadtree":164,"d3-timer":168}],161:[function(t,e,r){!function(t,n){"object"==typeof r&&"undefined"!=typeof e?n(r):n((t=t||self).d3=t.d3||{})}(this,(function(t){"use strict";function e(t,e){return t.parent===e.parent?1:2}function r(t,e){return t+e.x}function n(t,e){return Math.max(t,e.y)}function i(t){var e=0,r=t.children,n=r&&r.length;if(n)for(;--n>=0;)e+=r[n].value;else e=1;t.value=e}function a(t,e){var r,n,i,a,s,u=new c(t),f=+t.value&&(u.value=t.value),h=[u];for(null==e&&(e=o);r=h.pop();)if(f&&(r.value=+r.data.value),(i=e(r.data))&&(s=i.length))for(r.children=new Array(s),a=s-1;a>=0;--a)h.push(n=r.children[a]=new c(i[a])),n.parent=r,n.depth=r.depth+1;return u.eachBefore(l)}function o(t){return t.children}function s(t){t.data=t.data.data}function l(t){var e=0;do{t.height=e}while((t=t.parent)&&t.height<++e)}function c(t){this.data=t,this.depth=this.height=0,this.parent=null}c.prototype=a.prototype={constructor:c,count:function(){return this.eachAfter(i)},each:function(t){var e,r,n,i,a=this,o=[a];do{for(e=o.reverse(),o=[];a=e.pop();)if(t(a),r=a.children)for(n=0,i=r.length;n<i;++n)o.push(r[n])}while(o.length);return this},eachAfter:function(t){for(var e,r,n,i=this,a=[i],o=[];i=a.pop();)if(o.push(i),e=i.children)for(r=0,n=e.length;r<n;++r)a.push(e[r]);for(;i=o.pop();)t(i);return this},eachBefore:function(t){for(var e,r,n=this,i=[n];n=i.pop();)if(t(n),e=n.children)for(r=e.length-1;r>=0;--r)i.push(e[r]);return this},sum:function(t){return this.eachAfter((function(e){for(var r=+t(e.data)||0,n=e.children,i=n&&n.length;--i>=0;)r+=n[i].value;e.value=r}))},sort:function(t){return this.eachBefore((function(e){e.children&&e.children.sort(t)}))},path:function(t){for(var e=this,r=function(t,e){if(t===e)return t;var r=t.ancestors(),n=e.ancestors(),i=null;t=r.pop(),e=n.pop();for(;t===e;)i=t,t=r.pop(),e=n.pop();return i}(e,t),n=[e];e!==r;)e=e.parent,n.push(e);for(var i=n.length;t!==r;)n.splice(i,0,t),t=t.parent;return n},ancestors:function(){for(var t=this,e=[t];t=t.parent;)e.push(t);return e},descendants:function(){var t=[];return this.each((function(e){t.push(e)})),t},leaves:function(){var t=[];return this.eachBefore((function(e){e.children||t.push(e)})),t},links:function(){var t=this,e=[];return t.each((function(r){r!==t&&e.push({source:r.parent,target:r})})),e},copy:function(){return a(this).eachBefore(s)}};var u=Array.prototype.slice;function f(t){for(var e,r,n=0,i=(t=function(t){for(var e,r,n=t.length;n;)r=Math.random()*n--|0,e=t[n],t[n]=t[r],t[r]=e;return t}(u.call(t))).length,a=[];n<i;)e=t[n],r&&d(r,e)?++n:(r=m(a=h(a,e)),n=0);return r}function h(t,e){var r,n;if(g(e,t))return[e];for(r=0;r<t.length;++r)if(p(e,t[r])&&g(v(t[r],e),t))return[t[r],e];for(r=0;r<t.length-1;++r)for(n=r+1;n<t.length;++n)if(p(v(t[r],t[n]),e)&&p(v(t[r],e),t[n])&&p(v(t[n],e),t[r])&&g(y(t[r],t[n],e),t))return[t[r],t[n],e];throw new Error}function p(t,e){var r=t.r-e.r,n=e.x-t.x,i=e.y-t.y;return r<0||r*r<n*n+i*i}function d(t,e){var r=t.r-e.r+1e-6,n=e.x-t.x,i=e.y-t.y;return r>0&&r*r>n*n+i*i}function g(t,e){for(var r=0;r<e.length;++r)if(!d(t,e[r]))return!1;return!0}function m(t){switch(t.length){case 1:return{x:(e=t[0]).x,y:e.y,r:e.r};case 2:return v(t[0],t[1]);case 3:return y(t[0],t[1],t[2])}var e}function v(t,e){var r=t.x,n=t.y,i=t.r,a=e.x,o=e.y,s=e.r,l=a-r,c=o-n,u=s-i,f=Math.sqrt(l*l+c*c);return{x:(r+a+l/f*u)/2,y:(n+o+c/f*u)/2,r:(f+i+s)/2}}function y(t,e,r){var n=t.x,i=t.y,a=t.r,o=e.x,s=e.y,l=e.r,c=r.x,u=r.y,f=r.r,h=n-o,p=n-c,d=i-s,g=i-u,m=l-a,v=f-a,y=n*n+i*i-a*a,x=y-o*o-s*s+l*l,b=y-c*c-u*u+f*f,_=p*d-h*g,w=(d*b-g*x)/(2*_)-n,T=(g*m-d*v)/_,k=(p*x-h*b)/(2*_)-i,M=(h*v-p*m)/_,A=T*T+M*M-1,S=2*(a+w*T+k*M),E=w*w+k*k-a*a,C=-(A?(S+Math.sqrt(S*S-4*A*E))/(2*A):E/S);return{x:n+w+T*C,y:i+k+M*C,r:C}}function x(t,e,r){var n,i,a,o,s=t.x-e.x,l=t.y-e.y,c=s*s+l*l;c?(i=e.r+r.r,i*=i,o=t.r+r.r,i>(o*=o)?(n=(c+o-i)/(2*c),a=Math.sqrt(Math.max(0,o/c-n*n)),r.x=t.x-n*s-a*l,r.y=t.y-n*l+a*s):(n=(c+i-o)/(2*c),a=Math.sqrt(Math.max(0,i/c-n*n)),r.x=e.x+n*s-a*l,r.y=e.y+n*l+a*s)):(r.x=e.x+r.r,r.y=e.y)}function b(t,e){var r=t.r+e.r-1e-6,n=e.x-t.x,i=e.y-t.y;return r>0&&r*r>n*n+i*i}function _(t){var e=t._,r=t.next._,n=e.r+r.r,i=(e.x*r.r+r.x*e.r)/n,a=(e.y*r.r+r.y*e.r)/n;return i*i+a*a}function w(t){this._=t,this.next=null,this.previous=null}function T(t){if(!(i=t.length))return 0;var e,r,n,i,a,o,s,l,c,u,h;if((e=t[0]).x=0,e.y=0,!(i>1))return e.r;if(r=t[1],e.x=-r.r,r.x=e.r,r.y=0,!(i>2))return e.r+r.r;x(r,e,n=t[2]),e=new w(e),r=new w(r),n=new w(n),e.next=n.previous=r,r.next=e.previous=n,n.next=r.previous=e;t:for(s=3;s<i;++s){x(e._,r._,n=t[s]),n=new w(n),l=r.next,c=e.previous,u=r._.r,h=e._.r;do{if(u<=h){if(b(l._,n._)){r=l,e.next=r,r.previous=e,--s;continue t}u+=l._.r,l=l.next}else{if(b(c._,n._)){(e=c).next=r,r.previous=e,--s;continue t}h+=c._.r,c=c.previous}}while(l!==c.next);for(n.previous=e,n.next=r,e.next=r.previous=r=n,a=_(e);(n=n.next)!==r;)(o=_(n))<a&&(e=n,a=o);r=e.next}for(e=[r._],n=r;(n=n.next)!==r;)e.push(n._);for(n=f(e),s=0;s<i;++s)(e=t[s]).x-=n.x,e.y-=n.y;return n.r}function k(t){return null==t?null:M(t)}function M(t){if("function"!=typeof t)throw new Error;return t}function A(){return 0}function S(t){return function(){return t}}function E(t){return Math.sqrt(t.value)}function C(t){return function(e){e.children||(e.r=Math.max(0,+t(e)||0))}}function L(t,e){return function(r){if(n=r.children){var n,i,a,o=n.length,s=t(r)*e||0;if(s)for(i=0;i<o;++i)n[i].r+=s;if(a=T(n),s)for(i=0;i<o;++i)n[i].r-=s;r.r=a+s}}}function I(t){return function(e){var r=e.parent;e.r*=t,r&&(e.x=r.x+t*e.x,e.y=r.y+t*e.y)}}function P(t){t.x0=Math.round(t.x0),t.y0=Math.round(t.y0),t.x1=Math.round(t.x1),t.y1=Math.round(t.y1)}function z(t,e,r,n,i){for(var a,o=t.children,s=-1,l=o.length,c=t.value&&(n-e)/t.value;++s<l;)(a=o[s]).y0=r,a.y1=i,a.x0=e,a.x1=e+=a.value*c}var O={depth:-1},D={};function R(t){return t.id}function F(t){return t.parentId}function B(t,e){return t.parent===e.parent?1:2}function N(t){var e=t.children;return e?e[0]:t.t}function j(t){var e=t.children;return e?e[e.length-1]:t.t}function U(t,e,r){var n=r/(e.i-t.i);e.c-=n,e.s+=r,t.c+=n,e.z+=r,e.m+=r}function V(t,e,r){return t.a.parent===e.parent?t.a:r}function q(t,e){this._=t,this.parent=null,this.children=null,this.A=null,this.a=this,this.z=0,this.m=0,this.c=0,this.s=0,this.t=null,this.i=e}function H(t,e,r,n,i){for(var a,o=t.children,s=-1,l=o.length,c=t.value&&(i-r)/t.value;++s<l;)(a=o[s]).x0=e,a.x1=n,a.y0=r,a.y1=r+=a.value*c}q.prototype=Object.create(c.prototype);var G=(1+Math.sqrt(5))/2;function Y(t,e,r,n,i,a){for(var o,s,l,c,u,f,h,p,d,g,m,v=[],y=e.children,x=0,b=0,_=y.length,w=e.value;x<_;){l=i-r,c=a-n;do{u=y[b++].value}while(!u&&b<_);for(f=h=u,m=u*u*(g=Math.max(c/l,l/c)/(w*t)),d=Math.max(h/m,m/f);b<_;++b){if(u+=s=y[b].value,s<f&&(f=s),s>h&&(h=s),m=u*u*g,(p=Math.max(h/m,m/f))>d){u-=s;break}d=p}v.push(o={value:u,dice:l<c,children:y.slice(x,b)}),o.dice?z(o,r,n,i,w?n+=c*u/w:a):H(o,r,n,w?r+=l*u/w:i,a),w-=u,x=b}return v}var W=function t(e){function r(t,r,n,i,a){Y(e,t,r,n,i,a)}return r.ratio=function(e){return t((e=+e)>1?e:1)},r}(G);var X=function t(e){function r(t,r,n,i,a){if((o=t._squarify)&&o.ratio===e)for(var o,s,l,c,u,f=-1,h=o.length,p=t.value;++f<h;){for(l=(s=o[f]).children,c=s.value=0,u=l.length;c<u;++c)s.value+=l[c].value;s.dice?z(s,r,n,i,n+=(a-n)*s.value/p):H(s,r,n,r+=(i-r)*s.value/p,a),p-=s.value}else t._squarify=o=Y(e,t,r,n,i,a),o.ratio=e}return r.ratio=function(e){return t((e=+e)>1?e:1)},r}(G);t.cluster=function(){var t=e,i=1,a=1,o=!1;function s(e){var s,l=0;e.eachAfter((function(e){var i=e.children;i?(e.x=function(t){return t.reduce(r,0)/t.length}(i),e.y=function(t){return 1+t.reduce(n,0)}(i)):(e.x=s?l+=t(e,s):0,e.y=0,s=e)}));var c=function(t){for(var e;e=t.children;)t=e[0];return t}(e),u=function(t){for(var e;e=t.children;)t=e[e.length-1];return t}(e),f=c.x-t(c,u)/2,h=u.x+t(u,c)/2;return e.eachAfter(o?function(t){t.x=(t.x-e.x)*i,t.y=(e.y-t.y)*a}:function(t){t.x=(t.x-f)/(h-f)*i,t.y=(1-(e.y?t.y/e.y:1))*a})}return s.separation=function(e){return arguments.length?(t=e,s):t},s.size=function(t){return arguments.length?(o=!1,i=+t[0],a=+t[1],s):o?null:[i,a]},s.nodeSize=function(t){return arguments.length?(o=!0,i=+t[0],a=+t[1],s):o?[i,a]:null},s},t.hierarchy=a,t.pack=function(){var t=null,e=1,r=1,n=A;function i(i){return i.x=e/2,i.y=r/2,t?i.eachBefore(C(t)).eachAfter(L(n,.5)).eachBefore(I(1)):i.eachBefore(C(E)).eachAfter(L(A,1)).eachAfter(L(n,i.r/Math.min(e,r))).eachBefore(I(Math.min(e,r)/(2*i.r))),i}return i.radius=function(e){return arguments.length?(t=k(e),i):t},i.size=function(t){return arguments.length?(e=+t[0],r=+t[1],i):[e,r]},i.padding=function(t){return arguments.length?(n="function"==typeof t?t:S(+t),i):n},i},t.packEnclose=f,t.packSiblings=function(t){return T(t),t},t.partition=function(){var t=1,e=1,r=0,n=!1;function i(i){var a=i.height+1;return i.x0=i.y0=r,i.x1=t,i.y1=e/a,i.eachBefore(function(t,e){return function(n){n.children&&z(n,n.x0,t*(n.depth+1)/e,n.x1,t*(n.depth+2)/e);var i=n.x0,a=n.y0,o=n.x1-r,s=n.y1-r;o<i&&(i=o=(i+o)/2),s<a&&(a=s=(a+s)/2),n.x0=i,n.y0=a,n.x1=o,n.y1=s}}(e,a)),n&&i.eachBefore(P),i}return i.round=function(t){return arguments.length?(n=!!t,i):n},i.size=function(r){return arguments.length?(t=+r[0],e=+r[1],i):[t,e]},i.padding=function(t){return arguments.length?(r=+t,i):r},i},t.stratify=function(){var t=R,e=F;function r(r){var n,i,a,o,s,u,f,h=r.length,p=new Array(h),d={};for(i=0;i<h;++i)n=r[i],s=p[i]=new c(n),null!=(u=t(n,i,r))&&(u+="")&&(d[f="$"+(s.id=u)]=f in d?D:s);for(i=0;i<h;++i)if(s=p[i],null!=(u=e(r[i],i,r))&&(u+="")){if(!(o=d["$"+u]))throw new Error("missing: "+u);if(o===D)throw new Error("ambiguous: "+u);o.children?o.children.push(s):o.children=[s],s.parent=o}else{if(a)throw new Error("multiple roots");a=s}if(!a)throw new Error("no root");if(a.parent=O,a.eachBefore((function(t){t.depth=t.parent.depth+1,--h})).eachBefore(l),a.parent=null,h>0)throw new Error("cycle");return a}return r.id=function(e){return arguments.length?(t=M(e),r):t},r.parentId=function(t){return arguments.length?(e=M(t),r):e},r},t.tree=function(){var t=B,e=1,r=1,n=null;function i(i){var l=function(t){for(var e,r,n,i,a,o=new q(t,0),s=[o];e=s.pop();)if(n=e._.children)for(e.children=new Array(a=n.length),i=a-1;i>=0;--i)s.push(r=e.children[i]=new q(n[i],i)),r.parent=e;return(o.parent=new q(null,0)).children=[o],o}(i);if(l.eachAfter(a),l.parent.m=-l.z,l.eachBefore(o),n)i.eachBefore(s);else{var c=i,u=i,f=i;i.eachBefore((function(t){t.x<c.x&&(c=t),t.x>u.x&&(u=t),t.depth>f.depth&&(f=t)}));var h=c===u?1:t(c,u)/2,p=h-c.x,d=e/(u.x+h+p),g=r/(f.depth||1);i.eachBefore((function(t){t.x=(t.x+p)*d,t.y=t.depth*g}))}return i}function a(e){var r=e.children,n=e.parent.children,i=e.i?n[e.i-1]:null;if(r){!function(t){for(var e,r=0,n=0,i=t.children,a=i.length;--a>=0;)(e=i[a]).z+=r,e.m+=r,r+=e.s+(n+=e.c)}(e);var a=(r[0].z+r[r.length-1].z)/2;i?(e.z=i.z+t(e._,i._),e.m=e.z-a):e.z=a}else i&&(e.z=i.z+t(e._,i._));e.parent.A=function(e,r,n){if(r){for(var i,a=e,o=e,s=r,l=a.parent.children[0],c=a.m,u=o.m,f=s.m,h=l.m;s=j(s),a=N(a),s&&a;)l=N(l),(o=j(o)).a=e,(i=s.z+f-a.z-c+t(s._,a._))>0&&(U(V(s,e,n),e,i),c+=i,u+=i),f+=s.m,c+=a.m,h+=l.m,u+=o.m;s&&!j(o)&&(o.t=s,o.m+=f-u),a&&!N(l)&&(l.t=a,l.m+=c-h,n=e)}return n}(e,i,e.parent.A||n[0])}function o(t){t._.x=t.z+t.parent.m,t.m+=t.parent.m}function s(t){t.x*=e,t.y=t.depth*r}return i.separation=function(e){return arguments.length?(t=e,i):t},i.size=function(t){return arguments.length?(n=!1,e=+t[0],r=+t[1],i):n?null:[e,r]},i.nodeSize=function(t){return arguments.length?(n=!0,e=+t[0],r=+t[1],i):n?[e,r]:null},i},t.treemap=function(){var t=W,e=!1,r=1,n=1,i=[0],a=A,o=A,s=A,l=A,c=A;function u(t){return t.x0=t.y0=0,t.x1=r,t.y1=n,t.eachBefore(f),i=[0],e&&t.eachBefore(P),t}function f(e){var r=i[e.depth],n=e.x0+r,u=e.y0+r,f=e.x1-r,h=e.y1-r;f<n&&(n=f=(n+f)/2),h<u&&(u=h=(u+h)/2),e.x0=n,e.y0=u,e.x1=f,e.y1=h,e.children&&(r=i[e.depth+1]=a(e)/2,n+=c(e)-r,u+=o(e)-r,(f-=s(e)-r)<n&&(n=f=(n+f)/2),(h-=l(e)-r)<u&&(u=h=(u+h)/2),t(e,n,u,f,h))}return u.round=function(t){return arguments.length?(e=!!t,u):e},u.size=function(t){return arguments.length?(r=+t[0],n=+t[1],u):[r,n]},u.tile=function(e){return arguments.length?(t=M(e),u):t},u.padding=function(t){return arguments.length?u.paddingInner(t).paddingOuter(t):u.paddingInner()},u.paddingInner=function(t){return arguments.length?(a="function"==typeof t?t:S(+t),u):a},u.paddingOuter=function(t){return arguments.length?u.paddingTop(t).paddingRight(t).paddingBottom(t).paddingLeft(t):u.paddingTop()},u.paddingTop=function(t){return arguments.length?(o="function"==typeof t?t:S(+t),u):o},u.paddingRight=function(t){return arguments.length?(s="function"==typeof t?t:S(+t),u):s},u.paddingBottom=function(t){return arguments.length?(l="function"==typeof t?t:S(+t),u):l},u.paddingLeft=function(t){return arguments.length?(c="function"==typeof t?t:S(+t),u):c},u},t.treemapBinary=function(t,e,r,n,i){var a,o,s=t.children,l=s.length,c=new Array(l+1);for(c[0]=o=a=0;a<l;++a)c[a+1]=o+=s[a].value;!function t(e,r,n,i,a,o,l){if(e>=r-1){var u=s[e];return u.x0=i,u.y0=a,u.x1=o,void(u.y1=l)}var f=c[e],h=n/2+f,p=e+1,d=r-1;for(;p<d;){var g=p+d>>>1;c[g]<h?p=g+1:d=g}h-c[p-1]<c[p]-h&&e+1<p&&--p;var m=c[p]-f,v=n-m;if(o-i>l-a){var y=(i*v+o*m)/n;t(e,p,m,i,a,y,l),t(p,r,v,y,a,o,l)}else{var x=(a*v+l*m)/n;t(e,p,m,i,a,o,x),t(p,r,v,i,x,o,l)}}(0,l,t.value,e,r,n,i)},t.treemapDice=z,t.treemapResquarify=X,t.treemapSlice=H,t.treemapSliceDice=function(t,e,r,n,i){(1&t.depth?H:z)(t,e,r,n,i)},t.treemapSquarify=W,Object.defineProperty(t,"__esModule",{value:!0})}))},{}],162:[function(t,e,r){!function(n,i){"object"==typeof r&&"undefined"!=typeof e?i(r,t("d3-color")):i((n=n||self).d3=n.d3||{},n.d3)}(this,(function(t,e){"use strict";function r(t,e,r,n,i){var a=t*t,o=a*t;return((1-3*t+3*a-o)*e+(4-6*a+3*o)*r+(1+3*t+3*a-3*o)*n+o*i)/6}function n(t){var e=t.length-1;return function(n){var i=n<=0?n=0:n>=1?(n=1,e-1):Math.floor(n*e),a=t[i],o=t[i+1],s=i>0?t[i-1]:2*a-o,l=i<e-1?t[i+2]:2*o-a;return r((n-i/e)*e,s,a,o,l)}}function i(t){var e=t.length;return function(n){var i=Math.floor(((n%=1)<0?++n:n)*e),a=t[(i+e-1)%e],o=t[i%e],s=t[(i+1)%e],l=t[(i+2)%e];return r((n-i/e)*e,a,o,s,l)}}function a(t){return function(){return t}}function o(t,e){return function(r){return t+r*e}}function s(t,e){var r=e-t;return r?o(t,r>180||r<-180?r-360*Math.round(r/360):r):a(isNaN(t)?e:t)}function l(t){return 1==(t=+t)?c:function(e,r){return r-e?function(t,e,r){return t=Math.pow(t,r),e=Math.pow(e,r)-t,r=1/r,function(n){return Math.pow(t+n*e,r)}}(e,r,t):a(isNaN(e)?r:e)}}function c(t,e){var r=e-t;return r?o(t,r):a(isNaN(t)?e:t)}var u=function t(r){var n=l(r);function i(t,r){var i=n((t=e.rgb(t)).r,(r=e.rgb(r)).r),a=n(t.g,r.g),o=n(t.b,r.b),s=c(t.opacity,r.opacity);return function(e){return t.r=i(e),t.g=a(e),t.b=o(e),t.opacity=s(e),t+""}}return i.gamma=t,i}(1);function f(t){return function(r){var n,i,a=r.length,o=new Array(a),s=new Array(a),l=new Array(a);for(n=0;n<a;++n)i=e.rgb(r[n]),o[n]=i.r||0,s[n]=i.g||0,l[n]=i.b||0;return o=t(o),s=t(s),l=t(l),i.opacity=1,function(t){return i.r=o(t),i.g=s(t),i.b=l(t),i+""}}}var h=f(n),p=f(i);function d(t,e){e||(e=[]);var r,n=t?Math.min(e.length,t.length):0,i=e.slice();return function(a){for(r=0;r<n;++r)i[r]=t[r]*(1-a)+e[r]*a;return i}}function g(t){return ArrayBuffer.isView(t)&&!(t instanceof DataView)}function m(t,e){var r,n=e?e.length:0,i=t?Math.min(n,t.length):0,a=new Array(i),o=new Array(n);for(r=0;r<i;++r)a[r]=T(t[r],e[r]);for(;r<n;++r)o[r]=e[r];return function(t){for(r=0;r<i;++r)o[r]=a[r](t);return o}}function v(t,e){var r=new Date;return t=+t,e=+e,function(n){return r.setTime(t*(1-n)+e*n),r}}function y(t,e){return t=+t,e=+e,function(r){return t*(1-r)+e*r}}function x(t,e){var r,n={},i={};for(r in null!==t&&"object"==typeof t||(t={}),null!==e&&"object"==typeof e||(e={}),e)r in t?n[r]=T(t[r],e[r]):i[r]=e[r];return function(t){for(r in n)i[r]=n[r](t);return i}}var b=/[-+]?(?:\d+\.?\d*|\.?\d+)(?:[eE][-+]?\d+)?/g,_=new RegExp(b.source,"g");function w(t,e){var r,n,i,a=b.lastIndex=_.lastIndex=0,o=-1,s=[],l=[];for(t+="",e+="";(r=b.exec(t))&&(n=_.exec(e));)(i=n.index)>a&&(i=e.slice(a,i),s[o]?s[o]+=i:s[++o]=i),(r=r[0])===(n=n[0])?s[o]?s[o]+=n:s[++o]=n:(s[++o]=null,l.push({i:o,x:y(r,n)})),a=_.lastIndex;return a<e.length&&(i=e.slice(a),s[o]?s[o]+=i:s[++o]=i),s.length<2?l[0]?function(t){return function(e){return t(e)+""}}(l[0].x):function(t){return function(){return t}}(e):(e=l.length,function(t){for(var r,n=0;n<e;++n)s[(r=l[n]).i]=r.x(t);return s.join("")})}function T(t,r){var n,i=typeof r;return null==r||"boolean"===i?a(r):("number"===i?y:"string"===i?(n=e.color(r))?(r=n,u):w:r instanceof e.color?u:r instanceof Date?v:g(r)?d:Array.isArray(r)?m:"function"!=typeof r.valueOf&&"function"!=typeof r.toString||isNaN(r)?x:y)(t,r)}var k,M,A,S,E=180/Math.PI,C={translateX:0,translateY:0,rotate:0,skewX:0,scaleX:1,scaleY:1};function L(t,e,r,n,i,a){var o,s,l;return(o=Math.sqrt(t*t+e*e))&&(t/=o,e/=o),(l=t*r+e*n)&&(r-=t*l,n-=e*l),(s=Math.sqrt(r*r+n*n))&&(r/=s,n/=s,l/=s),t*n<e*r&&(t=-t,e=-e,l=-l,o=-o),{translateX:i,translateY:a,rotate:Math.atan2(e,t)*E,skewX:Math.atan(l)*E,scaleX:o,scaleY:s}}function I(t,e,r,n){function i(t){return t.length?t.pop()+" ":""}return function(a,o){var s=[],l=[];return a=t(a),o=t(o),function(t,n,i,a,o,s){if(t!==i||n!==a){var l=o.push("translate(",null,e,null,r);s.push({i:l-4,x:y(t,i)},{i:l-2,x:y(n,a)})}else(i||a)&&o.push("translate("+i+e+a+r)}(a.translateX,a.translateY,o.translateX,o.translateY,s,l),function(t,e,r,a){t!==e?(t-e>180?e+=360:e-t>180&&(t+=360),a.push({i:r.push(i(r)+"rotate(",null,n)-2,x:y(t,e)})):e&&r.push(i(r)+"rotate("+e+n)}(a.rotate,o.rotate,s,l),function(t,e,r,a){t!==e?a.push({i:r.push(i(r)+"skewX(",null,n)-2,x:y(t,e)}):e&&r.push(i(r)+"skewX("+e+n)}(a.skewX,o.skewX,s,l),function(t,e,r,n,a,o){if(t!==r||e!==n){var s=a.push(i(a)+"scale(",null,",",null,")");o.push({i:s-4,x:y(t,r)},{i:s-2,x:y(e,n)})}else 1===r&&1===n||a.push(i(a)+"scale("+r+","+n+")")}(a.scaleX,a.scaleY,o.scaleX,o.scaleY,s,l),a=o=null,function(t){for(var e,r=-1,n=l.length;++r<n;)s[(e=l[r]).i]=e.x(t);return s.join("")}}}var P=I((function(t){return"none"===t?C:(k||(k=document.createElement("DIV"),M=document.documentElement,A=document.defaultView),k.style.transform=t,t=A.getComputedStyle(M.appendChild(k),null).getPropertyValue("transform"),M.removeChild(k),L(+(t=t.slice(7,-1).split(","))[0],+t[1],+t[2],+t[3],+t[4],+t[5]))}),"px, ","px)","deg)"),z=I((function(t){return null==t?C:(S||(S=document.createElementNS("http://www.w3.org/2000/svg","g")),S.setAttribute("transform",t),(t=S.transform.baseVal.consolidate())?L((t=t.matrix).a,t.b,t.c,t.d,t.e,t.f):C)}),", ",")",")"),O=Math.SQRT2;function D(t){return((t=Math.exp(t))+1/t)/2}function R(t){return function(r,n){var i=t((r=e.hsl(r)).h,(n=e.hsl(n)).h),a=c(r.s,n.s),o=c(r.l,n.l),s=c(r.opacity,n.opacity);return function(t){return r.h=i(t),r.s=a(t),r.l=o(t),r.opacity=s(t),r+""}}}var F=R(s),B=R(c);function N(t){return function(r,n){var i=t((r=e.hcl(r)).h,(n=e.hcl(n)).h),a=c(r.c,n.c),o=c(r.l,n.l),s=c(r.opacity,n.opacity);return function(t){return r.h=i(t),r.c=a(t),r.l=o(t),r.opacity=s(t),r+""}}}var j=N(s),U=N(c);function V(t){return function r(n){function i(r,i){var a=t((r=e.cubehelix(r)).h,(i=e.cubehelix(i)).h),o=c(r.s,i.s),s=c(r.l,i.l),l=c(r.opacity,i.opacity);return function(t){return r.h=a(t),r.s=o(t),r.l=s(Math.pow(t,n)),r.opacity=l(t),r+""}}return n=+n,i.gamma=r,i}(1)}var q=V(s),H=V(c);t.interpolate=T,t.interpolateArray=function(t,e){return(g(e)?d:m)(t,e)},t.interpolateBasis=n,t.interpolateBasisClosed=i,t.interpolateCubehelix=q,t.interpolateCubehelixLong=H,t.interpolateDate=v,t.interpolateDiscrete=function(t){var e=t.length;return function(r){return t[Math.max(0,Math.min(e-1,Math.floor(r*e)))]}},t.interpolateHcl=j,t.interpolateHclLong=U,t.interpolateHsl=F,t.interpolateHslLong=B,t.interpolateHue=function(t,e){var r=s(+t,+e);return function(t){var e=r(t);return e-360*Math.floor(e/360)}},t.interpolateLab=function(t,r){var n=c((t=e.lab(t)).l,(r=e.lab(r)).l),i=c(t.a,r.a),a=c(t.b,r.b),o=c(t.opacity,r.opacity);return function(e){return t.l=n(e),t.a=i(e),t.b=a(e),t.opacity=o(e),t+""}},t.interpolateNumber=y,t.interpolateNumberArray=d,t.interpolateObject=x,t.interpolateRgb=u,t.interpolateRgbBasis=h,t.interpolateRgbBasisClosed=p,t.interpolateRound=function(t,e){return t=+t,e=+e,function(r){return Math.round(t*(1-r)+e*r)}},t.interpolateString=w,t.interpolateTransformCss=P,t.interpolateTransformSvg=z,t.interpolateZoom=function(t,e){var r,n,i=t[0],a=t[1],o=t[2],s=e[0],l=e[1],c=e[2],u=s-i,f=l-a,h=u*u+f*f;if(h<1e-12)n=Math.log(c/o)/O,r=function(t){return[i+t*u,a+t*f,o*Math.exp(O*t*n)]};else{var p=Math.sqrt(h),d=(c*c-o*o+4*h)/(2*o*2*p),g=(c*c-o*o-4*h)/(2*c*2*p),m=Math.log(Math.sqrt(d*d+1)-d),v=Math.log(Math.sqrt(g*g+1)-g);n=(v-m)/O,r=function(t){var e,r=t*n,s=D(m),l=o/(2*p)*(s*(e=O*r+m,((e=Math.exp(2*e))-1)/(e+1))-function(t){return((t=Math.exp(t))-1/t)/2}(m));return[i+l*u,a+l*f,o*s/D(O*r+m)]}}return r.duration=1e3*n,r},t.piecewise=function(t,e){for(var r=0,n=e.length-1,i=e[0],a=new Array(n<0?0:n);r<n;)a[r]=t(i,i=e[++r]);return function(t){var e=Math.max(0,Math.min(n-1,Math.floor(t*=n)));return a[e](t-e)}},t.quantize=function(t,e){for(var r=new Array(e),n=0;n<e;++n)r[n]=t(n/(e-1));return r},Object.defineProperty(t,"__esModule",{value:!0})}))},{"d3-color":158}],163:[function(t,e,r){!function(t,n){"object"==typeof r&&"undefined"!=typeof e?n(r):n((t=t||self).d3=t.d3||{})}(this,(function(t){"use strict";var e=Math.PI,r=2*e,n=r-1e-6;function i(){this._x0=this._y0=this._x1=this._y1=null,this._=""}function a(){return new i}i.prototype=a.prototype={constructor:i,moveTo:function(t,e){this._+="M"+(this._x0=this._x1=+t)+","+(this._y0=this._y1=+e)},closePath:function(){null!==this._x1&&(this._x1=this._x0,this._y1=this._y0,this._+="Z")},lineTo:function(t,e){this._+="L"+(this._x1=+t)+","+(this._y1=+e)},quadraticCurveTo:function(t,e,r,n){this._+="Q"+ +t+","+ +e+","+(this._x1=+r)+","+(this._y1=+n)},bezierCurveTo:function(t,e,r,n,i,a){this._+="C"+ +t+","+ +e+","+ +r+","+ +n+","+(this._x1=+i)+","+(this._y1=+a)},arcTo:function(t,r,n,i,a){t=+t,r=+r,n=+n,i=+i,a=+a;var o=this._x1,s=this._y1,l=n-t,c=i-r,u=o-t,f=s-r,h=u*u+f*f;if(a<0)throw new Error("negative radius: "+a);if(null===this._x1)this._+="M"+(this._x1=t)+","+(this._y1=r);else if(h>1e-6)if(Math.abs(f*l-c*u)>1e-6&&a){var p=n-o,d=i-s,g=l*l+c*c,m=p*p+d*d,v=Math.sqrt(g),y=Math.sqrt(h),x=a*Math.tan((e-Math.acos((g+h-m)/(2*v*y)))/2),b=x/y,_=x/v;Math.abs(b-1)>1e-6&&(this._+="L"+(t+b*u)+","+(r+b*f)),this._+="A"+a+","+a+",0,0,"+ +(f*p>u*d)+","+(this._x1=t+_*l)+","+(this._y1=r+_*c)}else this._+="L"+(this._x1=t)+","+(this._y1=r);else;},arc:function(t,i,a,o,s,l){t=+t,i=+i,l=!!l;var c=(a=+a)*Math.cos(o),u=a*Math.sin(o),f=t+c,h=i+u,p=1^l,d=l?o-s:s-o;if(a<0)throw new Error("negative radius: "+a);null===this._x1?this._+="M"+f+","+h:(Math.abs(this._x1-f)>1e-6||Math.abs(this._y1-h)>1e-6)&&(this._+="L"+f+","+h),a&&(d<0&&(d=d%r+r),d>n?this._+="A"+a+","+a+",0,1,"+p+","+(t-c)+","+(i-u)+"A"+a+","+a+",0,1,"+p+","+(this._x1=f)+","+(this._y1=h):d>1e-6&&(this._+="A"+a+","+a+",0,"+ +(d>=e)+","+p+","+(this._x1=t+a*Math.cos(s))+","+(this._y1=i+a*Math.sin(s))))},rect:function(t,e,r,n){this._+="M"+(this._x0=this._x1=+t)+","+(this._y0=this._y1=+e)+"h"+ +r+"v"+ +n+"h"+-r+"Z"},toString:function(){return this._}},t.path=a,Object.defineProperty(t,"__esModule",{value:!0})}))},{}],164:[function(t,e,r){!function(t,n){"object"==typeof r&&"undefined"!=typeof e?n(r):n((t=t||self).d3=t.d3||{})}(this,(function(t){"use strict";function e(t,e,r,n){if(isNaN(e)||isNaN(r))return t;var i,a,o,s,l,c,u,f,h,p=t._root,d={data:n},g=t._x0,m=t._y0,v=t._x1,y=t._y1;if(!p)return t._root=d,t;for(;p.length;)if((c=e>=(a=(g+v)/2))?g=a:v=a,(u=r>=(o=(m+y)/2))?m=o:y=o,i=p,!(p=p[f=u<<1|c]))return i[f]=d,t;if(s=+t._x.call(null,p.data),l=+t._y.call(null,p.data),e===s&&r===l)return d.next=p,i?i[f]=d:t._root=d,t;do{i=i?i[f]=new Array(4):t._root=new Array(4),(c=e>=(a=(g+v)/2))?g=a:v=a,(u=r>=(o=(m+y)/2))?m=o:y=o}while((f=u<<1|c)==(h=(l>=o)<<1|s>=a));return i[h]=p,i[f]=d,t}function r(t,e,r,n,i){this.node=t,this.x0=e,this.y0=r,this.x1=n,this.y1=i}function n(t){return t[0]}function i(t){return t[1]}function a(t,e,r){var a=new o(null==e?n:e,null==r?i:r,NaN,NaN,NaN,NaN);return null==t?a:a.addAll(t)}function o(t,e,r,n,i,a){this._x=t,this._y=e,this._x0=r,this._y0=n,this._x1=i,this._y1=a,this._root=void 0}function s(t){for(var e={data:t.data},r=e;t=t.next;)r=r.next={data:t.data};return e}var l=a.prototype=o.prototype;l.copy=function(){var t,e,r=new o(this._x,this._y,this._x0,this._y0,this._x1,this._y1),n=this._root;if(!n)return r;if(!n.length)return r._root=s(n),r;for(t=[{source:n,target:r._root=new Array(4)}];n=t.pop();)for(var i=0;i<4;++i)(e=n.source[i])&&(e.length?t.push({source:e,target:n.target[i]=new Array(4)}):n.target[i]=s(e));return r},l.add=function(t){var r=+this._x.call(null,t),n=+this._y.call(null,t);return e(this.cover(r,n),r,n,t)},l.addAll=function(t){var r,n,i,a,o=t.length,s=new Array(o),l=new Array(o),c=1/0,u=1/0,f=-1/0,h=-1/0;for(n=0;n<o;++n)isNaN(i=+this._x.call(null,r=t[n]))||isNaN(a=+this._y.call(null,r))||(s[n]=i,l[n]=a,i<c&&(c=i),i>f&&(f=i),a<u&&(u=a),a>h&&(h=a));if(c>f||u>h)return this;for(this.cover(c,u).cover(f,h),n=0;n<o;++n)e(this,s[n],l[n],t[n]);return this},l.cover=function(t,e){if(isNaN(t=+t)||isNaN(e=+e))return this;var r=this._x0,n=this._y0,i=this._x1,a=this._y1;if(isNaN(r))i=(r=Math.floor(t))+1,a=(n=Math.floor(e))+1;else{for(var o,s,l=i-r,c=this._root;r>t||t>=i||n>e||e>=a;)switch(s=(e<n)<<1|t<r,(o=new Array(4))[s]=c,c=o,l*=2,s){case 0:i=r+l,a=n+l;break;case 1:r=i-l,a=n+l;break;case 2:i=r+l,n=a-l;break;case 3:r=i-l,n=a-l}this._root&&this._root.length&&(this._root=c)}return this._x0=r,this._y0=n,this._x1=i,this._y1=a,this},l.data=function(){var t=[];return this.visit((function(e){if(!e.length)do{t.push(e.data)}while(e=e.next)})),t},l.extent=function(t){return arguments.length?this.cover(+t[0][0],+t[0][1]).cover(+t[1][0],+t[1][1]):isNaN(this._x0)?void 0:[[this._x0,this._y0],[this._x1,this._y1]]},l.find=function(t,e,n){var i,a,o,s,l,c,u,f=this._x0,h=this._y0,p=this._x1,d=this._y1,g=[],m=this._root;for(m&&g.push(new r(m,f,h,p,d)),null==n?n=1/0:(f=t-n,h=e-n,p=t+n,d=e+n,n*=n);c=g.pop();)if(!(!(m=c.node)||(a=c.x0)>p||(o=c.y0)>d||(s=c.x1)<f||(l=c.y1)<h))if(m.length){var v=(a+s)/2,y=(o+l)/2;g.push(new r(m[3],v,y,s,l),new r(m[2],a,y,v,l),new r(m[1],v,o,s,y),new r(m[0],a,o,v,y)),(u=(e>=y)<<1|t>=v)&&(c=g[g.length-1],g[g.length-1]=g[g.length-1-u],g[g.length-1-u]=c)}else{var x=t-+this._x.call(null,m.data),b=e-+this._y.call(null,m.data),_=x*x+b*b;if(_<n){var w=Math.sqrt(n=_);f=t-w,h=e-w,p=t+w,d=e+w,i=m.data}}return i},l.remove=function(t){if(isNaN(a=+this._x.call(null,t))||isNaN(o=+this._y.call(null,t)))return this;var e,r,n,i,a,o,s,l,c,u,f,h,p=this._root,d=this._x0,g=this._y0,m=this._x1,v=this._y1;if(!p)return this;if(p.length)for(;;){if((c=a>=(s=(d+m)/2))?d=s:m=s,(u=o>=(l=(g+v)/2))?g=l:v=l,e=p,!(p=p[f=u<<1|c]))return this;if(!p.length)break;(e[f+1&3]||e[f+2&3]||e[f+3&3])&&(r=e,h=f)}for(;p.data!==t;)if(n=p,!(p=p.next))return this;return(i=p.next)&&delete p.next,n?(i?n.next=i:delete n.next,this):e?(i?e[f]=i:delete e[f],(p=e[0]||e[1]||e[2]||e[3])&&p===(e[3]||e[2]||e[1]||e[0])&&!p.length&&(r?r[h]=p:this._root=p),this):(this._root=i,this)},l.removeAll=function(t){for(var e=0,r=t.length;e<r;++e)this.remove(t[e]);return this},l.root=function(){return this._root},l.size=function(){var t=0;return this.visit((function(e){if(!e.length)do{++t}while(e=e.next)})),t},l.visit=function(t){var e,n,i,a,o,s,l=[],c=this._root;for(c&&l.push(new r(c,this._x0,this._y0,this._x1,this._y1));e=l.pop();)if(!t(c=e.node,i=e.x0,a=e.y0,o=e.x1,s=e.y1)&&c.length){var u=(i+o)/2,f=(a+s)/2;(n=c[3])&&l.push(new r(n,u,f,o,s)),(n=c[2])&&l.push(new r(n,i,f,u,s)),(n=c[1])&&l.push(new r(n,u,a,o,f)),(n=c[0])&&l.push(new r(n,i,a,u,f))}return this},l.visitAfter=function(t){var e,n=[],i=[];for(this._root&&n.push(new r(this._root,this._x0,this._y0,this._x1,this._y1));e=n.pop();){var a=e.node;if(a.length){var o,s=e.x0,l=e.y0,c=e.x1,u=e.y1,f=(s+c)/2,h=(l+u)/2;(o=a[0])&&n.push(new r(o,s,l,f,h)),(o=a[1])&&n.push(new r(o,f,l,c,h)),(o=a[2])&&n.push(new r(o,s,h,f,u)),(o=a[3])&&n.push(new r(o,f,h,c,u))}i.push(e)}for(;e=i.pop();)t(e.node,e.x0,e.y0,e.x1,e.y1);return this},l.x=function(t){return arguments.length?(this._x=t,this):this._x},l.y=function(t){return arguments.length?(this._y=t,this):this._y},t.quadtree=a,Object.defineProperty(t,"__esModule",{value:!0})}))},{}],165:[function(t,e,r){!function(n,i){"object"==typeof r&&"undefined"!=typeof e?i(r,t("d3-path")):i((n=n||self).d3=n.d3||{},n.d3)}(this,(function(t,e){"use strict";function r(t){return function(){return t}}var n=Math.abs,i=Math.atan2,a=Math.cos,o=Math.max,s=Math.min,l=Math.sin,c=Math.sqrt,u=Math.PI,f=u/2,h=2*u;function p(t){return t>1?0:t<-1?u:Math.acos(t)}function d(t){return t>=1?f:t<=-1?-f:Math.asin(t)}function g(t){return t.innerRadius}function m(t){return t.outerRadius}function v(t){return t.startAngle}function y(t){return t.endAngle}function x(t){return t&&t.padAngle}function b(t,e,r,n,i,a,o,s){var l=r-t,c=n-e,u=o-i,f=s-a,h=f*l-u*c;if(!(h*h<1e-12))return[t+(h=(u*(e-a)-f*(t-i))/h)*l,e+h*c]}function _(t,e,r,n,i,a,s){var l=t-r,u=e-n,f=(s?a:-a)/c(l*l+u*u),h=f*u,p=-f*l,d=t+h,g=e+p,m=r+h,v=n+p,y=(d+m)/2,x=(g+v)/2,b=m-d,_=v-g,w=b*b+_*_,T=i-a,k=d*v-m*g,M=(_<0?-1:1)*c(o(0,T*T*w-k*k)),A=(k*_-b*M)/w,S=(-k*b-_*M)/w,E=(k*_+b*M)/w,C=(-k*b+_*M)/w,L=A-y,I=S-x,P=E-y,z=C-x;return L*L+I*I>P*P+z*z&&(A=E,S=C),{cx:A,cy:S,x01:-h,y01:-p,x11:A*(i/T-1),y11:S*(i/T-1)}}function w(t){this._context=t}function T(t){return new w(t)}function k(t){return t[0]}function M(t){return t[1]}function A(){var t=k,n=M,i=r(!0),a=null,o=T,s=null;function l(r){var l,c,u,f=r.length,h=!1;for(null==a&&(s=o(u=e.path())),l=0;l<=f;++l)!(l<f&&i(c=r[l],l,r))===h&&((h=!h)?s.lineStart():s.lineEnd()),h&&s.point(+t(c,l,r),+n(c,l,r));if(u)return s=null,u+""||null}return l.x=function(e){return arguments.length?(t="function"==typeof e?e:r(+e),l):t},l.y=function(t){return arguments.length?(n="function"==typeof t?t:r(+t),l):n},l.defined=function(t){return arguments.length?(i="function"==typeof t?t:r(!!t),l):i},l.curve=function(t){return arguments.length?(o=t,null!=a&&(s=o(a)),l):o},l.context=function(t){return arguments.length?(null==t?a=s=null:s=o(a=t),l):a},l}function S(){var t=k,n=null,i=r(0),a=M,o=r(!0),s=null,l=T,c=null;function u(r){var u,f,h,p,d,g=r.length,m=!1,v=new Array(g),y=new Array(g);for(null==s&&(c=l(d=e.path())),u=0;u<=g;++u){if(!(u<g&&o(p=r[u],u,r))===m)if(m=!m)f=u,c.areaStart(),c.lineStart();else{for(c.lineEnd(),c.lineStart(),h=u-1;h>=f;--h)c.point(v[h],y[h]);c.lineEnd(),c.areaEnd()}m&&(v[u]=+t(p,u,r),y[u]=+i(p,u,r),c.point(n?+n(p,u,r):v[u],a?+a(p,u,r):y[u]))}if(d)return c=null,d+""||null}function f(){return A().defined(o).curve(l).context(s)}return u.x=function(e){return arguments.length?(t="function"==typeof e?e:r(+e),n=null,u):t},u.x0=function(e){return arguments.length?(t="function"==typeof e?e:r(+e),u):t},u.x1=function(t){return arguments.length?(n=null==t?null:"function"==typeof t?t:r(+t),u):n},u.y=function(t){return arguments.length?(i="function"==typeof t?t:r(+t),a=null,u):i},u.y0=function(t){return arguments.length?(i="function"==typeof t?t:r(+t),u):i},u.y1=function(t){return arguments.length?(a=null==t?null:"function"==typeof t?t:r(+t),u):a},u.lineX0=u.lineY0=function(){return f().x(t).y(i)},u.lineY1=function(){return f().x(t).y(a)},u.lineX1=function(){return f().x(n).y(i)},u.defined=function(t){return arguments.length?(o="function"==typeof t?t:r(!!t),u):o},u.curve=function(t){return arguments.length?(l=t,null!=s&&(c=l(s)),u):l},u.context=function(t){return arguments.length?(null==t?s=c=null:c=l(s=t),u):s},u}function E(t,e){return e<t?-1:e>t?1:e>=t?0:NaN}function C(t){return t}w.prototype={areaStart:function(){this._line=0},areaEnd:function(){this._line=NaN},lineStart:function(){this._point=0},lineEnd:function(){(this._line||0!==this._line&&1===this._point)&&this._context.closePath(),this._line=1-this._line},point:function(t,e){switch(t=+t,e=+e,this._point){case 0:this._point=1,this._line?this._context.lineTo(t,e):this._context.moveTo(t,e);break;case 1:this._point=2;default:this._context.lineTo(t,e)}}};var L=P(T);function I(t){this._curve=t}function P(t){function e(e){return new I(t(e))}return e._curve=t,e}function z(t){var e=t.curve;return t.angle=t.x,delete t.x,t.radius=t.y,delete t.y,t.curve=function(t){return arguments.length?e(P(t)):e()._curve},t}function O(){return z(A().curve(L))}function D(){var t=S().curve(L),e=t.curve,r=t.lineX0,n=t.lineX1,i=t.lineY0,a=t.lineY1;return t.angle=t.x,delete t.x,t.startAngle=t.x0,delete t.x0,t.endAngle=t.x1,delete t.x1,t.radius=t.y,delete t.y,t.innerRadius=t.y0,delete t.y0,t.outerRadius=t.y1,delete t.y1,t.lineStartAngle=function(){return z(r())},delete t.lineX0,t.lineEndAngle=function(){return z(n())},delete t.lineX1,t.lineInnerRadius=function(){return z(i())},delete t.lineY0,t.lineOuterRadius=function(){return z(a())},delete t.lineY1,t.curve=function(t){return arguments.length?e(P(t)):e()._curve},t}function R(t,e){return[(e=+e)*Math.cos(t-=Math.PI/2),e*Math.sin(t)]}I.prototype={areaStart:function(){this._curve.areaStart()},areaEnd:function(){this._curve.areaEnd()},lineStart:function(){this._curve.lineStart()},lineEnd:function(){this._curve.lineEnd()},point:function(t,e){this._curve.point(e*Math.sin(t),e*-Math.cos(t))}};var F=Array.prototype.slice;function B(t){return t.source}function N(t){return t.target}function j(t){var n=B,i=N,a=k,o=M,s=null;function l(){var r,l=F.call(arguments),c=n.apply(this,l),u=i.apply(this,l);if(s||(s=r=e.path()),t(s,+a.apply(this,(l[0]=c,l)),+o.apply(this,l),+a.apply(this,(l[0]=u,l)),+o.apply(this,l)),r)return s=null,r+""||null}return l.source=function(t){return arguments.length?(n=t,l):n},l.target=function(t){return arguments.length?(i=t,l):i},l.x=function(t){return arguments.length?(a="function"==typeof t?t:r(+t),l):a},l.y=function(t){return arguments.length?(o="function"==typeof t?t:r(+t),l):o},l.context=function(t){return arguments.length?(s=null==t?null:t,l):s},l}function U(t,e,r,n,i){t.moveTo(e,r),t.bezierCurveTo(e=(e+n)/2,r,e,i,n,i)}function V(t,e,r,n,i){t.moveTo(e,r),t.bezierCurveTo(e,r=(r+i)/2,n,r,n,i)}function q(t,e,r,n,i){var a=R(e,r),o=R(e,r=(r+i)/2),s=R(n,r),l=R(n,i);t.moveTo(a[0],a[1]),t.bezierCurveTo(o[0],o[1],s[0],s[1],l[0],l[1])}var H={draw:function(t,e){var r=Math.sqrt(e/u);t.moveTo(r,0),t.arc(0,0,r,0,h)}},G={draw:function(t,e){var r=Math.sqrt(e/5)/2;t.moveTo(-3*r,-r),t.lineTo(-r,-r),t.lineTo(-r,-3*r),t.lineTo(r,-3*r),t.lineTo(r,-r),t.lineTo(3*r,-r),t.lineTo(3*r,r),t.lineTo(r,r),t.lineTo(r,3*r),t.lineTo(-r,3*r),t.lineTo(-r,r),t.lineTo(-3*r,r),t.closePath()}},Y=Math.sqrt(1/3),W=2*Y,X={draw:function(t,e){var r=Math.sqrt(e/W),n=r*Y;t.moveTo(0,-r),t.lineTo(n,0),t.lineTo(0,r),t.lineTo(-n,0),t.closePath()}},Z=Math.sin(u/10)/Math.sin(7*u/10),J=Math.sin(h/10)*Z,K=-Math.cos(h/10)*Z,Q={draw:function(t,e){var r=Math.sqrt(.8908130915292852*e),n=J*r,i=K*r;t.moveTo(0,-r),t.lineTo(n,i);for(var a=1;a<5;++a){var o=h*a/5,s=Math.cos(o),l=Math.sin(o);t.lineTo(l*r,-s*r),t.lineTo(s*n-l*i,l*n+s*i)}t.closePath()}},$={draw:function(t,e){var r=Math.sqrt(e),n=-r/2;t.rect(n,n,r,r)}},tt=Math.sqrt(3),et={draw:function(t,e){var r=-Math.sqrt(e/(3*tt));t.moveTo(0,2*r),t.lineTo(-tt*r,-r),t.lineTo(tt*r,-r),t.closePath()}},rt=-.5,nt=Math.sqrt(3)/2,it=1/Math.sqrt(12),at=3*(it/2+1),ot={draw:function(t,e){var r=Math.sqrt(e/at),n=r/2,i=r*it,a=n,o=r*it+r,s=-a,l=o;t.moveTo(n,i),t.lineTo(a,o),t.lineTo(s,l),t.lineTo(rt*n-nt*i,nt*n+rt*i),t.lineTo(rt*a-nt*o,nt*a+rt*o),t.lineTo(rt*s-nt*l,nt*s+rt*l),t.lineTo(rt*n+nt*i,rt*i-nt*n),t.lineTo(rt*a+nt*o,rt*o-nt*a),t.lineTo(rt*s+nt*l,rt*l-nt*s),t.closePath()}},st=[H,G,X,$,Q,et,ot];function lt(){}function ct(t,e,r){t._context.bezierCurveTo((2*t._x0+t._x1)/3,(2*t._y0+t._y1)/3,(t._x0+2*t._x1)/3,(t._y0+2*t._y1)/3,(t._x0+4*t._x1+e)/6,(t._y0+4*t._y1+r)/6)}function ut(t){this._context=t}function ft(t){this._context=t}function ht(t){this._context=t}function pt(t,e){this._basis=new ut(t),this._beta=e}ut.prototype={areaStart:function(){this._line=0},areaEnd:function(){this._line=NaN},lineStart:function(){this._x0=this._x1=this._y0=this._y1=NaN,this._point=0},lineEnd:function(){switch(this._point){case 3:ct(this,this._x1,this._y1);case 2:this._context.lineTo(this._x1,this._y1)}(this._line||0!==this._line&&1===this._point)&&this._context.closePath(),this._line=1-this._line},point:function(t,e){switch(t=+t,e=+e,this._point){case 0:this._point=1,this._line?this._context.lineTo(t,e):this._context.moveTo(t,e);break;case 1:this._point=2;break;case 2:this._point=3,this._context.lineTo((5*this._x0+this._x1)/6,(5*this._y0+this._y1)/6);default:ct(this,t,e)}this._x0=this._x1,this._x1=t,this._y0=this._y1,this._y1=e}},ft.prototype={areaStart:lt,areaEnd:lt,lineStart:function(){this._x0=this._x1=this._x2=this._x3=this._x4=this._y0=this._y1=this._y2=this._y3=this._y4=NaN,this._point=0},lineEnd:function(){switch(this._point){case 1:this._context.moveTo(this._x2,this._y2),this._context.closePath();break;case 2:this._context.moveTo((this._x2+2*this._x3)/3,(this._y2+2*this._y3)/3),this._context.lineTo((this._x3+2*this._x2)/3,(this._y3+2*this._y2)/3),this._context.closePath();break;case 3:this.point(this._x2,this._y2),this.point(this._x3,this._y3),this.point(this._x4,this._y4)}},point:function(t,e){switch(t=+t,e=+e,this._point){case 0:this._point=1,this._x2=t,this._y2=e;break;case 1:this._point=2,this._x3=t,this._y3=e;break;case 2:this._point=3,this._x4=t,this._y4=e,this._context.moveTo((this._x0+4*this._x1+t)/6,(this._y0+4*this._y1+e)/6);break;default:ct(this,t,e)}this._x0=this._x1,this._x1=t,this._y0=this._y1,this._y1=e}},ht.prototype={areaStart:function(){this._line=0},areaEnd:function(){this._line=NaN},lineStart:function(){this._x0=this._x1=this._y0=this._y1=NaN,this._point=0},lineEnd:function(){(this._line||0!==this._line&&3===this._point)&&this._context.closePath(),this._line=1-this._line},point:function(t,e){switch(t=+t,e=+e,this._point){case 0:this._point=1;break;case 1:this._point=2;break;case 2:this._point=3;var r=(this._x0+4*this._x1+t)/6,n=(this._y0+4*this._y1+e)/6;this._line?this._context.lineTo(r,n):this._context.moveTo(r,n);break;case 3:this._point=4;default:ct(this,t,e)}this._x0=this._x1,this._x1=t,this._y0=this._y1,this._y1=e}},pt.prototype={lineStart:function(){this._x=[],this._y=[],this._basis.lineStart()},lineEnd:function(){var t=this._x,e=this._y,r=t.length-1;if(r>0)for(var n,i=t[0],a=e[0],o=t[r]-i,s=e[r]-a,l=-1;++l<=r;)n=l/r,this._basis.point(this._beta*t[l]+(1-this._beta)*(i+n*o),this._beta*e[l]+(1-this._beta)*(a+n*s));this._x=this._y=null,this._basis.lineEnd()},point:function(t,e){this._x.push(+t),this._y.push(+e)}};var dt=function t(e){function r(t){return 1===e?new ut(t):new pt(t,e)}return r.beta=function(e){return t(+e)},r}(.85);function gt(t,e,r){t._context.bezierCurveTo(t._x1+t._k*(t._x2-t._x0),t._y1+t._k*(t._y2-t._y0),t._x2+t._k*(t._x1-e),t._y2+t._k*(t._y1-r),t._x2,t._y2)}function mt(t,e){this._context=t,this._k=(1-e)/6}mt.prototype={areaStart:function(){this._line=0},areaEnd:function(){this._line=NaN},lineStart:function(){this._x0=this._x1=this._x2=this._y0=this._y1=this._y2=NaN,this._point=0},lineEnd:function(){switch(this._point){case 2:this._context.lineTo(this._x2,this._y2);break;case 3:gt(this,this._x1,this._y1)}(this._line||0!==this._line&&1===this._point)&&this._context.closePath(),this._line=1-this._line},point:function(t,e){switch(t=+t,e=+e,this._point){case 0:this._point=1,this._line?this._context.lineTo(t,e):this._context.moveTo(t,e);break;case 1:this._point=2,this._x1=t,this._y1=e;break;case 2:this._point=3;default:gt(this,t,e)}this._x0=this._x1,this._x1=this._x2,this._x2=t,this._y0=this._y1,this._y1=this._y2,this._y2=e}};var vt=function t(e){function r(t){return new mt(t,e)}return r.tension=function(e){return t(+e)},r}(0);function yt(t,e){this._context=t,this._k=(1-e)/6}yt.prototype={areaStart:lt,areaEnd:lt,lineStart:function(){this._x0=this._x1=this._x2=this._x3=this._x4=this._x5=this._y0=this._y1=this._y2=this._y3=this._y4=this._y5=NaN,this._point=0},lineEnd:function(){switch(this._point){case 1:this._context.moveTo(this._x3,this._y3),this._context.closePath();break;case 2:this._context.lineTo(this._x3,this._y3),this._context.closePath();break;case 3:this.point(this._x3,this._y3),this.point(this._x4,this._y4),this.point(this._x5,this._y5)}},point:function(t,e){switch(t=+t,e=+e,this._point){case 0:this._point=1,this._x3=t,this._y3=e;break;case 1:this._point=2,this._context.moveTo(this._x4=t,this._y4=e);break;case 2:this._point=3,this._x5=t,this._y5=e;break;default:gt(this,t,e)}this._x0=this._x1,this._x1=this._x2,this._x2=t,this._y0=this._y1,this._y1=this._y2,this._y2=e}};var xt=function t(e){function r(t){return new yt(t,e)}return r.tension=function(e){return t(+e)},r}(0);function bt(t,e){this._context=t,this._k=(1-e)/6}bt.prototype={areaStart:function(){this._line=0},areaEnd:function(){this._line=NaN},lineStart:function(){this._x0=this._x1=this._x2=this._y0=this._y1=this._y2=NaN,this._point=0},lineEnd:function(){(this._line||0!==this._line&&3===this._point)&&this._context.closePath(),this._line=1-this._line},point:function(t,e){switch(t=+t,e=+e,this._point){case 0:this._point=1;break;case 1:this._point=2;break;case 2:this._point=3,this._line?this._context.lineTo(this._x2,this._y2):this._context.moveTo(this._x2,this._y2);break;case 3:this._point=4;default:gt(this,t,e)}this._x0=this._x1,this._x1=this._x2,this._x2=t,this._y0=this._y1,this._y1=this._y2,this._y2=e}};var _t=function t(e){function r(t){return new bt(t,e)}return r.tension=function(e){return t(+e)},r}(0);function wt(t,e,r){var n=t._x1,i=t._y1,a=t._x2,o=t._y2;if(t._l01_a>1e-12){var s=2*t._l01_2a+3*t._l01_a*t._l12_a+t._l12_2a,l=3*t._l01_a*(t._l01_a+t._l12_a);n=(n*s-t._x0*t._l12_2a+t._x2*t._l01_2a)/l,i=(i*s-t._y0*t._l12_2a+t._y2*t._l01_2a)/l}if(t._l23_a>1e-12){var c=2*t._l23_2a+3*t._l23_a*t._l12_a+t._l12_2a,u=3*t._l23_a*(t._l23_a+t._l12_a);a=(a*c+t._x1*t._l23_2a-e*t._l12_2a)/u,o=(o*c+t._y1*t._l23_2a-r*t._l12_2a)/u}t._context.bezierCurveTo(n,i,a,o,t._x2,t._y2)}function Tt(t,e){this._context=t,this._alpha=e}Tt.prototype={areaStart:function(){this._line=0},areaEnd:function(){this._line=NaN},lineStart:function(){this._x0=this._x1=this._x2=this._y0=this._y1=this._y2=NaN,this._l01_a=this._l12_a=this._l23_a=this._l01_2a=this._l12_2a=this._l23_2a=this._point=0},lineEnd:function(){switch(this._point){case 2:this._context.lineTo(this._x2,this._y2);break;case 3:this.point(this._x2,this._y2)}(this._line||0!==this._line&&1===this._point)&&this._context.closePath(),this._line=1-this._line},point:function(t,e){if(t=+t,e=+e,this._point){var r=this._x2-t,n=this._y2-e;this._l23_a=Math.sqrt(this._l23_2a=Math.pow(r*r+n*n,this._alpha))}switch(this._point){case 0:this._point=1,this._line?this._context.lineTo(t,e):this._context.moveTo(t,e);break;case 1:this._point=2;break;case 2:this._point=3;default:wt(this,t,e)}this._l01_a=this._l12_a,this._l12_a=this._l23_a,this._l01_2a=this._l12_2a,this._l12_2a=this._l23_2a,this._x0=this._x1,this._x1=this._x2,this._x2=t,this._y0=this._y1,this._y1=this._y2,this._y2=e}};var kt=function t(e){function r(t){return e?new Tt(t,e):new mt(t,0)}return r.alpha=function(e){return t(+e)},r}(.5);function Mt(t,e){this._context=t,this._alpha=e}Mt.prototype={areaStart:lt,areaEnd:lt,lineStart:function(){this._x0=this._x1=this._x2=this._x3=this._x4=this._x5=this._y0=this._y1=this._y2=this._y3=this._y4=this._y5=NaN,this._l01_a=this._l12_a=this._l23_a=this._l01_2a=this._l12_2a=this._l23_2a=this._point=0},lineEnd:function(){switch(this._point){case 1:this._context.moveTo(this._x3,this._y3),this._context.closePath();break;case 2:this._context.lineTo(this._x3,this._y3),this._context.closePath();break;case 3:this.point(this._x3,this._y3),this.point(this._x4,this._y4),this.point(this._x5,this._y5)}},point:function(t,e){if(t=+t,e=+e,this._point){var r=this._x2-t,n=this._y2-e;this._l23_a=Math.sqrt(this._l23_2a=Math.pow(r*r+n*n,this._alpha))}switch(this._point){case 0:this._point=1,this._x3=t,this._y3=e;break;case 1:this._point=2,this._context.moveTo(this._x4=t,this._y4=e);break;case 2:this._point=3,this._x5=t,this._y5=e;break;default:wt(this,t,e)}this._l01_a=this._l12_a,this._l12_a=this._l23_a,this._l01_2a=this._l12_2a,this._l12_2a=this._l23_2a,this._x0=this._x1,this._x1=this._x2,this._x2=t,this._y0=this._y1,this._y1=this._y2,this._y2=e}};var At=function t(e){function r(t){return e?new Mt(t,e):new yt(t,0)}return r.alpha=function(e){return t(+e)},r}(.5);function St(t,e){this._context=t,this._alpha=e}St.prototype={areaStart:function(){this._line=0},areaEnd:function(){this._line=NaN},lineStart:function(){this._x0=this._x1=this._x2=this._y0=this._y1=this._y2=NaN,this._l01_a=this._l12_a=this._l23_a=this._l01_2a=this._l12_2a=this._l23_2a=this._point=0},lineEnd:function(){(this._line||0!==this._line&&3===this._point)&&this._context.closePath(),this._line=1-this._line},point:function(t,e){if(t=+t,e=+e,this._point){var r=this._x2-t,n=this._y2-e;this._l23_a=Math.sqrt(this._l23_2a=Math.pow(r*r+n*n,this._alpha))}switch(this._point){case 0:this._point=1;break;case 1:this._point=2;break;case 2:this._point=3,this._line?this._context.lineTo(this._x2,this._y2):this._context.moveTo(this._x2,this._y2);break;case 3:this._point=4;default:wt(this,t,e)}this._l01_a=this._l12_a,this._l12_a=this._l23_a,this._l01_2a=this._l12_2a,this._l12_2a=this._l23_2a,this._x0=this._x1,this._x1=this._x2,this._x2=t,this._y0=this._y1,this._y1=this._y2,this._y2=e}};var Et=function t(e){function r(t){return e?new St(t,e):new bt(t,0)}return r.alpha=function(e){return t(+e)},r}(.5);function Ct(t){this._context=t}function Lt(t){return t<0?-1:1}function It(t,e,r){var n=t._x1-t._x0,i=e-t._x1,a=(t._y1-t._y0)/(n||i<0&&-0),o=(r-t._y1)/(i||n<0&&-0),s=(a*i+o*n)/(n+i);return(Lt(a)+Lt(o))*Math.min(Math.abs(a),Math.abs(o),.5*Math.abs(s))||0}function Pt(t,e){var r=t._x1-t._x0;return r?(3*(t._y1-t._y0)/r-e)/2:e}function zt(t,e,r){var n=t._x0,i=t._y0,a=t._x1,o=t._y1,s=(a-n)/3;t._context.bezierCurveTo(n+s,i+s*e,a-s,o-s*r,a,o)}function Ot(t){this._context=t}function Dt(t){this._context=new Rt(t)}function Rt(t){this._context=t}function Ft(t){this._context=t}function Bt(t){var e,r,n=t.length-1,i=new Array(n),a=new Array(n),o=new Array(n);for(i[0]=0,a[0]=2,o[0]=t[0]+2*t[1],e=1;e<n-1;++e)i[e]=1,a[e]=4,o[e]=4*t[e]+2*t[e+1];for(i[n-1]=2,a[n-1]=7,o[n-1]=8*t[n-1]+t[n],e=1;e<n;++e)r=i[e]/a[e-1],a[e]-=r,o[e]-=r*o[e-1];for(i[n-1]=o[n-1]/a[n-1],e=n-2;e>=0;--e)i[e]=(o[e]-i[e+1])/a[e];for(a[n-1]=(t[n]+i[n-1])/2,e=0;e<n-1;++e)a[e]=2*t[e+1]-i[e+1];return[i,a]}function Nt(t,e){this._context=t,this._t=e}function jt(t,e){if((i=t.length)>1)for(var r,n,i,a=1,o=t[e[0]],s=o.length;a<i;++a)for(n=o,o=t[e[a]],r=0;r<s;++r)o[r][1]+=o[r][0]=isNaN(n[r][1])?n[r][0]:n[r][1]}function Ut(t){for(var e=t.length,r=new Array(e);--e>=0;)r[e]=e;return r}function Vt(t,e){return t[e]}function qt(t){var e=t.map(Ht);return Ut(t).sort((function(t,r){return e[t]-e[r]}))}function Ht(t){for(var e,r=-1,n=0,i=t.length,a=-1/0;++r<i;)(e=+t[r][1])>a&&(a=e,n=r);return n}function Gt(t){var e=t.map(Yt);return Ut(t).sort((function(t,r){return e[t]-e[r]}))}function Yt(t){for(var e,r=0,n=-1,i=t.length;++n<i;)(e=+t[n][1])&&(r+=e);return r}Ct.prototype={areaStart:lt,areaEnd:lt,lineStart:function(){this._point=0},lineEnd:function(){this._point&&this._context.closePath()},point:function(t,e){t=+t,e=+e,this._point?this._context.lineTo(t,e):(this._point=1,this._context.moveTo(t,e))}},Ot.prototype={areaStart:function(){this._line=0},areaEnd:function(){this._line=NaN},lineStart:function(){this._x0=this._x1=this._y0=this._y1=this._t0=NaN,this._point=0},lineEnd:function(){switch(this._point){case 2:this._context.lineTo(this._x1,this._y1);break;case 3:zt(this,this._t0,Pt(this,this._t0))}(this._line||0!==this._line&&1===this._point)&&this._context.closePath(),this._line=1-this._line},point:function(t,e){var r=NaN;if(e=+e,(t=+t)!==this._x1||e!==this._y1){switch(this._point){case 0:this._point=1,this._line?this._context.lineTo(t,e):this._context.moveTo(t,e);break;case 1:this._point=2;break;case 2:this._point=3,zt(this,Pt(this,r=It(this,t,e)),r);break;default:zt(this,this._t0,r=It(this,t,e))}this._x0=this._x1,this._x1=t,this._y0=this._y1,this._y1=e,this._t0=r}}},(Dt.prototype=Object.create(Ot.prototype)).point=function(t,e){Ot.prototype.point.call(this,e,t)},Rt.prototype={moveTo:function(t,e){this._context.moveTo(e,t)},closePath:function(){this._context.closePath()},lineTo:function(t,e){this._context.lineTo(e,t)},bezierCurveTo:function(t,e,r,n,i,a){this._context.bezierCurveTo(e,t,n,r,a,i)}},Ft.prototype={areaStart:function(){this._line=0},areaEnd:function(){this._line=NaN},lineStart:function(){this._x=[],this._y=[]},lineEnd:function(){var t=this._x,e=this._y,r=t.length;if(r)if(this._line?this._context.lineTo(t[0],e[0]):this._context.moveTo(t[0],e[0]),2===r)this._context.lineTo(t[1],e[1]);else for(var n=Bt(t),i=Bt(e),a=0,o=1;o<r;++a,++o)this._context.bezierCurveTo(n[0][a],i[0][a],n[1][a],i[1][a],t[o],e[o]);(this._line||0!==this._line&&1===r)&&this._context.closePath(),this._line=1-this._line,this._x=this._y=null},point:function(t,e){this._x.push(+t),this._y.push(+e)}},Nt.prototype={areaStart:function(){this._line=0},areaEnd:function(){this._line=NaN},lineStart:function(){this._x=this._y=NaN,this._point=0},lineEnd:function(){0<this._t&&this._t<1&&2===this._point&&this._context.lineTo(this._x,this._y),(this._line||0!==this._line&&1===this._point)&&this._context.closePath(),this._line>=0&&(this._t=1-this._t,this._line=1-this._line)},point:function(t,e){switch(t=+t,e=+e,this._point){case 0:this._point=1,this._line?this._context.lineTo(t,e):this._context.moveTo(t,e);break;case 1:this._point=2;default:if(this._t<=0)this._context.lineTo(this._x,e),this._context.lineTo(t,e);else{var r=this._x*(1-this._t)+t*this._t;this._context.lineTo(r,this._y),this._context.lineTo(r,e)}}this._x=t,this._y=e}},t.arc=function(){var t=g,o=m,w=r(0),T=null,k=v,M=y,A=x,S=null;function E(){var r,g,m=+t.apply(this,arguments),v=+o.apply(this,arguments),y=k.apply(this,arguments)-f,x=M.apply(this,arguments)-f,E=n(x-y),C=x>y;if(S||(S=r=e.path()),v<m&&(g=v,v=m,m=g),v>1e-12)if(E>h-1e-12)S.moveTo(v*a(y),v*l(y)),S.arc(0,0,v,y,x,!C),m>1e-12&&(S.moveTo(m*a(x),m*l(x)),S.arc(0,0,m,x,y,C));else{var L,I,P=y,z=x,O=y,D=x,R=E,F=E,B=A.apply(this,arguments)/2,N=B>1e-12&&(T?+T.apply(this,arguments):c(m*m+v*v)),j=s(n(v-m)/2,+w.apply(this,arguments)),U=j,V=j;if(N>1e-12){var q=d(N/m*l(B)),H=d(N/v*l(B));(R-=2*q)>1e-12?(O+=q*=C?1:-1,D-=q):(R=0,O=D=(y+x)/2),(F-=2*H)>1e-12?(P+=H*=C?1:-1,z-=H):(F=0,P=z=(y+x)/2)}var G=v*a(P),Y=v*l(P),W=m*a(D),X=m*l(D);if(j>1e-12){var Z,J=v*a(z),K=v*l(z),Q=m*a(O),$=m*l(O);if(E<u&&(Z=b(G,Y,Q,$,J,K,W,X))){var tt=G-Z[0],et=Y-Z[1],rt=J-Z[0],nt=K-Z[1],it=1/l(p((tt*rt+et*nt)/(c(tt*tt+et*et)*c(rt*rt+nt*nt)))/2),at=c(Z[0]*Z[0]+Z[1]*Z[1]);U=s(j,(m-at)/(it-1)),V=s(j,(v-at)/(it+1))}}F>1e-12?V>1e-12?(L=_(Q,$,G,Y,v,V,C),I=_(J,K,W,X,v,V,C),S.moveTo(L.cx+L.x01,L.cy+L.y01),V<j?S.arc(L.cx,L.cy,V,i(L.y01,L.x01),i(I.y01,I.x01),!C):(S.arc(L.cx,L.cy,V,i(L.y01,L.x01),i(L.y11,L.x11),!C),S.arc(0,0,v,i(L.cy+L.y11,L.cx+L.x11),i(I.cy+I.y11,I.cx+I.x11),!C),S.arc(I.cx,I.cy,V,i(I.y11,I.x11),i(I.y01,I.x01),!C))):(S.moveTo(G,Y),S.arc(0,0,v,P,z,!C)):S.moveTo(G,Y),m>1e-12&&R>1e-12?U>1e-12?(L=_(W,X,J,K,m,-U,C),I=_(G,Y,Q,$,m,-U,C),S.lineTo(L.cx+L.x01,L.cy+L.y01),U<j?S.arc(L.cx,L.cy,U,i(L.y01,L.x01),i(I.y01,I.x01),!C):(S.arc(L.cx,L.cy,U,i(L.y01,L.x01),i(L.y11,L.x11),!C),S.arc(0,0,m,i(L.cy+L.y11,L.cx+L.x11),i(I.cy+I.y11,I.cx+I.x11),C),S.arc(I.cx,I.cy,U,i(I.y11,I.x11),i(I.y01,I.x01),!C))):S.arc(0,0,m,D,O,C):S.lineTo(W,X)}else S.moveTo(0,0);if(S.closePath(),r)return S=null,r+""||null}return E.centroid=function(){var e=(+t.apply(this,arguments)+ +o.apply(this,arguments))/2,r=(+k.apply(this,arguments)+ +M.apply(this,arguments))/2-u/2;return[a(r)*e,l(r)*e]},E.innerRadius=function(e){return arguments.length?(t="function"==typeof e?e:r(+e),E):t},E.outerRadius=function(t){return arguments.length?(o="function"==typeof t?t:r(+t),E):o},E.cornerRadius=function(t){return arguments.length?(w="function"==typeof t?t:r(+t),E):w},E.padRadius=function(t){return arguments.length?(T=null==t?null:"function"==typeof t?t:r(+t),E):T},E.startAngle=function(t){return arguments.length?(k="function"==typeof t?t:r(+t),E):k},E.endAngle=function(t){return arguments.length?(M="function"==typeof t?t:r(+t),E):M},E.padAngle=function(t){return arguments.length?(A="function"==typeof t?t:r(+t),E):A},E.context=function(t){return arguments.length?(S=null==t?null:t,E):S},E},t.area=S,t.areaRadial=D,t.curveBasis=function(t){return new ut(t)},t.curveBasisClosed=function(t){return new ft(t)},t.curveBasisOpen=function(t){return new ht(t)},t.curveBundle=dt,t.curveCardinal=vt,t.curveCardinalClosed=xt,t.curveCardinalOpen=_t,t.curveCatmullRom=kt,t.curveCatmullRomClosed=At,t.curveCatmullRomOpen=Et,t.curveLinear=T,t.curveLinearClosed=function(t){return new Ct(t)},t.curveMonotoneX=function(t){return new Ot(t)},t.curveMonotoneY=function(t){return new Dt(t)},t.curveNatural=function(t){return new Ft(t)},t.curveStep=function(t){return new Nt(t,.5)},t.curveStepAfter=function(t){return new Nt(t,1)},t.curveStepBefore=function(t){return new Nt(t,0)},t.line=A,t.lineRadial=O,t.linkHorizontal=function(){return j(U)},t.linkRadial=function(){var t=j(q);return t.angle=t.x,delete t.x,t.radius=t.y,delete t.y,t},t.linkVertical=function(){return j(V)},t.pie=function(){var t=C,e=E,n=null,i=r(0),a=r(h),o=r(0);function s(r){var s,l,c,u,f,p=r.length,d=0,g=new Array(p),m=new Array(p),v=+i.apply(this,arguments),y=Math.min(h,Math.max(-h,a.apply(this,arguments)-v)),x=Math.min(Math.abs(y)/p,o.apply(this,arguments)),b=x*(y<0?-1:1);for(s=0;s<p;++s)(f=m[g[s]=s]=+t(r[s],s,r))>0&&(d+=f);for(null!=e?g.sort((function(t,r){return e(m[t],m[r])})):null!=n&&g.sort((function(t,e){return n(r[t],r[e])})),s=0,c=d?(y-p*b)/d:0;s<p;++s,v=u)l=g[s],u=v+((f=m[l])>0?f*c:0)+b,m[l]={data:r[l],index:s,value:f,startAngle:v,endAngle:u,padAngle:x};return m}return s.value=function(e){return arguments.length?(t="function"==typeof e?e:r(+e),s):t},s.sortValues=function(t){return arguments.length?(e=t,n=null,s):e},s.sort=function(t){return arguments.length?(n=t,e=null,s):n},s.startAngle=function(t){return arguments.length?(i="function"==typeof t?t:r(+t),s):i},s.endAngle=function(t){return arguments.length?(a="function"==typeof t?t:r(+t),s):a},s.padAngle=function(t){return arguments.length?(o="function"==typeof t?t:r(+t),s):o},s},t.pointRadial=R,t.radialArea=D,t.radialLine=O,t.stack=function(){var t=r([]),e=Ut,n=jt,i=Vt;function a(r){var a,o,s=t.apply(this,arguments),l=r.length,c=s.length,u=new Array(c);for(a=0;a<c;++a){for(var f,h=s[a],p=u[a]=new Array(l),d=0;d<l;++d)p[d]=f=[0,+i(r[d],h,d,r)],f.data=r[d];p.key=h}for(a=0,o=e(u);a<c;++a)u[o[a]].index=a;return n(u,o),u}return a.keys=function(e){return arguments.length?(t="function"==typeof e?e:r(F.call(e)),a):t},a.value=function(t){return arguments.length?(i="function"==typeof t?t:r(+t),a):i},a.order=function(t){return arguments.length?(e=null==t?Ut:"function"==typeof t?t:r(F.call(t)),a):e},a.offset=function(t){return arguments.length?(n=null==t?jt:t,a):n},a},t.stackOffsetDiverging=function(t,e){if((s=t.length)>0)for(var r,n,i,a,o,s,l=0,c=t[e[0]].length;l<c;++l)for(a=o=0,r=0;r<s;++r)(i=(n=t[e[r]][l])[1]-n[0])>0?(n[0]=a,n[1]=a+=i):i<0?(n[1]=o,n[0]=o+=i):(n[0]=0,n[1]=i)},t.stackOffsetExpand=function(t,e){if((n=t.length)>0){for(var r,n,i,a=0,o=t[0].length;a<o;++a){for(i=r=0;r<n;++r)i+=t[r][a][1]||0;if(i)for(r=0;r<n;++r)t[r][a][1]/=i}jt(t,e)}},t.stackOffsetNone=jt,t.stackOffsetSilhouette=function(t,e){if((r=t.length)>0){for(var r,n=0,i=t[e[0]],a=i.length;n<a;++n){for(var o=0,s=0;o<r;++o)s+=t[o][n][1]||0;i[n][1]+=i[n][0]=-s/2}jt(t,e)}},t.stackOffsetWiggle=function(t,e){if((i=t.length)>0&&(n=(r=t[e[0]]).length)>0){for(var r,n,i,a=0,o=1;o<n;++o){for(var s=0,l=0,c=0;s<i;++s){for(var u=t[e[s]],f=u[o][1]||0,h=(f-(u[o-1][1]||0))/2,p=0;p<s;++p){var d=t[e[p]];h+=(d[o][1]||0)-(d[o-1][1]||0)}l+=f,c+=h*f}r[o-1][1]+=r[o-1][0]=a,l&&(a-=c/l)}r[o-1][1]+=r[o-1][0]=a,jt(t,e)}},t.stackOrderAppearance=qt,t.stackOrderAscending=Gt,t.stackOrderDescending=function(t){return Gt(t).reverse()},t.stackOrderInsideOut=function(t){var e,r,n=t.length,i=t.map(Yt),a=qt(t),o=0,s=0,l=[],c=[];for(e=0;e<n;++e)r=a[e],o<s?(o+=i[r],l.push(r)):(s+=i[r],c.push(r));return c.reverse().concat(l)},t.stackOrderNone=Ut,t.stackOrderReverse=function(t){return Ut(t).reverse()},t.symbol=function(){var t=r(H),n=r(64),i=null;function a(){var r;if(i||(i=r=e.path()),t.apply(this,arguments).draw(i,+n.apply(this,arguments)),r)return i=null,r+""||null}return a.type=function(e){return arguments.length?(t="function"==typeof e?e:r(e),a):t},a.size=function(t){return arguments.length?(n="function"==typeof t?t:r(+t),a):n},a.context=function(t){return arguments.length?(i=null==t?null:t,a):i},a},t.symbolCircle=H,t.symbolCross=G,t.symbolDiamond=X,t.symbolSquare=$,t.symbolStar=Q,t.symbolTriangle=et,t.symbolWye=ot,t.symbols=st,Object.defineProperty(t,"__esModule",{value:!0})}))},{"d3-path":163}],166:[function(t,e,r){!function(n,i){"object"==typeof r&&"undefined"!=typeof e?i(r,t("d3-time")):i((n=n||self).d3=n.d3||{},n.d3)}(this,(function(t,e){"use strict";function r(t){if(0<=t.y&&t.y<100){var e=new Date(-1,t.m,t.d,t.H,t.M,t.S,t.L);return e.setFullYear(t.y),e}return new Date(t.y,t.m,t.d,t.H,t.M,t.S,t.L)}function n(t){if(0<=t.y&&t.y<100){var e=new Date(Date.UTC(-1,t.m,t.d,t.H,t.M,t.S,t.L));return e.setUTCFullYear(t.y),e}return new Date(Date.UTC(t.y,t.m,t.d,t.H,t.M,t.S,t.L))}function i(t,e,r){return{y:t,m:e,d:r,H:0,M:0,S:0,L:0}}function a(t){var a=t.dateTime,o=t.date,l=t.time,c=t.periods,u=t.days,f=t.shortDays,h=t.months,yt=t.shortMonths,xt=p(c),bt=d(c),_t=p(u),wt=d(u),Tt=p(f),kt=d(f),Mt=p(h),At=d(h),St=p(yt),Et=d(yt),Ct={a:function(t){return f[t.getDay()]},A:function(t){return u[t.getDay()]},b:function(t){return yt[t.getMonth()]},B:function(t){return h[t.getMonth()]},c:null,d:D,e:D,f:j,H:R,I:F,j:B,L:N,m:U,M:V,p:function(t){return c[+(t.getHours()>=12)]},q:function(t){return 1+~~(t.getMonth()/3)},Q:mt,s:vt,S:q,u:H,U:G,V:Y,w:W,W:X,x:null,X:null,y:Z,Y:J,Z:K,"%":gt},Lt={a:function(t){return f[t.getUTCDay()]},A:function(t){return u[t.getUTCDay()]},b:function(t){return yt[t.getUTCMonth()]},B:function(t){return h[t.getUTCMonth()]},c:null,d:Q,e:Q,f:nt,H:$,I:tt,j:et,L:rt,m:it,M:at,p:function(t){return c[+(t.getUTCHours()>=12)]},q:function(t){return 1+~~(t.getUTCMonth()/3)},Q:mt,s:vt,S:ot,u:st,U:lt,V:ct,w:ut,W:ft,x:null,X:null,y:ht,Y:pt,Z:dt,"%":gt},It={a:function(t,e,r){var n=Tt.exec(e.slice(r));return n?(t.w=kt[n[0].toLowerCase()],r+n[0].length):-1},A:function(t,e,r){var n=_t.exec(e.slice(r));return n?(t.w=wt[n[0].toLowerCase()],r+n[0].length):-1},b:function(t,e,r){var n=St.exec(e.slice(r));return n?(t.m=Et[n[0].toLowerCase()],r+n[0].length):-1},B:function(t,e,r){var n=Mt.exec(e.slice(r));return n?(t.m=At[n[0].toLowerCase()],r+n[0].length):-1},c:function(t,e,r){return Ot(t,a,e,r)},d:M,e:M,f:I,H:S,I:S,j:A,L:L,m:k,M:E,p:function(t,e,r){var n=xt.exec(e.slice(r));return n?(t.p=bt[n[0].toLowerCase()],r+n[0].length):-1},q:T,Q:z,s:O,S:C,u:m,U:v,V:y,w:g,W:x,x:function(t,e,r){return Ot(t,o,e,r)},X:function(t,e,r){return Ot(t,l,e,r)},y:_,Y:b,Z:w,"%":P};function Pt(t,e){return function(r){var n,i,a,o=[],l=-1,c=0,u=t.length;for(r instanceof Date||(r=new Date(+r));++l<u;)37===t.charCodeAt(l)&&(o.push(t.slice(c,l)),null!=(i=s[n=t.charAt(++l)])?n=t.charAt(++l):i="e"===n?" ":"0",(a=e[n])&&(n=a(r,i)),o.push(n),c=l+1);return o.push(t.slice(c,l)),o.join("")}}function zt(t,a){return function(o){var s,l,c=i(1900,void 0,1);if(Ot(c,t,o+="",0)!=o.length)return null;if("Q"in c)return new Date(c.Q);if("s"in c)return new Date(1e3*c.s+("L"in c?c.L:0));if(a&&!("Z"in c)&&(c.Z=0),"p"in c&&(c.H=c.H%12+12*c.p),void 0===c.m&&(c.m="q"in c?c.q:0),"V"in c){if(c.V<1||c.V>53)return null;"w"in c||(c.w=1),"Z"in c?(l=(s=n(i(c.y,0,1))).getUTCDay(),s=l>4||0===l?e.utcMonday.ceil(s):e.utcMonday(s),s=e.utcDay.offset(s,7*(c.V-1)),c.y=s.getUTCFullYear(),c.m=s.getUTCMonth(),c.d=s.getUTCDate()+(c.w+6)%7):(l=(s=r(i(c.y,0,1))).getDay(),s=l>4||0===l?e.timeMonday.ceil(s):e.timeMonday(s),s=e.timeDay.offset(s,7*(c.V-1)),c.y=s.getFullYear(),c.m=s.getMonth(),c.d=s.getDate()+(c.w+6)%7)}else("W"in c||"U"in c)&&("w"in c||(c.w="u"in c?c.u%7:"W"in c?1:0),l="Z"in c?n(i(c.y,0,1)).getUTCDay():r(i(c.y,0,1)).getDay(),c.m=0,c.d="W"in c?(c.w+6)%7+7*c.W-(l+5)%7:c.w+7*c.U-(l+6)%7);return"Z"in c?(c.H+=c.Z/100|0,c.M+=c.Z%100,n(c)):r(c)}}function Ot(t,e,r,n){for(var i,a,o=0,l=e.length,c=r.length;o<l;){if(n>=c)return-1;if(37===(i=e.charCodeAt(o++))){if(i=e.charAt(o++),!(a=It[i in s?e.charAt(o++):i])||(n=a(t,r,n))<0)return-1}else if(i!=r.charCodeAt(n++))return-1}return n}return Ct.x=Pt(o,Ct),Ct.X=Pt(l,Ct),Ct.c=Pt(a,Ct),Lt.x=Pt(o,Lt),Lt.X=Pt(l,Lt),Lt.c=Pt(a,Lt),{format:function(t){var e=Pt(t+="",Ct);return e.toString=function(){return t},e},parse:function(t){var e=zt(t+="",!1);return e.toString=function(){return t},e},utcFormat:function(t){var e=Pt(t+="",Lt);return e.toString=function(){return t},e},utcParse:function(t){var e=zt(t+="",!0);return e.toString=function(){return t},e}}}var o,s={"-":"",_:" ",0:"0"},l=/^\s*\d+/,c=/^%/,u=/[\\^$*+?|[\]().{}]/g;function f(t,e,r){var n=t<0?"-":"",i=(n?-t:t)+"",a=i.length;return n+(a<r?new Array(r-a+1).join(e)+i:i)}function h(t){return t.replace(u,"\\$&")}function p(t){return new RegExp("^(?:"+t.map(h).join("|")+")","i")}function d(t){for(var e={},r=-1,n=t.length;++r<n;)e[t[r].toLowerCase()]=r;return e}function g(t,e,r){var n=l.exec(e.slice(r,r+1));return n?(t.w=+n[0],r+n[0].length):-1}function m(t,e,r){var n=l.exec(e.slice(r,r+1));return n?(t.u=+n[0],r+n[0].length):-1}function v(t,e,r){var n=l.exec(e.slice(r,r+2));return n?(t.U=+n[0],r+n[0].length):-1}function y(t,e,r){var n=l.exec(e.slice(r,r+2));return n?(t.V=+n[0],r+n[0].length):-1}function x(t,e,r){var n=l.exec(e.slice(r,r+2));return n?(t.W=+n[0],r+n[0].length):-1}function b(t,e,r){var n=l.exec(e.slice(r,r+4));return n?(t.y=+n[0],r+n[0].length):-1}function _(t,e,r){var n=l.exec(e.slice(r,r+2));return n?(t.y=+n[0]+(+n[0]>68?1900:2e3),r+n[0].length):-1}function w(t,e,r){var n=/^(Z)|([+-]\d\d)(?::?(\d\d))?/.exec(e.slice(r,r+6));return n?(t.Z=n[1]?0:-(n[2]+(n[3]||"00")),r+n[0].length):-1}function T(t,e,r){var n=l.exec(e.slice(r,r+1));return n?(t.q=3*n[0]-3,r+n[0].length):-1}function k(t,e,r){var n=l.exec(e.slice(r,r+2));return n?(t.m=n[0]-1,r+n[0].length):-1}function M(t,e,r){var n=l.exec(e.slice(r,r+2));return n?(t.d=+n[0],r+n[0].length):-1}function A(t,e,r){var n=l.exec(e.slice(r,r+3));return n?(t.m=0,t.d=+n[0],r+n[0].length):-1}function S(t,e,r){var n=l.exec(e.slice(r,r+2));return n?(t.H=+n[0],r+n[0].length):-1}function E(t,e,r){var n=l.exec(e.slice(r,r+2));return n?(t.M=+n[0],r+n[0].length):-1}function C(t,e,r){var n=l.exec(e.slice(r,r+2));return n?(t.S=+n[0],r+n[0].length):-1}function L(t,e,r){var n=l.exec(e.slice(r,r+3));return n?(t.L=+n[0],r+n[0].length):-1}function I(t,e,r){var n=l.exec(e.slice(r,r+6));return n?(t.L=Math.floor(n[0]/1e3),r+n[0].length):-1}function P(t,e,r){var n=c.exec(e.slice(r,r+1));return n?r+n[0].length:-1}function z(t,e,r){var n=l.exec(e.slice(r));return n?(t.Q=+n[0],r+n[0].length):-1}function O(t,e,r){var n=l.exec(e.slice(r));return n?(t.s=+n[0],r+n[0].length):-1}function D(t,e){return f(t.getDate(),e,2)}function R(t,e){return f(t.getHours(),e,2)}function F(t,e){return f(t.getHours()%12||12,e,2)}function B(t,r){return f(1+e.timeDay.count(e.timeYear(t),t),r,3)}function N(t,e){return f(t.getMilliseconds(),e,3)}function j(t,e){return N(t,e)+"000"}function U(t,e){return f(t.getMonth()+1,e,2)}function V(t,e){return f(t.getMinutes(),e,2)}function q(t,e){return f(t.getSeconds(),e,2)}function H(t){var e=t.getDay();return 0===e?7:e}function G(t,r){return f(e.timeSunday.count(e.timeYear(t)-1,t),r,2)}function Y(t,r){var n=t.getDay();return t=n>=4||0===n?e.timeThursday(t):e.timeThursday.ceil(t),f(e.timeThursday.count(e.timeYear(t),t)+(4===e.timeYear(t).getDay()),r,2)}function W(t){return t.getDay()}function X(t,r){return f(e.timeMonday.count(e.timeYear(t)-1,t),r,2)}function Z(t,e){return f(t.getFullYear()%100,e,2)}function J(t,e){return f(t.getFullYear()%1e4,e,4)}function K(t){var e=t.getTimezoneOffset();return(e>0?"-":(e*=-1,"+"))+f(e/60|0,"0",2)+f(e%60,"0",2)}function Q(t,e){return f(t.getUTCDate(),e,2)}function $(t,e){return f(t.getUTCHours(),e,2)}function tt(t,e){return f(t.getUTCHours()%12||12,e,2)}function et(t,r){return f(1+e.utcDay.count(e.utcYear(t),t),r,3)}function rt(t,e){return f(t.getUTCMilliseconds(),e,3)}function nt(t,e){return rt(t,e)+"000"}function it(t,e){return f(t.getUTCMonth()+1,e,2)}function at(t,e){return f(t.getUTCMinutes(),e,2)}function ot(t,e){return f(t.getUTCSeconds(),e,2)}function st(t){var e=t.getUTCDay();return 0===e?7:e}function lt(t,r){return f(e.utcSunday.count(e.utcYear(t)-1,t),r,2)}function ct(t,r){var n=t.getUTCDay();return t=n>=4||0===n?e.utcThursday(t):e.utcThursday.ceil(t),f(e.utcThursday.count(e.utcYear(t),t)+(4===e.utcYear(t).getUTCDay()),r,2)}function ut(t){return t.getUTCDay()}function ft(t,r){return f(e.utcMonday.count(e.utcYear(t)-1,t),r,2)}function ht(t,e){return f(t.getUTCFullYear()%100,e,2)}function pt(t,e){return f(t.getUTCFullYear()%1e4,e,4)}function dt(){return"+0000"}function gt(){return"%"}function mt(t){return+t}function vt(t){return Math.floor(+t/1e3)}function yt(e){return o=a(e),t.timeFormat=o.format,t.timeParse=o.parse,t.utcFormat=o.utcFormat,t.utcParse=o.utcParse,o}yt({dateTime:"%x, %X",date:"%-m/%-d/%Y",time:"%-I:%M:%S %p",periods:["AM","PM"],days:["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"],shortDays:["Sun","Mon","Tue","Wed","Thu","Fri","Sat"],months:["January","February","March","April","May","June","July","August","September","October","November","December"],shortMonths:["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"]});var xt=Date.prototype.toISOString?function(t){return t.toISOString()}:t.utcFormat("%Y-%m-%dT%H:%M:%S.%LZ");var bt=+new Date("2000-01-01T00:00:00.000Z")?function(t){var e=new Date(t);return isNaN(e)?null:e}:t.utcParse("%Y-%m-%dT%H:%M:%S.%LZ");t.isoFormat=xt,t.isoParse=bt,t.timeFormatDefaultLocale=yt,t.timeFormatLocale=a,Object.defineProperty(t,"__esModule",{value:!0})}))},{"d3-time":167}],167:[function(t,e,r){!function(t,n){"object"==typeof r&&"undefined"!=typeof e?n(r):n((t=t||self).d3=t.d3||{})}(this,(function(t){"use strict";var e=new Date,r=new Date;function n(t,i,a,o){function s(e){return t(e=0===arguments.length?new Date:new Date(+e)),e}return s.floor=function(e){return t(e=new Date(+e)),e},s.ceil=function(e){return t(e=new Date(e-1)),i(e,1),t(e),e},s.round=function(t){var e=s(t),r=s.ceil(t);return t-e<r-t?e:r},s.offset=function(t,e){return i(t=new Date(+t),null==e?1:Math.floor(e)),t},s.range=function(e,r,n){var a,o=[];if(e=s.ceil(e),n=null==n?1:Math.floor(n),!(e<r&&n>0))return o;do{o.push(a=new Date(+e)),i(e,n),t(e)}while(a<e&&e<r);return o},s.filter=function(e){return n((function(r){if(r>=r)for(;t(r),!e(r);)r.setTime(r-1)}),(function(t,r){if(t>=t)if(r<0)for(;++r<=0;)for(;i(t,-1),!e(t););else for(;--r>=0;)for(;i(t,1),!e(t););}))},a&&(s.count=function(n,i){return e.setTime(+n),r.setTime(+i),t(e),t(r),Math.floor(a(e,r))},s.every=function(t){return t=Math.floor(t),isFinite(t)&&t>0?t>1?s.filter(o?function(e){return o(e)%t==0}:function(e){return s.count(0,e)%t==0}):s:null}),s}var i=n((function(){}),(function(t,e){t.setTime(+t+e)}),(function(t,e){return e-t}));i.every=function(t){return t=Math.floor(t),isFinite(t)&&t>0?t>1?n((function(e){e.setTime(Math.floor(e/t)*t)}),(function(e,r){e.setTime(+e+r*t)}),(function(e,r){return(r-e)/t})):i:null};var a=i.range,o=n((function(t){t.setTime(t-t.getMilliseconds())}),(function(t,e){t.setTime(+t+1e3*e)}),(function(t,e){return(e-t)/1e3}),(function(t){return t.getUTCSeconds()})),s=o.range,l=n((function(t){t.setTime(t-t.getMilliseconds()-1e3*t.getSeconds())}),(function(t,e){t.setTime(+t+6e4*e)}),(function(t,e){return(e-t)/6e4}),(function(t){return t.getMinutes()})),c=l.range,u=n((function(t){t.setTime(t-t.getMilliseconds()-1e3*t.getSeconds()-6e4*t.getMinutes())}),(function(t,e){t.setTime(+t+36e5*e)}),(function(t,e){return(e-t)/36e5}),(function(t){return t.getHours()})),f=u.range,h=n((function(t){t.setHours(0,0,0,0)}),(function(t,e){t.setDate(t.getDate()+e)}),(function(t,e){return(e-t-6e4*(e.getTimezoneOffset()-t.getTimezoneOffset()))/864e5}),(function(t){return t.getDate()-1})),p=h.range;function d(t){return n((function(e){e.setDate(e.getDate()-(e.getDay()+7-t)%7),e.setHours(0,0,0,0)}),(function(t,e){t.setDate(t.getDate()+7*e)}),(function(t,e){return(e-t-6e4*(e.getTimezoneOffset()-t.getTimezoneOffset()))/6048e5}))}var g=d(0),m=d(1),v=d(2),y=d(3),x=d(4),b=d(5),_=d(6),w=g.range,T=m.range,k=v.range,M=y.range,A=x.range,S=b.range,E=_.range,C=n((function(t){t.setDate(1),t.setHours(0,0,0,0)}),(function(t,e){t.setMonth(t.getMonth()+e)}),(function(t,e){return e.getMonth()-t.getMonth()+12*(e.getFullYear()-t.getFullYear())}),(function(t){return t.getMonth()})),L=C.range,I=n((function(t){t.setMonth(0,1),t.setHours(0,0,0,0)}),(function(t,e){t.setFullYear(t.getFullYear()+e)}),(function(t,e){return e.getFullYear()-t.getFullYear()}),(function(t){return t.getFullYear()}));I.every=function(t){return isFinite(t=Math.floor(t))&&t>0?n((function(e){e.setFullYear(Math.floor(e.getFullYear()/t)*t),e.setMonth(0,1),e.setHours(0,0,0,0)}),(function(e,r){e.setFullYear(e.getFullYear()+r*t)})):null};var P=I.range,z=n((function(t){t.setUTCSeconds(0,0)}),(function(t,e){t.setTime(+t+6e4*e)}),(function(t,e){return(e-t)/6e4}),(function(t){return t.getUTCMinutes()})),O=z.range,D=n((function(t){t.setUTCMinutes(0,0,0)}),(function(t,e){t.setTime(+t+36e5*e)}),(function(t,e){return(e-t)/36e5}),(function(t){return t.getUTCHours()})),R=D.range,F=n((function(t){t.setUTCHours(0,0,0,0)}),(function(t,e){t.setUTCDate(t.getUTCDate()+e)}),(function(t,e){return(e-t)/864e5}),(function(t){return t.getUTCDate()-1})),B=F.range;function N(t){return n((function(e){e.setUTCDate(e.getUTCDate()-(e.getUTCDay()+7-t)%7),e.setUTCHours(0,0,0,0)}),(function(t,e){t.setUTCDate(t.getUTCDate()+7*e)}),(function(t,e){return(e-t)/6048e5}))}var j=N(0),U=N(1),V=N(2),q=N(3),H=N(4),G=N(5),Y=N(6),W=j.range,X=U.range,Z=V.range,J=q.range,K=H.range,Q=G.range,$=Y.range,tt=n((function(t){t.setUTCDate(1),t.setUTCHours(0,0,0,0)}),(function(t,e){t.setUTCMonth(t.getUTCMonth()+e)}),(function(t,e){return e.getUTCMonth()-t.getUTCMonth()+12*(e.getUTCFullYear()-t.getUTCFullYear())}),(function(t){return t.getUTCMonth()})),et=tt.range,rt=n((function(t){t.setUTCMonth(0,1),t.setUTCHours(0,0,0,0)}),(function(t,e){t.setUTCFullYear(t.getUTCFullYear()+e)}),(function(t,e){return e.getUTCFullYear()-t.getUTCFullYear()}),(function(t){return t.getUTCFullYear()}));rt.every=function(t){return isFinite(t=Math.floor(t))&&t>0?n((function(e){e.setUTCFullYear(Math.floor(e.getUTCFullYear()/t)*t),e.setUTCMonth(0,1),e.setUTCHours(0,0,0,0)}),(function(e,r){e.setUTCFullYear(e.getUTCFullYear()+r*t)})):null};var nt=rt.range;t.timeDay=h,t.timeDays=p,t.timeFriday=b,t.timeFridays=S,t.timeHour=u,t.timeHours=f,t.timeInterval=n,t.timeMillisecond=i,t.timeMilliseconds=a,t.timeMinute=l,t.timeMinutes=c,t.timeMonday=m,t.timeMondays=T,t.timeMonth=C,t.timeMonths=L,t.timeSaturday=_,t.timeSaturdays=E,t.timeSecond=o,t.timeSeconds=s,t.timeSunday=g,t.timeSundays=w,t.timeThursday=x,t.timeThursdays=A,t.timeTuesday=v,t.timeTuesdays=k,t.timeWednesday=y,t.timeWednesdays=M,t.timeWeek=g,t.timeWeeks=w,t.timeYear=I,t.timeYears=P,t.utcDay=F,t.utcDays=B,t.utcFriday=G,t.utcFridays=Q,t.utcHour=D,t.utcHours=R,t.utcMillisecond=i,t.utcMilliseconds=a,t.utcMinute=z,t.utcMinutes=O,t.utcMonday=U,t.utcMondays=X,t.utcMonth=tt,t.utcMonths=et,t.utcSaturday=Y,t.utcSaturdays=$,t.utcSecond=o,t.utcSeconds=s,t.utcSunday=j,t.utcSundays=W,t.utcThursday=H,t.utcThursdays=K,t.utcTuesday=V,t.utcTuesdays=Z,t.utcWednesday=q,t.utcWednesdays=J,t.utcWeek=j,t.utcWeeks=W,t.utcYear=rt,t.utcYears=nt,Object.defineProperty(t,"__esModule",{value:!0})}))},{}],168:[function(t,e,r){!function(t,n){"object"==typeof r&&"undefined"!=typeof e?n(r):n((t=t||self).d3=t.d3||{})}(this,(function(t){"use strict";var e,r,n=0,i=0,a=0,o=0,s=0,l=0,c="object"==typeof performance&&performance.now?performance:Date,u="object"==typeof window&&window.requestAnimationFrame?window.requestAnimationFrame.bind(window):function(t){setTimeout(t,17)};function f(){return s||(u(h),s=c.now()+l)}function h(){s=0}function p(){this._call=this._time=this._next=null}function d(t,e,r){var n=new p;return n.restart(t,e,r),n}function g(){f(),++n;for(var t,r=e;r;)(t=s-r._time)>=0&&r._call.call(null,t),r=r._next;--n}function m(){s=(o=c.now())+l,n=i=0;try{g()}finally{n=0,function(){var t,n,i=e,a=1/0;for(;i;)i._call?(a>i._time&&(a=i._time),t=i,i=i._next):(n=i._next,i._next=null,i=t?t._next=n:e=n);r=t,y(a)}(),s=0}}function v(){var t=c.now(),e=t-o;e>1e3&&(l-=e,o=t)}function y(t){n||(i&&(i=clearTimeout(i)),t-s>24?(t<1/0&&(i=setTimeout(m,t-c.now()-l)),a&&(a=clearInterval(a))):(a||(o=c.now(),a=setInterval(v,1e3)),n=1,u(m)))}p.prototype=d.prototype={constructor:p,restart:function(t,n,i){if("function"!=typeof t)throw new TypeError("callback is not a function");i=(null==i?f():+i)+(null==n?0:+n),this._next||r===this||(r?r._next=this:e=this,r=this),this._call=t,this._time=i,y()},stop:function(){this._call&&(this._call=null,this._time=1/0,y())}},t.interval=function(t,e,r){var n=new p,i=e;return null==e?(n.restart(t,e,r),n):(e=+e,r=null==r?f():+r,n.restart((function a(o){o+=i,n.restart(a,i+=e,r),t(o)}),e,r),n)},t.now=f,t.timeout=function(t,e,r){var n=new p;return e=null==e?0:+e,n.restart((function(r){n.stop(),t(r+e)}),e,r),n},t.timer=d,t.timerFlush=g,Object.defineProperty(t,"__esModule",{value:!0})}))},{}],169:[function(t,e,r){!function(){var t={version:"3.5.17"},r=[].slice,n=function(t){return r.call(t)},i=this.document;function a(t){return t&&(t.ownerDocument||t.document||t).documentElement}function o(t){return t&&(t.ownerDocument&&t.ownerDocument.defaultView||t.document&&t||t.defaultView)}if(i)try{n(i.documentElement.childNodes)[0].nodeType}catch(t){n=function(t){for(var e=t.length,r=new Array(e);e--;)r[e]=t[e];return r}}if(Date.now||(Date.now=function(){return+new Date}),i)try{i.createElement("DIV").style.setProperty("opacity",0,"")}catch(t){var s=this.Element.prototype,l=s.setAttribute,c=s.setAttributeNS,u=this.CSSStyleDeclaration.prototype,f=u.setProperty;s.setAttribute=function(t,e){l.call(this,t,e+"")},s.setAttributeNS=function(t,e,r){c.call(this,t,e,r+"")},u.setProperty=function(t,e,r){f.call(this,t,e+"",r)}}function h(t,e){return t<e?-1:t>e?1:t>=e?0:NaN}function p(t){return null===t?NaN:+t}function d(t){return!isNaN(t)}function g(t){return{left:function(e,r,n,i){for(arguments.length<3&&(n=0),arguments.length<4&&(i=e.length);n<i;){var a=n+i>>>1;t(e[a],r)<0?n=a+1:i=a}return n},right:function(e,r,n,i){for(arguments.length<3&&(n=0),arguments.length<4&&(i=e.length);n<i;){var a=n+i>>>1;t(e[a],r)>0?i=a:n=a+1}return n}}}t.ascending=h,t.descending=function(t,e){return e<t?-1:e>t?1:e>=t?0:NaN},t.min=function(t,e){var r,n,i=-1,a=t.length;if(1===arguments.length){for(;++i<a;)if(null!=(n=t[i])&&n>=n){r=n;break}for(;++i<a;)null!=(n=t[i])&&r>n&&(r=n)}else{for(;++i<a;)if(null!=(n=e.call(t,t[i],i))&&n>=n){r=n;break}for(;++i<a;)null!=(n=e.call(t,t[i],i))&&r>n&&(r=n)}return r},t.max=function(t,e){var r,n,i=-1,a=t.length;if(1===arguments.length){for(;++i<a;)if(null!=(n=t[i])&&n>=n){r=n;break}for(;++i<a;)null!=(n=t[i])&&n>r&&(r=n)}else{for(;++i<a;)if(null!=(n=e.call(t,t[i],i))&&n>=n){r=n;break}for(;++i<a;)null!=(n=e.call(t,t[i],i))&&n>r&&(r=n)}return r},t.extent=function(t,e){var r,n,i,a=-1,o=t.length;if(1===arguments.length){for(;++a<o;)if(null!=(n=t[a])&&n>=n){r=i=n;break}for(;++a<o;)null!=(n=t[a])&&(r>n&&(r=n),i<n&&(i=n))}else{for(;++a<o;)if(null!=(n=e.call(t,t[a],a))&&n>=n){r=i=n;break}for(;++a<o;)null!=(n=e.call(t,t[a],a))&&(r>n&&(r=n),i<n&&(i=n))}return[r,i]},t.sum=function(t,e){var r,n=0,i=t.length,a=-1;if(1===arguments.length)for(;++a<i;)d(r=+t[a])&&(n+=r);else for(;++a<i;)d(r=+e.call(t,t[a],a))&&(n+=r);return n},t.mean=function(t,e){var r,n=0,i=t.length,a=-1,o=i;if(1===arguments.length)for(;++a<i;)d(r=p(t[a]))?n+=r:--o;else for(;++a<i;)d(r=p(e.call(t,t[a],a)))?n+=r:--o;if(o)return n/o},t.quantile=function(t,e){var r=(t.length-1)*e+1,n=Math.floor(r),i=+t[n-1],a=r-n;return a?i+a*(t[n]-i):i},t.median=function(e,r){var n,i=[],a=e.length,o=-1;if(1===arguments.length)for(;++o<a;)d(n=p(e[o]))&&i.push(n);else for(;++o<a;)d(n=p(r.call(e,e[o],o)))&&i.push(n);if(i.length)return t.quantile(i.sort(h),.5)},t.variance=function(t,e){var r,n,i=t.length,a=0,o=0,s=-1,l=0;if(1===arguments.length)for(;++s<i;)d(r=p(t[s]))&&(o+=(n=r-a)*(r-(a+=n/++l)));else for(;++s<i;)d(r=p(e.call(t,t[s],s)))&&(o+=(n=r-a)*(r-(a+=n/++l)));if(l>1)return o/(l-1)},t.deviation=function(){var e=t.variance.apply(this,arguments);return e?Math.sqrt(e):e};var m=g(h);function v(t){return t.length}t.bisectLeft=m.left,t.bisect=t.bisectRight=m.right,t.bisector=function(t){return g(1===t.length?function(e,r){return h(t(e),r)}:t)},t.shuffle=function(t,e,r){(a=arguments.length)<3&&(r=t.length,a<2&&(e=0));for(var n,i,a=r-e;a;)i=Math.random()*a--|0,n=t[a+e],t[a+e]=t[i+e],t[i+e]=n;return t},t.permute=function(t,e){for(var r=e.length,n=new Array(r);r--;)n[r]=t[e[r]];return n},t.pairs=function(t){for(var e=0,r=t.length-1,n=t[0],i=new Array(r<0?0:r);e<r;)i[e]=[n,n=t[++e]];return i},t.transpose=function(e){if(!(a=e.length))return[];for(var r=-1,n=t.min(e,v),i=new Array(n);++r<n;)for(var a,o=-1,s=i[r]=new Array(a);++o<a;)s[o]=e[o][r];return i},t.zip=function(){return t.transpose(arguments)},t.keys=function(t){var e=[];for(var r in t)e.push(r);return e},t.values=function(t){var e=[];for(var r in t)e.push(t[r]);return e},t.entries=function(t){var e=[];for(var r in t)e.push({key:r,value:t[r]});return e},t.merge=function(t){for(var e,r,n,i=t.length,a=-1,o=0;++a<i;)o+=t[a].length;for(r=new Array(o);--i>=0;)for(e=(n=t[i]).length;--e>=0;)r[--o]=n[e];return r};var y=Math.abs;function x(t){for(var e=1;t*e%1;)e*=10;return e}function b(t,e){for(var r in e)Object.defineProperty(t.prototype,r,{value:e[r],enumerable:!1})}function _(){this._=Object.create(null)}t.range=function(t,e,r){if(arguments.length<3&&(r=1,arguments.length<2&&(e=t,t=0)),(e-t)/r==1/0)throw new Error("infinite range");var n,i=[],a=x(y(r)),o=-1;if(t*=a,e*=a,(r*=a)<0)for(;(n=t+r*++o)>e;)i.push(n/a);else for(;(n=t+r*++o)<e;)i.push(n/a);return i},t.map=function(t,e){var r=new _;if(t instanceof _)t.forEach((function(t,e){r.set(t,e)}));else if(Array.isArray(t)){var n,i=-1,a=t.length;if(1===arguments.length)for(;++i<a;)r.set(i,t[i]);else for(;++i<a;)r.set(e.call(t,n=t[i],i),n)}else for(var o in t)r.set(o,t[o]);return r};function w(t){return"__proto__"==(t+="")||"\0"===t[0]?"\0"+t:t}function T(t){return"\0"===(t+="")[0]?t.slice(1):t}function k(t){return w(t)in this._}function M(t){return(t=w(t))in this._&&delete this._[t]}function A(){var t=[];for(var e in this._)t.push(T(e));return t}function S(){var t=0;for(var e in this._)++t;return t}function E(){for(var t in this._)return!1;return!0}function C(){this._=Object.create(null)}function L(t){return t}function I(t,e,r){return function(){var n=r.apply(e,arguments);return n===e?t:n}}function P(t,e){if(e in t)return e;e=e.charAt(0).toUpperCase()+e.slice(1);for(var r=0,n=z.length;r<n;++r){var i=z[r]+e;if(i in t)return i}}b(_,{has:k,get:function(t){return this._[w(t)]},set:function(t,e){return this._[w(t)]=e},remove:M,keys:A,values:function(){var t=[];for(var e in this._)t.push(this._[e]);return t},entries:function(){var t=[];for(var e in this._)t.push({key:T(e),value:this._[e]});return t},size:S,empty:E,forEach:function(t){for(var e in this._)t.call(this,T(e),this._[e])}}),t.nest=function(){var e,r,n={},i=[],a=[];function o(t,a,s){if(s>=i.length)return r?r.call(n,a):e?a.sort(e):a;for(var l,c,u,f,h=-1,p=a.length,d=i[s++],g=new _;++h<p;)(f=g.get(l=d(c=a[h])))?f.push(c):g.set(l,[c]);return t?(c=t(),u=function(e,r){c.set(e,o(t,r,s))}):(c={},u=function(e,r){c[e]=o(t,r,s)}),g.forEach(u),c}return n.map=function(t,e){return o(e,t,0)},n.entries=function(e){return function t(e,r){if(r>=i.length)return e;var n=[],o=a[r++];return e.forEach((function(e,i){n.push({key:e,values:t(i,r)})})),o?n.sort((function(t,e){return o(t.key,e.key)})):n}(o(t.map,e,0),0)},n.key=function(t){return i.push(t),n},n.sortKeys=function(t){return a[i.length-1]=t,n},n.sortValues=function(t){return e=t,n},n.rollup=function(t){return r=t,n},n},t.set=function(t){var e=new C;if(t)for(var r=0,n=t.length;r<n;++r)e.add(t[r]);return e},b(C,{has:k,add:function(t){return this._[w(t+="")]=!0,t},remove:M,values:A,size:S,empty:E,forEach:function(t){for(var e in this._)t.call(this,T(e))}}),t.behavior={},t.rebind=function(t,e){for(var r,n=1,i=arguments.length;++n<i;)t[r=arguments[n]]=I(t,e,e[r]);return t};var z=["webkit","ms","moz","Moz","o","O"];function O(){}function D(){}function R(t){var e=[],r=new _;function n(){for(var r,n=e,i=-1,a=n.length;++i<a;)(r=n[i].on)&&r.apply(this,arguments);return t}return n.on=function(n,i){var a,o=r.get(n);return arguments.length<2?o&&o.on:(o&&(o.on=null,e=e.slice(0,a=e.indexOf(o)).concat(e.slice(a+1)),r.remove(n)),i&&e.push(r.set(n,{on:i})),t)},n}function F(){t.event.preventDefault()}function B(){for(var e,r=t.event;e=r.sourceEvent;)r=e;return r}function N(e){for(var r=new D,n=0,i=arguments.length;++n<i;)r[arguments[n]]=R(r);return r.of=function(n,i){return function(a){try{var o=a.sourceEvent=t.event;a.target=e,t.event=a,r[a.type].apply(n,i)}finally{t.event=o}}},r}t.dispatch=function(){for(var t=new D,e=-1,r=arguments.length;++e<r;)t[arguments[e]]=R(t);return t},D.prototype.on=function(t,e){var r=t.indexOf("."),n="";if(r>=0&&(n=t.slice(r+1),t=t.slice(0,r)),t)return arguments.length<2?this[t].on(n):this[t].on(n,e);if(2===arguments.length){if(null==e)for(t in this)this.hasOwnProperty(t)&&this[t].on(n,null);return this}},t.event=null,t.requote=function(t){return t.replace(j,"\\$&")};var j=/[\\\^\$\*\+\?\|\[\]\(\)\.\{\}]/g,U={}.__proto__?function(t,e){t.__proto__=e}:function(t,e){for(var r in e)t[r]=e[r]};function V(t){return U(t,Y),t}var q=function(t,e){return e.querySelector(t)},H=function(t,e){return e.querySelectorAll(t)},G=function(t,e){var r=t.matches||t[P(t,"matchesSelector")];return(G=function(t,e){return r.call(t,e)})(t,e)};"function"==typeof Sizzle&&(q=function(t,e){return Sizzle(t,e)[0]||null},H=Sizzle,G=Sizzle.matchesSelector),t.selection=function(){return t.select(i.documentElement)};var Y=t.selection.prototype=[];function W(t){return"function"==typeof t?t:function(){return q(t,this)}}function X(t){return"function"==typeof t?t:function(){return H(t,this)}}Y.select=function(t){var e,r,n,i,a=[];t=W(t);for(var o=-1,s=this.length;++o<s;){a.push(e=[]),e.parentNode=(n=this[o]).parentNode;for(var l=-1,c=n.length;++l<c;)(i=n[l])?(e.push(r=t.call(i,i.__data__,l,o)),r&&"__data__"in i&&(r.__data__=i.__data__)):e.push(null)}return V(a)},Y.selectAll=function(t){var e,r,i=[];t=X(t);for(var a=-1,o=this.length;++a<o;)for(var s=this[a],l=-1,c=s.length;++l<c;)(r=s[l])&&(i.push(e=n(t.call(r,r.__data__,l,a))),e.parentNode=r);return V(i)};var Z="http://www.w3.org/1999/xhtml",J={svg:"http://www.w3.org/2000/svg",xhtml:Z,xlink:"http://www.w3.org/1999/xlink",xml:"http://www.w3.org/XML/1998/namespace",xmlns:"http://www.w3.org/2000/xmlns/"};function K(e,r){return e=t.ns.qualify(e),null==r?e.local?function(){this.removeAttributeNS(e.space,e.local)}:function(){this.removeAttribute(e)}:"function"==typeof r?e.local?function(){var t=r.apply(this,arguments);null==t?this.removeAttributeNS(e.space,e.local):this.setAttributeNS(e.space,e.local,t)}:function(){var t=r.apply(this,arguments);null==t?this.removeAttribute(e):this.setAttribute(e,t)}:e.local?function(){this.setAttributeNS(e.space,e.local,r)}:function(){this.setAttribute(e,r)}}function Q(t){return t.trim().replace(/\s+/g," ")}function $(e){return new RegExp("(?:^|\\s+)"+t.requote(e)+"(?:\\s+|$)","g")}function tt(t){return(t+"").trim().split(/^|\s+/)}function et(t,e){var r=(t=tt(t).map(rt)).length;return"function"==typeof e?function(){for(var n=-1,i=e.apply(this,arguments);++n<r;)t[n](this,i)}:function(){for(var n=-1;++n<r;)t[n](this,e)}}function rt(t){var e=$(t);return function(r,n){if(i=r.classList)return n?i.add(t):i.remove(t);var i=r.getAttribute("class")||"";n?(e.lastIndex=0,e.test(i)||r.setAttribute("class",Q(i+" "+t))):r.setAttribute("class",Q(i.replace(e," ")))}}function nt(t,e,r){return null==e?function(){this.style.removeProperty(t)}:"function"==typeof e?function(){var n=e.apply(this,arguments);null==n?this.style.removeProperty(t):this.style.setProperty(t,n,r)}:function(){this.style.setProperty(t,e,r)}}function it(t,e){return null==e?function(){delete this[t]}:"function"==typeof e?function(){var r=e.apply(this,arguments);null==r?delete this[t]:this[t]=r}:function(){this[t]=e}}function at(e){return"function"==typeof e?e:(e=t.ns.qualify(e)).local?function(){return this.ownerDocument.createElementNS(e.space,e.local)}:function(){var t=this.ownerDocument,r=this.namespaceURI;return r===Z&&t.documentElement.namespaceURI===Z?t.createElement(e):t.createElementNS(r,e)}}function ot(){var t=this.parentNode;t&&t.removeChild(this)}function st(t){return{__data__:t}}function lt(t){return function(){return G(this,t)}}function ct(t){return arguments.length||(t=h),function(e,r){return e&&r?t(e.__data__,r.__data__):!e-!r}}function ut(t,e){for(var r=0,n=t.length;r<n;r++)for(var i,a=t[r],o=0,s=a.length;o<s;o++)(i=a[o])&&e(i,o,r);return t}function ft(t){return U(t,ht),t}t.ns={prefix:J,qualify:function(t){var e=t.indexOf(":"),r=t;return e>=0&&"xmlns"!==(r=t.slice(0,e))&&(t=t.slice(e+1)),J.hasOwnProperty(r)?{space:J[r],local:t}:t}},Y.attr=function(e,r){if(arguments.length<2){if("string"==typeof e){var n=this.node();return(e=t.ns.qualify(e)).local?n.getAttributeNS(e.space,e.local):n.getAttribute(e)}for(r in e)this.each(K(r,e[r]));return this}return this.each(K(e,r))},Y.classed=function(t,e){if(arguments.length<2){if("string"==typeof t){var r=this.node(),n=(t=tt(t)).length,i=-1;if(e=r.classList){for(;++i<n;)if(!e.contains(t[i]))return!1}else for(e=r.getAttribute("class");++i<n;)if(!$(t[i]).test(e))return!1;return!0}for(e in t)this.each(et(e,t[e]));return this}return this.each(et(t,e))},Y.style=function(t,e,r){var n=arguments.length;if(n<3){if("string"!=typeof t){for(r in n<2&&(e=""),t)this.each(nt(r,t[r],e));return this}if(n<2){var i=this.node();return o(i).getComputedStyle(i,null).getPropertyValue(t)}r=""}return this.each(nt(t,e,r))},Y.property=function(t,e){if(arguments.length<2){if("string"==typeof t)return this.node()[t];for(e in t)this.each(it(e,t[e]));return this}return this.each(it(t,e))},Y.text=function(t){return arguments.length?this.each("function"==typeof t?function(){var e=t.apply(this,arguments);this.textContent=null==e?"":e}:null==t?function(){this.textContent=""}:function(){this.textContent=t}):this.node().textContent},Y.html=function(t){return arguments.length?this.each("function"==typeof t?function(){var e=t.apply(this,arguments);this.innerHTML=null==e?"":e}:null==t?function(){this.innerHTML=""}:function(){this.innerHTML=t}):this.node().innerHTML},Y.append=function(t){return t=at(t),this.select((function(){return this.appendChild(t.apply(this,arguments))}))},Y.insert=function(t,e){return t=at(t),e=W(e),this.select((function(){return this.insertBefore(t.apply(this,arguments),e.apply(this,arguments)||null)}))},Y.remove=function(){return this.each(ot)},Y.data=function(t,e){var r,n,i=-1,a=this.length;if(!arguments.length){for(t=new Array(a=(r=this[0]).length);++i<a;)(n=r[i])&&(t[i]=n.__data__);return t}function o(t,r){var n,i,a,o=t.length,u=r.length,f=Math.min(o,u),h=new Array(u),p=new Array(u),d=new Array(o);if(e){var g,m=new _,v=new Array(o);for(n=-1;++n<o;)(i=t[n])&&(m.has(g=e.call(i,i.__data__,n))?d[n]=i:m.set(g,i),v[n]=g);for(n=-1;++n<u;)(i=m.get(g=e.call(r,a=r[n],n)))?!0!==i&&(h[n]=i,i.__data__=a):p[n]=st(a),m.set(g,!0);for(n=-1;++n<o;)n in v&&!0!==m.get(v[n])&&(d[n]=t[n])}else{for(n=-1;++n<f;)i=t[n],a=r[n],i?(i.__data__=a,h[n]=i):p[n]=st(a);for(;n<u;++n)p[n]=st(r[n]);for(;n<o;++n)d[n]=t[n]}p.update=h,p.parentNode=h.parentNode=d.parentNode=t.parentNode,s.push(p),l.push(h),c.push(d)}var s=ft([]),l=V([]),c=V([]);if("function"==typeof t)for(;++i<a;)o(r=this[i],t.call(r,r.parentNode.__data__,i));else for(;++i<a;)o(r=this[i],t);return l.enter=function(){return s},l.exit=function(){return c},l},Y.datum=function(t){return arguments.length?this.property("__data__",t):this.property("__data__")},Y.filter=function(t){var e,r,n,i=[];"function"!=typeof t&&(t=lt(t));for(var a=0,o=this.length;a<o;a++){i.push(e=[]),e.parentNode=(r=this[a]).parentNode;for(var s=0,l=r.length;s<l;s++)(n=r[s])&&t.call(n,n.__data__,s,a)&&e.push(n)}return V(i)},Y.order=function(){for(var t=-1,e=this.length;++t<e;)for(var r,n=this[t],i=n.length-1,a=n[i];--i>=0;)(r=n[i])&&(a&&a!==r.nextSibling&&a.parentNode.insertBefore(r,a),a=r);return this},Y.sort=function(t){t=ct.apply(this,arguments);for(var e=-1,r=this.length;++e<r;)this[e].sort(t);return this.order()},Y.each=function(t){return ut(this,(function(e,r,n){t.call(e,e.__data__,r,n)}))},Y.call=function(t){var e=n(arguments);return t.apply(e[0]=this,e),this},Y.empty=function(){return!this.node()},Y.node=function(){for(var t=0,e=this.length;t<e;t++)for(var r=this[t],n=0,i=r.length;n<i;n++){var a=r[n];if(a)return a}return null},Y.size=function(){var t=0;return ut(this,(function(){++t})),t};var ht=[];function pt(t){var e,r;return function(n,i,a){var o,s=t[a].update,l=s.length;for(a!=r&&(r=a,e=0),i>=e&&(e=i+1);!(o=s[e])&&++e<l;);return o}}function dt(e,r,i){var a="__on"+e,o=e.indexOf("."),s=mt;o>0&&(e=e.slice(0,o));var l=gt.get(e);function c(){var t=this[a];t&&(this.removeEventListener(e,t,t.$),delete this[a])}return l&&(e=l,s=vt),o?r?function(){var t=s(r,n(arguments));c.call(this),this.addEventListener(e,this[a]=t,t.$=i),t._=r}:c:r?O:function(){var r,n=new RegExp("^__on([^.]+)"+t.requote(e)+"$");for(var i in this)if(r=i.match(n)){var a=this[i];this.removeEventListener(r[1],a,a.$),delete this[i]}}}t.selection.enter=ft,t.selection.enter.prototype=ht,ht.append=Y.append,ht.empty=Y.empty,ht.node=Y.node,ht.call=Y.call,ht.size=Y.size,ht.select=function(t){for(var e,r,n,i,a,o=[],s=-1,l=this.length;++s<l;){n=(i=this[s]).update,o.push(e=[]),e.parentNode=i.parentNode;for(var c=-1,u=i.length;++c<u;)(a=i[c])?(e.push(n[c]=r=t.call(i.parentNode,a.__data__,c,s)),r.__data__=a.__data__):e.push(null)}return V(o)},ht.insert=function(t,e){return arguments.length<2&&(e=pt(this)),Y.insert.call(this,t,e)},t.select=function(t){var e;return"string"==typeof t?(e=[q(t,i)]).parentNode=i.documentElement:(e=[t]).parentNode=a(t),V([e])},t.selectAll=function(t){var e;return"string"==typeof t?(e=n(H(t,i))).parentNode=i.documentElement:(e=n(t)).parentNode=null,V([e])},Y.on=function(t,e,r){var n=arguments.length;if(n<3){if("string"!=typeof t){for(r in n<2&&(e=!1),t)this.each(dt(r,t[r],e));return this}if(n<2)return(n=this.node()["__on"+t])&&n._;r=!1}return this.each(dt(t,e,r))};var gt=t.map({mouseenter:"mouseover",mouseleave:"mouseout"});function mt(e,r){return function(n){var i=t.event;t.event=n,r[0]=this.__data__;try{e.apply(this,r)}finally{t.event=i}}}function vt(t,e){var r=mt(t,e);return function(t){var e=t.relatedTarget;e&&(e===this||8&e.compareDocumentPosition(this))||r.call(this,t)}}i&&gt.forEach((function(t){"on"+t in i&&gt.remove(t)}));var yt,xt=0;function bt(e){var r=".dragsuppress-"+ ++xt,n="click"+r,i=t.select(o(e)).on("touchmove"+r,F).on("dragstart"+r,F).on("selectstart"+r,F);if(null==yt&&(yt=!("onselectstart"in e)&&P(e.style,"userSelect")),yt){var s=a(e).style,l=s[yt];s[yt]="none"}return function(t){if(i.on(r,null),yt&&(s[yt]=l),t){var e=function(){i.on(n,null)};i.on(n,(function(){F(),e()}),!0),setTimeout(e,0)}}}t.mouse=function(t){return wt(t,B())};var _t=this.navigator&&/WebKit/.test(this.navigator.userAgent)?-1:0;function wt(e,r){r.changedTouches&&(r=r.changedTouches[0]);var n=e.ownerSVGElement||e;if(n.createSVGPoint){var i=n.createSVGPoint();if(_t<0){var a=o(e);if(a.scrollX||a.scrollY){var s=(n=t.select("body").append("svg").style({position:"absolute",top:0,left:0,margin:0,padding:0,border:"none"},"important"))[0][0].getScreenCTM();_t=!(s.f||s.e),n.remove()}}return _t?(i.x=r.pageX,i.y=r.pageY):(i.x=r.clientX,i.y=r.clientY),[(i=i.matrixTransform(e.getScreenCTM().inverse())).x,i.y]}var l=e.getBoundingClientRect();return[r.clientX-l.left-e.clientLeft,r.clientY-l.top-e.clientTop]}function Tt(){return t.event.changedTouches[0].identifier}t.touch=function(t,e,r){if(arguments.length<3&&(r=e,e=B().changedTouches),e)for(var n,i=0,a=e.length;i<a;++i)if((n=e[i]).identifier===r)return wt(t,n)},t.behavior.drag=function(){var e=N(a,"drag","dragstart","dragend"),r=null,n=s(O,t.mouse,o,"mousemove","mouseup"),i=s(Tt,t.touch,L,"touchmove","touchend");function a(){this.on("mousedown.drag",n).on("touchstart.drag",i)}function s(n,i,a,o,s){return function(){var l,c=this,u=t.event.target.correspondingElement||t.event.target,f=c.parentNode,h=e.of(c,arguments),p=0,d=n(),g=".drag"+(null==d?"":"-"+d),m=t.select(a(u)).on(o+g,x).on(s+g,b),v=bt(u),y=i(f,d);function x(){var t,e,r=i(f,d);r&&(t=r[0]-y[0],e=r[1]-y[1],p|=t|e,y=r,h({type:"drag",x:r[0]+l[0],y:r[1]+l[1],dx:t,dy:e}))}function b(){i(f,d)&&(m.on(o+g,null).on(s+g,null),v(p),h({type:"dragend"}))}l=r?[(l=r.apply(c,arguments)).x-y[0],l.y-y[1]]:[0,0],h({type:"dragstart"})}}return a.origin=function(t){return arguments.length?(r=t,a):r},t.rebind(a,e,"on")},t.touches=function(t,e){return arguments.length<2&&(e=B().touches),e?n(e).map((function(e){var r=wt(t,e);return r.identifier=e.identifier,r})):[]};var kt=1e-6,Mt=1e-12,At=Math.PI,St=2*At,Et=St-kt,Ct=At/2,Lt=At/180,It=180/At;function Pt(t){return t>0?1:t<0?-1:0}function zt(t,e,r){return(e[0]-t[0])*(r[1]-t[1])-(e[1]-t[1])*(r[0]-t[0])}function Ot(t){return t>1?0:t<-1?At:Math.acos(t)}function Dt(t){return t>1?Ct:t<-1?-Ct:Math.asin(t)}function Rt(t){return((t=Math.exp(t))+1/t)/2}function Ft(t){return(t=Math.sin(t/2))*t}var Bt=Math.SQRT2;t.interpolateZoom=function(t,e){var r,n,i=t[0],a=t[1],o=t[2],s=e[0],l=e[1],c=e[2],u=s-i,f=l-a,h=u*u+f*f;if(h<Mt)n=Math.log(c/o)/Bt,r=function(t){return[i+t*u,a+t*f,o*Math.exp(Bt*t*n)]};else{var p=Math.sqrt(h),d=(c*c-o*o+4*h)/(2*o*2*p),g=(c*c-o*o-4*h)/(2*c*2*p),m=Math.log(Math.sqrt(d*d+1)-d),v=Math.log(Math.sqrt(g*g+1)-g);n=(v-m)/Bt,r=function(t){var e,r=t*n,s=Rt(m),l=o/(2*p)*(s*(e=Bt*r+m,((e=Math.exp(2*e))-1)/(e+1))-function(t){return((t=Math.exp(t))-1/t)/2}(m));return[i+l*u,a+l*f,o*s/Rt(Bt*r+m)]}}return r.duration=1e3*n,r},t.behavior.zoom=function(){var e,r,n,a,s,l,c,u,f,h={x:0,y:0,k:1},p=[960,500],d=Ut,g=250,m=0,v="mousedown.zoom",y="mousemove.zoom",x="mouseup.zoom",b="touchstart.zoom",_=N(w,"zoomstart","zoom","zoomend");function w(t){t.on(v,I).on(jt+".zoom",z).on("dblclick.zoom",O).on(b,P)}function T(t){return[(t[0]-h.x)/h.k,(t[1]-h.y)/h.k]}function k(t){h.k=Math.max(d[0],Math.min(d[1],t))}function M(t,e){e=function(t){return[t[0]*h.k+h.x,t[1]*h.k+h.y]}(e),h.x+=t[0]-e[0],h.y+=t[1]-e[1]}function A(e,n,i,a){e.__chart__={x:h.x,y:h.y,k:h.k},k(Math.pow(2,a)),M(r=n,i),e=t.select(e),g>0&&(e=e.transition().duration(g)),e.call(w.event)}function S(){c&&c.domain(l.range().map((function(t){return(t-h.x)/h.k})).map(l.invert)),f&&f.domain(u.range().map((function(t){return(t-h.y)/h.k})).map(u.invert))}function E(t){m++||t({type:"zoomstart"})}function C(t){S(),t({type:"zoom",scale:h.k,translate:[h.x,h.y]})}function L(t){--m||(t({type:"zoomend"}),r=null)}function I(){var e=this,r=_.of(e,arguments),n=0,i=t.select(o(e)).on(y,l).on(x,c),a=T(t.mouse(e)),s=bt(e);function l(){n=1,M(t.mouse(e),a),C(r)}function c(){i.on(y,null).on(x,null),s(n),L(r)}vs.call(e),E(r)}function P(){var e,r=this,n=_.of(r,arguments),i={},a=0,o=".zoom-"+t.event.changedTouches[0].identifier,l="touchmove"+o,c="touchend"+o,u=[],f=t.select(r),p=bt(r);function d(){var n=t.touches(r);return e=h.k,n.forEach((function(t){t.identifier in i&&(i[t.identifier]=T(t))})),n}function g(){var e=t.event.target;t.select(e).on(l,m).on(c,y),u.push(e);for(var n=t.event.changedTouches,o=0,f=n.length;o<f;++o)i[n[o].identifier]=null;var p=d(),g=Date.now();if(1===p.length){if(g-s<500){var v=p[0];A(r,v,i[v.identifier],Math.floor(Math.log(h.k)/Math.LN2)+1),F()}s=g}else if(p.length>1){v=p[0];var x=p[1],b=v[0]-x[0],_=v[1]-x[1];a=b*b+_*_}}function m(){var o,l,c,u,f=t.touches(r);vs.call(r);for(var h=0,p=f.length;h<p;++h,u=null)if(c=f[h],u=i[c.identifier]){if(l)break;o=c,l=u}if(u){var d=(d=c[0]-o[0])*d+(d=c[1]-o[1])*d,g=a&&Math.sqrt(d/a);o=[(o[0]+c[0])/2,(o[1]+c[1])/2],l=[(l[0]+u[0])/2,(l[1]+u[1])/2],k(g*e)}s=null,M(o,l),C(n)}function y(){if(t.event.touches.length){for(var e=t.event.changedTouches,r=0,a=e.length;r<a;++r)delete i[e[r].identifier];for(var s in i)return void d()}t.selectAll(u).on(o,null),f.on(v,I).on(b,P),p(),L(n)}g(),E(n),f.on(v,null).on(b,g)}function z(){var i=_.of(this,arguments);a?clearTimeout(a):(vs.call(this),e=T(r=n||t.mouse(this)),E(i)),a=setTimeout((function(){a=null,L(i)}),50),F(),k(Math.pow(2,.002*Nt())*h.k),M(r,e),C(i)}function O(){var e=t.mouse(this),r=Math.log(h.k)/Math.LN2;A(this,e,T(e),t.event.shiftKey?Math.ceil(r)-1:Math.floor(r)+1)}return jt||(jt="onwheel"in i?(Nt=function(){return-t.event.deltaY*(t.event.deltaMode?120:1)},"wheel"):"onmousewheel"in i?(Nt=function(){return t.event.wheelDelta},"mousewheel"):(Nt=function(){return-t.event.detail},"MozMousePixelScroll")),w.event=function(e){e.each((function(){var e=_.of(this,arguments),n=h;bs?t.select(this).transition().each("start.zoom",(function(){h=this.__chart__||{x:0,y:0,k:1},E(e)})).tween("zoom:zoom",(function(){var i=p[0],a=p[1],o=r?r[0]:i/2,s=r?r[1]:a/2,l=t.interpolateZoom([(o-h.x)/h.k,(s-h.y)/h.k,i/h.k],[(o-n.x)/n.k,(s-n.y)/n.k,i/n.k]);return function(t){var r=l(t),n=i/r[2];this.__chart__=h={x:o-r[0]*n,y:s-r[1]*n,k:n},C(e)}})).each("interrupt.zoom",(function(){L(e)})).each("end.zoom",(function(){L(e)})):(this.__chart__=h,E(e),C(e),L(e))}))},w.translate=function(t){return arguments.length?(h={x:+t[0],y:+t[1],k:h.k},S(),w):[h.x,h.y]},w.scale=function(t){return arguments.length?(h={x:h.x,y:h.y,k:null},k(+t),S(),w):h.k},w.scaleExtent=function(t){return arguments.length?(d=null==t?Ut:[+t[0],+t[1]],w):d},w.center=function(t){return arguments.length?(n=t&&[+t[0],+t[1]],w):n},w.size=function(t){return arguments.length?(p=t&&[+t[0],+t[1]],w):p},w.duration=function(t){return arguments.length?(g=+t,w):g},w.x=function(t){return arguments.length?(c=t,l=t.copy(),h={x:0,y:0,k:1},w):c},w.y=function(t){return arguments.length?(f=t,u=t.copy(),h={x:0,y:0,k:1},w):f},t.rebind(w,_,"on")};var Nt,jt,Ut=[0,1/0];function Vt(){}function qt(t,e,r){return this instanceof qt?(this.h=+t,this.s=+e,void(this.l=+r)):arguments.length<2?t instanceof qt?new qt(t.h,t.s,t.l):le(""+t,ce,qt):new qt(t,e,r)}t.color=Vt,Vt.prototype.toString=function(){return this.rgb()+""},t.hsl=qt;var Ht=qt.prototype=new Vt;function Gt(t,e,r){var n,i;function a(t){return Math.round(255*function(t){return t>360?t-=360:t<0&&(t+=360),t<60?n+(i-n)*t/60:t<180?i:t<240?n+(i-n)*(240-t)/60:n}(t))}return t=isNaN(t)?0:(t%=360)<0?t+360:t,e=isNaN(e)||e<0?0:e>1?1:e,n=2*(r=r<0?0:r>1?1:r)-(i=r<=.5?r*(1+e):r+e-r*e),new ne(a(t+120),a(t),a(t-120))}function Yt(e,r,n){return this instanceof Yt?(this.h=+e,this.c=+r,void(this.l=+n)):arguments.length<2?e instanceof Yt?new Yt(e.h,e.c,e.l):$t(e instanceof Zt?e.l:(e=ue((e=t.rgb(e)).r,e.g,e.b)).l,e.a,e.b):new Yt(e,r,n)}Ht.brighter=function(t){return t=Math.pow(.7,arguments.length?t:1),new qt(this.h,this.s,this.l/t)},Ht.darker=function(t){return t=Math.pow(.7,arguments.length?t:1),new qt(this.h,this.s,t*this.l)},Ht.rgb=function(){return Gt(this.h,this.s,this.l)},t.hcl=Yt;var Wt=Yt.prototype=new Vt;function Xt(t,e,r){return isNaN(t)&&(t=0),isNaN(e)&&(e=0),new Zt(r,Math.cos(t*=Lt)*e,Math.sin(t)*e)}function Zt(t,e,r){return this instanceof Zt?(this.l=+t,this.a=+e,void(this.b=+r)):arguments.length<2?t instanceof Zt?new Zt(t.l,t.a,t.b):t instanceof Yt?Xt(t.h,t.c,t.l):ue((t=ne(t)).r,t.g,t.b):new Zt(t,e,r)}Wt.brighter=function(t){return new Yt(this.h,this.c,Math.min(100,this.l+Jt*(arguments.length?t:1)))},Wt.darker=function(t){return new Yt(this.h,this.c,Math.max(0,this.l-Jt*(arguments.length?t:1)))},Wt.rgb=function(){return Xt(this.h,this.c,this.l).rgb()},t.lab=Zt;var Jt=18,Kt=Zt.prototype=new Vt;function Qt(t,e,r){var n=(t+16)/116,i=n+e/500,a=n-r/200;return new ne(re(3.2404542*(i=.95047*te(i))-1.5371385*(n=1*te(n))-.4985314*(a=1.08883*te(a))),re(-.969266*i+1.8760108*n+.041556*a),re(.0556434*i-.2040259*n+1.0572252*a))}function $t(t,e,r){return t>0?new Yt(Math.atan2(r,e)*It,Math.sqrt(e*e+r*r),t):new Yt(NaN,NaN,t)}function te(t){return t>.206893034?t*t*t:(t-4/29)/7.787037}function ee(t){return t>.008856?Math.pow(t,1/3):7.787037*t+4/29}function re(t){return Math.round(255*(t<=.00304?12.92*t:1.055*Math.pow(t,1/2.4)-.055))}function ne(t,e,r){return this instanceof ne?(this.r=~~t,this.g=~~e,void(this.b=~~r)):arguments.length<2?t instanceof ne?new ne(t.r,t.g,t.b):le(""+t,ne,Gt):new ne(t,e,r)}function ie(t){return new ne(t>>16,t>>8&255,255&t)}function ae(t){return ie(t)+""}Kt.brighter=function(t){return new Zt(Math.min(100,this.l+Jt*(arguments.length?t:1)),this.a,this.b)},Kt.darker=function(t){return new Zt(Math.max(0,this.l-Jt*(arguments.length?t:1)),this.a,this.b)},Kt.rgb=function(){return Qt(this.l,this.a,this.b)},t.rgb=ne;var oe=ne.prototype=new Vt;function se(t){return t<16?"0"+Math.max(0,t).toString(16):Math.min(255,t).toString(16)}function le(t,e,r){var n,i,a,o=0,s=0,l=0;if(n=/([a-z]+)\((.*)\)/.exec(t=t.toLowerCase()))switch(i=n[2].split(","),n[1]){case"hsl":return r(parseFloat(i[0]),parseFloat(i[1])/100,parseFloat(i[2])/100);case"rgb":return e(he(i[0]),he(i[1]),he(i[2]))}return(a=pe.get(t))?e(a.r,a.g,a.b):(null==t||"#"!==t.charAt(0)||isNaN(a=parseInt(t.slice(1),16))||(4===t.length?(o=(3840&a)>>4,o|=o>>4,s=240&a,s|=s>>4,l=15&a,l|=l<<4):7===t.length&&(o=(16711680&a)>>16,s=(65280&a)>>8,l=255&a)),e(o,s,l))}function ce(t,e,r){var n,i,a=Math.min(t/=255,e/=255,r/=255),o=Math.max(t,e,r),s=o-a,l=(o+a)/2;return s?(i=l<.5?s/(o+a):s/(2-o-a),n=t==o?(e-r)/s+(e<r?6:0):e==o?(r-t)/s+2:(t-e)/s+4,n*=60):(n=NaN,i=l>0&&l<1?0:n),new qt(n,i,l)}function ue(t,e,r){var n=ee((.4124564*(t=fe(t))+.3575761*(e=fe(e))+.1804375*(r=fe(r)))/.95047),i=ee((.2126729*t+.7151522*e+.072175*r)/1);return Zt(116*i-16,500*(n-i),200*(i-ee((.0193339*t+.119192*e+.9503041*r)/1.08883)))}function fe(t){return(t/=255)<=.04045?t/12.92:Math.pow((t+.055)/1.055,2.4)}function he(t){var e=parseFloat(t);return"%"===t.charAt(t.length-1)?Math.round(2.55*e):e}oe.brighter=function(t){t=Math.pow(.7,arguments.length?t:1);var e=this.r,r=this.g,n=this.b,i=30;return e||r||n?(e&&e<i&&(e=i),r&&r<i&&(r=i),n&&n<i&&(n=i),new ne(Math.min(255,e/t),Math.min(255,r/t),Math.min(255,n/t))):new ne(i,i,i)},oe.darker=function(t){return new ne((t=Math.pow(.7,arguments.length?t:1))*this.r,t*this.g,t*this.b)},oe.hsl=function(){return ce(this.r,this.g,this.b)},oe.toString=function(){return"#"+se(this.r)+se(this.g)+se(this.b)};var pe=t.map({aliceblue:15792383,antiquewhite:16444375,aqua:65535,aquamarine:8388564,azure:15794175,beige:16119260,bisque:16770244,black:0,blanchedalmond:16772045,blue:255,blueviolet:9055202,brown:10824234,burlywood:14596231,cadetblue:6266528,chartreuse:8388352,chocolate:13789470,coral:16744272,cornflowerblue:6591981,cornsilk:16775388,crimson:14423100,cyan:65535,darkblue:139,darkcyan:35723,darkgoldenrod:12092939,darkgray:11119017,darkgreen:25600,darkgrey:11119017,darkkhaki:12433259,darkmagenta:9109643,darkolivegreen:5597999,darkorange:16747520,darkorchid:10040012,darkred:9109504,darksalmon:15308410,darkseagreen:9419919,darkslateblue:4734347,darkslategray:3100495,darkslategrey:3100495,darkturquoise:52945,darkviolet:9699539,deeppink:16716947,deepskyblue:49151,dimgray:6908265,dimgrey:6908265,dodgerblue:2003199,firebrick:11674146,floralwhite:16775920,forestgreen:2263842,fuchsia:16711935,gainsboro:14474460,ghostwhite:16316671,gold:16766720,goldenrod:14329120,gray:8421504,green:32768,greenyellow:11403055,grey:8421504,honeydew:15794160,hotpink:16738740,indianred:13458524,indigo:4915330,ivory:16777200,khaki:15787660,lavender:15132410,lavenderblush:16773365,lawngreen:8190976,lemonchiffon:16775885,lightblue:11393254,lightcoral:15761536,lightcyan:14745599,lightgoldenrodyellow:16448210,lightgray:13882323,lightgreen:9498256,lightgrey:13882323,lightpink:16758465,lightsalmon:16752762,lightseagreen:2142890,lightskyblue:8900346,lightslategray:7833753,lightslategrey:7833753,lightsteelblue:11584734,lightyellow:16777184,lime:65280,limegreen:3329330,linen:16445670,magenta:16711935,maroon:8388608,mediumaquamarine:6737322,mediumblue:205,mediumorchid:12211667,mediumpurple:9662683,mediumseagreen:3978097,mediumslateblue:8087790,mediumspringgreen:64154,mediumturquoise:4772300,mediumvioletred:13047173,midnightblue:1644912,mintcream:16121850,mistyrose:16770273,moccasin:16770229,navajowhite:16768685,navy:128,oldlace:16643558,olive:8421376,olivedrab:7048739,orange:16753920,orangered:16729344,orchid:14315734,palegoldenrod:15657130,palegreen:10025880,paleturquoise:11529966,palevioletred:14381203,papayawhip:16773077,peachpuff:16767673,peru:13468991,pink:16761035,plum:14524637,powderblue:11591910,purple:8388736,rebeccapurple:6697881,red:16711680,rosybrown:12357519,royalblue:4286945,saddlebrown:9127187,salmon:16416882,sandybrown:16032864,seagreen:3050327,seashell:16774638,sienna:10506797,silver:12632256,skyblue:8900331,slateblue:6970061,slategray:7372944,slategrey:7372944,snow:16775930,springgreen:65407,steelblue:4620980,tan:13808780,teal:32896,thistle:14204888,tomato:16737095,turquoise:4251856,violet:15631086,wheat:16113331,white:16777215,whitesmoke:16119285,yellow:16776960,yellowgreen:10145074});function de(t){return"function"==typeof t?t:function(){return t}}function ge(t){return function(e,r,n){return 2===arguments.length&&"function"==typeof r&&(n=r,r=null),me(e,r,t,n)}}function me(e,r,i,a){var o={},s=t.dispatch("beforesend","progress","load","error"),l={},c=new XMLHttpRequest,u=null;function f(){var t,e=c.status;if(!e&&function(t){var e=t.responseType;return e&&"text"!==e?t.response:t.responseText}(c)||e>=200&&e<300||304===e){try{t=i.call(o,c)}catch(t){return void s.error.call(o,t)}s.load.call(o,t)}else s.error.call(o,c)}return this.XDomainRequest&&!("withCredentials"in c)&&/^(http(s)?:)?\/\//.test(e)&&(c=new XDomainRequest),"onload"in c?c.onload=c.onerror=f:c.onreadystatechange=function(){c.readyState>3&&f()},c.onprogress=function(e){var r=t.event;t.event=e;try{s.progress.call(o,c)}finally{t.event=r}},o.header=function(t,e){return t=(t+"").toLowerCase(),arguments.length<2?l[t]:(null==e?delete l[t]:l[t]=e+"",o)},o.mimeType=function(t){return arguments.length?(r=null==t?null:t+"",o):r},o.responseType=function(t){return arguments.length?(u=t,o):u},o.response=function(t){return i=t,o},["get","post"].forEach((function(t){o[t]=function(){return o.send.apply(o,[t].concat(n(arguments)))}})),o.send=function(t,n,i){if(2===arguments.length&&"function"==typeof n&&(i=n,n=null),c.open(t,e,!0),null==r||"accept"in l||(l.accept=r+",*/*"),c.setRequestHeader)for(var a in l)c.setRequestHeader(a,l[a]);return null!=r&&c.overrideMimeType&&c.overrideMimeType(r),null!=u&&(c.responseType=u),null!=i&&o.on("error",i).on("load",(function(t){i(null,t)})),s.beforesend.call(o,c),c.send(null==n?null:n),o},o.abort=function(){return c.abort(),o},t.rebind(o,s,"on"),null==a?o:o.get(function(t){return 1===t.length?function(e,r){t(null==e?r:null)}:t}(a))}pe.forEach((function(t,e){pe.set(t,ie(e))})),t.functor=de,t.xhr=ge(L),t.dsv=function(t,e){var r=new RegExp('["'+t+"\n]"),n=t.charCodeAt(0);function i(t,r,n){arguments.length<3&&(n=r,r=null);var i=me(t,e,null==r?a:o(r),n);return i.row=function(t){return arguments.length?i.response(null==(r=t)?a:o(t)):r},i}function a(t){return i.parse(t.responseText)}function o(t){return function(e){return i.parse(e.responseText,t)}}function s(e){return e.map(l).join(t)}function l(t){return r.test(t)?'"'+t.replace(/\"/g,'""')+'"':t}return i.parse=function(t,e){var r;return i.parseRows(t,(function(t,n){if(r)return r(t,n-1);var i=new Function("d","return {"+t.map((function(t,e){return JSON.stringify(t)+": d["+e+"]"})).join(",")+"}");r=e?function(t,r){return e(i(t),r)}:i}))},i.parseRows=function(t,e){var r,i,a={},o={},s=[],l=t.length,c=0,u=0;function f(){if(c>=l)return o;if(i)return i=!1,a;var e=c;if(34===t.charCodeAt(e)){for(var r=e;r++<l;)if(34===t.charCodeAt(r)){if(34!==t.charCodeAt(r+1))break;++r}return c=r+2,13===(s=t.charCodeAt(r+1))?(i=!0,10===t.charCodeAt(r+2)&&++c):10===s&&(i=!0),t.slice(e+1,r).replace(/""/g,'"')}for(;c<l;){var s,u=1;if(10===(s=t.charCodeAt(c++)))i=!0;else if(13===s)i=!0,10===t.charCodeAt(c)&&(++c,++u);else if(s!==n)continue;return t.slice(e,c-u)}return t.slice(e)}for(;(r=f())!==o;){for(var h=[];r!==a&&r!==o;)h.push(r),r=f();e&&null==(h=e(h,u++))||s.push(h)}return s},i.format=function(e){if(Array.isArray(e[0]))return i.formatRows(e);var r=new C,n=[];return e.forEach((function(t){for(var e in t)r.has(e)||n.push(r.add(e))})),[n.map(l).join(t)].concat(e.map((function(e){return n.map((function(t){return l(e[t])})).join(t)}))).join("\n")},i.formatRows=function(t){return t.map(s).join("\n")},i},t.csv=t.dsv(",","text/csv"),t.tsv=t.dsv("\t","text/tab-separated-values");var ve,ye,xe,be,_e=this[P(this,"requestAnimationFrame")]||function(t){setTimeout(t,17)};function we(t,e,r){var n=arguments.length;n<2&&(e=0),n<3&&(r=Date.now());var i=r+e,a={c:t,t:i,n:null};return ye?ye.n=a:ve=a,ye=a,xe||(be=clearTimeout(be),xe=1,_e(Te)),a}function Te(){var t=ke(),e=Me()-t;e>24?(isFinite(e)&&(clearTimeout(be),be=setTimeout(Te,e)),xe=0):(xe=1,_e(Te))}function ke(){for(var t=Date.now(),e=ve;e;)t>=e.t&&e.c(t-e.t)&&(e.c=null),e=e.n;return t}function Me(){for(var t,e=ve,r=1/0;e;)e.c?(e.t<r&&(r=e.t),e=(t=e).n):e=t?t.n=e.n:ve=e.n;return ye=t,r}function Ae(t,e){return e-(t?Math.ceil(Math.log(t)/Math.LN10):1)}t.timer=function(){we.apply(this,arguments)},t.timer.flush=function(){ke(),Me()},t.round=function(t,e){return e?Math.round(t*(e=Math.pow(10,e)))/e:Math.round(t)};var Se=["y","z","a","f","p","n","\xb5","m","","k","M","G","T","P","E","Z","Y"].map((function(t,e){var r=Math.pow(10,3*y(8-e));return{scale:e>8?function(t){return t/r}:function(t){return t*r},symbol:t}}));function Ee(e){var r=e.decimal,n=e.thousands,i=e.grouping,a=e.currency,o=i&&n?function(t,e){for(var r=t.length,a=[],o=0,s=i[0],l=0;r>0&&s>0&&(l+s+1>e&&(s=Math.max(1,e-l)),a.push(t.substring(r-=s,r+s)),!((l+=s+1)>e));)s=i[o=(o+1)%i.length];return a.reverse().join(n)}:L;return function(e){var n=Ce.exec(e),i=n[1]||" ",s=n[2]||">",l=n[3]||"-",c=n[4]||"",u=n[5],f=+n[6],h=n[7],p=n[8],d=n[9],g=1,m="",v="",y=!1,x=!0;switch(p&&(p=+p.substring(1)),(u||"0"===i&&"="===s)&&(u=i="0",s="="),d){case"n":h=!0,d="g";break;case"%":g=100,v="%",d="f";break;case"p":g=100,v="%",d="r";break;case"b":case"o":case"x":case"X":"#"===c&&(m="0"+d.toLowerCase());case"c":x=!1;case"d":y=!0,p=0;break;case"s":g=-1,d="r"}"$"===c&&(m=a[0],v=a[1]),"r"!=d||p||(d="g"),null!=p&&("g"==d?p=Math.max(1,Math.min(21,p)):"e"!=d&&"f"!=d||(p=Math.max(0,Math.min(20,p)))),d=Le.get(d)||Ie;var b=u&&h;return function(e){var n=v;if(y&&e%1)return"";var a=e<0||0===e&&1/e<0?(e=-e,"-"):"-"===l?"":l;if(g<0){var c=t.formatPrefix(e,p);e=c.scale(e),n=c.symbol+v}else e*=g;var _,w,T=(e=d(e,p)).lastIndexOf(".");if(T<0){var k=x?e.lastIndexOf("e"):-1;k<0?(_=e,w=""):(_=e.substring(0,k),w=e.substring(k))}else _=e.substring(0,T),w=r+e.substring(T+1);!u&&h&&(_=o(_,1/0));var M=m.length+_.length+w.length+(b?0:a.length),A=M<f?new Array(M=f-M+1).join(i):"";return b&&(_=o(A+_,A.length?f-w.length:1/0)),a+=m,e=_+w,("<"===s?a+e+A:">"===s?A+a+e:"^"===s?A.substring(0,M>>=1)+a+e+A.substring(M):a+(b?e:A+e))+n}}}t.formatPrefix=function(e,r){var n=0;return(e=+e)&&(e<0&&(e*=-1),r&&(e=t.round(e,Ae(e,r))),n=1+Math.floor(1e-12+Math.log(e)/Math.LN10),n=Math.max(-24,Math.min(24,3*Math.floor((n-1)/3)))),Se[8+n/3]};var Ce=/(?:([^{])?([<>=^]))?([+\- ])?([$#])?(0)?(\d+)?(,)?(\.-?\d+)?([a-z%])?/i,Le=t.map({b:function(t){return t.toString(2)},c:function(t){return String.fromCharCode(t)},o:function(t){return t.toString(8)},x:function(t){return t.toString(16)},X:function(t){return t.toString(16).toUpperCase()},g:function(t,e){return t.toPrecision(e)},e:function(t,e){return t.toExponential(e)},f:function(t,e){return t.toFixed(e)},r:function(e,r){return(e=t.round(e,Ae(e,r))).toFixed(Math.max(0,Math.min(20,Ae(e*(1+1e-15),r))))}});function Ie(t){return t+""}var Pe=t.time={},ze=Date;function Oe(){this._=new Date(arguments.length>1?Date.UTC.apply(this,arguments):arguments[0])}Oe.prototype={getDate:function(){return this._.getUTCDate()},getDay:function(){return this._.getUTCDay()},getFullYear:function(){return this._.getUTCFullYear()},getHours:function(){return this._.getUTCHours()},getMilliseconds:function(){return this._.getUTCMilliseconds()},getMinutes:function(){return this._.getUTCMinutes()},getMonth:function(){return this._.getUTCMonth()},getSeconds:function(){return this._.getUTCSeconds()},getTime:function(){return this._.getTime()},getTimezoneOffset:function(){return 0},valueOf:function(){return this._.valueOf()},setDate:function(){De.setUTCDate.apply(this._,arguments)},setDay:function(){De.setUTCDay.apply(this._,arguments)},setFullYear:function(){De.setUTCFullYear.apply(this._,arguments)},setHours:function(){De.setUTCHours.apply(this._,arguments)},setMilliseconds:function(){De.setUTCMilliseconds.apply(this._,arguments)},setMinutes:function(){De.setUTCMinutes.apply(this._,arguments)},setMonth:function(){De.setUTCMonth.apply(this._,arguments)},setSeconds:function(){De.setUTCSeconds.apply(this._,arguments)},setTime:function(){De.setTime.apply(this._,arguments)}};var De=Date.prototype;function Re(t,e,r){function n(e){var r=t(e),n=a(r,1);return e-r<n-e?r:n}function i(r){return e(r=t(new ze(r-1)),1),r}function a(t,r){return e(t=new ze(+t),r),t}function o(t,n,a){var o=i(t),s=[];if(a>1)for(;o<n;)r(o)%a||s.push(new Date(+o)),e(o,1);else for(;o<n;)s.push(new Date(+o)),e(o,1);return s}t.floor=t,t.round=n,t.ceil=i,t.offset=a,t.range=o;var s=t.utc=Fe(t);return s.floor=s,s.round=Fe(n),s.ceil=Fe(i),s.offset=Fe(a),s.range=function(t,e,r){try{ze=Oe;var n=new Oe;return n._=t,o(n,e,r)}finally{ze=Date}},t}function Fe(t){return function(e,r){try{ze=Oe;var n=new Oe;return n._=e,t(n,r)._}finally{ze=Date}}}function Be(e){var r=e.dateTime,n=e.date,i=e.time,a=e.periods,o=e.days,s=e.shortDays,l=e.months,c=e.shortMonths;function u(t){var e=t.length;function r(r){for(var n,i,a,o=[],s=-1,l=0;++s<e;)37===t.charCodeAt(s)&&(o.push(t.slice(l,s)),null!=(i=Ne[n=t.charAt(++s)])&&(n=t.charAt(++s)),(a=_[n])&&(n=a(r,null==i?"e"===n?" ":"0":i)),o.push(n),l=s+1);return o.push(t.slice(l,s)),o.join("")}return r.parse=function(e){var r={y:1900,m:0,d:1,H:0,M:0,S:0,L:0,Z:null};if(f(r,t,e,0)!=e.length)return null;"p"in r&&(r.H=r.H%12+12*r.p);var n=null!=r.Z&&ze!==Oe,i=new(n?Oe:ze);return"j"in r?i.setFullYear(r.y,0,r.j):"W"in r||"U"in r?("w"in r||(r.w="W"in r?1:0),i.setFullYear(r.y,0,1),i.setFullYear(r.y,0,"W"in r?(r.w+6)%7+7*r.W-(i.getDay()+5)%7:r.w+7*r.U-(i.getDay()+6)%7)):i.setFullYear(r.y,r.m,r.d),i.setHours(r.H+(r.Z/100|0),r.M+r.Z%100,r.S,r.L),n?i._:i},r.toString=function(){return t},r}function f(t,e,r,n){for(var i,a,o,s=0,l=e.length,c=r.length;s<l;){if(n>=c)return-1;if(37===(i=e.charCodeAt(s++))){if(o=e.charAt(s++),!(a=w[o in Ne?e.charAt(s++):o])||(n=a(t,r,n))<0)return-1}else if(i!=r.charCodeAt(n++))return-1}return n}u.utc=function(t){var e=u(t);function r(t){try{var r=new(ze=Oe);return r._=t,e(r)}finally{ze=Date}}return r.parse=function(t){try{ze=Oe;var r=e.parse(t);return r&&r._}finally{ze=Date}},r.toString=e.toString,r},u.multi=u.utc.multi=or;var h=t.map(),p=qe(o),d=He(o),g=qe(s),m=He(s),v=qe(l),y=He(l),x=qe(c),b=He(c);a.forEach((function(t,e){h.set(t.toLowerCase(),e)}));var _={a:function(t){return s[t.getDay()]},A:function(t){return o[t.getDay()]},b:function(t){return c[t.getMonth()]},B:function(t){return l[t.getMonth()]},c:u(r),d:function(t,e){return Ve(t.getDate(),e,2)},e:function(t,e){return Ve(t.getDate(),e,2)},H:function(t,e){return Ve(t.getHours(),e,2)},I:function(t,e){return Ve(t.getHours()%12||12,e,2)},j:function(t,e){return Ve(1+Pe.dayOfYear(t),e,3)},L:function(t,e){return Ve(t.getMilliseconds(),e,3)},m:function(t,e){return Ve(t.getMonth()+1,e,2)},M:function(t,e){return Ve(t.getMinutes(),e,2)},p:function(t){return a[+(t.getHours()>=12)]},S:function(t,e){return Ve(t.getSeconds(),e,2)},U:function(t,e){return Ve(Pe.sundayOfYear(t),e,2)},w:function(t){return t.getDay()},W:function(t,e){return Ve(Pe.mondayOfYear(t),e,2)},x:u(n),X:u(i),y:function(t,e){return Ve(t.getFullYear()%100,e,2)},Y:function(t,e){return Ve(t.getFullYear()%1e4,e,4)},Z:ir,"%":function(){return"%"}},w={a:function(t,e,r){g.lastIndex=0;var n=g.exec(e.slice(r));return n?(t.w=m.get(n[0].toLowerCase()),r+n[0].length):-1},A:function(t,e,r){p.lastIndex=0;var n=p.exec(e.slice(r));return n?(t.w=d.get(n[0].toLowerCase()),r+n[0].length):-1},b:function(t,e,r){x.lastIndex=0;var n=x.exec(e.slice(r));return n?(t.m=b.get(n[0].toLowerCase()),r+n[0].length):-1},B:function(t,e,r){v.lastIndex=0;var n=v.exec(e.slice(r));return n?(t.m=y.get(n[0].toLowerCase()),r+n[0].length):-1},c:function(t,e,r){return f(t,_.c.toString(),e,r)},d:Qe,e:Qe,H:tr,I:tr,j:$e,L:nr,m:Ke,M:er,p:function(t,e,r){var n=h.get(e.slice(r,r+=2).toLowerCase());return null==n?-1:(t.p=n,r)},S:rr,U:Ye,w:Ge,W:We,x:function(t,e,r){return f(t,_.x.toString(),e,r)},X:function(t,e,r){return f(t,_.X.toString(),e,r)},y:Ze,Y:Xe,Z:Je,"%":ar};return u}Pe.year=Re((function(t){return(t=Pe.day(t)).setMonth(0,1),t}),(function(t,e){t.setFullYear(t.getFullYear()+e)}),(function(t){return t.getFullYear()})),Pe.years=Pe.year.range,Pe.years.utc=Pe.year.utc.range,Pe.day=Re((function(t){var e=new ze(2e3,0);return e.setFullYear(t.getFullYear(),t.getMonth(),t.getDate()),e}),(function(t,e){t.setDate(t.getDate()+e)}),(function(t){return t.getDate()-1})),Pe.days=Pe.day.range,Pe.days.utc=Pe.day.utc.range,Pe.dayOfYear=function(t){var e=Pe.year(t);return Math.floor((t-e-6e4*(t.getTimezoneOffset()-e.getTimezoneOffset()))/864e5)},["sunday","monday","tuesday","wednesday","thursday","friday","saturday"].forEach((function(t,e){e=7-e;var r=Pe[t]=Re((function(t){return(t=Pe.day(t)).setDate(t.getDate()-(t.getDay()+e)%7),t}),(function(t,e){t.setDate(t.getDate()+7*Math.floor(e))}),(function(t){var r=Pe.year(t).getDay();return Math.floor((Pe.dayOfYear(t)+(r+e)%7)/7)-(r!==e)}));Pe[t+"s"]=r.range,Pe[t+"s"].utc=r.utc.range,Pe[t+"OfYear"]=function(t){var r=Pe.year(t).getDay();return Math.floor((Pe.dayOfYear(t)+(r+e)%7)/7)}})),Pe.week=Pe.sunday,Pe.weeks=Pe.sunday.range,Pe.weeks.utc=Pe.sunday.utc.range,Pe.weekOfYear=Pe.sundayOfYear;var Ne={"-":"",_:" ",0:"0"},je=/^\s*\d+/,Ue=/^%/;function Ve(t,e,r){var n=t<0?"-":"",i=(n?-t:t)+"",a=i.length;return n+(a<r?new Array(r-a+1).join(e)+i:i)}function qe(e){return new RegExp("^(?:"+e.map(t.requote).join("|")+")","i")}function He(t){for(var e=new _,r=-1,n=t.length;++r<n;)e.set(t[r].toLowerCase(),r);return e}function Ge(t,e,r){je.lastIndex=0;var n=je.exec(e.slice(r,r+1));return n?(t.w=+n[0],r+n[0].length):-1}function Ye(t,e,r){je.lastIndex=0;var n=je.exec(e.slice(r));return n?(t.U=+n[0],r+n[0].length):-1}function We(t,e,r){je.lastIndex=0;var n=je.exec(e.slice(r));return n?(t.W=+n[0],r+n[0].length):-1}function Xe(t,e,r){je.lastIndex=0;var n=je.exec(e.slice(r,r+4));return n?(t.y=+n[0],r+n[0].length):-1}function Ze(t,e,r){je.lastIndex=0;var n,i=je.exec(e.slice(r,r+2));return i?(t.y=(n=+i[0])+(n>68?1900:2e3),r+i[0].length):-1}function Je(t,e,r){return/^[+-]\d{4}$/.test(e=e.slice(r,r+5))?(t.Z=-e,r+5):-1}function Ke(t,e,r){je.lastIndex=0;var n=je.exec(e.slice(r,r+2));return n?(t.m=n[0]-1,r+n[0].length):-1}function Qe(t,e,r){je.lastIndex=0;var n=je.exec(e.slice(r,r+2));return n?(t.d=+n[0],r+n[0].length):-1}function $e(t,e,r){je.lastIndex=0;var n=je.exec(e.slice(r,r+3));return n?(t.j=+n[0],r+n[0].length):-1}function tr(t,e,r){je.lastIndex=0;var n=je.exec(e.slice(r,r+2));return n?(t.H=+n[0],r+n[0].length):-1}function er(t,e,r){je.lastIndex=0;var n=je.exec(e.slice(r,r+2));return n?(t.M=+n[0],r+n[0].length):-1}function rr(t,e,r){je.lastIndex=0;var n=je.exec(e.slice(r,r+2));return n?(t.S=+n[0],r+n[0].length):-1}function nr(t,e,r){je.lastIndex=0;var n=je.exec(e.slice(r,r+3));return n?(t.L=+n[0],r+n[0].length):-1}function ir(t){var e=t.getTimezoneOffset(),r=e>0?"-":"+",n=y(e)/60|0,i=y(e)%60;return r+Ve(n,"0",2)+Ve(i,"0",2)}function ar(t,e,r){Ue.lastIndex=0;var n=Ue.exec(e.slice(r,r+1));return n?r+n[0].length:-1}function or(t){for(var e=t.length,r=-1;++r<e;)t[r][0]=this(t[r][0]);return function(e){for(var r=0,n=t[r];!n[1](e);)n=t[++r];return n[0](e)}}t.locale=function(t){return{numberFormat:Ee(t),timeFormat:Be(t)}};var sr=t.locale({decimal:".",thousands:",",grouping:[3],currency:["$",""],dateTime:"%a %b %e %X %Y",date:"%m/%d/%Y",time:"%H:%M:%S",periods:["AM","PM"],days:["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"],shortDays:["Sun","Mon","Tue","Wed","Thu","Fri","Sat"],months:["January","February","March","April","May","June","July","August","September","October","November","December"],shortMonths:["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"]});function lr(){}t.format=sr.numberFormat,t.geo={},lr.prototype={s:0,t:0,add:function(t){ur(t,this.t,cr),ur(cr.s,this.s,this),this.s?this.t+=cr.t:this.s=cr.t},reset:function(){this.s=this.t=0},valueOf:function(){return this.s}};var cr=new lr;function ur(t,e,r){var n=r.s=t+e,i=n-t,a=n-i;r.t=t-a+(e-i)}function fr(t,e){t&&pr.hasOwnProperty(t.type)&&pr[t.type](t,e)}t.geo.stream=function(t,e){t&&hr.hasOwnProperty(t.type)?hr[t.type](t,e):fr(t,e)};var hr={Feature:function(t,e){fr(t.geometry,e)},FeatureCollection:function(t,e){for(var r=t.features,n=-1,i=r.length;++n<i;)fr(r[n].geometry,e)}},pr={Sphere:function(t,e){e.sphere()},Point:function(t,e){t=t.coordinates,e.point(t[0],t[1],t[2])},MultiPoint:function(t,e){for(var r=t.coordinates,n=-1,i=r.length;++n<i;)t=r[n],e.point(t[0],t[1],t[2])},LineString:function(t,e){dr(t.coordinates,e,0)},MultiLineString:function(t,e){for(var r=t.coordinates,n=-1,i=r.length;++n<i;)dr(r[n],e,0)},Polygon:function(t,e){gr(t.coordinates,e)},MultiPolygon:function(t,e){for(var r=t.coordinates,n=-1,i=r.length;++n<i;)gr(r[n],e)},GeometryCollection:function(t,e){for(var r=t.geometries,n=-1,i=r.length;++n<i;)fr(r[n],e)}};function dr(t,e,r){var n,i=-1,a=t.length-r;for(e.lineStart();++i<a;)n=t[i],e.point(n[0],n[1],n[2]);e.lineEnd()}function gr(t,e){var r=-1,n=t.length;for(e.polygonStart();++r<n;)dr(t[r],e,1);e.polygonEnd()}t.geo.area=function(e){return mr=0,t.geo.stream(e,Cr),mr};var mr,vr,yr,xr,br,_r,wr,Tr,kr,Mr,Ar,Sr,Er=new lr,Cr={sphere:function(){mr+=4*At},point:O,lineStart:O,lineEnd:O,polygonStart:function(){Er.reset(),Cr.lineStart=Lr},polygonEnd:function(){var t=2*Er;mr+=t<0?4*At+t:t,Cr.lineStart=Cr.lineEnd=Cr.point=O}};function Lr(){var t,e,r,n,i;function a(t,e){e=e*Lt/2+At/4;var a=(t*=Lt)-r,o=a>=0?1:-1,s=o*a,l=Math.cos(e),c=Math.sin(e),u=i*c,f=n*l+u*Math.cos(s),h=u*o*Math.sin(s);Er.add(Math.atan2(h,f)),r=t,n=l,i=c}Cr.point=function(o,s){Cr.point=a,r=(t=o)*Lt,n=Math.cos(s=(e=s)*Lt/2+At/4),i=Math.sin(s)},Cr.lineEnd=function(){a(t,e)}}function Ir(t){var e=t[0],r=t[1],n=Math.cos(r);return[n*Math.cos(e),n*Math.sin(e),Math.sin(r)]}function Pr(t,e){return t[0]*e[0]+t[1]*e[1]+t[2]*e[2]}function zr(t,e){return[t[1]*e[2]-t[2]*e[1],t[2]*e[0]-t[0]*e[2],t[0]*e[1]-t[1]*e[0]]}function Or(t,e){t[0]+=e[0],t[1]+=e[1],t[2]+=e[2]}function Dr(t,e){return[t[0]*e,t[1]*e,t[2]*e]}function Rr(t){var e=Math.sqrt(t[0]*t[0]+t[1]*t[1]+t[2]*t[2]);t[0]/=e,t[1]/=e,t[2]/=e}function Fr(t){return[Math.atan2(t[1],t[0]),Dt(t[2])]}function Br(t,e){return y(t[0]-e[0])<kt&&y(t[1]-e[1])<kt}t.geo.bounds=function(){var e,r,n,i,a,o,s,l,c,u,f,h={point:p,lineStart:g,lineEnd:m,polygonStart:function(){h.point=v,h.lineStart=x,h.lineEnd=b,c=0,Cr.polygonStart()},polygonEnd:function(){Cr.polygonEnd(),h.point=p,h.lineStart=g,h.lineEnd=m,Er<0?(e=-(n=180),r=-(i=90)):c>kt?i=90:c<-kt&&(r=-90),f[0]=e,f[1]=n}};function p(t,a){u.push(f=[e=t,n=t]),a<r&&(r=a),a>i&&(i=a)}function d(t,o){var s=Ir([t*Lt,o*Lt]);if(l){var c=zr(l,s),u=zr([c[1],-c[0],0],c);Rr(u),u=Fr(u);var f=t-a,h=f>0?1:-1,d=u[0]*It*h,g=y(f)>180;if(g^(h*a<d&&d<h*t))(m=u[1]*It)>i&&(i=m);else if(g^(h*a<(d=(d+360)%360-180)&&d<h*t)){var m;(m=-u[1]*It)<r&&(r=m)}else o<r&&(r=o),o>i&&(i=o);g?t<a?_(e,t)>_(e,n)&&(n=t):_(t,n)>_(e,n)&&(e=t):n>=e?(t<e&&(e=t),t>n&&(n=t)):t>a?_(e,t)>_(e,n)&&(n=t):_(t,n)>_(e,n)&&(e=t)}else p(t,o);l=s,a=t}function g(){h.point=d}function m(){f[0]=e,f[1]=n,h.point=p,l=null}function v(t,e){if(l){var r=t-a;c+=y(r)>180?r+(r>0?360:-360):r}else o=t,s=e;Cr.point(t,e),d(t,e)}function x(){Cr.lineStart()}function b(){v(o,s),Cr.lineEnd(),y(c)>kt&&(e=-(n=180)),f[0]=e,f[1]=n,l=null}function _(t,e){return(e-=t)<0?e+360:e}function w(t,e){return t[0]-e[0]}function T(t,e){return e[0]<=e[1]?e[0]<=t&&t<=e[1]:t<e[0]||e[1]<t}return function(a){if(i=n=-(e=r=1/0),u=[],t.geo.stream(a,h),c=u.length){u.sort(w);for(var o=1,s=[g=u[0]];o<c;++o)T((p=u[o])[0],g)||T(p[1],g)?(_(g[0],p[1])>_(g[0],g[1])&&(g[1]=p[1]),_(p[0],g[1])>_(g[0],g[1])&&(g[0]=p[0])):s.push(g=p);for(var l,c,p,d=-1/0,g=(o=0,s[c=s.length-1]);o<=c;g=p,++o)p=s[o],(l=_(g[1],p[0]))>d&&(d=l,e=p[0],n=g[1])}return u=f=null,e===1/0||r===1/0?[[NaN,NaN],[NaN,NaN]]:[[e,r],[n,i]]}}(),t.geo.centroid=function(e){vr=yr=xr=br=_r=wr=Tr=kr=Mr=Ar=Sr=0,t.geo.stream(e,Nr);var r=Mr,n=Ar,i=Sr,a=r*r+n*n+i*i;return a<Mt&&(r=wr,n=Tr,i=kr,yr<kt&&(r=xr,n=br,i=_r),(a=r*r+n*n+i*i)<Mt)?[NaN,NaN]:[Math.atan2(n,r)*It,Dt(i/Math.sqrt(a))*It]};var Nr={sphere:O,point:jr,lineStart:Vr,lineEnd:qr,polygonStart:function(){Nr.lineStart=Hr},polygonEnd:function(){Nr.lineStart=Vr}};function jr(t,e){t*=Lt;var r=Math.cos(e*=Lt);Ur(r*Math.cos(t),r*Math.sin(t),Math.sin(e))}function Ur(t,e,r){++vr,xr+=(t-xr)/vr,br+=(e-br)/vr,_r+=(r-_r)/vr}function Vr(){var t,e,r;function n(n,i){n*=Lt;var a=Math.cos(i*=Lt),o=a*Math.cos(n),s=a*Math.sin(n),l=Math.sin(i),c=Math.atan2(Math.sqrt((c=e*l-r*s)*c+(c=r*o-t*l)*c+(c=t*s-e*o)*c),t*o+e*s+r*l);yr+=c,wr+=c*(t+(t=o)),Tr+=c*(e+(e=s)),kr+=c*(r+(r=l)),Ur(t,e,r)}Nr.point=function(i,a){i*=Lt;var o=Math.cos(a*=Lt);t=o*Math.cos(i),e=o*Math.sin(i),r=Math.sin(a),Nr.point=n,Ur(t,e,r)}}function qr(){Nr.point=jr}function Hr(){var t,e,r,n,i;function a(t,e){t*=Lt;var a=Math.cos(e*=Lt),o=a*Math.cos(t),s=a*Math.sin(t),l=Math.sin(e),c=n*l-i*s,u=i*o-r*l,f=r*s-n*o,h=Math.sqrt(c*c+u*u+f*f),p=r*o+n*s+i*l,d=h&&-Ot(p)/h,g=Math.atan2(h,p);Mr+=d*c,Ar+=d*u,Sr+=d*f,yr+=g,wr+=g*(r+(r=o)),Tr+=g*(n+(n=s)),kr+=g*(i+(i=l)),Ur(r,n,i)}Nr.point=function(o,s){t=o,e=s,Nr.point=a,o*=Lt;var l=Math.cos(s*=Lt);r=l*Math.cos(o),n=l*Math.sin(o),i=Math.sin(s),Ur(r,n,i)},Nr.lineEnd=function(){a(t,e),Nr.lineEnd=qr,Nr.point=jr}}function Gr(t,e){function r(r,n){return r=t(r,n),e(r[0],r[1])}return t.invert&&e.invert&&(r.invert=function(r,n){return(r=e.invert(r,n))&&t.invert(r[0],r[1])}),r}function Yr(){return!0}function Wr(t,e,r,n,i){var a=[],o=[];if(t.forEach((function(t){if(!((e=t.length-1)<=0)){var e,r=t[0],n=t[e];if(Br(r,n)){i.lineStart();for(var s=0;s<e;++s)i.point((r=t[s])[0],r[1]);i.lineEnd()}else{var l=new Zr(r,t,null,!0),c=new Zr(r,null,l,!1);l.o=c,a.push(l),o.push(c),l=new Zr(n,t,null,!1),c=new Zr(n,null,l,!0),l.o=c,a.push(l),o.push(c)}}})),o.sort(e),Xr(a),Xr(o),a.length){for(var s=0,l=r,c=o.length;s<c;++s)o[s].e=l=!l;for(var u,f,h=a[0];;){for(var p=h,d=!0;p.v;)if((p=p.n)===h)return;u=p.z,i.lineStart();do{if(p.v=p.o.v=!0,p.e){if(d)for(s=0,c=u.length;s<c;++s)i.point((f=u[s])[0],f[1]);else n(p.x,p.n.x,1,i);p=p.n}else{if(d)for(s=(u=p.p.z).length-1;s>=0;--s)i.point((f=u[s])[0],f[1]);else n(p.x,p.p.x,-1,i);p=p.p}u=(p=p.o).z,d=!d}while(!p.v);i.lineEnd()}}}function Xr(t){if(e=t.length){for(var e,r,n=0,i=t[0];++n<e;)i.n=r=t[n],r.p=i,i=r;i.n=r=t[0],r.p=i}}function Zr(t,e,r,n){this.x=t,this.z=e,this.o=r,this.e=n,this.v=!1,this.n=this.p=null}function Jr(e,r,n,i){return function(a,o){var s,l=r(o),c=a.invert(i[0],i[1]),u={point:f,lineStart:p,lineEnd:d,polygonStart:function(){u.point=b,u.lineStart=_,u.lineEnd=w,s=[],g=[]},polygonEnd:function(){u.point=f,u.lineStart=p,u.lineEnd=d,s=t.merge(s);var e=function(t,e){var r=t[0],n=t[1],i=[Math.sin(r),-Math.cos(r),0],a=0,o=0;Er.reset();for(var s=0,l=e.length;s<l;++s){var c=e[s],u=c.length;if(u)for(var f=c[0],h=f[0],p=f[1]/2+At/4,d=Math.sin(p),g=Math.cos(p),m=1;;){m===u&&(m=0);var v=(t=c[m])[0],y=t[1]/2+At/4,x=Math.sin(y),b=Math.cos(y),_=v-h,w=_>=0?1:-1,T=w*_,k=T>At,M=d*x;if(Er.add(Math.atan2(M*w*Math.sin(T),g*b+M*Math.cos(T))),a+=k?_+w*St:_,k^h>=r^v>=r){var A=zr(Ir(f),Ir(t));Rr(A);var S=zr(i,A);Rr(S);var E=(k^_>=0?-1:1)*Dt(S[2]);(n>E||n===E&&(A[0]||A[1]))&&(o+=k^_>=0?1:-1)}if(!m++)break;h=v,d=x,g=b,f=t}}return(a<-kt||a<kt&&Er<-kt)^1&o}(c,g);s.length?(x||(o.polygonStart(),x=!0),Wr(s,$r,e,n,o)):e&&(x||(o.polygonStart(),x=!0),o.lineStart(),n(null,null,1,o),o.lineEnd()),x&&(o.polygonEnd(),x=!1),s=g=null},sphere:function(){o.polygonStart(),o.lineStart(),n(null,null,1,o),o.lineEnd(),o.polygonEnd()}};function f(t,r){var n=a(t,r);e(t=n[0],r=n[1])&&o.point(t,r)}function h(t,e){var r=a(t,e);l.point(r[0],r[1])}function p(){u.point=h,l.lineStart()}function d(){u.point=f,l.lineEnd()}var g,m,v=Qr(),y=r(v),x=!1;function b(t,e){m.push([t,e]);var r=a(t,e);y.point(r[0],r[1])}function _(){y.lineStart(),m=[]}function w(){b(m[0][0],m[0][1]),y.lineEnd();var t,e=y.clean(),r=v.buffer(),n=r.length;if(m.pop(),g.push(m),m=null,n)if(1&e){var i,a=-1;if((n=(t=r[0]).length-1)>0){for(x||(o.polygonStart(),x=!0),o.lineStart();++a<n;)o.point((i=t[a])[0],i[1]);o.lineEnd()}}else n>1&&2&e&&r.push(r.pop().concat(r.shift())),s.push(r.filter(Kr))}return u}}function Kr(t){return t.length>1}function Qr(){var t,e=[];return{lineStart:function(){e.push(t=[])},point:function(e,r){t.push([e,r])},lineEnd:O,buffer:function(){var r=e;return e=[],t=null,r},rejoin:function(){e.length>1&&e.push(e.pop().concat(e.shift()))}}}function $r(t,e){return((t=t.x)[0]<0?t[1]-Ct-kt:Ct-t[1])-((e=e.x)[0]<0?e[1]-Ct-kt:Ct-e[1])}var tn=Jr(Yr,(function(t){var e,r=NaN,n=NaN,i=NaN;return{lineStart:function(){t.lineStart(),e=1},point:function(a,o){var s=a>0?At:-At,l=y(a-r);y(l-At)<kt?(t.point(r,n=(n+o)/2>0?Ct:-Ct),t.point(i,n),t.lineEnd(),t.lineStart(),t.point(s,n),t.point(a,n),e=0):i!==s&&l>=At&&(y(r-i)<kt&&(r-=i*kt),y(a-s)<kt&&(a-=s*kt),n=function(t,e,r,n){var i,a,o=Math.sin(t-r);return y(o)>kt?Math.atan((Math.sin(e)*(a=Math.cos(n))*Math.sin(r)-Math.sin(n)*(i=Math.cos(e))*Math.sin(t))/(i*a*o)):(e+n)/2}(r,n,a,o),t.point(i,n),t.lineEnd(),t.lineStart(),t.point(s,n),e=0),t.point(r=a,n=o),i=s},lineEnd:function(){t.lineEnd(),r=n=NaN},clean:function(){return 2-e}}}),(function(t,e,r,n){var i;if(null==t)i=r*Ct,n.point(-At,i),n.point(0,i),n.point(At,i),n.point(At,0),n.point(At,-i),n.point(0,-i),n.point(-At,-i),n.point(-At,0),n.point(-At,i);else if(y(t[0]-e[0])>kt){var a=t[0]<e[0]?At:-At;i=r*a/2,n.point(-a,i),n.point(0,i),n.point(a,i)}else n.point(e[0],e[1])}),[-At,-At/2]);function en(t){var e=Math.cos(t),r=e>0,n=y(e)>kt;return Jr(i,(function(t){var e,s,l,c,u;return{lineStart:function(){c=l=!1,u=1},point:function(f,h){var p,d=[f,h],g=i(f,h),m=r?g?0:o(f,h):g?o(f+(f<0?At:-At),h):0;if(!e&&(c=l=g)&&t.lineStart(),g!==l&&(p=a(e,d),(Br(e,p)||Br(d,p))&&(d[0]+=kt,d[1]+=kt,g=i(d[0],d[1]))),g!==l)u=0,g?(t.lineStart(),p=a(d,e),t.point(p[0],p[1])):(p=a(e,d),t.point(p[0],p[1]),t.lineEnd()),e=p;else if(n&&e&&r^g){var v;m&s||!(v=a(d,e,!0))||(u=0,r?(t.lineStart(),t.point(v[0][0],v[0][1]),t.point(v[1][0],v[1][1]),t.lineEnd()):(t.point(v[1][0],v[1][1]),t.lineEnd(),t.lineStart(),t.point(v[0][0],v[0][1])))}!g||e&&Br(e,d)||t.point(d[0],d[1]),e=d,l=g,s=m},lineEnd:function(){l&&t.lineEnd(),e=null},clean:function(){return u|(c&&l)<<1}}}),Bn(t,6*Lt),r?[0,-t]:[-At,t-At]);function i(t,r){return Math.cos(t)*Math.cos(r)>e}function a(t,r,n){var i=[1,0,0],a=zr(Ir(t),Ir(r)),o=Pr(a,a),s=a[0],l=o-s*s;if(!l)return!n&&t;var c=e*o/l,u=-e*s/l,f=zr(i,a),h=Dr(i,c);Or(h,Dr(a,u));var p=f,d=Pr(h,p),g=Pr(p,p),m=d*d-g*(Pr(h,h)-1);if(!(m<0)){var v=Math.sqrt(m),x=Dr(p,(-d-v)/g);if(Or(x,h),x=Fr(x),!n)return x;var b,_=t[0],w=r[0],T=t[1],k=r[1];w<_&&(b=_,_=w,w=b);var M=w-_,A=y(M-At)<kt;if(!A&&k<T&&(b=T,T=k,k=b),A||M<kt?A?T+k>0^x[1]<(y(x[0]-_)<kt?T:k):T<=x[1]&&x[1]<=k:M>At^(_<=x[0]&&x[0]<=w)){var S=Dr(p,(-d+v)/g);return Or(S,h),[x,Fr(S)]}}}function o(e,n){var i=r?t:At-t,a=0;return e<-i?a|=1:e>i&&(a|=2),n<-i?a|=4:n>i&&(a|=8),a}}function rn(t,e,r,n){return function(i){var a,o=i.a,s=i.b,l=o.x,c=o.y,u=0,f=1,h=s.x-l,p=s.y-c;if(a=t-l,h||!(a>0)){if(a/=h,h<0){if(a<u)return;a<f&&(f=a)}else if(h>0){if(a>f)return;a>u&&(u=a)}if(a=r-l,h||!(a<0)){if(a/=h,h<0){if(a>f)return;a>u&&(u=a)}else if(h>0){if(a<u)return;a<f&&(f=a)}if(a=e-c,p||!(a>0)){if(a/=p,p<0){if(a<u)return;a<f&&(f=a)}else if(p>0){if(a>f)return;a>u&&(u=a)}if(a=n-c,p||!(a<0)){if(a/=p,p<0){if(a>f)return;a>u&&(u=a)}else if(p>0){if(a<u)return;a<f&&(f=a)}return u>0&&(i.a={x:l+u*h,y:c+u*p}),f<1&&(i.b={x:l+f*h,y:c+f*p}),i}}}}}}function nn(e,r,n,i){return function(l){var c,u,f,h,p,d,g,m,v,y,x,b=l,_=Qr(),w=rn(e,r,n,i),T={point:A,lineStart:function(){T.point=S,u&&u.push(f=[]);y=!0,v=!1,g=m=NaN},lineEnd:function(){c&&(S(h,p),d&&v&&_.rejoin(),c.push(_.buffer()));T.point=A,v&&l.lineEnd()},polygonStart:function(){l=_,c=[],u=[],x=!0},polygonEnd:function(){l=b,c=t.merge(c);var r=function(t){for(var e=0,r=u.length,n=t[1],i=0;i<r;++i)for(var a,o=1,s=u[i],l=s.length,c=s[0];o<l;++o)a=s[o],c[1]<=n?a[1]>n&&zt(c,a,t)>0&&++e:a[1]<=n&&zt(c,a,t)<0&&--e,c=a;return 0!==e}([e,i]),n=x&&r,a=c.length;(n||a)&&(l.polygonStart(),n&&(l.lineStart(),k(null,null,1,l),l.lineEnd()),a&&Wr(c,o,r,k,l),l.polygonEnd()),c=u=f=null}};function k(t,o,l,c){var u=0,f=0;if(null==t||(u=a(t,l))!==(f=a(o,l))||s(t,o)<0^l>0)do{c.point(0===u||3===u?e:n,u>1?i:r)}while((u=(u+l+4)%4)!==f);else c.point(o[0],o[1])}function M(t,a){return e<=t&&t<=n&&r<=a&&a<=i}function A(t,e){M(t,e)&&l.point(t,e)}function S(t,e){var r=M(t=Math.max(-1e9,Math.min(1e9,t)),e=Math.max(-1e9,Math.min(1e9,e)));if(u&&f.push([t,e]),y)h=t,p=e,d=r,y=!1,r&&(l.lineStart(),l.point(t,e));else if(r&&v)l.point(t,e);else{var n={a:{x:g,y:m},b:{x:t,y:e}};w(n)?(v||(l.lineStart(),l.point(n.a.x,n.a.y)),l.point(n.b.x,n.b.y),r||l.lineEnd(),x=!1):r&&(l.lineStart(),l.point(t,e),x=!1)}g=t,m=e,v=r}return T};function a(t,i){return y(t[0]-e)<kt?i>0?0:3:y(t[0]-n)<kt?i>0?2:1:y(t[1]-r)<kt?i>0?1:0:i>0?3:2}function o(t,e){return s(t.x,e.x)}function s(t,e){var r=a(t,1),n=a(e,1);return r!==n?r-n:0===r?e[1]-t[1]:1===r?t[0]-e[0]:2===r?t[1]-e[1]:e[0]-t[0]}}function an(t){var e=0,r=At/3,n=Ln(t),i=n(e,r);return i.parallels=function(t){return arguments.length?n(e=t[0]*At/180,r=t[1]*At/180):[e/At*180,r/At*180]},i}function on(t,e){var r=Math.sin(t),n=(r+Math.sin(e))/2,i=1+r*(2*n-r),a=Math.sqrt(i)/n;function o(t,e){var r=Math.sqrt(i-2*n*Math.sin(e))/n;return[r*Math.sin(t*=n),a-r*Math.cos(t)]}return o.invert=function(t,e){var r=a-e;return[Math.atan2(t,r)/n,Dt((i-(t*t+r*r)*n*n)/(2*n))]},o}t.geo.clipExtent=function(){var t,e,r,n,i,a,o={stream:function(t){return i&&(i.valid=!1),(i=a(t)).valid=!0,i},extent:function(s){return arguments.length?(a=nn(t=+s[0][0],e=+s[0][1],r=+s[1][0],n=+s[1][1]),i&&(i.valid=!1,i=null),o):[[t,e],[r,n]]}};return o.extent([[0,0],[960,500]])},(t.geo.conicEqualArea=function(){return an(on)}).raw=on,t.geo.albers=function(){return t.geo.conicEqualArea().rotate([96,0]).center([-.6,38.7]).parallels([29.5,45.5]).scale(1070)},t.geo.albersUsa=function(){var e,r,n,i,a=t.geo.albers(),o=t.geo.conicEqualArea().rotate([154,0]).center([-2,58.5]).parallels([55,65]),s=t.geo.conicEqualArea().rotate([157,0]).center([-3,19.9]).parallels([8,18]),l={point:function(t,r){e=[t,r]}};function c(t){var a=t[0],o=t[1];return e=null,r(a,o),e||(n(a,o),e)||i(a,o),e}return c.invert=function(t){var e=a.scale(),r=a.translate(),n=(t[0]-r[0])/e,i=(t[1]-r[1])/e;return(i>=.12&&i<.234&&n>=-.425&&n<-.214?o:i>=.166&&i<.234&&n>=-.214&&n<-.115?s:a).invert(t)},c.stream=function(t){var e=a.stream(t),r=o.stream(t),n=s.stream(t);return{point:function(t,i){e.point(t,i),r.point(t,i),n.point(t,i)},sphere:function(){e.sphere(),r.sphere(),n.sphere()},lineStart:function(){e.lineStart(),r.lineStart(),n.lineStart()},lineEnd:function(){e.lineEnd(),r.lineEnd(),n.lineEnd()},polygonStart:function(){e.polygonStart(),r.polygonStart(),n.polygonStart()},polygonEnd:function(){e.polygonEnd(),r.polygonEnd(),n.polygonEnd()}}},c.precision=function(t){return arguments.length?(a.precision(t),o.precision(t),s.precision(t),c):a.precision()},c.scale=function(t){return arguments.length?(a.scale(t),o.scale(.35*t),s.scale(t),c.translate(a.translate())):a.scale()},c.translate=function(t){if(!arguments.length)return a.translate();var e=a.scale(),u=+t[0],f=+t[1];return r=a.translate(t).clipExtent([[u-.455*e,f-.238*e],[u+.455*e,f+.238*e]]).stream(l).point,n=o.translate([u-.307*e,f+.201*e]).clipExtent([[u-.425*e+kt,f+.12*e+kt],[u-.214*e-kt,f+.234*e-kt]]).stream(l).point,i=s.translate([u-.205*e,f+.212*e]).clipExtent([[u-.214*e+kt,f+.166*e+kt],[u-.115*e-kt,f+.234*e-kt]]).stream(l).point,c},c.scale(1070)};var sn,ln,cn,un,fn,hn,pn={point:O,lineStart:O,lineEnd:O,polygonStart:function(){ln=0,pn.lineStart=dn},polygonEnd:function(){pn.lineStart=pn.lineEnd=pn.point=O,sn+=y(ln/2)}};function dn(){var t,e,r,n;function i(t,e){ln+=n*t-r*e,r=t,n=e}pn.point=function(a,o){pn.point=i,t=r=a,e=n=o},pn.lineEnd=function(){i(t,e)}}var gn={point:function(t,e){t<cn&&(cn=t);t>fn&&(fn=t);e<un&&(un=e);e>hn&&(hn=e)},lineStart:O,lineEnd:O,polygonStart:O,polygonEnd:O};function mn(){var t=vn(4.5),e=[],r={point:n,lineStart:function(){r.point=i},lineEnd:o,polygonStart:function(){r.lineEnd=s},polygonEnd:function(){r.lineEnd=o,r.point=n},pointRadius:function(e){return t=vn(e),r},result:function(){if(e.length){var t=e.join("");return e=[],t}}};function n(r,n){e.push("M",r,",",n,t)}function i(t,n){e.push("M",t,",",n),r.point=a}function a(t,r){e.push("L",t,",",r)}function o(){r.point=n}function s(){e.push("Z")}return r}function vn(t){return"m0,"+t+"a"+t+","+t+" 0 1,1 0,"+-2*t+"a"+t+","+t+" 0 1,1 0,"+2*t+"z"}var yn,xn={point:bn,lineStart:_n,lineEnd:wn,polygonStart:function(){xn.lineStart=Tn},polygonEnd:function(){xn.point=bn,xn.lineStart=_n,xn.lineEnd=wn}};function bn(t,e){xr+=t,br+=e,++_r}function _n(){var t,e;function r(r,n){var i=r-t,a=n-e,o=Math.sqrt(i*i+a*a);wr+=o*(t+r)/2,Tr+=o*(e+n)/2,kr+=o,bn(t=r,e=n)}xn.point=function(n,i){xn.point=r,bn(t=n,e=i)}}function wn(){xn.point=bn}function Tn(){var t,e,r,n;function i(t,e){var i=t-r,a=e-n,o=Math.sqrt(i*i+a*a);wr+=o*(r+t)/2,Tr+=o*(n+e)/2,kr+=o,Mr+=(o=n*t-r*e)*(r+t),Ar+=o*(n+e),Sr+=3*o,bn(r=t,n=e)}xn.point=function(a,o){xn.point=i,bn(t=r=a,e=n=o)},xn.lineEnd=function(){i(t,e)}}function kn(t){var e=4.5,r={point:n,lineStart:function(){r.point=i},lineEnd:o,polygonStart:function(){r.lineEnd=s},polygonEnd:function(){r.lineEnd=o,r.point=n},pointRadius:function(t){return e=t,r},result:O};function n(r,n){t.moveTo(r+e,n),t.arc(r,n,e,0,St)}function i(e,n){t.moveTo(e,n),r.point=a}function a(e,r){t.lineTo(e,r)}function o(){r.point=n}function s(){t.closePath()}return r}function Mn(t){var e=.5,r=Math.cos(30*Lt),n=16;function i(t){return(n?o:a)(t)}function a(e){return En(e,(function(r,n){r=t(r,n),e.point(r[0],r[1])}))}function o(e){var r,i,a,o,l,c,u,f,h,p,d,g,m={point:v,lineStart:y,lineEnd:b,polygonStart:function(){e.polygonStart(),m.lineStart=_},polygonEnd:function(){e.polygonEnd(),m.lineStart=y}};function v(r,n){r=t(r,n),e.point(r[0],r[1])}function y(){f=NaN,m.point=x,e.lineStart()}function x(r,i){var a=Ir([r,i]),o=t(r,i);s(f,h,u,p,d,g,f=o[0],h=o[1],u=r,p=a[0],d=a[1],g=a[2],n,e),e.point(f,h)}function b(){m.point=v,e.lineEnd()}function _(){y(),m.point=w,m.lineEnd=T}function w(t,e){x(r=t,e),i=f,a=h,o=p,l=d,c=g,m.point=x}function T(){s(f,h,u,p,d,g,i,a,r,o,l,c,n,e),m.lineEnd=b,b()}return m}function s(n,i,a,o,l,c,u,f,h,p,d,g,m,v){var x=u-n,b=f-i,_=x*x+b*b;if(_>4*e&&m--){var w=o+p,T=l+d,k=c+g,M=Math.sqrt(w*w+T*T+k*k),A=Math.asin(k/=M),S=y(y(k)-1)<kt||y(a-h)<kt?(a+h)/2:Math.atan2(T,w),E=t(S,A),C=E[0],L=E[1],I=C-n,P=L-i,z=b*I-x*P;(z*z/_>e||y((x*I+b*P)/_-.5)>.3||o*p+l*d+c*g<r)&&(s(n,i,a,o,l,c,C,L,S,w/=M,T/=M,k,m,v),v.point(C,L),s(C,L,S,w,T,k,u,f,h,p,d,g,m,v))}}return i.precision=function(t){return arguments.length?(n=(e=t*t)>0&&16,i):Math.sqrt(e)},i}function An(t){var e=Mn((function(e,r){return t([e*It,r*It])}));return function(t){return In(e(t))}}function Sn(t){this.stream=t}function En(t,e){return{point:e,sphere:function(){t.sphere()},lineStart:function(){t.lineStart()},lineEnd:function(){t.lineEnd()},polygonStart:function(){t.polygonStart()},polygonEnd:function(){t.polygonEnd()}}}function Cn(t){return Ln((function(){return t}))()}function Ln(e){var r,n,i,a,o,s,l=Mn((function(t,e){return[(t=r(t,e))[0]*c+a,o-t[1]*c]})),c=150,u=480,f=250,h=0,p=0,d=0,g=0,m=0,v=tn,y=L,x=null,b=null;function _(t){return[(t=i(t[0]*Lt,t[1]*Lt))[0]*c+a,o-t[1]*c]}function w(t){return(t=i.invert((t[0]-a)/c,(o-t[1])/c))&&[t[0]*It,t[1]*It]}function T(){i=Gr(n=On(d,g,m),r);var t=r(h,p);return a=u-t[0]*c,o=f+t[1]*c,k()}function k(){return s&&(s.valid=!1,s=null),_}return _.stream=function(t){return s&&(s.valid=!1),(s=In(v(n,l(y(t))))).valid=!0,s},_.clipAngle=function(t){return arguments.length?(v=null==t?(x=t,tn):en((x=+t)*Lt),k()):x},_.clipExtent=function(t){return arguments.length?(b=t,y=t?nn(t[0][0],t[0][1],t[1][0],t[1][1]):L,k()):b},_.scale=function(t){return arguments.length?(c=+t,T()):c},_.translate=function(t){return arguments.length?(u=+t[0],f=+t[1],T()):[u,f]},_.center=function(t){return arguments.length?(h=t[0]%360*Lt,p=t[1]%360*Lt,T()):[h*It,p*It]},_.rotate=function(t){return arguments.length?(d=t[0]%360*Lt,g=t[1]%360*Lt,m=t.length>2?t[2]%360*Lt:0,T()):[d*It,g*It,m*It]},t.rebind(_,l,"precision"),function(){return r=e.apply(this,arguments),_.invert=r.invert&&w,T()}}function In(t){return En(t,(function(e,r){t.point(e*Lt,r*Lt)}))}function Pn(t,e){return[t,e]}function zn(t,e){return[t>At?t-St:t<-At?t+St:t,e]}function On(t,e,r){return t?e||r?Gr(Rn(t),Fn(e,r)):Rn(t):e||r?Fn(e,r):zn}function Dn(t){return function(e,r){return[(e+=t)>At?e-St:e<-At?e+St:e,r]}}function Rn(t){var e=Dn(t);return e.invert=Dn(-t),e}function Fn(t,e){var r=Math.cos(t),n=Math.sin(t),i=Math.cos(e),a=Math.sin(e);function o(t,e){var o=Math.cos(e),s=Math.cos(t)*o,l=Math.sin(t)*o,c=Math.sin(e),u=c*r+s*n;return[Math.atan2(l*i-u*a,s*r-c*n),Dt(u*i+l*a)]}return o.invert=function(t,e){var o=Math.cos(e),s=Math.cos(t)*o,l=Math.sin(t)*o,c=Math.sin(e),u=c*i-l*a;return[Math.atan2(l*i+c*a,s*r+u*n),Dt(u*r-s*n)]},o}function Bn(t,e){var r=Math.cos(t),n=Math.sin(t);return function(i,a,o,s){var l=o*e;null!=i?(i=Nn(r,i),a=Nn(r,a),(o>0?i<a:i>a)&&(i+=o*St)):(i=t+o*St,a=t-.5*l);for(var c,u=i;o>0?u>a:u<a;u-=l)s.point((c=Fr([r,-n*Math.cos(u),-n*Math.sin(u)]))[0],c[1])}}function Nn(t,e){var r=Ir(e);r[0]-=t,Rr(r);var n=Ot(-r[1]);return((-r[2]<0?-n:n)+2*Math.PI-kt)%(2*Math.PI)}function jn(e,r,n){var i=t.range(e,r-kt,n).concat(r);return function(t){return i.map((function(e){return[t,e]}))}}function Un(e,r,n){var i=t.range(e,r-kt,n).concat(r);return function(t){return i.map((function(e){return[e,t]}))}}function Vn(t){return t.source}function qn(t){return t.target}t.geo.path=function(){var e,r,n,i,a,o=4.5;function s(e){return e&&("function"==typeof o&&i.pointRadius(+o.apply(this,arguments)),a&&a.valid||(a=n(i)),t.geo.stream(e,a)),i.result()}function l(){return a=null,s}return s.area=function(e){return sn=0,t.geo.stream(e,n(pn)),sn},s.centroid=function(e){return xr=br=_r=wr=Tr=kr=Mr=Ar=Sr=0,t.geo.stream(e,n(xn)),Sr?[Mr/Sr,Ar/Sr]:kr?[wr/kr,Tr/kr]:_r?[xr/_r,br/_r]:[NaN,NaN]},s.bounds=function(e){return fn=hn=-(cn=un=1/0),t.geo.stream(e,n(gn)),[[cn,un],[fn,hn]]},s.projection=function(t){return arguments.length?(n=(e=t)?t.stream||An(t):L,l()):e},s.context=function(t){return arguments.length?(i=null==(r=t)?new mn:new kn(t),"function"!=typeof o&&i.pointRadius(o),l()):r},s.pointRadius=function(t){return arguments.length?(o="function"==typeof t?t:(i.pointRadius(+t),+t),s):o},s.projection(t.geo.albersUsa()).context(null)},t.geo.transform=function(t){return{stream:function(e){var r=new Sn(e);for(var n in t)r[n]=t[n];return r}}},Sn.prototype={point:function(t,e){this.stream.point(t,e)},sphere:function(){this.stream.sphere()},lineStart:function(){this.stream.lineStart()},lineEnd:function(){this.stream.lineEnd()},polygonStart:function(){this.stream.polygonStart()},polygonEnd:function(){this.stream.polygonEnd()}},t.geo.projection=Cn,t.geo.projectionMutator=Ln,(t.geo.equirectangular=function(){return Cn(Pn)}).raw=Pn.invert=Pn,t.geo.rotation=function(t){function e(e){return(e=t(e[0]*Lt,e[1]*Lt))[0]*=It,e[1]*=It,e}return t=On(t[0]%360*Lt,t[1]*Lt,t.length>2?t[2]*Lt:0),e.invert=function(e){return(e=t.invert(e[0]*Lt,e[1]*Lt))[0]*=It,e[1]*=It,e},e},zn.invert=Pn,t.geo.circle=function(){var t,e,r=[0,0],n=6;function i(){var t="function"==typeof r?r.apply(this,arguments):r,n=On(-t[0]*Lt,-t[1]*Lt,0).invert,i=[];return e(null,null,1,{point:function(t,e){i.push(t=n(t,e)),t[0]*=It,t[1]*=It}}),{type:"Polygon",coordinates:[i]}}return i.origin=function(t){return arguments.length?(r=t,i):r},i.angle=function(r){return arguments.length?(e=Bn((t=+r)*Lt,n*Lt),i):t},i.precision=function(r){return arguments.length?(e=Bn(t*Lt,(n=+r)*Lt),i):n},i.angle(90)},t.geo.distance=function(t,e){var r,n=(e[0]-t[0])*Lt,i=t[1]*Lt,a=e[1]*Lt,o=Math.sin(n),s=Math.cos(n),l=Math.sin(i),c=Math.cos(i),u=Math.sin(a),f=Math.cos(a);return Math.atan2(Math.sqrt((r=f*o)*r+(r=c*u-l*f*s)*r),l*u+c*f*s)},t.geo.graticule=function(){var e,r,n,i,a,o,s,l,c,u,f,h,p=10,d=p,g=90,m=360,v=2.5;function x(){return{type:"MultiLineString",coordinates:b()}}function b(){return t.range(Math.ceil(i/g)*g,n,g).map(f).concat(t.range(Math.ceil(l/m)*m,s,m).map(h)).concat(t.range(Math.ceil(r/p)*p,e,p).filter((function(t){return y(t%g)>kt})).map(c)).concat(t.range(Math.ceil(o/d)*d,a,d).filter((function(t){return y(t%m)>kt})).map(u))}return x.lines=function(){return b().map((function(t){return{type:"LineString",coordinates:t}}))},x.outline=function(){return{type:"Polygon",coordinates:[f(i).concat(h(s).slice(1),f(n).reverse().slice(1),h(l).reverse().slice(1))]}},x.extent=function(t){return arguments.length?x.majorExtent(t).minorExtent(t):x.minorExtent()},x.majorExtent=function(t){return arguments.length?(i=+t[0][0],n=+t[1][0],l=+t[0][1],s=+t[1][1],i>n&&(t=i,i=n,n=t),l>s&&(t=l,l=s,s=t),x.precision(v)):[[i,l],[n,s]]},x.minorExtent=function(t){return arguments.length?(r=+t[0][0],e=+t[1][0],o=+t[0][1],a=+t[1][1],r>e&&(t=r,r=e,e=t),o>a&&(t=o,o=a,a=t),x.precision(v)):[[r,o],[e,a]]},x.step=function(t){return arguments.length?x.majorStep(t).minorStep(t):x.minorStep()},x.majorStep=function(t){return arguments.length?(g=+t[0],m=+t[1],x):[g,m]},x.minorStep=function(t){return arguments.length?(p=+t[0],d=+t[1],x):[p,d]},x.precision=function(t){return arguments.length?(v=+t,c=jn(o,a,90),u=Un(r,e,v),f=jn(l,s,90),h=Un(i,n,v),x):v},x.majorExtent([[-180,-90+kt],[180,90-kt]]).minorExtent([[-180,-80-kt],[180,80+kt]])},t.geo.greatArc=function(){var e,r,n=Vn,i=qn;function a(){return{type:"LineString",coordinates:[e||n.apply(this,arguments),r||i.apply(this,arguments)]}}return a.distance=function(){return t.geo.distance(e||n.apply(this,arguments),r||i.apply(this,arguments))},a.source=function(t){return arguments.length?(n=t,e="function"==typeof t?null:t,a):n},a.target=function(t){return arguments.length?(i=t,r="function"==typeof t?null:t,a):i},a.precision=function(){return arguments.length?a:0},a},t.geo.interpolate=function(t,e){return r=t[0]*Lt,n=t[1]*Lt,i=e[0]*Lt,a=e[1]*Lt,o=Math.cos(n),s=Math.sin(n),l=Math.cos(a),c=Math.sin(a),u=o*Math.cos(r),f=o*Math.sin(r),h=l*Math.cos(i),p=l*Math.sin(i),d=2*Math.asin(Math.sqrt(Ft(a-n)+o*l*Ft(i-r))),g=1/Math.sin(d),(m=d?function(t){var e=Math.sin(t*=d)*g,r=Math.sin(d-t)*g,n=r*u+e*h,i=r*f+e*p,a=r*s+e*c;return[Math.atan2(i,n)*It,Math.atan2(a,Math.sqrt(n*n+i*i))*It]}:function(){return[r*It,n*It]}).distance=d,m;var r,n,i,a,o,s,l,c,u,f,h,p,d,g,m},t.geo.length=function(e){return yn=0,t.geo.stream(e,Hn),yn};var Hn={sphere:O,point:O,lineStart:function(){var t,e,r;function n(n,i){var a=Math.sin(i*=Lt),o=Math.cos(i),s=y((n*=Lt)-t),l=Math.cos(s);yn+=Math.atan2(Math.sqrt((s=o*Math.sin(s))*s+(s=r*a-e*o*l)*s),e*a+r*o*l),t=n,e=a,r=o}Hn.point=function(i,a){t=i*Lt,e=Math.sin(a*=Lt),r=Math.cos(a),Hn.point=n},Hn.lineEnd=function(){Hn.point=Hn.lineEnd=O}},lineEnd:O,polygonStart:O,polygonEnd:O};function Gn(t,e){function r(e,r){var n=Math.cos(e),i=Math.cos(r),a=t(n*i);return[a*i*Math.sin(e),a*Math.sin(r)]}return r.invert=function(t,r){var n=Math.sqrt(t*t+r*r),i=e(n),a=Math.sin(i),o=Math.cos(i);return[Math.atan2(t*a,n*o),Math.asin(n&&r*a/n)]},r}var Yn=Gn((function(t){return Math.sqrt(2/(1+t))}),(function(t){return 2*Math.asin(t/2)}));(t.geo.azimuthalEqualArea=function(){return Cn(Yn)}).raw=Yn;var Wn=Gn((function(t){var e=Math.acos(t);return e&&e/Math.sin(e)}),L);function Xn(t,e){var r=Math.cos(t),n=function(t){return Math.tan(At/4+t/2)},i=t===e?Math.sin(t):Math.log(r/Math.cos(e))/Math.log(n(e)/n(t)),a=r*Math.pow(n(t),i)/i;if(!i)return Kn;function o(t,e){a>0?e<-Ct+kt&&(e=-Ct+kt):e>Ct-kt&&(e=Ct-kt);var r=a/Math.pow(n(e),i);return[r*Math.sin(i*t),a-r*Math.cos(i*t)]}return o.invert=function(t,e){var r=a-e,n=Pt(i)*Math.sqrt(t*t+r*r);return[Math.atan2(t,r)/i,2*Math.atan(Math.pow(a/n,1/i))-Ct]},o}function Zn(t,e){var r=Math.cos(t),n=t===e?Math.sin(t):(r-Math.cos(e))/(e-t),i=r/n+t;if(y(n)<kt)return Pn;function a(t,e){var r=i-e;return[r*Math.sin(n*t),i-r*Math.cos(n*t)]}return a.invert=function(t,e){var r=i-e;return[Math.atan2(t,r)/n,i-Pt(n)*Math.sqrt(t*t+r*r)]},a}(t.geo.azimuthalEquidistant=function(){return Cn(Wn)}).raw=Wn,(t.geo.conicConformal=function(){return an(Xn)}).raw=Xn,(t.geo.conicEquidistant=function(){return an(Zn)}).raw=Zn;var Jn=Gn((function(t){return 1/t}),Math.atan);function Kn(t,e){return[t,Math.log(Math.tan(At/4+e/2))]}function Qn(t){var e,r=Cn(t),n=r.scale,i=r.translate,a=r.clipExtent;return r.scale=function(){var t=n.apply(r,arguments);return t===r?e?r.clipExtent(null):r:t},r.translate=function(){var t=i.apply(r,arguments);return t===r?e?r.clipExtent(null):r:t},r.clipExtent=function(t){var o=a.apply(r,arguments);if(o===r){if(e=null==t){var s=At*n(),l=i();a([[l[0]-s,l[1]-s],[l[0]+s,l[1]+s]])}}else e&&(o=null);return o},r.clipExtent(null)}(t.geo.gnomonic=function(){return Cn(Jn)}).raw=Jn,Kn.invert=function(t,e){return[t,2*Math.atan(Math.exp(e))-Ct]},(t.geo.mercator=function(){return Qn(Kn)}).raw=Kn;var $n=Gn((function(){return 1}),Math.asin);(t.geo.orthographic=function(){return Cn($n)}).raw=$n;var ti=Gn((function(t){return 1/(1+t)}),(function(t){return 2*Math.atan(t)}));function ei(t,e){return[Math.log(Math.tan(At/4+e/2)),-t]}function ri(t){return t[0]}function ni(t){return t[1]}function ii(t){for(var e=t.length,r=[0,1],n=2,i=2;i<e;i++){for(;n>1&&zt(t[r[n-2]],t[r[n-1]],t[i])<=0;)--n;r[n++]=i}return r.slice(0,n)}function ai(t,e){return t[0]-e[0]||t[1]-e[1]}(t.geo.stereographic=function(){return Cn(ti)}).raw=ti,ei.invert=function(t,e){return[-e,2*Math.atan(Math.exp(t))-Ct]},(t.geo.transverseMercator=function(){var t=Qn(ei),e=t.center,r=t.rotate;return t.center=function(t){return t?e([-t[1],t[0]]):[(t=e())[1],-t[0]]},t.rotate=function(t){return t?r([t[0],t[1],t.length>2?t[2]+90:90]):[(t=r())[0],t[1],t[2]-90]},r([0,0,90])}).raw=ei,t.geom={},t.geom.hull=function(t){var e=ri,r=ni;if(arguments.length)return n(t);function n(t){if(t.length<3)return[];var n,i=de(e),a=de(r),o=t.length,s=[],l=[];for(n=0;n<o;n++)s.push([+i.call(this,t[n],n),+a.call(this,t[n],n),n]);for(s.sort(ai),n=0;n<o;n++)l.push([s[n][0],-s[n][1]]);var c=ii(s),u=ii(l),f=u[0]===c[0],h=u[u.length-1]===c[c.length-1],p=[];for(n=c.length-1;n>=0;--n)p.push(t[s[c[n]][2]]);for(n=+f;n<u.length-h;++n)p.push(t[s[u[n]][2]]);return p}return n.x=function(t){return arguments.length?(e=t,n):e},n.y=function(t){return arguments.length?(r=t,n):r},n},t.geom.polygon=function(t){return U(t,oi),t};var oi=t.geom.polygon.prototype=[];function si(t,e,r){return(r[0]-e[0])*(t[1]-e[1])<(r[1]-e[1])*(t[0]-e[0])}function li(t,e,r,n){var i=t[0],a=r[0],o=e[0]-i,s=n[0]-a,l=t[1],c=r[1],u=e[1]-l,f=n[1]-c,h=(s*(l-c)-f*(i-a))/(f*o-s*u);return[i+h*o,l+h*u]}function ci(t){var e=t[0],r=t[t.length-1];return!(e[0]-r[0]||e[1]-r[1])}oi.area=function(){for(var t,e=-1,r=this.length,n=this[r-1],i=0;++e<r;)t=n,n=this[e],i+=t[1]*n[0]-t[0]*n[1];return.5*i},oi.centroid=function(t){var e,r,n=-1,i=this.length,a=0,o=0,s=this[i-1];for(arguments.length||(t=-1/(6*this.area()));++n<i;)e=s,s=this[n],r=e[0]*s[1]-s[0]*e[1],a+=(e[0]+s[0])*r,o+=(e[1]+s[1])*r;return[a*t,o*t]},oi.clip=function(t){for(var e,r,n,i,a,o,s=ci(t),l=-1,c=this.length-ci(this),u=this[c-1];++l<c;){for(e=t.slice(),t.length=0,i=this[l],a=e[(n=e.length-s)-1],r=-1;++r<n;)si(o=e[r],u,i)?(si(a,u,i)||t.push(li(a,o,u,i)),t.push(o)):si(a,u,i)&&t.push(li(a,o,u,i)),a=o;s&&t.push(t[0]),u=i}return t};var ui,fi,hi,pi,di,gi=[],mi=[];function vi(){Ri(this),this.edge=this.site=this.circle=null}function yi(t){var e=gi.pop()||new vi;return e.site=t,e}function xi(t){Ei(t),hi.remove(t),gi.push(t),Ri(t)}function bi(t){var e=t.circle,r=e.x,n=e.cy,i={x:r,y:n},a=t.P,o=t.N,s=[t];xi(t);for(var l=a;l.circle&&y(r-l.circle.x)<kt&&y(n-l.circle.cy)<kt;)a=l.P,s.unshift(l),xi(l),l=a;s.unshift(l),Ei(l);for(var c=o;c.circle&&y(r-c.circle.x)<kt&&y(n-c.circle.cy)<kt;)o=c.N,s.push(c),xi(c),c=o;s.push(c),Ei(c);var u,f=s.length;for(u=1;u<f;++u)c=s[u],l=s[u-1],zi(c.edge,l.site,c.site,i);l=s[0],(c=s[f-1]).edge=Ii(l.site,c.site,null,i),Si(l),Si(c)}function _i(t){for(var e,r,n,i,a=t.x,o=t.y,s=hi._;s;)if((n=wi(s,o)-a)>kt)s=s.L;else{if(!((i=a-Ti(s,o))>kt)){n>-kt?(e=s.P,r=s):i>-kt?(e=s,r=s.N):e=r=s;break}if(!s.R){e=s;break}s=s.R}var l=yi(t);if(hi.insert(e,l),e||r){if(e===r)return Ei(e),r=yi(e.site),hi.insert(l,r),l.edge=r.edge=Ii(e.site,l.site),Si(e),void Si(r);if(r){Ei(e),Ei(r);var c=e.site,u=c.x,f=c.y,h=t.x-u,p=t.y-f,d=r.site,g=d.x-u,m=d.y-f,v=2*(h*m-p*g),y=h*h+p*p,x=g*g+m*m,b={x:(m*y-p*x)/v+u,y:(h*x-g*y)/v+f};zi(r.edge,c,d,b),l.edge=Ii(c,t,null,b),r.edge=Ii(t,d,null,b),Si(e),Si(r)}else l.edge=Ii(e.site,l.site)}}function wi(t,e){var r=t.site,n=r.x,i=r.y,a=i-e;if(!a)return n;var o=t.P;if(!o)return-1/0;var s=(r=o.site).x,l=r.y,c=l-e;if(!c)return s;var u=s-n,f=1/a-1/c,h=u/c;return f?(-h+Math.sqrt(h*h-2*f*(u*u/(-2*c)-l+c/2+i-a/2)))/f+n:(n+s)/2}function Ti(t,e){var r=t.N;if(r)return wi(r,e);var n=t.site;return n.y===e?n.x:1/0}function ki(t){this.site=t,this.edges=[]}function Mi(t,e){return e.angle-t.angle}function Ai(){Ri(this),this.x=this.y=this.arc=this.site=this.cy=null}function Si(t){var e=t.P,r=t.N;if(e&&r){var n=e.site,i=t.site,a=r.site;if(n!==a){var o=i.x,s=i.y,l=n.x-o,c=n.y-s,u=a.x-o,f=2*(l*(m=a.y-s)-c*u);if(!(f>=-Mt)){var h=l*l+c*c,p=u*u+m*m,d=(m*h-c*p)/f,g=(l*p-u*h)/f,m=g+s,v=mi.pop()||new Ai;v.arc=t,v.site=i,v.x=d+o,v.y=m+Math.sqrt(d*d+g*g),v.cy=m,t.circle=v;for(var y=null,x=di._;x;)if(v.y<x.y||v.y===x.y&&v.x<=x.x){if(!x.L){y=x.P;break}x=x.L}else{if(!x.R){y=x;break}x=x.R}di.insert(y,v),y||(pi=v)}}}}function Ei(t){var e=t.circle;e&&(e.P||(pi=e.N),di.remove(e),mi.push(e),Ri(e),t.circle=null)}function Ci(t,e){var r=t.b;if(r)return!0;var n,i,a=t.a,o=e[0][0],s=e[1][0],l=e[0][1],c=e[1][1],u=t.l,f=t.r,h=u.x,p=u.y,d=f.x,g=f.y,m=(h+d)/2,v=(p+g)/2;if(g===p){if(m<o||m>=s)return;if(h>d){if(a){if(a.y>=c)return}else a={x:m,y:l};r={x:m,y:c}}else{if(a){if(a.y<l)return}else a={x:m,y:c};r={x:m,y:l}}}else if(i=v-(n=(h-d)/(g-p))*m,n<-1||n>1)if(h>d){if(a){if(a.y>=c)return}else a={x:(l-i)/n,y:l};r={x:(c-i)/n,y:c}}else{if(a){if(a.y<l)return}else a={x:(c-i)/n,y:c};r={x:(l-i)/n,y:l}}else if(p<g){if(a){if(a.x>=s)return}else a={x:o,y:n*o+i};r={x:s,y:n*s+i}}else{if(a){if(a.x<o)return}else a={x:s,y:n*s+i};r={x:o,y:n*o+i}}return t.a=a,t.b=r,!0}function Li(t,e){this.l=t,this.r=e,this.a=this.b=null}function Ii(t,e,r,n){var i=new Li(t,e);return ui.push(i),r&&zi(i,t,e,r),n&&zi(i,e,t,n),fi[t.i].edges.push(new Oi(i,t,e)),fi[e.i].edges.push(new Oi(i,e,t)),i}function Pi(t,e,r){var n=new Li(t,null);return n.a=e,n.b=r,ui.push(n),n}function zi(t,e,r,n){t.a||t.b?t.l===r?t.b=n:t.a=n:(t.a=n,t.l=e,t.r=r)}function Oi(t,e,r){var n=t.a,i=t.b;this.edge=t,this.site=e,this.angle=r?Math.atan2(r.y-e.y,r.x-e.x):t.l===e?Math.atan2(i.x-n.x,n.y-i.y):Math.atan2(n.x-i.x,i.y-n.y)}function Di(){this._=null}function Ri(t){t.U=t.C=t.L=t.R=t.P=t.N=null}function Fi(t,e){var r=e,n=e.R,i=r.U;i?i.L===r?i.L=n:i.R=n:t._=n,n.U=i,r.U=n,r.R=n.L,r.R&&(r.R.U=r),n.L=r}function Bi(t,e){var r=e,n=e.L,i=r.U;i?i.L===r?i.L=n:i.R=n:t._=n,n.U=i,r.U=n,r.L=n.R,r.L&&(r.L.U=r),n.R=r}function Ni(t){for(;t.L;)t=t.L;return t}function ji(t,e){var r,n,i,a=t.sort(Ui).pop();for(ui=[],fi=new Array(t.length),hi=new Di,di=new Di;;)if(i=pi,a&&(!i||a.y<i.y||a.y===i.y&&a.x<i.x))a.x===r&&a.y===n||(fi[a.i]=new ki(a),_i(a),r=a.x,n=a.y),a=t.pop();else{if(!i)break;bi(i.arc)}e&&(function(t){for(var e,r=ui,n=rn(t[0][0],t[0][1],t[1][0],t[1][1]),i=r.length;i--;)(!Ci(e=r[i],t)||!n(e)||y(e.a.x-e.b.x)<kt&&y(e.a.y-e.b.y)<kt)&&(e.a=e.b=null,r.splice(i,1))}(e),function(t){for(var e,r,n,i,a,o,s,l,c,u,f=t[0][0],h=t[1][0],p=t[0][1],d=t[1][1],g=fi,m=g.length;m--;)if((a=g[m])&&a.prepare())for(l=(s=a.edges).length,o=0;o<l;)n=(u=s[o].end()).x,i=u.y,e=(c=s[++o%l].start()).x,r=c.y,(y(n-e)>kt||y(i-r)>kt)&&(s.splice(o,0,new Oi(Pi(a.site,u,y(n-f)<kt&&d-i>kt?{x:f,y:y(e-f)<kt?r:d}:y(i-d)<kt&&h-n>kt?{x:y(r-d)<kt?e:h,y:d}:y(n-h)<kt&&i-p>kt?{x:h,y:y(e-h)<kt?r:p}:y(i-p)<kt&&n-f>kt?{x:y(r-p)<kt?e:f,y:p}:null),a.site,null)),++l)}(e));var o={cells:fi,edges:ui};return hi=di=ui=fi=null,o}function Ui(t,e){return e.y-t.y||e.x-t.x}ki.prototype.prepare=function(){for(var t,e=this.edges,r=e.length;r--;)(t=e[r].edge).b&&t.a||e.splice(r,1);return e.sort(Mi),e.length},Oi.prototype={start:function(){return this.edge.l===this.site?this.edge.a:this.edge.b},end:function(){return this.edge.l===this.site?this.edge.b:this.edge.a}},Di.prototype={insert:function(t,e){var r,n,i;if(t){if(e.P=t,e.N=t.N,t.N&&(t.N.P=e),t.N=e,t.R){for(t=t.R;t.L;)t=t.L;t.L=e}else t.R=e;r=t}else this._?(t=Ni(this._),e.P=null,e.N=t,t.P=t.L=e,r=t):(e.P=e.N=null,this._=e,r=null);for(e.L=e.R=null,e.U=r,e.C=!0,t=e;r&&r.C;)r===(n=r.U).L?(i=n.R)&&i.C?(r.C=i.C=!1,n.C=!0,t=n):(t===r.R&&(Fi(this,r),r=(t=r).U),r.C=!1,n.C=!0,Bi(this,n)):(i=n.L)&&i.C?(r.C=i.C=!1,n.C=!0,t=n):(t===r.L&&(Bi(this,r),r=(t=r).U),r.C=!1,n.C=!0,Fi(this,n)),r=t.U;this._.C=!1},remove:function(t){t.N&&(t.N.P=t.P),t.P&&(t.P.N=t.N),t.N=t.P=null;var e,r,n,i=t.U,a=t.L,o=t.R;if(r=a?o?Ni(o):a:o,i?i.L===t?i.L=r:i.R=r:this._=r,a&&o?(n=r.C,r.C=t.C,r.L=a,a.U=r,r!==o?(i=r.U,r.U=t.U,t=r.R,i.L=t,r.R=o,o.U=r):(r.U=i,i=r,t=r.R)):(n=t.C,t=r),t&&(t.U=i),!n)if(t&&t.C)t.C=!1;else{do{if(t===this._)break;if(t===i.L){if((e=i.R).C&&(e.C=!1,i.C=!0,Fi(this,i),e=i.R),e.L&&e.L.C||e.R&&e.R.C){e.R&&e.R.C||(e.L.C=!1,e.C=!0,Bi(this,e),e=i.R),e.C=i.C,i.C=e.R.C=!1,Fi(this,i),t=this._;break}}else if((e=i.L).C&&(e.C=!1,i.C=!0,Bi(this,i),e=i.L),e.L&&e.L.C||e.R&&e.R.C){e.L&&e.L.C||(e.R.C=!1,e.C=!0,Fi(this,e),e=i.L),e.C=i.C,i.C=e.L.C=!1,Bi(this,i),t=this._;break}e.C=!0,t=i,i=i.U}while(!t.C);t&&(t.C=!1)}}},t.geom.voronoi=function(t){var e=ri,r=ni,n=e,i=r,a=Vi;if(t)return o(t);function o(t){var e=new Array(t.length),r=a[0][0],n=a[0][1],i=a[1][0],o=a[1][1];return ji(s(t),a).cells.forEach((function(a,s){var l=a.edges,c=a.site;(e[s]=l.length?l.map((function(t){var e=t.start();return[e.x,e.y]})):c.x>=r&&c.x<=i&&c.y>=n&&c.y<=o?[[r,o],[i,o],[i,n],[r,n]]:[]).point=t[s]})),e}function s(t){return t.map((function(t,e){return{x:Math.round(n(t,e)/kt)*kt,y:Math.round(i(t,e)/kt)*kt,i:e}}))}return o.links=function(t){return ji(s(t)).edges.filter((function(t){return t.l&&t.r})).map((function(e){return{source:t[e.l.i],target:t[e.r.i]}}))},o.triangles=function(t){var e=[];return ji(s(t)).cells.forEach((function(r,n){for(var i,a,o,s,l=r.site,c=r.edges.sort(Mi),u=-1,f=c.length,h=c[f-1].edge,p=h.l===l?h.r:h.l;++u<f;)h,i=p,p=(h=c[u].edge).l===l?h.r:h.l,n<i.i&&n<p.i&&(o=i,s=p,((a=l).x-s.x)*(o.y-a.y)-(a.x-o.x)*(s.y-a.y)<0)&&e.push([t[n],t[i.i],t[p.i]])})),e},o.x=function(t){return arguments.length?(n=de(e=t),o):e},o.y=function(t){return arguments.length?(i=de(r=t),o):r},o.clipExtent=function(t){return arguments.length?(a=null==t?Vi:t,o):a===Vi?null:a},o.size=function(t){return arguments.length?o.clipExtent(t&&[[0,0],t]):a===Vi?null:a&&a[1]},o};var Vi=[[-1e6,-1e6],[1e6,1e6]];function qi(t){return t.x}function Hi(t){return t.y}function Gi(t,e,r,n,i,a){if(!t(e,r,n,i,a)){var o=.5*(r+i),s=.5*(n+a),l=e.nodes;l[0]&&Gi(t,l[0],r,n,o,s),l[1]&&Gi(t,l[1],o,n,i,s),l[2]&&Gi(t,l[2],r,s,o,a),l[3]&&Gi(t,l[3],o,s,i,a)}}function Yi(t,e,r,n,i,a,o){var s,l=1/0;return function t(c,u,f,h,p){if(!(u>a||f>o||h<n||p<i)){if(d=c.point){var d,g=e-c.x,m=r-c.y,v=g*g+m*m;if(v<l){var y=Math.sqrt(l=v);n=e-y,i=r-y,a=e+y,o=r+y,s=d}}for(var x=c.nodes,b=.5*(u+h),_=.5*(f+p),w=(r>=_)<<1|e>=b,T=w+4;w<T;++w)if(c=x[3&w])switch(3&w){case 0:t(c,u,f,b,_);break;case 1:t(c,b,f,h,_);break;case 2:t(c,u,_,b,p);break;case 3:t(c,b,_,h,p)}}}(t,n,i,a,o),s}function Wi(e,r){e=t.rgb(e),r=t.rgb(r);var n=e.r,i=e.g,a=e.b,o=r.r-n,s=r.g-i,l=r.b-a;return function(t){return"#"+se(Math.round(n+o*t))+se(Math.round(i+s*t))+se(Math.round(a+l*t))}}function Xi(t,e){var r,n={},i={};for(r in t)r in e?n[r]=$i(t[r],e[r]):i[r]=t[r];for(r in e)r in t||(i[r]=e[r]);return function(t){for(r in n)i[r]=n[r](t);return i}}function Zi(t,e){return t=+t,e=+e,function(r){return t*(1-r)+e*r}}function Ji(t,e){var r,n,i,a=Ki.lastIndex=Qi.lastIndex=0,o=-1,s=[],l=[];for(t+="",e+="";(r=Ki.exec(t))&&(n=Qi.exec(e));)(i=n.index)>a&&(i=e.slice(a,i),s[o]?s[o]+=i:s[++o]=i),(r=r[0])===(n=n[0])?s[o]?s[o]+=n:s[++o]=n:(s[++o]=null,l.push({i:o,x:Zi(r,n)})),a=Qi.lastIndex;return a<e.length&&(i=e.slice(a),s[o]?s[o]+=i:s[++o]=i),s.length<2?l[0]?(e=l[0].x,function(t){return e(t)+""}):function(){return e}:(e=l.length,function(t){for(var r,n=0;n<e;++n)s[(r=l[n]).i]=r.x(t);return s.join("")})}t.geom.delaunay=function(e){return t.geom.voronoi().triangles(e)},t.geom.quadtree=function(t,e,r,n,i){var a,o=ri,s=ni;if(a=arguments.length)return o=qi,s=Hi,3===a&&(i=r,n=e,r=e=0),l(t);function l(t){var l,c,u,f,h,p,d,g,m,v=de(o),x=de(s);if(null!=e)p=e,d=r,g=n,m=i;else if(g=m=-(p=d=1/0),c=[],u=[],h=t.length,a)for(f=0;f<h;++f)(l=t[f]).x<p&&(p=l.x),l.y<d&&(d=l.y),l.x>g&&(g=l.x),l.y>m&&(m=l.y),c.push(l.x),u.push(l.y);else for(f=0;f<h;++f){var b=+v(l=t[f],f),_=+x(l,f);b<p&&(p=b),_<d&&(d=_),b>g&&(g=b),_>m&&(m=_),c.push(b),u.push(_)}var w=g-p,T=m-d;function k(t,e,r,n,i,a,o,s){if(!isNaN(r)&&!isNaN(n))if(t.leaf){var l=t.x,c=t.y;if(null!=l)if(y(l-r)+y(c-n)<.01)M(t,e,r,n,i,a,o,s);else{var u=t.point;t.x=t.y=t.point=null,M(t,u,l,c,i,a,o,s),M(t,e,r,n,i,a,o,s)}else t.x=r,t.y=n,t.point=e}else M(t,e,r,n,i,a,o,s)}function M(t,e,r,n,i,a,o,s){var l=.5*(i+o),c=.5*(a+s),u=r>=l,f=n>=c,h=f<<1|u;t.leaf=!1,u?i=l:o=l,f?a=c:s=c,k(t=t.nodes[h]||(t.nodes[h]={leaf:!0,nodes:[],point:null,x:null,y:null}),e,r,n,i,a,o,s)}w>T?m=d+w:g=p+T;var A={leaf:!0,nodes:[],point:null,x:null,y:null,add:function(t){k(A,t,+v(t,++f),+x(t,f),p,d,g,m)},visit:function(t){Gi(t,A,p,d,g,m)},find:function(t){return Yi(A,t[0],t[1],p,d,g,m)}};if(f=-1,null==e){for(;++f<h;)k(A,t[f],c[f],u[f],p,d,g,m);--f}else t.forEach(A.add);return c=u=t=l=null,A}return l.x=function(t){return arguments.length?(o=t,l):o},l.y=function(t){return arguments.length?(s=t,l):s},l.extent=function(t){return arguments.length?(null==t?e=r=n=i=null:(e=+t[0][0],r=+t[0][1],n=+t[1][0],i=+t[1][1]),l):null==e?null:[[e,r],[n,i]]},l.size=function(t){return arguments.length?(null==t?e=r=n=i=null:(e=r=0,n=+t[0],i=+t[1]),l):null==e?null:[n-e,i-r]},l},t.interpolateRgb=Wi,t.interpolateObject=Xi,t.interpolateNumber=Zi,t.interpolateString=Ji;var Ki=/[-+]?(?:\d+\.?\d*|\.?\d+)(?:[eE][-+]?\d+)?/g,Qi=new RegExp(Ki.source,"g");function $i(e,r){for(var n,i=t.interpolators.length;--i>=0&&!(n=t.interpolators[i](e,r)););return n}function ta(t,e){var r,n=[],i=[],a=t.length,o=e.length,s=Math.min(t.length,e.length);for(r=0;r<s;++r)n.push($i(t[r],e[r]));for(;r<a;++r)i[r]=t[r];for(;r<o;++r)i[r]=e[r];return function(t){for(r=0;r<s;++r)i[r]=n[r](t);return i}}t.interpolate=$i,t.interpolators=[function(t,e){var r=typeof e;return("string"===r?pe.has(e.toLowerCase())||/^(#|rgb\(|hsl\()/i.test(e)?Wi:Ji:e instanceof Vt?Wi:Array.isArray(e)?ta:"object"===r&&isNaN(e)?Xi:Zi)(t,e)}],t.interpolateArray=ta;var ea=function(){return L},ra=t.map({linear:ea,poly:function(t){return function(e){return Math.pow(e,t)}},quad:function(){return sa},cubic:function(){return la},sin:function(){return ua},exp:function(){return fa},circle:function(){return ha},elastic:function(t,e){var r;arguments.length<2&&(e=.45);arguments.length?r=e/St*Math.asin(1/t):(t=1,r=e/4);return function(n){return 1+t*Math.pow(2,-10*n)*Math.sin((n-r)*St/e)}},back:function(t){t||(t=1.70158);return function(e){return e*e*((t+1)*e-t)}},bounce:function(){return pa}}),na=t.map({in:L,out:aa,"in-out":oa,"out-in":function(t){return oa(aa(t))}});function ia(t){return function(e){return e<=0?0:e>=1?1:t(e)}}function aa(t){return function(e){return 1-t(1-e)}}function oa(t){return function(e){return.5*(e<.5?t(2*e):2-t(2-2*e))}}function sa(t){return t*t}function la(t){return t*t*t}function ca(t){if(t<=0)return 0;if(t>=1)return 1;var e=t*t,r=e*t;return 4*(t<.5?r:3*(t-e)+r-.75)}function ua(t){return 1-Math.cos(t*Ct)}function fa(t){return Math.pow(2,10*(t-1))}function ha(t){return 1-Math.sqrt(1-t*t)}function pa(t){return t<1/2.75?7.5625*t*t:t<2/2.75?7.5625*(t-=1.5/2.75)*t+.75:t<2.5/2.75?7.5625*(t-=2.25/2.75)*t+.9375:7.5625*(t-=2.625/2.75)*t+.984375}function da(t,e){return e-=t,function(r){return Math.round(t+e*r)}}function ga(t){var e,r,n,i=[t.a,t.b],a=[t.c,t.d],o=va(i),s=ma(i,a),l=va(((e=a)[0]+=(n=-s)*(r=i)[0],e[1]+=n*r[1],e))||0;i[0]*a[1]<a[0]*i[1]&&(i[0]*=-1,i[1]*=-1,o*=-1,s*=-1),this.rotate=(o?Math.atan2(i[1],i[0]):Math.atan2(-a[0],a[1]))*It,this.translate=[t.e,t.f],this.scale=[o,l],this.skew=l?Math.atan2(s,l)*It:0}function ma(t,e){return t[0]*e[0]+t[1]*e[1]}function va(t){var e=Math.sqrt(ma(t,t));return e&&(t[0]/=e,t[1]/=e),e}t.ease=function(t){var e=t.indexOf("-"),n=e>=0?t.slice(0,e):t,i=e>=0?t.slice(e+1):"in";return n=ra.get(n)||ea,ia((i=na.get(i)||L)(n.apply(null,r.call(arguments,1))))},t.interpolateHcl=function(e,r){e=t.hcl(e),r=t.hcl(r);var n=e.h,i=e.c,a=e.l,o=r.h-n,s=r.c-i,l=r.l-a;isNaN(s)&&(s=0,i=isNaN(i)?r.c:i);isNaN(o)?(o=0,n=isNaN(n)?r.h:n):o>180?o-=360:o<-180&&(o+=360);return function(t){return Xt(n+o*t,i+s*t,a+l*t)+""}},t.interpolateHsl=function(e,r){e=t.hsl(e),r=t.hsl(r);var n=e.h,i=e.s,a=e.l,o=r.h-n,s=r.s-i,l=r.l-a;isNaN(s)&&(s=0,i=isNaN(i)?r.s:i);isNaN(o)?(o=0,n=isNaN(n)?r.h:n):o>180?o-=360:o<-180&&(o+=360);return function(t){return Gt(n+o*t,i+s*t,a+l*t)+""}},t.interpolateLab=function(e,r){e=t.lab(e),r=t.lab(r);var n=e.l,i=e.a,a=e.b,o=r.l-n,s=r.a-i,l=r.b-a;return function(t){return Qt(n+o*t,i+s*t,a+l*t)+""}},t.interpolateRound=da,t.transform=function(e){var r=i.createElementNS(t.ns.prefix.svg,"g");return(t.transform=function(t){if(null!=t){r.setAttribute("transform",t);var e=r.transform.baseVal.consolidate()}return new ga(e?e.matrix:ya)})(e)},ga.prototype.toString=function(){return"translate("+this.translate+")rotate("+this.rotate+")skewX("+this.skew+")scale("+this.scale+")"};var ya={a:1,b:0,c:0,d:1,e:0,f:0};function xa(t){return t.length?t.pop()+",":""}function ba(e,r){var n=[],i=[];return e=t.transform(e),r=t.transform(r),function(t,e,r,n){if(t[0]!==e[0]||t[1]!==e[1]){var i=r.push("translate(",null,",",null,")");n.push({i:i-4,x:Zi(t[0],e[0])},{i:i-2,x:Zi(t[1],e[1])})}else(e[0]||e[1])&&r.push("translate("+e+")")}(e.translate,r.translate,n,i),function(t,e,r,n){t!==e?(t-e>180?e+=360:e-t>180&&(t+=360),n.push({i:r.push(xa(r)+"rotate(",null,")")-2,x:Zi(t,e)})):e&&r.push(xa(r)+"rotate("+e+")")}(e.rotate,r.rotate,n,i),function(t,e,r,n){t!==e?n.push({i:r.push(xa(r)+"skewX(",null,")")-2,x:Zi(t,e)}):e&&r.push(xa(r)+"skewX("+e+")")}(e.skew,r.skew,n,i),function(t,e,r,n){if(t[0]!==e[0]||t[1]!==e[1]){var i=r.push(xa(r)+"scale(",null,",",null,")");n.push({i:i-4,x:Zi(t[0],e[0])},{i:i-2,x:Zi(t[1],e[1])})}else 1===e[0]&&1===e[1]||r.push(xa(r)+"scale("+e+")")}(e.scale,r.scale,n,i),e=r=null,function(t){for(var e,r=-1,a=i.length;++r<a;)n[(e=i[r]).i]=e.x(t);return n.join("")}}function _a(t,e){return e=(e-=t=+t)||1/e,function(r){return(r-t)/e}}function wa(t,e){return e=(e-=t=+t)||1/e,function(r){return Math.max(0,Math.min(1,(r-t)/e))}}function Ta(t){for(var e=t.source,r=t.target,n=function(t,e){if(t===e)return t;var r=ka(t),n=ka(e),i=r.pop(),a=n.pop(),o=null;for(;i===a;)o=i,i=r.pop(),a=n.pop();return o}(e,r),i=[e];e!==n;)e=e.parent,i.push(e);for(var a=i.length;r!==n;)i.splice(a,0,r),r=r.parent;return i}function ka(t){for(var e=[],r=t.parent;null!=r;)e.push(t),t=r,r=r.parent;return e.push(t),e}function Ma(t){t.fixed|=2}function Aa(t){t.fixed&=-7}function Sa(t){t.fixed|=4,t.px=t.x,t.py=t.y}function Ea(t){t.fixed&=-5}t.interpolateTransform=ba,t.layout={},t.layout.bundle=function(){return function(t){for(var e=[],r=-1,n=t.length;++r<n;)e.push(Ta(t[r]));return e}},t.layout.chord=function(){var e,r,n,i,a,o,s,l={},c=0;function u(){var l,u,h,p,d,g={},m=[],v=t.range(i),y=[];for(e=[],r=[],l=0,p=-1;++p<i;){for(u=0,d=-1;++d<i;)u+=n[p][d];m.push(u),y.push(t.range(i)),l+=u}for(a&&v.sort((function(t,e){return a(m[t],m[e])})),o&&y.forEach((function(t,e){t.sort((function(t,r){return o(n[e][t],n[e][r])}))})),l=(St-c*i)/l,u=0,p=-1;++p<i;){for(h=u,d=-1;++d<i;){var x=v[p],b=y[x][d],_=n[x][b],w=u,T=u+=_*l;g[x+"-"+b]={index:x,subindex:b,startAngle:w,endAngle:T,value:_}}r[x]={index:x,startAngle:h,endAngle:u,value:m[x]},u+=c}for(p=-1;++p<i;)for(d=p-1;++d<i;){var k=g[p+"-"+d],M=g[d+"-"+p];(k.value||M.value)&&e.push(k.value<M.value?{source:M,target:k}:{source:k,target:M})}s&&f()}function f(){e.sort((function(t,e){return s((t.source.value+t.target.value)/2,(e.source.value+e.target.value)/2)}))}return l.matrix=function(t){return arguments.length?(i=(n=t)&&n.length,e=r=null,l):n},l.padding=function(t){return arguments.length?(c=t,e=r=null,l):c},l.sortGroups=function(t){return arguments.length?(a=t,e=r=null,l):a},l.sortSubgroups=function(t){return arguments.length?(o=t,e=null,l):o},l.sortChords=function(t){return arguments.length?(s=t,e&&f(),l):s},l.chords=function(){return e||u(),e},l.groups=function(){return r||u(),r},l},t.layout.force=function(){var e,r,n,i,a,o,s={},l=t.dispatch("start","tick","end"),c=[1,1],u=.9,f=Ca,h=La,p=-30,d=Ia,g=.1,m=.64,v=[],y=[];function x(t){return function(e,r,n,i){if(e.point!==t){var a=e.cx-t.x,o=e.cy-t.y,s=i-r,l=a*a+o*o;if(s*s/m<l){if(l<d){var c=e.charge/l;t.px-=a*c,t.py-=o*c}return!0}if(e.point&&l&&l<d){c=e.pointCharge/l;t.px-=a*c,t.py-=o*c}}return!e.charge}}function b(e){e.px=t.event.x,e.py=t.event.y,s.resume()}return s.tick=function(){if((n*=.99)<.005)return e=null,l.end({type:"end",alpha:n=0}),!0;var r,s,f,h,d,m,b,_,w,T=v.length,k=y.length;for(s=0;s<k;++s)h=(f=y[s]).source,(m=(_=(d=f.target).x-h.x)*_+(w=d.y-h.y)*w)&&(_*=m=n*a[s]*((m=Math.sqrt(m))-i[s])/m,w*=m,d.x-=_*(b=h.weight+d.weight?h.weight/(h.weight+d.weight):.5),d.y-=w*b,h.x+=_*(b=1-b),h.y+=w*b);if((b=n*g)&&(_=c[0]/2,w=c[1]/2,s=-1,b))for(;++s<T;)(f=v[s]).x+=(_-f.x)*b,f.y+=(w-f.y)*b;if(p)for(!function t(e,r,n){var i=0,a=0;if(e.charge=0,!e.leaf)for(var o,s=e.nodes,l=s.length,c=-1;++c<l;)null!=(o=s[c])&&(t(o,r,n),e.charge+=o.charge,i+=o.charge*o.cx,a+=o.charge*o.cy);if(e.point){e.leaf||(e.point.x+=Math.random()-.5,e.point.y+=Math.random()-.5);var u=r*n[e.point.index];e.charge+=e.pointCharge=u,i+=u*e.point.x,a+=u*e.point.y}e.cx=i/e.charge,e.cy=a/e.charge}(r=t.geom.quadtree(v),n,o),s=-1;++s<T;)(f=v[s]).fixed||r.visit(x(f));for(s=-1;++s<T;)(f=v[s]).fixed?(f.x=f.px,f.y=f.py):(f.x-=(f.px-(f.px=f.x))*u,f.y-=(f.py-(f.py=f.y))*u);l.tick({type:"tick",alpha:n})},s.nodes=function(t){return arguments.length?(v=t,s):v},s.links=function(t){return arguments.length?(y=t,s):y},s.size=function(t){return arguments.length?(c=t,s):c},s.linkDistance=function(t){return arguments.length?(f="function"==typeof t?t:+t,s):f},s.distance=s.linkDistance,s.linkStrength=function(t){return arguments.length?(h="function"==typeof t?t:+t,s):h},s.friction=function(t){return arguments.length?(u=+t,s):u},s.charge=function(t){return arguments.length?(p="function"==typeof t?t:+t,s):p},s.chargeDistance=function(t){return arguments.length?(d=t*t,s):Math.sqrt(d)},s.gravity=function(t){return arguments.length?(g=+t,s):g},s.theta=function(t){return arguments.length?(m=t*t,s):Math.sqrt(m)},s.alpha=function(t){return arguments.length?(t=+t,n?t>0?n=t:(e.c=null,e.t=NaN,e=null,l.end({type:"end",alpha:n=0})):t>0&&(l.start({type:"start",alpha:n=t}),e=we(s.tick)),s):n},s.start=function(){var t,e,r,n=v.length,l=y.length,u=c[0],d=c[1];for(t=0;t<n;++t)(r=v[t]).index=t,r.weight=0;for(t=0;t<l;++t)"number"==typeof(r=y[t]).source&&(r.source=v[r.source]),"number"==typeof r.target&&(r.target=v[r.target]),++r.source.weight,++r.target.weight;for(t=0;t<n;++t)r=v[t],isNaN(r.x)&&(r.x=g("x",u)),isNaN(r.y)&&(r.y=g("y",d)),isNaN(r.px)&&(r.px=r.x),isNaN(r.py)&&(r.py=r.y);if(i=[],"function"==typeof f)for(t=0;t<l;++t)i[t]=+f.call(this,y[t],t);else for(t=0;t<l;++t)i[t]=f;if(a=[],"function"==typeof h)for(t=0;t<l;++t)a[t]=+h.call(this,y[t],t);else for(t=0;t<l;++t)a[t]=h;if(o=[],"function"==typeof p)for(t=0;t<n;++t)o[t]=+p.call(this,v[t],t);else for(t=0;t<n;++t)o[t]=p;function g(r,i){if(!e){for(e=new Array(n),c=0;c<n;++c)e[c]=[];for(c=0;c<l;++c){var a=y[c];e[a.source.index].push(a.target),e[a.target.index].push(a.source)}}for(var o,s=e[t],c=-1,u=s.length;++c<u;)if(!isNaN(o=s[c][r]))return o;return Math.random()*i}return s.resume()},s.resume=function(){return s.alpha(.1)},s.stop=function(){return s.alpha(0)},s.drag=function(){if(r||(r=t.behavior.drag().origin(L).on("dragstart.force",Ma).on("drag.force",b).on("dragend.force",Aa)),!arguments.length)return r;this.on("mouseover.force",Sa).on("mouseout.force",Ea).call(r)},t.rebind(s,l,"on")};var Ca=20,La=1,Ia=1/0;function Pa(e,r){return t.rebind(e,r,"sort","children","value"),e.nodes=e,e.links=Ba,e}function za(t,e){for(var r=[t];null!=(t=r.pop());)if(e(t),(i=t.children)&&(n=i.length))for(var n,i;--n>=0;)r.push(i[n])}function Oa(t,e){for(var r=[t],n=[];null!=(t=r.pop());)if(n.push(t),(a=t.children)&&(i=a.length))for(var i,a,o=-1;++o<i;)r.push(a[o]);for(;null!=(t=n.pop());)e(t)}function Da(t){return t.children}function Ra(t){return t.value}function Fa(t,e){return e.value-t.value}function Ba(e){return t.merge(e.map((function(t){return(t.children||[]).map((function(e){return{source:t,target:e}}))})))}t.layout.hierarchy=function(){var t=Fa,e=Da,r=Ra;function n(i){var a,o=[i],s=[];for(i.depth=0;null!=(a=o.pop());)if(s.push(a),(c=e.call(n,a,a.depth))&&(l=c.length)){for(var l,c,u;--l>=0;)o.push(u=c[l]),u.parent=a,u.depth=a.depth+1;r&&(a.value=0),a.children=c}else r&&(a.value=+r.call(n,a,a.depth)||0),delete a.children;return Oa(i,(function(e){var n,i;t&&(n=e.children)&&n.sort(t),r&&(i=e.parent)&&(i.value+=e.value)})),s}return n.sort=function(e){return arguments.length?(t=e,n):t},n.children=function(t){return arguments.length?(e=t,n):e},n.value=function(t){return arguments.length?(r=t,n):r},n.revalue=function(t){return r&&(za(t,(function(t){t.children&&(t.value=0)})),Oa(t,(function(t){var e;t.children||(t.value=+r.call(n,t,t.depth)||0),(e=t.parent)&&(e.value+=t.value)}))),t},n},t.layout.partition=function(){var e=t.layout.hierarchy(),r=[1,1];function n(t,n){var i=e.call(this,t,n);return function t(e,r,n,i){var a=e.children;if(e.x=r,e.y=e.depth*i,e.dx=n,e.dy=i,a&&(o=a.length)){var o,s,l,c=-1;for(n=e.value?n/e.value:0;++c<o;)t(s=a[c],r,l=s.value*n,i),r+=l}}(i[0],0,r[0],r[1]/function t(e){var r=e.children,n=0;if(r&&(i=r.length))for(var i,a=-1;++a<i;)n=Math.max(n,t(r[a]));return 1+n}(i[0])),i}return n.size=function(t){return arguments.length?(r=t,n):r},Pa(n,e)},t.layout.pie=function(){var e=Number,r=Na,n=0,i=St,a=0;function o(s){var l,c=s.length,u=s.map((function(t,r){return+e.call(o,t,r)})),f=+("function"==typeof n?n.apply(this,arguments):n),h=("function"==typeof i?i.apply(this,arguments):i)-f,p=Math.min(Math.abs(h)/c,+("function"==typeof a?a.apply(this,arguments):a)),d=p*(h<0?-1:1),g=t.sum(u),m=g?(h-c*d)/g:0,v=t.range(c),y=[];return null!=r&&v.sort(r===Na?function(t,e){return u[e]-u[t]}:function(t,e){return r(s[t],s[e])}),v.forEach((function(t){y[t]={data:s[t],value:l=u[t],startAngle:f,endAngle:f+=l*m+d,padAngle:p}})),y}return o.value=function(t){return arguments.length?(e=t,o):e},o.sort=function(t){return arguments.length?(r=t,o):r},o.startAngle=function(t){return arguments.length?(n=t,o):n},o.endAngle=function(t){return arguments.length?(i=t,o):i},o.padAngle=function(t){return arguments.length?(a=t,o):a},o};var Na={};function ja(t){return t.x}function Ua(t){return t.y}function Va(t,e,r){t.y0=e,t.y=r}t.layout.stack=function(){var e=L,r=Ga,n=Ya,i=Va,a=ja,o=Ua;function s(l,c){if(!(p=l.length))return l;var u=l.map((function(t,r){return e.call(s,t,r)})),f=u.map((function(t){return t.map((function(t,e){return[a.call(s,t,e),o.call(s,t,e)]}))})),h=r.call(s,f,c);u=t.permute(u,h),f=t.permute(f,h);var p,d,g,m,v=n.call(s,f,c),y=u[0].length;for(g=0;g<y;++g)for(i.call(s,u[0][g],m=v[g],f[0][g][1]),d=1;d<p;++d)i.call(s,u[d][g],m+=f[d-1][g][1],f[d][g][1]);return l}return s.values=function(t){return arguments.length?(e=t,s):e},s.order=function(t){return arguments.length?(r="function"==typeof t?t:qa.get(t)||Ga,s):r},s.offset=function(t){return arguments.length?(n="function"==typeof t?t:Ha.get(t)||Ya,s):n},s.x=function(t){return arguments.length?(a=t,s):a},s.y=function(t){return arguments.length?(o=t,s):o},s.out=function(t){return arguments.length?(i=t,s):i},s};var qa=t.map({"inside-out":function(e){var r,n,i=e.length,a=e.map(Wa),o=e.map(Xa),s=t.range(i).sort((function(t,e){return a[t]-a[e]})),l=0,c=0,u=[],f=[];for(r=0;r<i;++r)n=s[r],l<c?(l+=o[n],u.push(n)):(c+=o[n],f.push(n));return f.reverse().concat(u)},reverse:function(e){return t.range(e.length).reverse()},default:Ga}),Ha=t.map({silhouette:function(t){var e,r,n,i=t.length,a=t[0].length,o=[],s=0,l=[];for(r=0;r<a;++r){for(e=0,n=0;e<i;e++)n+=t[e][r][1];n>s&&(s=n),o.push(n)}for(r=0;r<a;++r)l[r]=(s-o[r])/2;return l},wiggle:function(t){var e,r,n,i,a,o,s,l,c,u=t.length,f=t[0],h=f.length,p=[];for(p[0]=l=c=0,r=1;r<h;++r){for(e=0,i=0;e<u;++e)i+=t[e][r][1];for(e=0,a=0,s=f[r][0]-f[r-1][0];e<u;++e){for(n=0,o=(t[e][r][1]-t[e][r-1][1])/(2*s);n<e;++n)o+=(t[n][r][1]-t[n][r-1][1])/s;a+=o*t[e][r][1]}p[r]=l-=i?a/i*s:0,l<c&&(c=l)}for(r=0;r<h;++r)p[r]-=c;return p},expand:function(t){var e,r,n,i=t.length,a=t[0].length,o=1/i,s=[];for(r=0;r<a;++r){for(e=0,n=0;e<i;e++)n+=t[e][r][1];if(n)for(e=0;e<i;e++)t[e][r][1]/=n;else for(e=0;e<i;e++)t[e][r][1]=o}for(r=0;r<a;++r)s[r]=0;return s},zero:Ya});function Ga(e){return t.range(e.length)}function Ya(t){for(var e=-1,r=t[0].length,n=[];++e<r;)n[e]=0;return n}function Wa(t){for(var e,r=1,n=0,i=t[0][1],a=t.length;r<a;++r)(e=t[r][1])>i&&(n=r,i=e);return n}function Xa(t){return t.reduce(Za,0)}function Za(t,e){return t+e[1]}function Ja(t,e){return Ka(t,Math.ceil(Math.log(e.length)/Math.LN2+1))}function Ka(t,e){for(var r=-1,n=+t[0],i=(t[1]-n)/e,a=[];++r<=e;)a[r]=i*r+n;return a}function Qa(e){return[t.min(e),t.max(e)]}function $a(t,e){return t.value-e.value}function to(t,e){var r=t._pack_next;t._pack_next=e,e._pack_prev=t,e._pack_next=r,r._pack_prev=e}function eo(t,e){t._pack_next=e,e._pack_prev=t}function ro(t,e){var r=e.x-t.x,n=e.y-t.y,i=t.r+e.r;return.999*i*i>r*r+n*n}function no(t){if((e=t.children)&&(l=e.length)){var e,r,n,i,a,o,s,l,c=1/0,u=-1/0,f=1/0,h=-1/0;if(e.forEach(io),(r=e[0]).x=-r.r,r.y=0,x(r),l>1&&((n=e[1]).x=n.r,n.y=0,x(n),l>2))for(oo(r,n,i=e[2]),x(i),to(r,i),r._pack_prev=i,to(i,n),n=r._pack_next,a=3;a<l;a++){oo(r,n,i=e[a]);var p=0,d=1,g=1;for(o=n._pack_next;o!==n;o=o._pack_next,d++)if(ro(o,i)){p=1;break}if(1==p)for(s=r._pack_prev;s!==o._pack_prev&&!ro(s,i);s=s._pack_prev,g++);p?(d<g||d==g&&n.r<r.r?eo(r,n=o):eo(r=s,n),a--):(to(r,i),n=i,x(i))}var m=(c+u)/2,v=(f+h)/2,y=0;for(a=0;a<l;a++)(i=e[a]).x-=m,i.y-=v,y=Math.max(y,i.r+Math.sqrt(i.x*i.x+i.y*i.y));t.r=y,e.forEach(ao)}function x(t){c=Math.min(t.x-t.r,c),u=Math.max(t.x+t.r,u),f=Math.min(t.y-t.r,f),h=Math.max(t.y+t.r,h)}}function io(t){t._pack_next=t._pack_prev=t}function ao(t){delete t._pack_next,delete t._pack_prev}function oo(t,e,r){var n=t.r+r.r,i=e.x-t.x,a=e.y-t.y;if(n&&(i||a)){var o=e.r+r.r,s=i*i+a*a,l=.5+((n*=n)-(o*=o))/(2*s),c=Math.sqrt(Math.max(0,2*o*(n+s)-(n-=s)*n-o*o))/(2*s);r.x=t.x+l*i+c*a,r.y=t.y+l*a-c*i}else r.x=t.x+n,r.y=t.y}function so(t,e){return t.parent==e.parent?1:2}function lo(t){var e=t.children;return e.length?e[0]:t.t}function co(t){var e,r=t.children;return(e=r.length)?r[e-1]:t.t}function uo(t,e,r){var n=r/(e.i-t.i);e.c-=n,e.s+=r,t.c+=n,e.z+=r,e.m+=r}function fo(t,e,r){return t.a.parent===e.parent?t.a:r}function ho(t){return{x:t.x,y:t.y,dx:t.dx,dy:t.dy}}function po(t,e){var r=t.x+e[3],n=t.y+e[0],i=t.dx-e[1]-e[3],a=t.dy-e[0]-e[2];return i<0&&(r+=i/2,i=0),a<0&&(n+=a/2,a=0),{x:r,y:n,dx:i,dy:a}}function go(t){var e=t[0],r=t[t.length-1];return e<r?[e,r]:[r,e]}function mo(t){return t.rangeExtent?t.rangeExtent():go(t.range())}function vo(t,e,r,n){var i=r(t[0],t[1]),a=n(e[0],e[1]);return function(t){return a(i(t))}}function yo(t,e){var r,n=0,i=t.length-1,a=t[n],o=t[i];return o<a&&(r=n,n=i,i=r,r=a,a=o,o=r),t[n]=e.floor(a),t[i]=e.ceil(o),t}function xo(t){return t?{floor:function(e){return Math.floor(e/t)*t},ceil:function(e){return Math.ceil(e/t)*t}}:bo}t.layout.histogram=function(){var e=!0,r=Number,n=Qa,i=Ja;function a(a,o){for(var s,l,c=[],u=a.map(r,this),f=n.call(this,u,o),h=i.call(this,f,u,o),p=(o=-1,u.length),d=h.length-1,g=e?1:1/p;++o<d;)(s=c[o]=[]).dx=h[o+1]-(s.x=h[o]),s.y=0;if(d>0)for(o=-1;++o<p;)(l=u[o])>=f[0]&&l<=f[1]&&((s=c[t.bisect(h,l,1,d)-1]).y+=g,s.push(a[o]));return c}return a.value=function(t){return arguments.length?(r=t,a):r},a.range=function(t){return arguments.length?(n=de(t),a):n},a.bins=function(t){return arguments.length?(i="number"==typeof t?function(e){return Ka(e,t)}:de(t),a):i},a.frequency=function(t){return arguments.length?(e=!!t,a):e},a},t.layout.pack=function(){var e,r=t.layout.hierarchy().sort($a),n=0,i=[1,1];function a(t,a){var o=r.call(this,t,a),s=o[0],l=i[0],c=i[1],u=null==e?Math.sqrt:"function"==typeof e?e:function(){return e};if(s.x=s.y=0,Oa(s,(function(t){t.r=+u(t.value)})),Oa(s,no),n){var f=n*(e?1:Math.max(2*s.r/l,2*s.r/c))/2;Oa(s,(function(t){t.r+=f})),Oa(s,no),Oa(s,(function(t){t.r-=f}))}return function t(e,r,n,i){var a=e.children;if(e.x=r+=i*e.x,e.y=n+=i*e.y,e.r*=i,a)for(var o=-1,s=a.length;++o<s;)t(a[o],r,n,i)}(s,l/2,c/2,e?1:1/Math.max(2*s.r/l,2*s.r/c)),o}return a.size=function(t){return arguments.length?(i=t,a):i},a.radius=function(t){return arguments.length?(e=null==t||"function"==typeof t?t:+t,a):e},a.padding=function(t){return arguments.length?(n=+t,a):n},Pa(a,r)},t.layout.tree=function(){var e=t.layout.hierarchy().sort(null).value(null),r=so,n=[1,1],i=null;function a(t,a){var c=e.call(this,t,a),u=c[0],f=function(t){var e,r={A:null,children:[t]},n=[r];for(;null!=(e=n.pop());)for(var i,a=e.children,o=0,s=a.length;o<s;++o)n.push((a[o]=i={_:a[o],parent:e,children:(i=a[o].children)&&i.slice()||[],A:null,a:null,z:0,m:0,c:0,s:0,t:null,i:o}).a=i);return r.children[0]}(u);if(Oa(f,o),f.parent.m=-f.z,za(f,s),i)za(u,l);else{var h=u,p=u,d=u;za(u,(function(t){t.x<h.x&&(h=t),t.x>p.x&&(p=t),t.depth>d.depth&&(d=t)}));var g=r(h,p)/2-h.x,m=n[0]/(p.x+r(p,h)/2+g),v=n[1]/(d.depth||1);za(u,(function(t){t.x=(t.x+g)*m,t.y=t.depth*v}))}return c}function o(t){var e=t.children,n=t.parent.children,i=t.i?n[t.i-1]:null;if(e.length){!function(t){var e,r=0,n=0,i=t.children,a=i.length;for(;--a>=0;)(e=i[a]).z+=r,e.m+=r,r+=e.s+(n+=e.c)}(t);var a=(e[0].z+e[e.length-1].z)/2;i?(t.z=i.z+r(t._,i._),t.m=t.z-a):t.z=a}else i&&(t.z=i.z+r(t._,i._));t.parent.A=function(t,e,n){if(e){for(var i,a=t,o=t,s=e,l=a.parent.children[0],c=a.m,u=o.m,f=s.m,h=l.m;s=co(s),a=lo(a),s&&a;)l=lo(l),(o=co(o)).a=t,(i=s.z+f-a.z-c+r(s._,a._))>0&&(uo(fo(s,t,n),t,i),c+=i,u+=i),f+=s.m,c+=a.m,h+=l.m,u+=o.m;s&&!co(o)&&(o.t=s,o.m+=f-u),a&&!lo(l)&&(l.t=a,l.m+=c-h,n=t)}return n}(t,i,t.parent.A||n[0])}function s(t){t._.x=t.z+t.parent.m,t.m+=t.parent.m}function l(t){t.x*=n[0],t.y=t.depth*n[1]}return a.separation=function(t){return arguments.length?(r=t,a):r},a.size=function(t){return arguments.length?(i=null==(n=t)?l:null,a):i?null:n},a.nodeSize=function(t){return arguments.length?(i=null==(n=t)?null:l,a):i?n:null},Pa(a,e)},t.layout.cluster=function(){var e=t.layout.hierarchy().sort(null).value(null),r=so,n=[1,1],i=!1;function a(a,o){var s,l=e.call(this,a,o),c=l[0],u=0;Oa(c,(function(e){var n=e.children;n&&n.length?(e.x=function(t){return t.reduce((function(t,e){return t+e.x}),0)/t.length}(n),e.y=function(e){return 1+t.max(e,(function(t){return t.y}))}(n)):(e.x=s?u+=r(e,s):0,e.y=0,s=e)}));var f=function t(e){var r=e.children;return r&&r.length?t(r[0]):e}(c),h=function t(e){var r,n=e.children;return n&&(r=n.length)?t(n[r-1]):e}(c),p=f.x-r(f,h)/2,d=h.x+r(h,f)/2;return Oa(c,i?function(t){t.x=(t.x-c.x)*n[0],t.y=(c.y-t.y)*n[1]}:function(t){t.x=(t.x-p)/(d-p)*n[0],t.y=(1-(c.y?t.y/c.y:1))*n[1]}),l}return a.separation=function(t){return arguments.length?(r=t,a):r},a.size=function(t){return arguments.length?(i=null==(n=t),a):i?null:n},a.nodeSize=function(t){return arguments.length?(i=null!=(n=t),a):i?n:null},Pa(a,e)},t.layout.treemap=function(){var e,r=t.layout.hierarchy(),n=Math.round,i=[1,1],a=null,o=ho,s=!1,l="squarify",c=.5*(1+Math.sqrt(5));function u(t,e){for(var r,n,i=-1,a=t.length;++i<a;)n=(r=t[i]).value*(e<0?0:e),r.area=isNaN(n)||n<=0?0:n}function f(t){var e=t.children;if(e&&e.length){var r,n,i,a=o(t),s=[],c=e.slice(),h=1/0,g="slice"===l?a.dx:"dice"===l?a.dy:"slice-dice"===l?1&t.depth?a.dy:a.dx:Math.min(a.dx,a.dy);for(u(c,a.dx*a.dy/t.value),s.area=0;(i=c.length)>0;)s.push(r=c[i-1]),s.area+=r.area,"squarify"!==l||(n=p(s,g))<=h?(c.pop(),h=n):(s.area-=s.pop().area,d(s,g,a,!1),g=Math.min(a.dx,a.dy),s.length=s.area=0,h=1/0);s.length&&(d(s,g,a,!0),s.length=s.area=0),e.forEach(f)}}function h(t){var e=t.children;if(e&&e.length){var r,n=o(t),i=e.slice(),a=[];for(u(i,n.dx*n.dy/t.value),a.area=0;r=i.pop();)a.push(r),a.area+=r.area,null!=r.z&&(d(a,r.z?n.dx:n.dy,n,!i.length),a.length=a.area=0);e.forEach(h)}}function p(t,e){for(var r,n=t.area,i=0,a=1/0,o=-1,s=t.length;++o<s;)(r=t[o].area)&&(r<a&&(a=r),r>i&&(i=r));return e*=e,(n*=n)?Math.max(e*i*c/n,n/(e*a*c)):1/0}function d(t,e,r,i){var a,o=-1,s=t.length,l=r.x,c=r.y,u=e?n(t.area/e):0;if(e==r.dx){for((i||u>r.dy)&&(u=r.dy);++o<s;)(a=t[o]).x=l,a.y=c,a.dy=u,l+=a.dx=Math.min(r.x+r.dx-l,u?n(a.area/u):0);a.z=!0,a.dx+=r.x+r.dx-l,r.y+=u,r.dy-=u}else{for((i||u>r.dx)&&(u=r.dx);++o<s;)(a=t[o]).x=l,a.y=c,a.dx=u,c+=a.dy=Math.min(r.y+r.dy-c,u?n(a.area/u):0);a.z=!1,a.dy+=r.y+r.dy-c,r.x+=u,r.dx-=u}}function g(t){var n=e||r(t),a=n[0];return a.x=a.y=0,a.value?(a.dx=i[0],a.dy=i[1]):a.dx=a.dy=0,e&&r.revalue(a),u([a],a.dx*a.dy/a.value),(e?h:f)(a),s&&(e=n),n}return g.size=function(t){return arguments.length?(i=t,g):i},g.padding=function(t){if(!arguments.length)return a;function e(e){var r=t.call(g,e,e.depth);return null==r?ho(e):po(e,"number"==typeof r?[r,r,r,r]:r)}function r(e){return po(e,t)}var n;return o=null==(a=t)?ho:"function"==(n=typeof t)?e:"number"===n?(t=[t,t,t,t],r):r,g},g.round=function(t){return arguments.length?(n=t?Math.round:Number,g):n!=Number},g.sticky=function(t){return arguments.length?(s=t,e=null,g):s},g.ratio=function(t){return arguments.length?(c=t,g):c},g.mode=function(t){return arguments.length?(l=t+"",g):l},Pa(g,r)},t.random={normal:function(t,e){var r=arguments.length;return r<2&&(e=1),r<1&&(t=0),function(){var r,n,i;do{i=(r=2*Math.random()-1)*r+(n=2*Math.random()-1)*n}while(!i||i>1);return t+e*r*Math.sqrt(-2*Math.log(i)/i)}},logNormal:function(){var e=t.random.normal.apply(t,arguments);return function(){return Math.exp(e())}},bates:function(e){var r=t.random.irwinHall(e);return function(){return r()/e}},irwinHall:function(t){return function(){for(var e=0,r=0;r<t;r++)e+=Math.random();return e}}},t.scale={};var bo={floor:L,ceil:L};function _o(e,r,n,i){var a=[],o=[],s=0,l=Math.min(e.length,r.length)-1;for(e[l]<e[0]&&(e=e.slice().reverse(),r=r.slice().reverse());++s<=l;)a.push(n(e[s-1],e[s])),o.push(i(r[s-1],r[s]));return function(r){var n=t.bisect(e,r,1,l)-1;return o[n](a[n](r))}}function wo(e,r){return t.rebind(e,r,"range","rangeRound","interpolate","clamp")}function To(t,e){return yo(t,xo(ko(t,e)[2])),yo(t,xo(ko(t,e)[2])),t}function ko(t,e){null==e&&(e=10);var r=go(t),n=r[1]-r[0],i=Math.pow(10,Math.floor(Math.log(n/e)/Math.LN10)),a=e/n*i;return a<=.15?i*=10:a<=.35?i*=5:a<=.75&&(i*=2),r[0]=Math.ceil(r[0]/i)*i,r[1]=Math.floor(r[1]/i)*i+.5*i,r[2]=i,r}function Mo(e,r){return t.range.apply(t,ko(e,r))}function Ao(e,r,n){var i=ko(e,r);if(n){var a=Ce.exec(n);if(a.shift(),"s"===a[8]){var o=t.formatPrefix(Math.max(y(i[0]),y(i[1])));return a[7]||(a[7]="."+Eo(o.scale(i[2]))),a[8]="f",n=t.format(a.join("")),function(t){return n(o.scale(t))+o.symbol}}a[7]||(a[7]="."+function(t,e){var r=Eo(e[2]);return t in So?Math.abs(r-Eo(Math.max(y(e[0]),y(e[1]))))+ +("e"!==t):r-2*("%"===t)}(a[8],i)),n=a.join("")}else n=",."+Eo(i[2])+"f";return t.format(n)}t.scale.linear=function(){return function t(e,r,n,i){var a,o;function s(){var t=Math.min(e.length,r.length)>2?_o:vo,s=i?wa:_a;return a=t(e,r,s,n),o=t(r,e,s,$i),l}function l(t){return a(t)}return l.invert=function(t){return o(t)},l.domain=function(t){return arguments.length?(e=t.map(Number),s()):e},l.range=function(t){return arguments.length?(r=t,s()):r},l.rangeRound=function(t){return l.range(t).interpolate(da)},l.clamp=function(t){return arguments.length?(i=t,s()):i},l.interpolate=function(t){return arguments.length?(n=t,s()):n},l.ticks=function(t){return Mo(e,t)},l.tickFormat=function(t,r){return Ao(e,t,r)},l.nice=function(t){return To(e,t),s()},l.copy=function(){return t(e,r,n,i)},s()}([0,1],[0,1],$i,!1)};var So={s:1,g:1,p:1,r:1,e:1};function Eo(t){return-Math.floor(Math.log(t)/Math.LN10+.01)}t.scale.log=function(){return function e(r,n,i,a){function o(t){return(i?Math.log(t<0?0:t):-Math.log(t>0?0:-t))/Math.log(n)}function s(t){return i?Math.pow(n,t):-Math.pow(n,-t)}function l(t){return r(o(t))}return l.invert=function(t){return s(r.invert(t))},l.domain=function(t){return arguments.length?(i=t[0]>=0,r.domain((a=t.map(Number)).map(o)),l):a},l.base=function(t){return arguments.length?(n=+t,r.domain(a.map(o)),l):n},l.nice=function(){var t=yo(a.map(o),i?Math:Lo);return r.domain(t),a=t.map(s),l},l.ticks=function(){var t=go(a),e=[],r=t[0],l=t[1],c=Math.floor(o(r)),u=Math.ceil(o(l)),f=n%1?2:n;if(isFinite(u-c)){if(i){for(;c<u;c++)for(var h=1;h<f;h++)e.push(s(c)*h);e.push(s(c))}else for(e.push(s(c));c++<u;)for(h=f-1;h>0;h--)e.push(s(c)*h);for(c=0;e[c]<r;c++);for(u=e.length;e[u-1]>l;u--);e=e.slice(c,u)}return e},l.tickFormat=function(e,r){if(!arguments.length)return Co;arguments.length<2?r=Co:"function"!=typeof r&&(r=t.format(r));var i=Math.max(1,n*e/l.ticks().length);return function(t){var e=t/s(Math.round(o(t)));return e*n<n-.5&&(e*=n),e<=i?r(t):""}},l.copy=function(){return e(r.copy(),n,i,a)},wo(l,r)}(t.scale.linear().domain([0,1]),10,!0,[1,10])};var Co=t.format(".0e"),Lo={floor:function(t){return-Math.ceil(-t)},ceil:function(t){return-Math.floor(-t)}};function Io(t){return function(e){return e<0?-Math.pow(-e,t):Math.pow(e,t)}}t.scale.pow=function(){return function t(e,r,n){var i=Io(r),a=Io(1/r);function o(t){return e(i(t))}return o.invert=function(t){return a(e.invert(t))},o.domain=function(t){return arguments.length?(e.domain((n=t.map(Number)).map(i)),o):n},o.ticks=function(t){return Mo(n,t)},o.tickFormat=function(t,e){return Ao(n,t,e)},o.nice=function(t){return o.domain(To(n,t))},o.exponent=function(t){return arguments.length?(i=Io(r=t),a=Io(1/r),e.domain(n.map(i)),o):r},o.copy=function(){return t(e.copy(),r,n)},wo(o,e)}(t.scale.linear(),1,[0,1])},t.scale.sqrt=function(){return t.scale.pow().exponent(.5)},t.scale.ordinal=function(){return function e(r,n){var i,a,o;function s(t){return a[((i.get(t)||("range"===n.t?i.set(t,r.push(t)):NaN))-1)%a.length]}function l(e,n){return t.range(r.length).map((function(t){return e+n*t}))}return s.domain=function(t){if(!arguments.length)return r;r=[],i=new _;for(var e,a=-1,o=t.length;++a<o;)i.has(e=t[a])||i.set(e,r.push(e));return s[n.t].apply(s,n.a)},s.range=function(t){return arguments.length?(a=t,o=0,n={t:"range",a:arguments},s):a},s.rangePoints=function(t,e){arguments.length<2&&(e=0);var i=t[0],c=t[1],u=r.length<2?(i=(i+c)/2,0):(c-i)/(r.length-1+e);return a=l(i+u*e/2,u),o=0,n={t:"rangePoints",a:arguments},s},s.rangeRoundPoints=function(t,e){arguments.length<2&&(e=0);var i=t[0],c=t[1],u=r.length<2?(i=c=Math.round((i+c)/2),0):(c-i)/(r.length-1+e)|0;return a=l(i+Math.round(u*e/2+(c-i-(r.length-1+e)*u)/2),u),o=0,n={t:"rangeRoundPoints",a:arguments},s},s.rangeBands=function(t,e,i){arguments.length<2&&(e=0),arguments.length<3&&(i=e);var c=t[1]<t[0],u=t[c-0],f=t[1-c],h=(f-u)/(r.length-e+2*i);return a=l(u+h*i,h),c&&a.reverse(),o=h*(1-e),n={t:"rangeBands",a:arguments},s},s.rangeRoundBands=function(t,e,i){arguments.length<2&&(e=0),arguments.length<3&&(i=e);var c=t[1]<t[0],u=t[c-0],f=t[1-c],h=Math.floor((f-u)/(r.length-e+2*i));return a=l(u+Math.round((f-u-(r.length-e)*h)/2),h),c&&a.reverse(),o=Math.round(h*(1-e)),n={t:"rangeRoundBands",a:arguments},s},s.rangeBand=function(){return o},s.rangeExtent=function(){return go(n.a[0])},s.copy=function(){return e(r,n)},s.domain(r)}([],{t:"range",a:[[]]})},t.scale.category10=function(){return t.scale.ordinal().range(Po)},t.scale.category20=function(){return t.scale.ordinal().range(zo)},t.scale.category20b=function(){return t.scale.ordinal().range(Oo)},t.scale.category20c=function(){return t.scale.ordinal().range(Do)};var Po=[2062260,16744206,2924588,14034728,9725885,9197131,14907330,8355711,12369186,1556175].map(ae),zo=[2062260,11454440,16744206,16759672,2924588,10018698,14034728,16750742,9725885,12955861,9197131,12885140,14907330,16234194,8355711,13092807,12369186,14408589,1556175,10410725].map(ae),Oo=[3750777,5395619,7040719,10264286,6519097,9216594,11915115,13556636,9202993,12426809,15186514,15190932,8666169,11356490,14049643,15177372,8077683,10834324,13528509,14589654].map(ae),Do=[3244733,7057110,10406625,13032431,15095053,16616764,16625259,16634018,3253076,7652470,10607003,13101504,7695281,10394312,12369372,14342891,6513507,9868950,12434877,14277081].map(ae);function Ro(){return 0}t.scale.quantile=function(){return function e(r,n){var i;function a(){var e=0,a=n.length;for(i=[];++e<a;)i[e-1]=t.quantile(r,e/a);return o}function o(e){if(!isNaN(e=+e))return n[t.bisect(i,e)]}return o.domain=function(t){return arguments.length?(r=t.map(p).filter(d).sort(h),a()):r},o.range=function(t){return arguments.length?(n=t,a()):n},o.quantiles=function(){return i},o.invertExtent=function(t){return(t=n.indexOf(t))<0?[NaN,NaN]:[t>0?i[t-1]:r[0],t<i.length?i[t]:r[r.length-1]]},o.copy=function(){return e(r,n)},a()}([],[])},t.scale.quantize=function(){return function t(e,r,n){var i,a;function o(t){return n[Math.max(0,Math.min(a,Math.floor(i*(t-e))))]}function s(){return i=n.length/(r-e),a=n.length-1,o}return o.domain=function(t){return arguments.length?(e=+t[0],r=+t[t.length-1],s()):[e,r]},o.range=function(t){return arguments.length?(n=t,s()):n},o.invertExtent=function(t){return[t=(t=n.indexOf(t))<0?NaN:t/i+e,t+1/i]},o.copy=function(){return t(e,r,n)},s()}(0,1,[0,1])},t.scale.threshold=function(){return function e(r,n){function i(e){if(e<=e)return n[t.bisect(r,e)]}return i.domain=function(t){return arguments.length?(r=t,i):r},i.range=function(t){return arguments.length?(n=t,i):n},i.invertExtent=function(t){return t=n.indexOf(t),[r[t-1],r[t]]},i.copy=function(){return e(r,n)},i}([.5],[0,1])},t.scale.identity=function(){return function t(e){function r(t){return+t}return r.invert=r,r.domain=r.range=function(t){return arguments.length?(e=t.map(r),r):e},r.ticks=function(t){return Mo(e,t)},r.tickFormat=function(t,r){return Ao(e,t,r)},r.copy=function(){return t(e)},r}([0,1])},t.svg={},t.svg.arc=function(){var t=Bo,e=No,r=Ro,n=Fo,i=jo,a=Uo,o=Vo;function s(){var s=Math.max(0,+t.apply(this,arguments)),c=Math.max(0,+e.apply(this,arguments)),u=i.apply(this,arguments)-Ct,f=a.apply(this,arguments)-Ct,h=Math.abs(f-u),p=u>f?0:1;if(c<s&&(d=c,c=s,s=d),h>=Et)return l(c,p)+(s?l(s,1-p):"")+"Z";var d,g,m,v,y,x,b,_,w,T,k,M,A=0,S=0,E=[];if((v=(+o.apply(this,arguments)||0)/2)&&(m=n===Fo?Math.sqrt(s*s+c*c):+n.apply(this,arguments),p||(S*=-1),c&&(S=Dt(m/c*Math.sin(v))),s&&(A=Dt(m/s*Math.sin(v)))),c){y=c*Math.cos(u+S),x=c*Math.sin(u+S),b=c*Math.cos(f-S),_=c*Math.sin(f-S);var C=Math.abs(f-u-2*S)<=At?0:1;if(S&&qo(y,x,b,_)===p^C){var L=(u+f)/2;y=c*Math.cos(L),x=c*Math.sin(L),b=_=null}}else y=x=0;if(s){w=s*Math.cos(f-A),T=s*Math.sin(f-A),k=s*Math.cos(u+A),M=s*Math.sin(u+A);var I=Math.abs(u-f+2*A)<=At?0:1;if(A&&qo(w,T,k,M)===1-p^I){var P=(u+f)/2;w=s*Math.cos(P),T=s*Math.sin(P),k=M=null}}else w=T=0;if(h>kt&&(d=Math.min(Math.abs(c-s)/2,+r.apply(this,arguments)))>.001){g=s<c^p?0:1;var z=d,O=d;if(h<At){var D=null==k?[w,T]:null==b?[y,x]:li([y,x],[k,M],[b,_],[w,T]),R=y-D[0],F=x-D[1],B=b-D[0],N=_-D[1],j=1/Math.sin(Math.acos((R*B+F*N)/(Math.sqrt(R*R+F*F)*Math.sqrt(B*B+N*N)))/2),U=Math.sqrt(D[0]*D[0]+D[1]*D[1]);O=Math.min(d,(s-U)/(j-1)),z=Math.min(d,(c-U)/(j+1))}if(null!=b){var V=Ho(null==k?[w,T]:[k,M],[y,x],c,z,p),q=Ho([b,_],[w,T],c,z,p);d===z?E.push("M",V[0],"A",z,",",z," 0 0,",g," ",V[1],"A",c,",",c," 0 ",1-p^qo(V[1][0],V[1][1],q[1][0],q[1][1]),",",p," ",q[1],"A",z,",",z," 0 0,",g," ",q[0]):E.push("M",V[0],"A",z,",",z," 0 1,",g," ",q[0])}else E.push("M",y,",",x);if(null!=k){var H=Ho([y,x],[k,M],s,-O,p),G=Ho([w,T],null==b?[y,x]:[b,_],s,-O,p);d===O?E.push("L",G[0],"A",O,",",O," 0 0,",g," ",G[1],"A",s,",",s," 0 ",p^qo(G[1][0],G[1][1],H[1][0],H[1][1]),",",1-p," ",H[1],"A",O,",",O," 0 0,",g," ",H[0]):E.push("L",G[0],"A",O,",",O," 0 0,",g," ",H[0])}else E.push("L",w,",",T)}else E.push("M",y,",",x),null!=b&&E.push("A",c,",",c," 0 ",C,",",p," ",b,",",_),E.push("L",w,",",T),null!=k&&E.push("A",s,",",s," 0 ",I,",",1-p," ",k,",",M);return E.push("Z"),E.join("")}function l(t,e){return"M0,"+t+"A"+t+","+t+" 0 1,"+e+" 0,"+-t+"A"+t+","+t+" 0 1,"+e+" 0,"+t}return s.innerRadius=function(e){return arguments.length?(t=de(e),s):t},s.outerRadius=function(t){return arguments.length?(e=de(t),s):e},s.cornerRadius=function(t){return arguments.length?(r=de(t),s):r},s.padRadius=function(t){return arguments.length?(n=t==Fo?Fo:de(t),s):n},s.startAngle=function(t){return arguments.length?(i=de(t),s):i},s.endAngle=function(t){return arguments.length?(a=de(t),s):a},s.padAngle=function(t){return arguments.length?(o=de(t),s):o},s.centroid=function(){var r=(+t.apply(this,arguments)+ +e.apply(this,arguments))/2,n=(+i.apply(this,arguments)+ +a.apply(this,arguments))/2-Ct;return[Math.cos(n)*r,Math.sin(n)*r]},s};var Fo="auto";function Bo(t){return t.innerRadius}function No(t){return t.outerRadius}function jo(t){return t.startAngle}function Uo(t){return t.endAngle}function Vo(t){return t&&t.padAngle}function qo(t,e,r,n){return(t-r)*e-(e-n)*t>0?0:1}function Ho(t,e,r,n,i){var a=t[0]-e[0],o=t[1]-e[1],s=(i?n:-n)/Math.sqrt(a*a+o*o),l=s*o,c=-s*a,u=t[0]+l,f=t[1]+c,h=e[0]+l,p=e[1]+c,d=(u+h)/2,g=(f+p)/2,m=h-u,v=p-f,y=m*m+v*v,x=r-n,b=u*p-h*f,_=(v<0?-1:1)*Math.sqrt(Math.max(0,x*x*y-b*b)),w=(b*v-m*_)/y,T=(-b*m-v*_)/y,k=(b*v+m*_)/y,M=(-b*m+v*_)/y,A=w-d,S=T-g,E=k-d,C=M-g;return A*A+S*S>E*E+C*C&&(w=k,T=M),[[w-l,T-c],[w*r/x,T*r/x]]}function Go(t){var e=ri,r=ni,n=Yr,i=Wo,a=i.key,o=.7;function s(a){var s,l=[],c=[],u=-1,f=a.length,h=de(e),p=de(r);function d(){l.push("M",i(t(c),o))}for(;++u<f;)n.call(this,s=a[u],u)?c.push([+h.call(this,s,u),+p.call(this,s,u)]):c.length&&(d(),c=[]);return c.length&&d(),l.length?l.join(""):null}return s.x=function(t){return arguments.length?(e=t,s):e},s.y=function(t){return arguments.length?(r=t,s):r},s.defined=function(t){return arguments.length?(n=t,s):n},s.interpolate=function(t){return arguments.length?(a="function"==typeof t?i=t:(i=Yo.get(t)||Wo).key,s):a},s.tension=function(t){return arguments.length?(o=t,s):o},s}t.svg.line=function(){return Go(L)};var Yo=t.map({linear:Wo,"linear-closed":Xo,step:function(t){var e=0,r=t.length,n=t[0],i=[n[0],",",n[1]];for(;++e<r;)i.push("H",(n[0]+(n=t[e])[0])/2,"V",n[1]);r>1&&i.push("H",n[0]);return i.join("")},"step-before":Zo,"step-after":Jo,basis:$o,"basis-open":function(t){if(t.length<4)return Wo(t);var e,r=[],n=-1,i=t.length,a=[0],o=[0];for(;++n<3;)e=t[n],a.push(e[0]),o.push(e[1]);r.push(ts(ns,a)+","+ts(ns,o)),--n;for(;++n<i;)e=t[n],a.shift(),a.push(e[0]),o.shift(),o.push(e[1]),is(r,a,o);return r.join("")},"basis-closed":function(t){var e,r,n=-1,i=t.length,a=i+4,o=[],s=[];for(;++n<4;)r=t[n%i],o.push(r[0]),s.push(r[1]);e=[ts(ns,o),",",ts(ns,s)],--n;for(;++n<a;)r=t[n%i],o.shift(),o.push(r[0]),s.shift(),s.push(r[1]),is(e,o,s);return e.join("")},bundle:function(t,e){var r=t.length-1;if(r)for(var n,i,a=t[0][0],o=t[0][1],s=t[r][0]-a,l=t[r][1]-o,c=-1;++c<=r;)n=t[c],i=c/r,n[0]=e*n[0]+(1-e)*(a+i*s),n[1]=e*n[1]+(1-e)*(o+i*l);return $o(t)},cardinal:function(t,e){return t.length<3?Wo(t):t[0]+Ko(t,Qo(t,e))},"cardinal-open":function(t,e){return t.length<4?Wo(t):t[1]+Ko(t.slice(1,-1),Qo(t,e))},"cardinal-closed":function(t,e){return t.length<3?Xo(t):t[0]+Ko((t.push(t[0]),t),Qo([t[t.length-2]].concat(t,[t[1]]),e))},monotone:function(t){return t.length<3?Wo(t):t[0]+Ko(t,function(t){var e,r,n,i,a=[],o=function(t){var e=0,r=t.length-1,n=[],i=t[0],a=t[1],o=n[0]=as(i,a);for(;++e<r;)n[e]=(o+(o=as(i=a,a=t[e+1])))/2;return n[e]=o,n}(t),s=-1,l=t.length-1;for(;++s<l;)e=as(t[s],t[s+1]),y(e)<kt?o[s]=o[s+1]=0:(r=o[s]/e,n=o[s+1]/e,(i=r*r+n*n)>9&&(i=3*e/Math.sqrt(i),o[s]=i*r,o[s+1]=i*n));s=-1;for(;++s<=l;)i=(t[Math.min(l,s+1)][0]-t[Math.max(0,s-1)][0])/(6*(1+o[s]*o[s])),a.push([i||0,o[s]*i||0]);return a}(t))}});function Wo(t){return t.length>1?t.join("L"):t+"Z"}function Xo(t){return t.join("L")+"Z"}function Zo(t){for(var e=0,r=t.length,n=t[0],i=[n[0],",",n[1]];++e<r;)i.push("V",(n=t[e])[1],"H",n[0]);return i.join("")}function Jo(t){for(var e=0,r=t.length,n=t[0],i=[n[0],",",n[1]];++e<r;)i.push("H",(n=t[e])[0],"V",n[1]);return i.join("")}function Ko(t,e){if(e.length<1||t.length!=e.length&&t.length!=e.length+2)return Wo(t);var r=t.length!=e.length,n="",i=t[0],a=t[1],o=e[0],s=o,l=1;if(r&&(n+="Q"+(a[0]-2*o[0]/3)+","+(a[1]-2*o[1]/3)+","+a[0]+","+a[1],i=t[1],l=2),e.length>1){s=e[1],a=t[l],l++,n+="C"+(i[0]+o[0])+","+(i[1]+o[1])+","+(a[0]-s[0])+","+(a[1]-s[1])+","+a[0]+","+a[1];for(var c=2;c<e.length;c++,l++)a=t[l],s=e[c],n+="S"+(a[0]-s[0])+","+(a[1]-s[1])+","+a[0]+","+a[1]}if(r){var u=t[l];n+="Q"+(a[0]+2*s[0]/3)+","+(a[1]+2*s[1]/3)+","+u[0]+","+u[1]}return n}function Qo(t,e){for(var r,n=[],i=(1-e)/2,a=t[0],o=t[1],s=1,l=t.length;++s<l;)r=a,a=o,o=t[s],n.push([i*(o[0]-r[0]),i*(o[1]-r[1])]);return n}function $o(t){if(t.length<3)return Wo(t);var e=1,r=t.length,n=t[0],i=n[0],a=n[1],o=[i,i,i,(n=t[1])[0]],s=[a,a,a,n[1]],l=[i,",",a,"L",ts(ns,o),",",ts(ns,s)];for(t.push(t[r-1]);++e<=r;)n=t[e],o.shift(),o.push(n[0]),s.shift(),s.push(n[1]),is(l,o,s);return t.pop(),l.push("L",n),l.join("")}function ts(t,e){return t[0]*e[0]+t[1]*e[1]+t[2]*e[2]+t[3]*e[3]}Yo.forEach((function(t,e){e.key=t,e.closed=/-closed$/.test(t)}));var es=[0,2/3,1/3,0],rs=[0,1/3,2/3,0],ns=[0,1/6,2/3,1/6];function is(t,e,r){t.push("C",ts(es,e),",",ts(es,r),",",ts(rs,e),",",ts(rs,r),",",ts(ns,e),",",ts(ns,r))}function as(t,e){return(e[1]-t[1])/(e[0]-t[0])}function os(t){for(var e,r,n,i=-1,a=t.length;++i<a;)r=(e=t[i])[0],n=e[1]-Ct,e[0]=r*Math.cos(n),e[1]=r*Math.sin(n);return t}function ss(t){var e=ri,r=ri,n=0,i=ni,a=Yr,o=Wo,s=o.key,l=o,c="L",u=.7;function f(s){var f,h,p,d=[],g=[],m=[],v=-1,y=s.length,x=de(e),b=de(n),_=e===r?function(){return h}:de(r),w=n===i?function(){return p}:de(i);function T(){d.push("M",o(t(m),u),c,l(t(g.reverse()),u),"Z")}for(;++v<y;)a.call(this,f=s[v],v)?(g.push([h=+x.call(this,f,v),p=+b.call(this,f,v)]),m.push([+_.call(this,f,v),+w.call(this,f,v)])):g.length&&(T(),g=[],m=[]);return g.length&&T(),d.length?d.join(""):null}return f.x=function(t){return arguments.length?(e=r=t,f):r},f.x0=function(t){return arguments.length?(e=t,f):e},f.x1=function(t){return arguments.length?(r=t,f):r},f.y=function(t){return arguments.length?(n=i=t,f):i},f.y0=function(t){return arguments.length?(n=t,f):n},f.y1=function(t){return arguments.length?(i=t,f):i},f.defined=function(t){return arguments.length?(a=t,f):a},f.interpolate=function(t){return arguments.length?(s="function"==typeof t?o=t:(o=Yo.get(t)||Wo).key,l=o.reverse||o,c=o.closed?"M":"L",f):s},f.tension=function(t){return arguments.length?(u=t,f):u},f}function ls(t){return t.radius}function cs(t){return[t.x,t.y]}function us(t){return function(){var e=t.apply(this,arguments),r=e[0],n=e[1]-Ct;return[r*Math.cos(n),r*Math.sin(n)]}}function fs(){return 64}function hs(){return"circle"}function ps(t){var e=Math.sqrt(t/At);return"M0,"+e+"A"+e+","+e+" 0 1,1 0,"+-e+"A"+e+","+e+" 0 1,1 0,"+e+"Z"}t.svg.line.radial=function(){var t=Go(os);return t.radius=t.x,delete t.x,t.angle=t.y,delete t.y,t},Zo.reverse=Jo,Jo.reverse=Zo,t.svg.area=function(){return ss(L)},t.svg.area.radial=function(){var t=ss(os);return t.radius=t.x,delete t.x,t.innerRadius=t.x0,delete t.x0,t.outerRadius=t.x1,delete t.x1,t.angle=t.y,delete t.y,t.startAngle=t.y0,delete t.y0,t.endAngle=t.y1,delete t.y1,t},t.svg.chord=function(){var t=Vn,e=qn,r=ls,n=jo,i=Uo;function a(r,n){var i,a,c=o(this,t,r,n),u=o(this,e,r,n);return"M"+c.p0+s(c.r,c.p1,c.a1-c.a0)+(a=u,((i=c).a0==a.a0&&i.a1==a.a1?l(c.r,c.p1,c.r,c.p0):l(c.r,c.p1,u.r,u.p0)+s(u.r,u.p1,u.a1-u.a0)+l(u.r,u.p1,c.r,c.p0))+"Z")}function o(t,e,a,o){var s=e.call(t,a,o),l=r.call(t,s,o),c=n.call(t,s,o)-Ct,u=i.call(t,s,o)-Ct;return{r:l,a0:c,a1:u,p0:[l*Math.cos(c),l*Math.sin(c)],p1:[l*Math.cos(u),l*Math.sin(u)]}}function s(t,e,r){return"A"+t+","+t+" 0 "+ +(r>At)+",1 "+e}function l(t,e,r,n){return"Q 0,0 "+n}return a.radius=function(t){return arguments.length?(r=de(t),a):r},a.source=function(e){return arguments.length?(t=de(e),a):t},a.target=function(t){return arguments.length?(e=de(t),a):e},a.startAngle=function(t){return arguments.length?(n=de(t),a):n},a.endAngle=function(t){return arguments.length?(i=de(t),a):i},a},t.svg.diagonal=function(){var t=Vn,e=qn,r=cs;function n(n,i){var a=t.call(this,n,i),o=e.call(this,n,i),s=(a.y+o.y)/2,l=[a,{x:a.x,y:s},{x:o.x,y:s},o];return"M"+(l=l.map(r))[0]+"C"+l[1]+" "+l[2]+" "+l[3]}return n.source=function(e){return arguments.length?(t=de(e),n):t},n.target=function(t){return arguments.length?(e=de(t),n):e},n.projection=function(t){return arguments.length?(r=t,n):r},n},t.svg.diagonal.radial=function(){var e=t.svg.diagonal(),r=cs,n=e.projection;return e.projection=function(t){return arguments.length?n(us(r=t)):r},e},t.svg.symbol=function(){var t=hs,e=fs;function r(r,n){return(ds.get(t.call(this,r,n))||ps)(e.call(this,r,n))}return r.type=function(e){return arguments.length?(t=de(e),r):t},r.size=function(t){return arguments.length?(e=de(t),r):e},r};var ds=t.map({circle:ps,cross:function(t){var e=Math.sqrt(t/5)/2;return"M"+-3*e+","+-e+"H"+-e+"V"+-3*e+"H"+e+"V"+-e+"H"+3*e+"V"+e+"H"+e+"V"+3*e+"H"+-e+"V"+e+"H"+-3*e+"Z"},diamond:function(t){var e=Math.sqrt(t/(2*ms)),r=e*ms;return"M0,"+-e+"L"+r+",0 0,"+e+" "+-r+",0Z"},square:function(t){var e=Math.sqrt(t)/2;return"M"+-e+","+-e+"L"+e+","+-e+" "+e+","+e+" "+-e+","+e+"Z"},"triangle-down":function(t){var e=Math.sqrt(t/gs),r=e*gs/2;return"M0,"+r+"L"+e+","+-r+" "+-e+","+-r+"Z"},"triangle-up":function(t){var e=Math.sqrt(t/gs),r=e*gs/2;return"M0,"+-r+"L"+e+","+r+" "+-e+","+r+"Z"}});t.svg.symbolTypes=ds.keys();var gs=Math.sqrt(3),ms=Math.tan(30*Lt);Y.transition=function(t){for(var e,r,n=bs||++Ts,i=As(t),a=[],o=_s||{time:Date.now(),ease:ca,delay:0,duration:250},s=-1,l=this.length;++s<l;){a.push(e=[]);for(var c=this[s],u=-1,f=c.length;++u<f;)(r=c[u])&&Ss(r,u,i,n,o),e.push(r)}return xs(a,i,n)},Y.interrupt=function(t){return this.each(null==t?vs:ys(As(t)))};var vs=ys(As());function ys(t){return function(){var e,r,n;(e=this[t])&&(n=e[r=e.active])&&(n.timer.c=null,n.timer.t=NaN,--e.count?delete e[r]:delete this[t],e.active+=.5,n.event&&n.event.interrupt.call(this,this.__data__,n.index))}}function xs(t,e,r){return U(t,ws),t.namespace=e,t.id=r,t}var bs,_s,ws=[],Ts=0;function ks(t,e,r,n){var i=t.id,a=t.namespace;return ut(t,"function"==typeof r?function(t,o,s){t[a][i].tween.set(e,n(r.call(t,t.__data__,o,s)))}:(r=n(r),function(t){t[a][i].tween.set(e,r)}))}function Ms(t){return null==t&&(t=""),function(){this.textContent=t}}function As(t){return null==t?"__transition__":"__transition_"+t+"__"}function Ss(t,e,r,n,i){var a,o,s,l,c,u=t[r]||(t[r]={active:0,count:0}),f=u[n];function h(r){var i=u.active,h=u[i];for(var d in h&&(h.timer.c=null,h.timer.t=NaN,--u.count,delete u[i],h.event&&h.event.interrupt.call(t,t.__data__,h.index)),u)if(+d<n){var g=u[d];g.timer.c=null,g.timer.t=NaN,--u.count,delete u[d]}o.c=p,we((function(){return o.c&&p(r||1)&&(o.c=null,o.t=NaN),1}),0,a),u.active=n,f.event&&f.event.start.call(t,t.__data__,e),c=[],f.tween.forEach((function(r,n){(n=n.call(t,t.__data__,e))&&c.push(n)})),l=f.ease,s=f.duration}function p(i){for(var a=i/s,o=l(a),h=c.length;h>0;)c[--h].call(t,o);if(a>=1)return f.event&&f.event.end.call(t,t.__data__,e),--u.count?delete u[n]:delete t[r],1}f||(a=i.time,o=we((function(t){var e=f.delay;if(o.t=e+a,e<=t)return h(t-e);o.c=h}),0,a),f=u[n]={tween:new _,time:a,timer:o,delay:i.delay,duration:i.duration,ease:i.ease,index:e},i=null,++u.count)}ws.call=Y.call,ws.empty=Y.empty,ws.node=Y.node,ws.size=Y.size,t.transition=function(e,r){return e&&e.transition?bs?e.transition(r):e:t.selection().transition(e)},t.transition.prototype=ws,ws.select=function(t){var e,r,n,i=this.id,a=this.namespace,o=[];t=W(t);for(var s=-1,l=this.length;++s<l;){o.push(e=[]);for(var c=this[s],u=-1,f=c.length;++u<f;)(n=c[u])&&(r=t.call(n,n.__data__,u,s))?("__data__"in n&&(r.__data__=n.__data__),Ss(r,u,a,i,n[a][i]),e.push(r)):e.push(null)}return xs(o,a,i)},ws.selectAll=function(t){var e,r,n,i,a,o=this.id,s=this.namespace,l=[];t=X(t);for(var c=-1,u=this.length;++c<u;)for(var f=this[c],h=-1,p=f.length;++h<p;)if(n=f[h]){a=n[s][o],r=t.call(n,n.__data__,h,c),l.push(e=[]);for(var d=-1,g=r.length;++d<g;)(i=r[d])&&Ss(i,d,s,o,a),e.push(i)}return xs(l,s,o)},ws.filter=function(t){var e,r,n=[];"function"!=typeof t&&(t=lt(t));for(var i=0,a=this.length;i<a;i++){n.push(e=[]);for(var o,s=0,l=(o=this[i]).length;s<l;s++)(r=o[s])&&t.call(r,r.__data__,s,i)&&e.push(r)}return xs(n,this.namespace,this.id)},ws.tween=function(t,e){var r=this.id,n=this.namespace;return arguments.length<2?this.node()[n][r].tween.get(t):ut(this,null==e?function(e){e[n][r].tween.remove(t)}:function(i){i[n][r].tween.set(t,e)})},ws.attr=function(e,r){if(arguments.length<2){for(r in e)this.attr(r,e[r]);return this}var n="transform"==e?ba:$i,i=t.ns.qualify(e);function a(){this.removeAttribute(i)}function o(){this.removeAttributeNS(i.space,i.local)}function s(t){return null==t?a:(t+="",function(){var e,r=this.getAttribute(i);return r!==t&&(e=n(r,t),function(t){this.setAttribute(i,e(t))})})}function l(t){return null==t?o:(t+="",function(){var e,r=this.getAttributeNS(i.space,i.local);return r!==t&&(e=n(r,t),function(t){this.setAttributeNS(i.space,i.local,e(t))})})}return ks(this,"attr."+e,r,i.local?l:s)},ws.attrTween=function(e,r){var n=t.ns.qualify(e);return this.tween("attr."+e,n.local?function(t,e){var i=r.call(this,t,e,this.getAttributeNS(n.space,n.local));return i&&function(t){this.setAttributeNS(n.space,n.local,i(t))}}:function(t,e){var i=r.call(this,t,e,this.getAttribute(n));return i&&function(t){this.setAttribute(n,i(t))}})},ws.style=function(t,e,r){var n=arguments.length;if(n<3){if("string"!=typeof t){for(r in n<2&&(e=""),t)this.style(r,t[r],e);return this}r=""}function i(){this.style.removeProperty(t)}function a(e){return null==e?i:(e+="",function(){var n,i=o(this).getComputedStyle(this,null).getPropertyValue(t);return i!==e&&(n=$i(i,e),function(e){this.style.setProperty(t,n(e),r)})})}return ks(this,"style."+t,e,a)},ws.styleTween=function(t,e,r){function n(n,i){var a=e.call(this,n,i,o(this).getComputedStyle(this,null).getPropertyValue(t));return a&&function(e){this.style.setProperty(t,a(e),r)}}return arguments.length<3&&(r=""),this.tween("style."+t,n)},ws.text=function(t){return ks(this,"text",t,Ms)},ws.remove=function(){var t=this.namespace;return this.each("end.transition",(function(){var e;this[t].count<2&&(e=this.parentNode)&&e.removeChild(this)}))},ws.ease=function(e){var r=this.id,n=this.namespace;return arguments.length<1?this.node()[n][r].ease:("function"!=typeof e&&(e=t.ease.apply(t,arguments)),ut(this,(function(t){t[n][r].ease=e})))},ws.delay=function(t){var e=this.id,r=this.namespace;return arguments.length<1?this.node()[r][e].delay:ut(this,"function"==typeof t?function(n,i,a){n[r][e].delay=+t.call(n,n.__data__,i,a)}:(t=+t,function(n){n[r][e].delay=t}))},ws.duration=function(t){var e=this.id,r=this.namespace;return arguments.length<1?this.node()[r][e].duration:ut(this,"function"==typeof t?function(n,i,a){n[r][e].duration=Math.max(1,t.call(n,n.__data__,i,a))}:(t=Math.max(1,t),function(n){n[r][e].duration=t}))},ws.each=function(e,r){var n=this.id,i=this.namespace;if(arguments.length<2){var a=_s,o=bs;try{bs=n,ut(this,(function(t,r,a){_s=t[i][n],e.call(t,t.__data__,r,a)}))}finally{_s=a,bs=o}}else ut(this,(function(a){var o=a[i][n];(o.event||(o.event=t.dispatch("start","end","interrupt"))).on(e,r)}));return this},ws.transition=function(){for(var t,e,r,n=this.id,i=++Ts,a=this.namespace,o=[],s=0,l=this.length;s<l;s++){o.push(t=[]);for(var c,u=0,f=(c=this[s]).length;u<f;u++)(e=c[u])&&Ss(e,u,a,i,{time:(r=e[a][n]).time,ease:r.ease,delay:r.delay+r.duration,duration:r.duration}),t.push(e)}return xs(o,a,i)},t.svg.axis=function(){var e,r=t.scale.linear(),i=Es,a=6,o=6,s=3,l=[10],c=null;function u(n){n.each((function(){var n,u=t.select(this),f=this.__chart__||r,h=this.__chart__=r.copy(),p=null==c?h.ticks?h.ticks.apply(h,l):h.domain():c,d=null==e?h.tickFormat?h.tickFormat.apply(h,l):L:e,g=u.selectAll(".tick").data(p,h),m=g.enter().insert("g",".domain").attr("class","tick").style("opacity",kt),v=t.transition(g.exit()).style("opacity",kt).remove(),y=t.transition(g.order()).style("opacity",1),x=Math.max(a,0)+s,b=mo(h),_=u.selectAll(".domain").data([0]),w=(_.enter().append("path").attr("class","domain"),t.transition(_));m.append("line"),m.append("text");var T,k,M,A,S=m.select("line"),E=y.select("line"),C=g.select("text").text(d),I=m.select("text"),P=y.select("text"),z="top"===i||"left"===i?-1:1;if("bottom"===i||"top"===i?(n=Ls,T="x",M="y",k="x2",A="y2",C.attr("dy",z<0?"0em":".71em").style("text-anchor","middle"),w.attr("d","M"+b[0]+","+z*o+"V0H"+b[1]+"V"+z*o)):(n=Is,T="y",M="x",k="y2",A="x2",C.attr("dy",".32em").style("text-anchor",z<0?"end":"start"),w.attr("d","M"+z*o+","+b[0]+"H0V"+b[1]+"H"+z*o)),S.attr(A,z*a),I.attr(M,z*x),E.attr(k,0).attr(A,z*a),P.attr(T,0).attr(M,z*x),h.rangeBand){var O=h,D=O.rangeBand()/2;f=h=function(t){return O(t)+D}}else f.rangeBand?f=h:v.call(n,h,f);m.call(n,f,h),y.call(n,h,h)}))}return u.scale=function(t){return arguments.length?(r=t,u):r},u.orient=function(t){return arguments.length?(i=t in Cs?t+"":Es,u):i},u.ticks=function(){return arguments.length?(l=n(arguments),u):l},u.tickValues=function(t){return arguments.length?(c=t,u):c},u.tickFormat=function(t){return arguments.length?(e=t,u):e},u.tickSize=function(t){var e=arguments.length;return e?(a=+t,o=+arguments[e-1],u):a},u.innerTickSize=function(t){return arguments.length?(a=+t,u):a},u.outerTickSize=function(t){return arguments.length?(o=+t,u):o},u.tickPadding=function(t){return arguments.length?(s=+t,u):s},u.tickSubdivide=function(){return arguments.length&&u},u};var Es="bottom",Cs={top:1,right:1,bottom:1,left:1};function Ls(t,e,r){t.attr("transform",(function(t){var n=e(t);return"translate("+(isFinite(n)?n:r(t))+",0)"}))}function Is(t,e,r){t.attr("transform",(function(t){var n=e(t);return"translate(0,"+(isFinite(n)?n:r(t))+")"}))}t.svg.brush=function(){var e,r,n=N(h,"brushstart","brush","brushend"),i=null,a=null,s=[0,0],l=[0,0],c=!0,u=!0,f=zs[0];function h(e){e.each((function(){var e=t.select(this).style("pointer-events","all").style("-webkit-tap-highlight-color","rgba(0,0,0,0)").on("mousedown.brush",m).on("touchstart.brush",m),r=e.selectAll(".background").data([0]);r.enter().append("rect").attr("class","background").style("visibility","hidden").style("cursor","crosshair"),e.selectAll(".extent").data([0]).enter().append("rect").attr("class","extent").style("cursor","move");var n=e.selectAll(".resize").data(f,L);n.exit().remove(),n.enter().append("g").attr("class",(function(t){return"resize "+t})).style("cursor",(function(t){return Ps[t]})).append("rect").attr("x",(function(t){return/[ew]$/.test(t)?-3:null})).attr("y",(function(t){return/^[ns]/.test(t)?-3:null})).attr("width",6).attr("height",6).style("visibility","hidden"),n.style("display",h.empty()?"none":null);var o,s=t.transition(e),l=t.transition(r);i&&(o=mo(i),l.attr("x",o[0]).attr("width",o[1]-o[0]),d(s)),a&&(o=mo(a),l.attr("y",o[0]).attr("height",o[1]-o[0]),g(s)),p(s)}))}function p(t){t.selectAll(".resize").attr("transform",(function(t){return"translate("+s[+/e$/.test(t)]+","+l[+/^s/.test(t)]+")"}))}function d(t){t.select(".extent").attr("x",s[0]),t.selectAll(".extent,.n>rect,.s>rect").attr("width",s[1]-s[0])}function g(t){t.select(".extent").attr("y",l[0]),t.selectAll(".extent,.e>rect,.w>rect").attr("height",l[1]-l[0])}function m(){var f,m,v=this,y=t.select(t.event.target),x=n.of(v,arguments),b=t.select(v),_=y.datum(),w=!/^(n|s)$/.test(_)&&i,T=!/^(e|w)$/.test(_)&&a,k=y.classed("extent"),M=bt(v),A=t.mouse(v),S=t.select(o(v)).on("keydown.brush",L).on("keyup.brush",I);if(t.event.changedTouches?S.on("touchmove.brush",P).on("touchend.brush",O):S.on("mousemove.brush",P).on("mouseup.brush",O),b.interrupt().selectAll("*").interrupt(),k)A[0]=s[0]-A[0],A[1]=l[0]-A[1];else if(_){var E=+/w$/.test(_),C=+/^n/.test(_);m=[s[1-E]-A[0],l[1-C]-A[1]],A[0]=s[E],A[1]=l[C]}else t.event.altKey&&(f=A.slice());function L(){32==t.event.keyCode&&(k||(f=null,A[0]-=s[1],A[1]-=l[1],k=2),F())}function I(){32==t.event.keyCode&&2==k&&(A[0]+=s[1],A[1]+=l[1],k=0,F())}function P(){var e=t.mouse(v),r=!1;m&&(e[0]+=m[0],e[1]+=m[1]),k||(t.event.altKey?(f||(f=[(s[0]+s[1])/2,(l[0]+l[1])/2]),A[0]=s[+(e[0]<f[0])],A[1]=l[+(e[1]<f[1])]):f=null),w&&z(e,i,0)&&(d(b),r=!0),T&&z(e,a,1)&&(g(b),r=!0),r&&(p(b),x({type:"brush",mode:k?"move":"resize"}))}function z(t,n,i){var a,o,h=mo(n),p=h[0],d=h[1],g=A[i],m=i?l:s,v=m[1]-m[0];if(k&&(p-=g,d-=v+g),a=(i?u:c)?Math.max(p,Math.min(d,t[i])):t[i],k?o=(a+=g)+v:(f&&(g=Math.max(p,Math.min(d,2*f[i]-a))),g<a?(o=a,a=g):o=g),m[0]!=a||m[1]!=o)return i?r=null:e=null,m[0]=a,m[1]=o,!0}function O(){P(),b.style("pointer-events","all").selectAll(".resize").style("display",h.empty()?"none":null),t.select("body").style("cursor",null),S.on("mousemove.brush",null).on("mouseup.brush",null).on("touchmove.brush",null).on("touchend.brush",null).on("keydown.brush",null).on("keyup.brush",null),M(),x({type:"brushend"})}b.style("pointer-events","none").selectAll(".resize").style("display",null),t.select("body").style("cursor",y.style("cursor")),x({type:"brushstart"}),P()}return h.event=function(i){i.each((function(){var i=n.of(this,arguments),a={x:s,y:l,i:e,j:r},o=this.__chart__||a;this.__chart__=a,bs?t.select(this).transition().each("start.brush",(function(){e=o.i,r=o.j,s=o.x,l=o.y,i({type:"brushstart"})})).tween("brush:brush",(function(){var t=ta(s,a.x),n=ta(l,a.y);return e=r=null,function(e){s=a.x=t(e),l=a.y=n(e),i({type:"brush",mode:"resize"})}})).each("end.brush",(function(){e=a.i,r=a.j,i({type:"brush",mode:"resize"}),i({type:"brushend"})})):(i({type:"brushstart"}),i({type:"brush",mode:"resize"}),i({type:"brushend"}))}))},h.x=function(t){return arguments.length?(f=zs[!(i=t)<<1|!a],h):i},h.y=function(t){return arguments.length?(f=zs[!i<<1|!(a=t)],h):a},h.clamp=function(t){return arguments.length?(i&&a?(c=!!t[0],u=!!t[1]):i?c=!!t:a&&(u=!!t),h):i&&a?[c,u]:i?c:a?u:null},h.extent=function(t){var n,o,c,u,f;return arguments.length?(i&&(n=t[0],o=t[1],a&&(n=n[0],o=o[0]),e=[n,o],i.invert&&(n=i(n),o=i(o)),o<n&&(f=n,n=o,o=f),n==s[0]&&o==s[1]||(s=[n,o])),a&&(c=t[0],u=t[1],i&&(c=c[1],u=u[1]),r=[c,u],a.invert&&(c=a(c),u=a(u)),u<c&&(f=c,c=u,u=f),c==l[0]&&u==l[1]||(l=[c,u])),h):(i&&(e?(n=e[0],o=e[1]):(n=s[0],o=s[1],i.invert&&(n=i.invert(n),o=i.invert(o)),o<n&&(f=n,n=o,o=f))),a&&(r?(c=r[0],u=r[1]):(c=l[0],u=l[1],a.invert&&(c=a.invert(c),u=a.invert(u)),u<c&&(f=c,c=u,u=f))),i&&a?[[n,c],[o,u]]:i?[n,o]:a&&[c,u])},h.clear=function(){return h.empty()||(s=[0,0],l=[0,0],e=r=null),h},h.empty=function(){return!!i&&s[0]==s[1]||!!a&&l[0]==l[1]},t.rebind(h,n,"on")};var Ps={n:"ns-resize",e:"ew-resize",s:"ns-resize",w:"ew-resize",nw:"nwse-resize",ne:"nesw-resize",se:"nwse-resize",sw:"nesw-resize"},zs=[["n","e","s","w","nw","ne","se","sw"],["e","w"],["n","s"],[]],Os=Pe.format=sr.timeFormat,Ds=Os.utc,Rs=Ds("%Y-%m-%dT%H:%M:%S.%LZ");function Fs(t){return t.toISOString()}function Bs(e,r,n){function i(t){return e(t)}function a(e,n){var i=(e[1]-e[0])/n,a=t.bisect(js,i);return a==js.length?[r.year,ko(e.map((function(t){return t/31536e6})),n)[2]]:a?r[i/js[a-1]<js[a]/i?a-1:a]:[qs,ko(e,n)[2]]}return i.invert=function(t){return Ns(e.invert(t))},i.domain=function(t){return arguments.length?(e.domain(t),i):e.domain().map(Ns)},i.nice=function(t,e){var r=i.domain(),n=go(r),o=null==t?a(n,10):"number"==typeof t&&a(n,t);function s(r){return!isNaN(r)&&!t.range(r,Ns(+r+1),e).length}return o&&(t=o[0],e=o[1]),i.domain(yo(r,e>1?{floor:function(e){for(;s(e=t.floor(e));)e=Ns(e-1);return e},ceil:function(e){for(;s(e=t.ceil(e));)e=Ns(+e+1);return e}}:t))},i.ticks=function(t,e){var r=go(i.domain()),n=null==t?a(r,10):"number"==typeof t?a(r,t):!t.range&&[{range:t},e];return n&&(t=n[0],e=n[1]),t.range(r[0],Ns(+r[1]+1),e<1?1:e)},i.tickFormat=function(){return n},i.copy=function(){return Bs(e.copy(),r,n)},wo(i,e)}function Ns(t){return new Date(t)}Os.iso=Date.prototype.toISOString&&+new Date("2000-01-01T00:00:00.000Z")?Fs:Rs,Fs.parse=function(t){var e=new Date(t);return isNaN(e)?null:e},Fs.toString=Rs.toString,Pe.second=Re((function(t){return new ze(1e3*Math.floor(t/1e3))}),(function(t,e){t.setTime(t.getTime()+1e3*Math.floor(e))}),(function(t){return t.getSeconds()})),Pe.seconds=Pe.second.range,Pe.seconds.utc=Pe.second.utc.range,Pe.minute=Re((function(t){return new ze(6e4*Math.floor(t/6e4))}),(function(t,e){t.setTime(t.getTime()+6e4*Math.floor(e))}),(function(t){return t.getMinutes()})),Pe.minutes=Pe.minute.range,Pe.minutes.utc=Pe.minute.utc.range,Pe.hour=Re((function(t){var e=t.getTimezoneOffset()/60;return new ze(36e5*(Math.floor(t/36e5-e)+e))}),(function(t,e){t.setTime(t.getTime()+36e5*Math.floor(e))}),(function(t){return t.getHours()})),Pe.hours=Pe.hour.range,Pe.hours.utc=Pe.hour.utc.range,Pe.month=Re((function(t){return(t=Pe.day(t)).setDate(1),t}),(function(t,e){t.setMonth(t.getMonth()+e)}),(function(t){return t.getMonth()})),Pe.months=Pe.month.range,Pe.months.utc=Pe.month.utc.range;var js=[1e3,5e3,15e3,3e4,6e4,3e5,9e5,18e5,36e5,108e5,216e5,432e5,864e5,1728e5,6048e5,2592e6,7776e6,31536e6],Us=[[Pe.second,1],[Pe.second,5],[Pe.second,15],[Pe.second,30],[Pe.minute,1],[Pe.minute,5],[Pe.minute,15],[Pe.minute,30],[Pe.hour,1],[Pe.hour,3],[Pe.hour,6],[Pe.hour,12],[Pe.day,1],[Pe.day,2],[Pe.week,1],[Pe.month,1],[Pe.month,3],[Pe.year,1]],Vs=Os.multi([[".%L",function(t){return t.getMilliseconds()}],[":%S",function(t){return t.getSeconds()}],["%I:%M",function(t){return t.getMinutes()}],["%I %p",function(t){return t.getHours()}],["%a %d",function(t){return t.getDay()&&1!=t.getDate()}],["%b %d",function(t){return 1!=t.getDate()}],["%B",function(t){return t.getMonth()}],["%Y",Yr]]),qs={range:function(e,r,n){return t.range(Math.ceil(e/n)*n,+r,n).map(Ns)},floor:L,ceil:L};Us.year=Pe.year,Pe.scale=function(){return Bs(t.scale.linear(),Us,Vs)};var Hs=Us.map((function(t){return[t[0].utc,t[1]]})),Gs=Ds.multi([[".%L",function(t){return t.getUTCMilliseconds()}],[":%S",function(t){return t.getUTCSeconds()}],["%I:%M",function(t){return t.getUTCMinutes()}],["%I %p",function(t){return t.getUTCHours()}],["%a %d",function(t){return t.getUTCDay()&&1!=t.getUTCDate()}],["%b %d",function(t){return 1!=t.getUTCDate()}],["%B",function(t){return t.getUTCMonth()}],["%Y",Yr]]);function Ys(t){return JSON.parse(t.responseText)}function Ws(t){var e=i.createRange();return e.selectNode(i.body),e.createContextualFragment(t.responseText)}Hs.year=Pe.year.utc,Pe.scale.utc=function(){return Bs(t.scale.linear(),Hs,Gs)},t.text=ge((function(t){return t.responseText})),t.json=function(t,e){return me(t,"application/json",Ys,e)},t.html=function(t,e){return me(t,"text/html",Ws,e)},t.xml=ge((function(t){return t.responseXML})),"object"==typeof e&&e.exports?e.exports=t:this.d3=t}()},{}],170:[function(t,e,r){e.exports=function(){for(var t=0;t<arguments.length;t++)if(void 0!==arguments[t])return arguments[t]}},{}],171:[function(t,e,r){"use strict";var n=t("incremental-convex-hull"),i=t("uniq");function a(t,e){this.point=t,this.index=e}function o(t,e){for(var r=t.point,n=e.point,i=r.length,a=0;a<i;++a){var o=n[a]-r[a];if(o)return o}return 0}e.exports=function(t,e){var r=t.length;if(0===r)return[];var s=t[0].length;if(s<1)return[];if(1===s)return function(t,e,r){if(1===t)return r?[[-1,0]]:[];var n=e.map((function(t,e){return[t[0],e]}));n.sort((function(t,e){return t[0]-e[0]}));for(var i=new Array(t-1),a=1;a<t;++a){var o=n[a-1],s=n[a];i[a-1]=[o[1],s[1]]}r&&i.push([-1,i[0][1]],[i[t-1][1],-1]);return i}(r,t,e);for(var l=new Array(r),c=1,u=0;u<r;++u){for(var f=t[u],h=new Array(s+1),p=0,d=0;d<s;++d){var g=f[d];h[d]=g,p+=g*g}h[s]=p,l[u]=new a(h,u),c=Math.max(p,c)}i(l,o),r=l.length;var m=new Array(r+s+1),v=new Array(r+s+1),y=(s+1)*(s+1)*c,x=new Array(s+1);for(u=0;u<=s;++u)x[u]=0;x[s]=y,m[0]=x.slice(),v[0]=-1;for(u=0;u<=s;++u){(h=x.slice())[u]=1,m[u+1]=h,v[u+1]=-1}for(u=0;u<r;++u){var b=l[u];m[u+s+1]=b.point,v[u+s+1]=b.index}var _=n(m,!1);_=e?_.filter((function(t){for(var e=0,r=0;r<=s;++r){var n=v[t[r]];if(n<0&&++e>=2)return!1;t[r]=n}return!0})):_.filter((function(t){for(var e=0;e<=s;++e){var r=v[t[e]];if(r<0)return!1;t[e]=r}return!0}));if(1&s)for(u=0;u<_.length;++u){h=(b=_[u])[0];b[0]=b[1],b[1]=h}return _}},{"incremental-convex-hull":459,uniq:597}],172:[function(t,e,r){"use strict";e.exports=a;var n=(a.canvas=document.createElement("canvas")).getContext("2d"),i=o([32,126]);function a(t,e){Array.isArray(t)&&(t=t.join(", "));var r,a={},s=16,l=.05;e&&(2===e.length&&"number"==typeof e[0]?r=o(e):Array.isArray(e)?r=e:(e.o?r=o(e.o):e.pairs&&(r=e.pairs),e.fontSize&&(s=e.fontSize),null!=e.threshold&&(l=e.threshold))),r||(r=i),n.font=s+"px "+t;for(var c=0;c<r.length;c++){var u=r[c],f=n.measureText(u[0]).width+n.measureText(u[1]).width,h=n.measureText(u).width;if(Math.abs(f-h)>s*l){var p=(h-f)/s;a[u]=1e3*p}}return a}function o(t){for(var e=[],r=t[0];r<=t[1];r++)for(var n=String.fromCharCode(r),i=t[0];i<t[1];i++){var a=n+String.fromCharCode(i);e.push(a)}return e}a.createPairs=o,a.ascii=i},{}],173:[function(t,e,r){(function(t){(function(){var r=!1;if("undefined"!=typeof Float64Array){var n=new Float64Array(1),i=new Uint32Array(n.buffer);if(n[0]=1,r=!0,1072693248===i[1]){e.exports=function(t){return n[0]=t,[i[0],i[1]]},e.exports.pack=function(t,e){return i[0]=t,i[1]=e,n[0]},e.exports.lo=function(t){return n[0]=t,i[0]},e.exports.hi=function(t){return n[0]=t,i[1]}}else if(1072693248===i[0]){e.exports=function(t){return n[0]=t,[i[1],i[0]]},e.exports.pack=function(t,e){return i[1]=t,i[0]=e,n[0]},e.exports.lo=function(t){return n[0]=t,i[1]},e.exports.hi=function(t){return n[0]=t,i[0]}}else r=!1}if(!r){var a=new t(8);e.exports=function(t){return a.writeDoubleLE(t,0,!0),[a.readUInt32LE(0,!0),a.readUInt32LE(4,!0)]},e.exports.pack=function(t,e){return a.writeUInt32LE(t,0,!0),a.writeUInt32LE(e,4,!0),a.readDoubleLE(0,!0)},e.exports.lo=function(t){return a.writeDoubleLE(t,0,!0),a.readUInt32LE(0,!0)},e.exports.hi=function(t){return a.writeDoubleLE(t,0,!0),a.readUInt32LE(4,!0)}}e.exports.sign=function(t){return e.exports.hi(t)>>>31},e.exports.exponent=function(t){return(e.exports.hi(t)<<1>>>21)-1023},e.exports.fraction=function(t){var r=e.exports.lo(t),n=e.exports.hi(t),i=1048575&n;return 2146435072&n&&(i+=1<<20),[r,i]},e.exports.denormalized=function(t){return!(2146435072&e.exports.hi(t))}}).call(this)}).call(this,t("buffer").Buffer)},{buffer:111}],174:[function(t,e,r){var n=t("abs-svg-path"),i=t("normalize-svg-path"),a={M:"moveTo",C:"bezierCurveTo"};e.exports=function(t,e){t.beginPath(),i(n(e)).forEach((function(e){var r=e[0],n=e.slice(1);t[a[r]].apply(t,n)})),t.closePath()}},{"abs-svg-path":65,"normalize-svg-path":497}],175:[function(t,e,r){e.exports=function(t){switch(t){case"int8":return Int8Array;case"int16":return Int16Array;case"int32":return Int32Array;case"uint8":return Uint8Array;case"uint16":return Uint16Array;case"uint32":return Uint32Array;case"float32":return Float32Array;case"float64":return Float64Array;case"array":return Array;case"uint8_clamped":return Uint8ClampedArray}}},{}],176:[function(t,e,r){"use strict";e.exports=function(t,e){switch("undefined"==typeof e&&(e=0),typeof t){case"number":if(t>0)return function(t,e){var r,n;for(r=new Array(t),n=0;n<t;++n)r[n]=e;return r}(0|t,e);break;case"object":if("number"==typeof t.length)return function t(e,r,n){var i=0|e[n];if(i<=0)return[];var a,o=new Array(i);if(n===e.length-1)for(a=0;a<i;++a)o[a]=r;else for(a=0;a<i;++a)o[a]=t(e,r,n+1);return o}(t,e,0)}return[]}},{}],177:[function(t,e,r){"use strict";function n(t,e,r){r=r||2;var n,s,l,c,u,p,d,m=e&&e.length,v=m?e[0]*r:t.length,y=i(t,0,v,r,!0),x=[];if(!y||y.next===y.prev)return x;if(m&&(y=function(t,e,r,n){var o,s,l,c,u,p=[];for(o=0,s=e.length;o<s;o++)l=e[o]*n,c=o<s-1?e[o+1]*n:t.length,(u=i(t,l,c,n,!1))===u.next&&(u.steiner=!0),p.push(g(u));for(p.sort(f),o=0;o<p.length;o++)h(p[o],r),r=a(r,r.next);return r}(t,e,y,r)),t.length>80*r){n=l=t[0],s=c=t[1];for(var b=r;b<v;b+=r)(u=t[b])<n&&(n=u),(p=t[b+1])<s&&(s=p),u>l&&(l=u),p>c&&(c=p);d=0!==(d=Math.max(l-n,c-s))?1/d:0}return o(y,x,r,n,s,d),x}function i(t,e,r,n,i){var a,o;if(i===E(t,e,r,n)>0)for(a=e;a<r;a+=n)o=M(a,t[a],t[a+1],o);else for(a=r-n;a>=e;a-=n)o=M(a,t[a],t[a+1],o);return o&&x(o,o.next)&&(A(o),o=o.next),o}function a(t,e){if(!t)return t;e||(e=t);var r,n=t;do{if(r=!1,n.steiner||!x(n,n.next)&&0!==y(n.prev,n,n.next))n=n.next;else{if(A(n),(n=e=n.prev)===n.next)break;r=!0}}while(r||n!==e);return e}function o(t,e,r,n,i,f,h){if(t){!h&&f&&function(t,e,r,n){var i=t;do{null===i.z&&(i.z=d(i.x,i.y,e,r,n)),i.prevZ=i.prev,i.nextZ=i.next,i=i.next}while(i!==t);i.prevZ.nextZ=null,i.prevZ=null,function(t){var e,r,n,i,a,o,s,l,c=1;do{for(r=t,t=null,a=null,o=0;r;){for(o++,n=r,s=0,e=0;e<c&&(s++,n=n.nextZ);e++);for(l=c;s>0||l>0&&n;)0!==s&&(0===l||!n||r.z<=n.z)?(i=r,r=r.nextZ,s--):(i=n,n=n.nextZ,l--),a?a.nextZ=i:t=i,i.prevZ=a,a=i;r=n}a.nextZ=null,c*=2}while(o>1)}(i)}(t,n,i,f);for(var p,g,m=t;t.prev!==t.next;)if(p=t.prev,g=t.next,f?l(t,n,i,f):s(t))e.push(p.i/r),e.push(t.i/r),e.push(g.i/r),A(t),t=g.next,m=g.next;else if((t=g)===m){h?1===h?o(t=c(a(t),e,r),e,r,n,i,f,2):2===h&&u(t,e,r,n,i,f):o(a(t),e,r,n,i,f,1);break}}}function s(t){var e=t.prev,r=t,n=t.next;if(y(e,r,n)>=0)return!1;for(var i=t.next.next;i!==t.prev;){if(m(e.x,e.y,r.x,r.y,n.x,n.y,i.x,i.y)&&y(i.prev,i,i.next)>=0)return!1;i=i.next}return!0}function l(t,e,r,n){var i=t.prev,a=t,o=t.next;if(y(i,a,o)>=0)return!1;for(var s=i.x<a.x?i.x<o.x?i.x:o.x:a.x<o.x?a.x:o.x,l=i.y<a.y?i.y<o.y?i.y:o.y:a.y<o.y?a.y:o.y,c=i.x>a.x?i.x>o.x?i.x:o.x:a.x>o.x?a.x:o.x,u=i.y>a.y?i.y>o.y?i.y:o.y:a.y>o.y?a.y:o.y,f=d(s,l,e,r,n),h=d(c,u,e,r,n),p=t.prevZ,g=t.nextZ;p&&p.z>=f&&g&&g.z<=h;){if(p!==t.prev&&p!==t.next&&m(i.x,i.y,a.x,a.y,o.x,o.y,p.x,p.y)&&y(p.prev,p,p.next)>=0)return!1;if(p=p.prevZ,g!==t.prev&&g!==t.next&&m(i.x,i.y,a.x,a.y,o.x,o.y,g.x,g.y)&&y(g.prev,g,g.next)>=0)return!1;g=g.nextZ}for(;p&&p.z>=f;){if(p!==t.prev&&p!==t.next&&m(i.x,i.y,a.x,a.y,o.x,o.y,p.x,p.y)&&y(p.prev,p,p.next)>=0)return!1;p=p.prevZ}for(;g&&g.z<=h;){if(g!==t.prev&&g!==t.next&&m(i.x,i.y,a.x,a.y,o.x,o.y,g.x,g.y)&&y(g.prev,g,g.next)>=0)return!1;g=g.nextZ}return!0}function c(t,e,r){var n=t;do{var i=n.prev,o=n.next.next;!x(i,o)&&b(i,n,n.next,o)&&T(i,o)&&T(o,i)&&(e.push(i.i/r),e.push(n.i/r),e.push(o.i/r),A(n),A(n.next),n=t=o),n=n.next}while(n!==t);return a(n)}function u(t,e,r,n,i,s){var l=t;do{for(var c=l.next.next;c!==l.prev;){if(l.i!==c.i&&v(l,c)){var u=k(l,c);return l=a(l,l.next),u=a(u,u.next),o(l,e,r,n,i,s),void o(u,e,r,n,i,s)}c=c.next}l=l.next}while(l!==t)}function f(t,e){return t.x-e.x}function h(t,e){if(e=function(t,e){var r,n=e,i=t.x,a=t.y,o=-1/0;do{if(a<=n.y&&a>=n.next.y&&n.next.y!==n.y){var s=n.x+(a-n.y)*(n.next.x-n.x)/(n.next.y-n.y);if(s<=i&&s>o){if(o=s,s===i){if(a===n.y)return n;if(a===n.next.y)return n.next}r=n.x<n.next.x?n:n.next}}n=n.next}while(n!==e);if(!r)return null;if(i===o)return r;var l,c=r,u=r.x,f=r.y,h=1/0;n=r;do{i>=n.x&&n.x>=u&&i!==n.x&&m(a<f?i:o,a,u,f,a<f?o:i,a,n.x,n.y)&&(l=Math.abs(a-n.y)/(i-n.x),T(n,t)&&(l<h||l===h&&(n.x>r.x||n.x===r.x&&p(r,n)))&&(r=n,h=l)),n=n.next}while(n!==c);return r}(t,e)){var r=k(e,t);a(e,e.next),a(r,r.next)}}function p(t,e){return y(t.prev,t,e.prev)<0&&y(e.next,t,t.next)<0}function d(t,e,r,n,i){return(t=1431655765&((t=858993459&((t=252645135&((t=16711935&((t=32767*(t-r)*i)|t<<8))|t<<4))|t<<2))|t<<1))|(e=1431655765&((e=858993459&((e=252645135&((e=16711935&((e=32767*(e-n)*i)|e<<8))|e<<4))|e<<2))|e<<1))<<1}function g(t){var e=t,r=t;do{(e.x<r.x||e.x===r.x&&e.y<r.y)&&(r=e),e=e.next}while(e!==t);return r}function m(t,e,r,n,i,a,o,s){return(i-o)*(e-s)-(t-o)*(a-s)>=0&&(t-o)*(n-s)-(r-o)*(e-s)>=0&&(r-o)*(a-s)-(i-o)*(n-s)>=0}function v(t,e){return t.next.i!==e.i&&t.prev.i!==e.i&&!function(t,e){var r=t;do{if(r.i!==t.i&&r.next.i!==t.i&&r.i!==e.i&&r.next.i!==e.i&&b(r,r.next,t,e))return!0;r=r.next}while(r!==t);return!1}(t,e)&&(T(t,e)&&T(e,t)&&function(t,e){var r=t,n=!1,i=(t.x+e.x)/2,a=(t.y+e.y)/2;do{r.y>a!=r.next.y>a&&r.next.y!==r.y&&i<(r.next.x-r.x)*(a-r.y)/(r.next.y-r.y)+r.x&&(n=!n),r=r.next}while(r!==t);return n}(t,e)&&(y(t.prev,t,e.prev)||y(t,e.prev,e))||x(t,e)&&y(t.prev,t,t.next)>0&&y(e.prev,e,e.next)>0)}function y(t,e,r){return(e.y-t.y)*(r.x-e.x)-(e.x-t.x)*(r.y-e.y)}function x(t,e){return t.x===e.x&&t.y===e.y}function b(t,e,r,n){var i=w(y(t,e,r)),a=w(y(t,e,n)),o=w(y(r,n,t)),s=w(y(r,n,e));return i!==a&&o!==s||(!(0!==i||!_(t,r,e))||(!(0!==a||!_(t,n,e))||(!(0!==o||!_(r,t,n))||!(0!==s||!_(r,e,n)))))}function _(t,e,r){return e.x<=Math.max(t.x,r.x)&&e.x>=Math.min(t.x,r.x)&&e.y<=Math.max(t.y,r.y)&&e.y>=Math.min(t.y,r.y)}function w(t){return t>0?1:t<0?-1:0}function T(t,e){return y(t.prev,t,t.next)<0?y(t,e,t.next)>=0&&y(t,t.prev,e)>=0:y(t,e,t.prev)<0||y(t,t.next,e)<0}function k(t,e){var r=new S(t.i,t.x,t.y),n=new S(e.i,e.x,e.y),i=t.next,a=e.prev;return t.next=e,e.prev=t,r.next=i,i.prev=r,n.next=r,r.prev=n,a.next=n,n.prev=a,n}function M(t,e,r,n){var i=new S(t,e,r);return n?(i.next=n.next,i.prev=n,n.next.prev=i,n.next=i):(i.prev=i,i.next=i),i}function A(t){t.next.prev=t.prev,t.prev.next=t.next,t.prevZ&&(t.prevZ.nextZ=t.nextZ),t.nextZ&&(t.nextZ.prevZ=t.prevZ)}function S(t,e,r){this.i=t,this.x=e,this.y=r,this.prev=null,this.next=null,this.z=null,this.prevZ=null,this.nextZ=null,this.steiner=!1}function E(t,e,r,n){for(var i=0,a=e,o=r-n;a<r;a+=n)i+=(t[o]-t[a])*(t[a+1]+t[o+1]),o=a;return i}e.exports=n,e.exports.default=n,n.deviation=function(t,e,r,n){var i=e&&e.length,a=i?e[0]*r:t.length,o=Math.abs(E(t,0,a,r));if(i)for(var s=0,l=e.length;s<l;s++){var c=e[s]*r,u=s<l-1?e[s+1]*r:t.length;o-=Math.abs(E(t,c,u,r))}var f=0;for(s=0;s<n.length;s+=3){var h=n[s]*r,p=n[s+1]*r,d=n[s+2]*r;f+=Math.abs((t[h]-t[d])*(t[p+1]-t[h+1])-(t[h]-t[p])*(t[d+1]-t[h+1]))}return 0===o&&0===f?0:Math.abs((f-o)/o)},n.flatten=function(t){for(var e=t[0][0].length,r={vertices:[],holes:[],dimensions:e},n=0,i=0;i<t.length;i++){for(var a=0;a<t[i].length;a++)for(var o=0;o<e;o++)r.vertices.push(t[i][a][o]);i>0&&(n+=t[i-1].length,r.holes.push(n))}return r}},{}],178:[function(t,e,r){"use strict";e.exports=function(t,e){var r=t.length;if("number"!=typeof e){e=0;for(var i=0;i<r;++i){var a=t[i];e=Math.max(e,a[0],a[1])}e=1+(0|e)}e|=0;var o=new Array(e);for(i=0;i<e;++i)o[i]=[];for(i=0;i<r;++i){a=t[i];o[a[0]].push(a[1]),o[a[1]].push(a[0])}for(var s=0;s<e;++s)n(o[s],(function(t,e){return t-e}));return o};var n=t("uniq")},{uniq:597}],179:[function(t,e,r){var n=t("strongly-connected-components");e.exports=function(t,e){var r,i=[],a=[],o=[],s={},l=[];function c(t){var e,n,i=!1;for(a.push(t),o[t]=!0,e=0;e<l[t].length;e++)(n=l[t][e])===r?(u(r,a),i=!0):o[n]||(i=c(n));if(i)!function t(e){o[e]=!1,s.hasOwnProperty(e)&&Object.keys(s[e]).forEach((function(r){delete s[e][r],o[r]&&t(r)}))}(t);else for(e=0;e<l[t].length;e++){n=l[t][e];var f=s[n];f||(f={},s[n]=f),f[n]=!0}return a.pop(),i}function u(t,r){var n=[].concat(r).concat(t);e?e(c):i.push(n)}function f(e){!function(e){for(var r=0;r<t.length;r++)r<e&&(t[r]=[]),t[r]=t[r].filter((function(t){return t>=e}))}(e);for(var r,i=n(t).components.filter((function(t){return t.length>1})),a=1/0,o=0;o<i.length;o++)for(var s=0;s<i[o].length;s++)i[o][s]<a&&(a=i[o][s],r=o);var l=i[r];return!!l&&{leastVertex:a,adjList:t.map((function(t,e){return-1===l.indexOf(e)?[]:t.filter((function(t){return-1!==l.indexOf(t)}))}))}}r=0;for(var h=t.length;r<h;){var p=f(r);if(r=p.leastVertex,l=p.adjList){for(var d=0;d<l.length;d++)for(var g=0;g<l[d].length;g++){var m=l[d][g];o[+m]=!1,s[m]={}}c(r),r+=1}else r=h}return e?void 0:i}},{"strongly-connected-components":569}],180:[function(t,e,r){"use strict";var n=t("../../object/valid-value");e.exports=function(){return n(this).length=0,this}},{"../../object/valid-value":211}],181:[function(t,e,r){"use strict";e.exports=t("./is-implemented")()?Array.from:t("./shim")},{"./is-implemented":182,"./shim":183}],182:[function(t,e,r){"use strict";e.exports=function(){var t,e,r=Array.from;return"function"==typeof r&&(e=r(t=["raz","dwa"]),Boolean(e&&e!==t&&"dwa"===e[1]))}},{}],183:[function(t,e,r){"use strict";var n=t("es6-symbol").iterator,i=t("../../function/is-arguments"),a=t("../../function/is-function"),o=t("../../number/to-pos-integer"),s=t("../../object/valid-callable"),l=t("../../object/valid-value"),c=t("../../object/is-value"),u=t("../../string/is-string"),f=Array.isArray,h=Function.prototype.call,p={configurable:!0,enumerable:!0,writable:!0,value:null},d=Object.defineProperty;e.exports=function(t){var e,r,g,m,v,y,x,b,_,w,T=arguments[1],k=arguments[2];if(t=Object(l(t)),c(T)&&s(T),this&&this!==Array&&a(this))e=this;else{if(!T){if(i(t))return 1!==(v=t.length)?Array.apply(null,t):((m=new Array(1))[0]=t[0],m);if(f(t)){for(m=new Array(v=t.length),r=0;r<v;++r)m[r]=t[r];return m}}m=[]}if(!f(t))if(void 0!==(_=t[n])){for(x=s(_).call(t),e&&(m=new e),b=x.next(),r=0;!b.done;)w=T?h.call(T,k,b.value,r):b.value,e?(p.value=w,d(m,r,p)):m[r]=w,b=x.next(),++r;v=r}else if(u(t)){for(v=t.length,e&&(m=new e),r=0,g=0;r<v;++r)w=t[r],r+1<v&&(y=w.charCodeAt(0))>=55296&&y<=56319&&(w+=t[++r]),w=T?h.call(T,k,w,g):w,e?(p.value=w,d(m,g,p)):m[g]=w,++g;v=g}if(void 0===v)for(v=o(t.length),e&&(m=new e(v)),r=0;r<v;++r)w=T?h.call(T,k,t[r],r):t[r],e?(p.value=w,d(m,r,p)):m[r]=w;return e&&(p.value=null,m.length=v),m}},{"../../function/is-arguments":184,"../../function/is-function":185,"../../number/to-pos-integer":191,"../../object/is-value":200,"../../object/valid-callable":209,"../../object/valid-value":211,"../../string/is-string":215,"es6-symbol":225}],184:[function(t,e,r){"use strict";var n=Object.prototype.toString,i=n.call(function(){return arguments}());e.exports=function(t){return n.call(t)===i}},{}],185:[function(t,e,r){"use strict";var n=Object.prototype.toString,i=RegExp.prototype.test.bind(/^[object [A-Za-z0-9]*Function]$/);e.exports=function(t){return"function"==typeof t&&i(n.call(t))}},{}],186:[function(t,e,r){"use strict";e.exports=function(){}},{}],187:[function(t,e,r){"use strict";e.exports=t("./is-implemented")()?Math.sign:t("./shim")},{"./is-implemented":188,"./shim":189}],188:[function(t,e,r){"use strict";e.exports=function(){var t=Math.sign;return"function"==typeof t&&(1===t(10)&&-1===t(-20))}},{}],189:[function(t,e,r){"use strict";e.exports=function(t){return t=Number(t),isNaN(t)||0===t?t:t>0?1:-1}},{}],190:[function(t,e,r){"use strict";var n=t("../math/sign"),i=Math.abs,a=Math.floor;e.exports=function(t){return isNaN(t)?0:0!==(t=Number(t))&&isFinite(t)?n(t)*a(i(t)):t}},{"../math/sign":187}],191:[function(t,e,r){"use strict";var n=t("./to-integer"),i=Math.max;e.exports=function(t){return i(0,n(t))}},{"./to-integer":190}],192:[function(t,e,r){"use strict";var n=t("./valid-callable"),i=t("./valid-value"),a=Function.prototype.bind,o=Function.prototype.call,s=Object.keys,l=Object.prototype.propertyIsEnumerable;e.exports=function(t,e){return function(r,c){var u,f=arguments[2],h=arguments[3];return r=Object(i(r)),n(c),u=s(r),h&&u.sort("function"==typeof h?a.call(h,r):void 0),"function"!=typeof t&&(t=u[t]),o.call(t,u,(function(t,n){return l.call(r,t)?o.call(c,f,r[t],t,r,n):e}))}}},{"./valid-callable":209,"./valid-value":211}],193:[function(t,e,r){"use strict";e.exports=t("./is-implemented")()?Object.assign:t("./shim")},{"./is-implemented":194,"./shim":195}],194:[function(t,e,r){"use strict";e.exports=function(){var t,e=Object.assign;return"function"==typeof e&&(e(t={foo:"raz"},{bar:"dwa"},{trzy:"trzy"}),t.foo+t.bar+t.trzy==="razdwatrzy")}},{}],195:[function(t,e,r){"use strict";var n=t("../keys"),i=t("../valid-value"),a=Math.max;e.exports=function(t,e){var r,o,s,l=a(arguments.length,2);for(t=Object(i(t)),s=function(n){try{t[n]=e[n]}catch(t){r||(r=t)}},o=1;o<l;++o)n(e=arguments[o]).forEach(s);if(void 0!==r)throw r;return t}},{"../keys":201,"../valid-value":211}],196:[function(t,e,r){"use strict";var n=t("../array/from"),i=t("./assign"),a=t("./valid-value");e.exports=function(t){var e=Object(a(t)),r=arguments[1],o=Object(arguments[2]);if(e!==t&&!r)return e;var s={};return r?n(r,(function(e){(o.ensure||e in t)&&(s[e]=t[e])})):i(s,t),s}},{"../array/from":181,"./assign":193,"./valid-value":211}],197:[function(t,e,r){"use strict";var n,i,a,o,s=Object.create;t("./set-prototype-of/is-implemented")()||(n=t("./set-prototype-of/shim")),e.exports=n?1!==n.level?s:(i={},a={},o={configurable:!1,enumerable:!1,writable:!0,value:void 0},Object.getOwnPropertyNames(Object.prototype).forEach((function(t){a[t]="__proto__"!==t?o:{configurable:!0,enumerable:!1,writable:!0,value:void 0}})),Object.defineProperties(i,a),Object.defineProperty(n,"nullPolyfill",{configurable:!1,enumerable:!1,writable:!1,value:i}),function(t,e){return s(null===t?i:t,e)}):s},{"./set-prototype-of/is-implemented":207,"./set-prototype-of/shim":208}],198:[function(t,e,r){"use strict";e.exports=t("./_iterate")("forEach")},{"./_iterate":192}],199:[function(t,e,r){"use strict";var n=t("./is-value"),i={function:!0,object:!0};e.exports=function(t){return n(t)&&i[typeof t]||!1}},{"./is-value":200}],200:[function(t,e,r){"use strict";var n=t("../function/noop")();e.exports=function(t){return t!==n&&null!==t}},{"../function/noop":186}],201:[function(t,e,r){"use strict";e.exports=t("./is-implemented")()?Object.keys:t("./shim")},{"./is-implemented":202,"./shim":203}],202:[function(t,e,r){"use strict";e.exports=function(){try{return Object.keys("primitive"),!0}catch(t){return!1}}},{}],203:[function(t,e,r){"use strict";var n=t("../is-value"),i=Object.keys;e.exports=function(t){return i(n(t)?Object(t):t)}},{"../is-value":200}],204:[function(t,e,r){"use strict";var n=t("./valid-callable"),i=t("./for-each"),a=Function.prototype.call;e.exports=function(t,e){var r={},o=arguments[2];return n(e),i(t,(function(t,n,i,s){r[n]=a.call(e,o,t,n,i,s)})),r}},{"./for-each":198,"./valid-callable":209}],205:[function(t,e,r){"use strict";var n=t("./is-value"),i=Array.prototype.forEach,a=Object.create,o=function(t,e){var r;for(r in t)e[r]=t[r]};e.exports=function(t){var e=a(null);return i.call(arguments,(function(t){n(t)&&o(Object(t),e)})),e}},{"./is-value":200}],206:[function(t,e,r){"use strict";e.exports=t("./is-implemented")()?Object.setPrototypeOf:t("./shim")},{"./is-implemented":207,"./shim":208}],207:[function(t,e,r){"use strict";var n=Object.create,i=Object.getPrototypeOf,a={};e.exports=function(){var t=Object.setPrototypeOf,e=arguments[0]||n;return"function"==typeof t&&i(t(e(null),a))===a}},{}],208:[function(t,e,r){"use strict";var n,i=t("../is-object"),a=t("../valid-value"),o=Object.prototype.isPrototypeOf,s=Object.defineProperty,l={configurable:!0,enumerable:!1,writable:!0,value:void 0};n=function(t,e){if(a(t),null===e||i(e))return t;throw new TypeError("Prototype must be null or an object")},e.exports=function(t){var e,r;return t?(2===t.level?t.set?(r=t.set,e=function(t,e){return r.call(n(t,e),e),t}):e=function(t,e){return n(t,e).__proto__=e,t}:e=function t(e,r){var i;return n(e,r),(i=o.call(t.nullPolyfill,e))&&delete t.nullPolyfill.__proto__,null===r&&(r=t.nullPolyfill),e.__proto__=r,i&&s(t.nullPolyfill,"__proto__",l),e},Object.defineProperty(e,"level",{configurable:!1,enumerable:!1,writable:!1,value:t.level})):null}(function(){var t,e=Object.create(null),r={},n=Object.getOwnPropertyDescriptor(Object.prototype,"__proto__");if(n){try{(t=n.set).call(e,r)}catch(t){}if(Object.getPrototypeOf(e)===r)return{set:t,level:2}}return e.__proto__=r,Object.getPrototypeOf(e)===r?{level:2}:((e={}).__proto__=r,Object.getPrototypeOf(e)===r&&{level:1})}()),t("../create")},{"../create":197,"../is-object":199,"../valid-value":211}],209:[function(t,e,r){"use strict";e.exports=function(t){if("function"!=typeof t)throw new TypeError(t+" is not a function");return t}},{}],210:[function(t,e,r){"use strict";var n=t("./is-object");e.exports=function(t){if(!n(t))throw new TypeError(t+" is not an Object");return t}},{"./is-object":199}],211:[function(t,e,r){"use strict";var n=t("./is-value");e.exports=function(t){if(!n(t))throw new TypeError("Cannot use null or undefined");return t}},{"./is-value":200}],212:[function(t,e,r){"use strict";e.exports=t("./is-implemented")()?String.prototype.contains:t("./shim")},{"./is-implemented":213,"./shim":214}],213:[function(t,e,r){"use strict";var n="razdwatrzy";e.exports=function(){return"function"==typeof n.contains&&(!0===n.contains("dwa")&&!1===n.contains("foo"))}},{}],214:[function(t,e,r){"use strict";var n=String.prototype.indexOf;e.exports=function(t){return n.call(this,t,arguments[1])>-1}},{}],215:[function(t,e,r){"use strict";var n=Object.prototype.toString,i=n.call("");e.exports=function(t){return"string"==typeof t||t&&"object"==typeof t&&(t instanceof String||n.call(t)===i)||!1}},{}],216:[function(t,e,r){"use strict";var n=Object.create(null),i=Math.random;e.exports=function(){var t;do{t=i().toString(36).slice(2)}while(n[t]);return t}},{}],217:[function(t,e,r){"use strict";var n,i=t("es5-ext/object/set-prototype-of"),a=t("es5-ext/string/#/contains"),o=t("d"),s=t("es6-symbol"),l=t("./"),c=Object.defineProperty;n=e.exports=function(t,e){if(!(this instanceof n))throw new TypeError("Constructor requires 'new'");l.call(this,t),e=e?a.call(e,"key+value")?"key+value":a.call(e,"key")?"key":"value":"value",c(this,"__kind__",o("",e))},i&&i(n,l),delete n.prototype.constructor,n.prototype=Object.create(l.prototype,{_resolve:o((function(t){return"value"===this.__kind__?this.__list__[t]:"key+value"===this.__kind__?[t,this.__list__[t]]:t}))}),c(n.prototype,s.toStringTag,o("c","Array Iterator"))},{"./":220,d:155,"es5-ext/object/set-prototype-of":206,"es5-ext/string/#/contains":212,"es6-symbol":225}],218:[function(t,e,r){"use strict";var n=t("es5-ext/function/is-arguments"),i=t("es5-ext/object/valid-callable"),a=t("es5-ext/string/is-string"),o=t("./get"),s=Array.isArray,l=Function.prototype.call,c=Array.prototype.some;e.exports=function(t,e){var r,u,f,h,p,d,g,m,v=arguments[2];if(s(t)||n(t)?r="array":a(t)?r="string":t=o(t),i(e),f=function(){h=!0},"array"!==r)if("string"!==r)for(u=t.next();!u.done;){if(l.call(e,v,u.value,f),h)return;u=t.next()}else for(d=t.length,p=0;p<d&&(g=t[p],p+1<d&&(m=g.charCodeAt(0))>=55296&&m<=56319&&(g+=t[++p]),l.call(e,v,g,f),!h);++p);else c.call(t,(function(t){return l.call(e,v,t,f),h}))}},{"./get":219,"es5-ext/function/is-arguments":184,"es5-ext/object/valid-callable":209,"es5-ext/string/is-string":215}],219:[function(t,e,r){"use strict";var n=t("es5-ext/function/is-arguments"),i=t("es5-ext/string/is-string"),a=t("./array"),o=t("./string"),s=t("./valid-iterable"),l=t("es6-symbol").iterator;e.exports=function(t){return"function"==typeof s(t)[l]?t[l]():n(t)?new a(t):i(t)?new o(t):new a(t)}},{"./array":217,"./string":222,"./valid-iterable":223,"es5-ext/function/is-arguments":184,"es5-ext/string/is-string":215,"es6-symbol":225}],220:[function(t,e,r){"use strict";var n,i=t("es5-ext/array/#/clear"),a=t("es5-ext/object/assign"),o=t("es5-ext/object/valid-callable"),s=t("es5-ext/object/valid-value"),l=t("d"),c=t("d/auto-bind"),u=t("es6-symbol"),f=Object.defineProperty,h=Object.defineProperties;e.exports=n=function(t,e){if(!(this instanceof n))throw new TypeError("Constructor requires 'new'");h(this,{__list__:l("w",s(t)),__context__:l("w",e),__nextIndex__:l("w",0)}),e&&(o(e.on),e.on("_add",this._onAdd),e.on("_delete",this._onDelete),e.on("_clear",this._onClear))},delete n.prototype.constructor,h(n.prototype,a({_next:l((function(){var t;if(this.__list__)return this.__redo__&&void 0!==(t=this.__redo__.shift())?t:this.__nextIndex__<this.__list__.length?this.__nextIndex__++:void this._unBind()})),next:l((function(){return this._createResult(this._next())})),_createResult:l((function(t){return void 0===t?{done:!0,value:void 0}:{done:!1,value:this._resolve(t)}})),_resolve:l((function(t){return this.__list__[t]})),_unBind:l((function(){this.__list__=null,delete this.__redo__,this.__context__&&(this.__context__.off("_add",this._onAdd),this.__context__.off("_delete",this._onDelete),this.__context__.off("_clear",this._onClear),this.__context__=null)})),toString:l((function(){return"[object "+(this[u.toStringTag]||"Object")+"]"}))},c({_onAdd:l((function(t){t>=this.__nextIndex__||(++this.__nextIndex__,this.__redo__?(this.__redo__.forEach((function(e,r){e>=t&&(this.__redo__[r]=++e)}),this),this.__redo__.push(t)):f(this,"__redo__",l("c",[t])))})),_onDelete:l((function(t){var e;t>=this.__nextIndex__||(--this.__nextIndex__,this.__redo__&&(-1!==(e=this.__redo__.indexOf(t))&&this.__redo__.splice(e,1),this.__redo__.forEach((function(e,r){e>t&&(this.__redo__[r]=--e)}),this)))})),_onClear:l((function(){this.__redo__&&i.call(this.__redo__),this.__nextIndex__=0}))}))),f(n.prototype,u.iterator,l((function(){return this})))},{d:155,"d/auto-bind":154,"es5-ext/array/#/clear":180,"es5-ext/object/assign":193,"es5-ext/object/valid-callable":209,"es5-ext/object/valid-value":211,"es6-symbol":225}],221:[function(t,e,r){"use strict";var n=t("es5-ext/function/is-arguments"),i=t("es5-ext/object/is-value"),a=t("es5-ext/string/is-string"),o=t("es6-symbol").iterator,s=Array.isArray;e.exports=function(t){return!!i(t)&&(!!s(t)||(!!a(t)||(!!n(t)||"function"==typeof t[o])))}},{"es5-ext/function/is-arguments":184,"es5-ext/object/is-value":200,"es5-ext/string/is-string":215,"es6-symbol":225}],222:[function(t,e,r){"use strict";var n,i=t("es5-ext/object/set-prototype-of"),a=t("d"),o=t("es6-symbol"),s=t("./"),l=Object.defineProperty;n=e.exports=function(t){if(!(this instanceof n))throw new TypeError("Constructor requires 'new'");t=String(t),s.call(this,t),l(this,"__length__",a("",t.length))},i&&i(n,s),delete n.prototype.constructor,n.prototype=Object.create(s.prototype,{_next:a((function(){if(this.__list__)return this.__nextIndex__<this.__length__?this.__nextIndex__++:void this._unBind()})),_resolve:a((function(t){var e,r=this.__list__[t];return this.__nextIndex__===this.__length__?r:(e=r.charCodeAt(0))>=55296&&e<=56319?r+this.__list__[this.__nextIndex__++]:r}))}),l(n.prototype,o.toStringTag,a("c","String Iterator"))},{"./":220,d:155,"es5-ext/object/set-prototype-of":206,"es6-symbol":225}],223:[function(t,e,r){"use strict";var n=t("./is-iterable");e.exports=function(t){if(!n(t))throw new TypeError(t+" is not iterable");return t}},{"./is-iterable":221}],224:[function(t,e,r){(function(n,i){(function(){
/*!
 * @overview es6-promise - a tiny implementation of Promises/A+.
 * @copyright Copyright (c) 2014 Yehuda Katz, Tom Dale, Stefan Penner and contributors (Conversion to ES6 API by Jake Archibald)
 * @license   Licensed under MIT license
 *            See https://raw.githubusercontent.com/stefanpenner/es6-promise/master/LICENSE
 * @version   v4.2.8+1e68dce6
 */
/*!
 * Determine if an object is a Buffer
 *
 * @author   Feross Aboukhadijeh <https://feross.org>
 * @license  MIT
 */
/*
object-assign
(c) Sindre Sorhus
@license MIT
*/
"use strict";var n=Object.getOwnPropertySymbols,i=Object.prototype.hasOwnProperty,a=Object.prototype.propertyIsEnumerable;function o(t){if(null==t)throw new TypeError("Object.assign cannot be called with null or undefined");return Object(t)}e.exports=function(){try{if(!Object.assign)return!1;var t=new String("abc");if(t[5]="de","5"===Object.getOwnPropertyNames(t)[0])return!1;for(var e={},r=0;r<10;r++)e["_"+String.fromCharCode(r)]=r;if("0123456789"!==Object.getOwnPropertyNames(e).map((function(t){return e[t]})).join(""))return!1;var n={};return"abcdefghijklmnopqrst".split("").forEach((function(t){n[t]=t})),"abcdefghijklmnopqrst"===Object.keys(Object.assign({},n)).join("")}catch(t){return!1}}()?Object.assign:function(t,e){for(var r,s,l=o(t),c=1;c<arguments.length;c++){for(var u in r=Object(arguments[c]))i.call(r,u)&&(l[u]=r[u]);if(n){s=n(r);for(var f=0;f<s.length;f++)a.call(r,s[f])&&(l[s[f]]=r[s[f]])}}return l}},{}],500:[function(t,e,r){"use strict";e.exports=function(t,e,r,n,i,a,o,s,l,c){var u=e+a+c;if(f>0){var f=Math.sqrt(u+1);t[0]=.5*(o-l)/f,t[1]=.5*(s-n)/f,t[2]=.5*(r-a)/f,t[3]=.5*f}else{var h=Math.max(e,a,c);f=Math.sqrt(2*h-u+1);e>=h?(t[0]=.5*f,t[1]=.5*(i+r)/f,t[2]=.5*(s+n)/f,t[3]=.5*(o-l)/f):a>=h?(t[0]=.5*(r+i)/f,t[1]=.5*f,t[2]=.5*(l+o)/f,t[3]=.5*(s-n)/f):(t[0]=.5*(n+s)/f,t[1]=.5*(o+l)/f,t[2]=.5*f,t[3]=.5*(r-i)/f)}return t}},{}],501:[function(t,e,r){"use strict";e.exports=function(t){var e=(t=t||{}).center||[0,0,0],r=t.rotation||[0,0,0,1],n=t.radius||1;e=[].slice.call(e,0,3),u(r=[].slice.call(r,0,4),r);var i=new f(r,e,Math.log(n));i.setDistanceLimits(t.zoomMin,t.zoomMax),("eye"in t||"up"in t)&&i.lookAt(0,t.eye,t.center,t.up);return i};var n=t("filtered-vector"),i=t("gl-mat4/lookAt"),a=t("gl-mat4/fromQuat"),o=t("gl-mat4/invert"),s=t("./lib/quatFromFrame");function l(t,e,r){return Math.sqrt(Math.pow(t,2)+Math.pow(e,2)+Math.pow(r,2))}function c(t,e,r,n){return Math.sqrt(Math.pow(t,2)+Math.pow(e,2)+Math.pow(r,2)+Math.pow(n,2))}function u(t,e){var r=e[0],n=e[1],i=e[2],a=e[3],o=c(r,n,i,a);o>1e-6?(t[0]=r/o,t[1]=n/o,t[2]=i/o,t[3]=a/o):(t[0]=t[1]=t[2]=0,t[3]=1)}function f(t,e,r){this.radius=n([r]),this.center=n(e),this.rotation=n(t),this.computedRadius=this.radius.curve(0),this.computedCenter=this.center.curve(0),this.computedRotation=this.rotation.curve(0),this.computedUp=[.1,0,0],this.computedEye=[.1,0,0],this.computedMatrix=[.1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],this.recalcMatrix(0)}var h=f.prototype;h.lastT=function(){return Math.max(this.radius.lastT(),this.center.lastT(),this.rotation.lastT())},h.recalcMatrix=function(t){this.radius.curve(t),this.center.curve(t),this.rotation.curve(t);var e=this.computedRotation;u(e,e);var r=this.computedMatrix;a(r,e);var n=this.computedCenter,i=this.computedEye,o=this.computedUp,s=Math.exp(this.computedRadius[0]);i[0]=n[0]+s*r[2],i[1]=n[1]+s*r[6],i[2]=n[2]+s*r[10],o[0]=r[1],o[1]=r[5],o[2]=r[9];for(var l=0;l<3;++l){for(var c=0,f=0;f<3;++f)c+=r[l+4*f]*i[f];r[12+l]=-c}},h.getMatrix=function(t,e){this.recalcMatrix(t);var r=this.computedMatrix;if(e){for(var n=0;n<16;++n)e[n]=r[n];return e}return r},h.idle=function(t){this.center.idle(t),this.radius.idle(t),this.rotation.idle(t)},h.flush=function(t){this.center.flush(t),this.radius.flush(t),this.rotation.flush(t)},h.pan=function(t,e,r,n){e=e||0,r=r||0,n=n||0,this.recalcMatrix(t);var i=this.computedMatrix,a=i[1],o=i[5],s=i[9],c=l(a,o,s);a/=c,o/=c,s/=c;var u=i[0],f=i[4],h=i[8],p=u*a+f*o+h*s,d=l(u-=a*p,f-=o*p,h-=s*p);u/=d,f/=d,h/=d;var g=i[2],m=i[6],v=i[10],y=g*a+m*o+v*s,x=g*u+m*f+v*h,b=l(g-=y*a+x*u,m-=y*o+x*f,v-=y*s+x*h);g/=b,m/=b,v/=b;var _=u*e+a*r,w=f*e+o*r,T=h*e+s*r;this.center.move(t,_,w,T);var k=Math.exp(this.computedRadius[0]);k=Math.max(1e-4,k+n),this.radius.set(t,Math.log(k))},h.rotate=function(t,e,r,n){this.recalcMatrix(t),e=e||0,r=r||0;var i=this.computedMatrix,a=i[0],o=i[4],s=i[8],u=i[1],f=i[5],h=i[9],p=i[2],d=i[6],g=i[10],m=e*a+r*u,v=e*o+r*f,y=e*s+r*h,x=-(d*y-g*v),b=-(g*m-p*y),_=-(p*v-d*m),w=Math.sqrt(Math.max(0,1-Math.pow(x,2)-Math.pow(b,2)-Math.pow(_,2))),T=c(x,b,_,w);T>1e-6?(x/=T,b/=T,_/=T,w/=T):(x=b=_=0,w=1);var k=this.computedRotation,M=k[0],A=k[1],S=k[2],E=k[3],C=M*w+E*x+A*_-S*b,L=A*w+E*b+S*x-M*_,I=S*w+E*_+M*b-A*x,P=E*w-M*x-A*b-S*_;if(n){x=p,b=d,_=g;var z=Math.sin(n)/l(x,b,_);x*=z,b*=z,_*=z,P=P*(w=Math.cos(e))-(C=C*w+P*x+L*_-I*b)*x-(L=L*w+P*b+I*x-C*_)*b-(I=I*w+P*_+C*b-L*x)*_}var O=c(C,L,I,P);O>1e-6?(C/=O,L/=O,I/=O,P/=O):(C=L=I=0,P=1),this.rotation.set(t,C,L,I,P)},h.lookAt=function(t,e,r,n){this.recalcMatrix(t),r=r||this.computedCenter,e=e||this.computedEye,n=n||this.computedUp;var a=this.computedMatrix;i(a,e,r,n);var o=this.computedRotation;s(o,a[0],a[1],a[2],a[4],a[5],a[6],a[8],a[9],a[10]),u(o,o),this.rotation.set(t,o[0],o[1],o[2],o[3]);for(var l=0,c=0;c<3;++c)l+=Math.pow(r[c]-e[c],2);this.radius.set(t,.5*Math.log(Math.max(l,1e-6))),this.center.set(t,r[0],r[1],r[2])},h.translate=function(t,e,r,n){this.center.move(t,e||0,r||0,n||0)},h.setMatrix=function(t,e){var r=this.computedRotation;s(r,e[0],e[1],e[2],e[4],e[5],e[6],e[8],e[9],e[10]),u(r,r),this.rotation.set(t,r[0],r[1],r[2],r[3]);var n=this.computedMatrix;o(n,e);var i=n[15];if(Math.abs(i)>1e-6){var a=n[12]/i,l=n[13]/i,c=n[14]/i;this.recalcMatrix(t);var f=Math.exp(this.computedRadius[0]);this.center.set(t,a-n[2]*f,l-n[6]*f,c-n[10]*f),this.radius.idle(t)}else this.center.idle(t),this.radius.idle(t)},h.setDistance=function(t,e){e>0&&this.radius.set(t,Math.log(e))},h.setDistanceLimits=function(t,e){t=t>0?Math.log(t):-1/0,e=e>0?Math.log(e):1/0,e=Math.max(e,t),this.radius.bounds[0][0]=t,this.radius.bounds[1][0]=e},h.getDistanceLimits=function(t){var e=this.radius.bounds;return t?(t[0]=Math.exp(e[0][0]),t[1]=Math.exp(e[1][0]),t):[Math.exp(e[0][0]),Math.exp(e[1][0])]},h.toJSON=function(){return this.recalcMatrix(this.lastT()),{center:this.computedCenter.slice(),rotation:this.computedRotation.slice(),distance:Math.log(this.computedRadius[0]),zoomMin:this.radius.bounds[0][0],zoomMax:this.radius.bounds[1][0]}},h.fromJSON=function(t){var e=this.lastT(),r=t.center;r&&this.center.set(e,r[0],r[1],r[2]);var n=t.rotation;n&&this.rotation.set(e,n[0],n[1],n[2],n[3]);var i=t.distance;i&&i>0&&this.radius.set(e,Math.log(i)),this.setDistanceLimits(t.zoomMin,t.zoomMax)}},{"./lib/quatFromFrame":500,"filtered-vector":242,"gl-mat4/fromQuat":282,"gl-mat4/invert":293,"gl-mat4/lookAt":294}],502:[function(t,e,r){
/*!
 * pad-left <https://github.com/jonschlinkert/pad-left>
 *
 * Copyright (c) 2014-2015, Jon Schlinkert.
 * Licensed under the MIT license.
 */
"use strict";var n=t("repeat-string");e.exports=function(t,e,r){return n(r="undefined"!=typeof r?r+"":" ",e)+t}},{"repeat-string":541}],503:[function(t,e,r){"use strict";function n(t,e){if("string"!=typeof t)return[t];var r=[t];"string"==typeof e||Array.isArray(e)?e={brackets:e}:e||(e={});var n=e.brackets?Array.isArray(e.brackets)?e.brackets:[e.brackets]:["{}","[]","()"],i=e.escape||"___",a=!!e.flat;n.forEach((function(t){var e=new RegExp(["\\",t[0],"[^\\",t[0],"\\",t[1],"]*\\",t[1]].join("")),n=[];function a(e,a,o){var s=r.push(e.slice(t[0].length,-t[1].length))-1;return n.push(s),i+s+i}r.forEach((function(t,n){for(var i,o=0;t!=i;)if(i=t,t=t.replace(e,a),o++>1e4)throw Error("References have circular dependency. Please, check them.");r[n]=t})),n=n.reverse(),r=r.map((function(e){return n.forEach((function(r){e=e.replace(new RegExp("(\\"+i+r+"\\"+i+")","g"),t[0]+"$1"+t[1])})),e}))}));var o=new RegExp("\\"+i+"([0-9]+)\\"+i);return a?r:function t(e,r,n){for(var i,a=[],s=0;i=o.exec(e);){if(s++>1e4)throw Error("Circular references in parenthesis");a.push(e.slice(0,i.index)),a.push(t(r[i[1]],r)),e=e.slice(i.index+i[0].length)}return a.push(e),a}(r[0],r)}function i(t,e){if(e&&e.flat){var r,n=e&&e.escape||"___",i=t[0];if(!i)return"";for(var a=new RegExp("\\"+n+"([0-9]+)\\"+n),o=0;i!=r;){if(o++>1e4)throw Error("Circular references in "+t);r=i,i=i.replace(a,s)}return i}return t.reduce((function t(e,r){return Array.isArray(r)&&(r=r.reduce(t,"")),e+r}),"");function s(e,r){if(null==t[r])throw Error("Reference "+r+"is undefined");return t[r]}}function a(t,e){return Array.isArray(t)?i(t,e):n(t,e)}a.parse=n,a.stringify=i,e.exports=a},{}],504:[function(t,e,r){"use strict";var n=t("pick-by-alias");e.exports=function(t){var e;arguments.length>1&&(t=arguments);"string"==typeof t?t=t.split(/\s/).map(parseFloat):"number"==typeof t&&(t=[t]);t.length&&"number"==typeof t[0]?e=1===t.length?{width:t[0],height:t[0],x:0,y:0}:2===t.length?{width:t[0],height:t[1],x:0,y:0}:{x:t[0],y:t[1],width:t[2]-t[0]||0,height:t[3]-t[1]||0}:t&&(t=n(t,{left:"x l left Left",top:"y t top Top",width:"w width W Width",height:"h height W Width",bottom:"b bottom Bottom",right:"r right Right"}),e={x:t.left||0,y:t.top||0},null==t.width?t.right?e.width=t.right-e.x:e.width=0:e.width=t.width,null==t.height?t.bottom?e.height=t.bottom-e.y:e.height=0:e.height=t.height);return e}},{"pick-by-alias":511}],505:[function(t,e,r){e.exports=function(t){var e=[];return t.replace(i,(function(t,r,i){var o=r.toLowerCase();for(i=function(t){var e=t.match(a);return e?e.map(Number):[]}(i),"m"==o&&i.length>2&&(e.push([r].concat(i.splice(0,2))),o="l",r="m"==r?"l":"L");;){if(i.length==n[o])return i.unshift(r),e.push(i);if(i.length<n[o])throw new Error("malformed path data");e.push([r].concat(i.splice(0,n[o])))}})),e};var n={a:7,c:6,h:1,l:2,m:2,q:4,s:4,t:2,v:1,z:0},i=/([astvzqmhlc])([^astvzqmhlc]*)/gi;var a=/-?[0-9]*\.?[0-9]+(?:e[-+]?\d+)?/gi},{}],506:[function(t,e,r){e.exports=function(t,e){e||(e=[0,""]),t=String(t);var r=parseFloat(t,10);return e[0]=r,e[1]=t.match(/[\d.\-\+]*\s*(.*)/)[1]||"",e}},{}],507:[function(t,e,r){(function(t){(function(){"use strict";function r(t){if("string"!=typeof t)throw new TypeError("Path must be a string. Received "+JSON.stringify(t))}function n(t,e){for(var r,n="",i=0,a=-1,o=0,s=0;s<=t.length;++s){if(s<t.length)r=t.charCodeAt(s);else{if(47===r)break;r=47}if(47===r){if(a===s-1||1===o);else if(a!==s-1&&2===o){if(n.length<2||2!==i||46!==n.charCodeAt(n.length-1)||46!==n.charCodeAt(n.length-2))if(n.length>2){var l=n.lastIndexOf("/");if(l!==n.length-1){-1===l?(n="",i=0):i=(n=n.slice(0,l)).length-1-n.lastIndexOf("/"),a=s,o=0;continue}}else if(2===n.length||1===n.length){n="",i=0,a=s,o=0;continue}e&&(n.length>0?n+="/..":n="..",i=2)}else n.length>0?n+="/"+t.slice(a+1,s):n=t.slice(a+1,s),i=s-a-1;a=s,o=0}else 46===r&&-1!==o?++o:o=-1}return n}var i={resolve:function(){for(var e,i="",a=!1,o=arguments.length-1;o>=-1&&!a;o--){var s;o>=0?s=arguments[o]:(void 0===e&&(e=t.cwd()),s=e),r(s),0!==s.length&&(i=s+"/"+i,a=47===s.charCodeAt(0))}return i=n(i,!a),a?i.length>0?"/"+i:"/":i.length>0?i:"."},normalize:function(t){if(r(t),0===t.length)return".";var e=47===t.charCodeAt(0),i=47===t.charCodeAt(t.length-1);return 0!==(t=n(t,!e)).length||e||(t="."),t.length>0&&i&&(t+="/"),e?"/"+t:t},isAbsolute:function(t){return r(t),t.length>0&&47===t.charCodeAt(0)},join:function(){if(0===arguments.length)return".";for(var t,e=0;e<arguments.length;++e){var n=arguments[e];r(n),n.length>0&&(void 0===t?t=n:t+="/"+n)}return void 0===t?".":i.normalize(t)},relative:function(t,e){if(r(t),r(e),t===e)return"";if((t=i.resolve(t))===(e=i.resolve(e)))return"";for(var n=1;n<t.length&&47===t.charCodeAt(n);++n);for(var a=t.length,o=a-n,s=1;s<e.length&&47===e.charCodeAt(s);++s);for(var l=e.length-s,c=o<l?o:l,u=-1,f=0;f<=c;++f){if(f===c){if(l>c){if(47===e.charCodeAt(s+f))return e.slice(s+f+1);if(0===f)return e.slice(s+f)}else o>c&&(47===t.charCodeAt(n+f)?u=f:0===f&&(u=0));break}var h=t.charCodeAt(n+f);if(h!==e.charCodeAt(s+f))break;47===h&&(u=f)}var p="";for(f=n+u+1;f<=a;++f)f!==a&&47!==t.charCodeAt(f)||(0===p.length?p+="..":p+="/..");return p.length>0?p+e.slice(s+u):(s+=u,47===e.charCodeAt(s)&&++s,e.slice(s))},_makeLong:function(t){return t},dirname:function(t){if(r(t),0===t.length)return".";for(var e=t.charCodeAt(0),n=47===e,i=-1,a=!0,o=t.length-1;o>=1;--o)if(47===(e=t.charCodeAt(o))){if(!a){i=o;break}}else a=!1;return-1===i?n?"/":".":n&&1===i?"//":t.slice(0,i)},basename:function(t,e){if(void 0!==e&&"string"!=typeof e)throw new TypeError('"ext" argument must be a string');r(t);var n,i=0,a=-1,o=!0;if(void 0!==e&&e.length>0&&e.length<=t.length){if(e.length===t.length&&e===t)return"";var s=e.length-1,l=-1;for(n=t.length-1;n>=0;--n){var c=t.charCodeAt(n);if(47===c){if(!o){i=n+1;break}}else-1===l&&(o=!1,l=n+1),s>=0&&(c===e.charCodeAt(s)?-1==--s&&(a=n):(s=-1,a=l))}return i===a?a=l:-1===a&&(a=t.length),t.slice(i,a)}for(n=t.length-1;n>=0;--n)if(47===t.charCodeAt(n)){if(!o){i=n+1;break}}else-1===a&&(o=!1,a=n+1);return-1===a?"":t.slice(i,a)},extname:function(t){r(t);for(var e=-1,n=0,i=-1,a=!0,o=0,s=t.length-1;s>=0;--s){var l=t.charCodeAt(s);if(47!==l)-1===i&&(a=!1,i=s+1),46===l?-1===e?e=s:1!==o&&(o=1):-1!==e&&(o=-1);else if(!a){n=s+1;break}}return-1===e||-1===i||0===o||1===o&&e===i-1&&e===n+1?"":t.slice(e,i)},format:function(t){if(null===t||"object"!=typeof t)throw new TypeError('The "pathObject" argument must be of type Object. Received type '+typeof t);return function(t,e){var r=e.dir||e.root,n=e.base||(e.name||"")+(e.ext||"");return r?r===e.root?r+n:r+t+n:n}("/",t)},parse:function(t){r(t);var e={root:"",dir:"",base:"",ext:"",name:""};if(0===t.length)return e;var n,i=t.charCodeAt(0),a=47===i;a?(e.root="/",n=1):n=0;for(var o=-1,s=0,l=-1,c=!0,u=t.length-1,f=0;u>=n;--u)if(47!==(i=t.charCodeAt(u)))-1===l&&(c=!1,l=u+1),46===i?-1===o?o=u:1!==f&&(f=1):-1!==o&&(f=-1);else if(!c){s=u+1;break}return-1===o||-1===l||0===f||1===f&&o===l-1&&o===s+1?-1!==l&&(e.base=e.name=0===s&&a?t.slice(1,l):t.slice(s,l)):(0===s&&a?(e.name=t.slice(1,o),e.base=t.slice(1,l)):(e.name=t.slice(s,o),e.base=t.slice(s,l)),e.ext=t.slice(o,l)),s>0?e.dir=t.slice(0,s-1):a&&(e.dir="/"),e},sep:"/",delimiter:":",win32:null,posix:null};i.posix=i,e.exports=i}).call(this)}).call(this,t("_process"))},{_process:526}],508:[function(t,e,r){(function(t){(function(){(function(){var r,n,i,a,o,s;"undefined"!=typeof performance&&null!==performance&&performance.now?e.exports=function(){return performance.now()}:"undefined"!=typeof t&&null!==t&&t.hrtime?(e.exports=function(){return(r()-o)/1e6},n=t.hrtime,a=(r=function(){var t;return 1e9*(t=n())[0]+t[1]})(),s=1e9*t.uptime(),o=a-s):Date.now?(e.exports=function(){return Date.now()-i},i=Date.now()):(e.exports=function(){return(new Date).getTime()-i},i=(new Date).getTime())}).call(this)}).call(this)}).call(this,t("_process"))},{_process:526}],509:[function(t,e,r){"use strict";e.exports=function(t){var e=t.length;if(e<32){for(var r=1,i=0;i<e;++i)for(var a=0;a<i;++a)if(t[i]<t[a])r=-r;else if(t[i]===t[a])return 0;return r}var o=n.mallocUint8(e);for(i=0;i<e;++i)o[i]=0;for(r=1,i=0;i<e;++i)if(!o[i]){var s=1;o[i]=1;for(a=t[i];a!==i;a=t[a]){if(o[a])return n.freeUint8(o),0;s+=1,o[a]=1}1&s||(r=-r)}return n.freeUint8(o),r};var n=t("typedarray-pool")},{"typedarray-pool":595}],510:[function(t,e,r){"use strict";var n=t("typedarray-pool"),i=t("invert-permutation");r.rank=function(t){var e=t.length;switch(e){case 0:case 1:return 0;case 2:return t[1]}var r,a,o,s=n.mallocUint32(e),l=n.mallocUint32(e),c=0;for(i(t,l),o=0;o<e;++o)s[o]=t[o];for(o=e-1;o>0;--o)a=l[o],r=s[o],s[o]=s[a],s[a]=r,l[o]=l[r],l[r]=a,c=(c+r)*o;return n.freeUint32(l),n.freeUint32(s),c},r.unrank=function(t,e,r){switch(t){case 0:return r||[];case 1:return r?(r[0]=0,r):[0];case 2:return r?(e?(r[0]=0,r[1]=1):(r[0]=1,r[1]=0),r):e?[0,1]:[1,0]}var n,i,a,o=1;for((r=r||new Array(t))[0]=0,a=1;a<t;++a)r[a]=a,o=o*a|0;for(a=t-1;a>0;--a)e=e-(n=e/o|0)*o|0,o=o/a|0,i=0|r[a],r[a]=0|r[n],r[n]=0|i;return r}},{"invert-permutation":462,"typedarray-pool":595}],511:[function(t,e,r){"use strict";e.exports=function(t,e,r){var n,a,o={};if("string"==typeof e&&(e=i(e)),Array.isArray(e)){var s={};for(a=0;a<e.length;a++)s[e[a]]=!0;e=s}for(n in e)e[n]=i(e[n]);var l={};for(n in e){var c=e[n];if(Array.isArray(c))for(a=0;a<c.length;a++){var u=c[a];if(r&&(l[u]=!0),u in t){if(o[n]=t[u],r)for(var f=a;f<c.length;f++)l[c[f]]=!0;break}}else n in t&&(e[n]&&(o[n]=t[n]),r&&(l[n]=!0))}if(r)for(n in t)l[n]||(o[n]=t[n]);return o};var n={};function i(t){return n[t]?n[t]:("string"==typeof t&&(t=n[t]=t.split(/\s*,\s*|\s+/)),t)}},{}],512:[function(t,e,r){"use strict";e.exports=function(t,e){for(var r=0|e.length,i=t.length,a=[new Array(r),new Array(r)],o=0;o<r;++o)a[0][o]=[],a[1][o]=[];for(o=0;o<i;++o){var s=t[o];a[0][s[0]].push(s),a[1][s[1]].push(s)}var l=[];for(o=0;o<r;++o)a[0][o].length+a[1][o].length===0&&l.push([o]);function c(t,e){var r=a[e][t[e]];r.splice(r.indexOf(t),1)}function u(t,r,i){for(var o,s,l,u=0;u<2;++u)if(a[u][r].length>0){o=a[u][r][0],l=u;break}s=o[1^l];for(var f=0;f<2;++f)for(var h=a[f][r],p=0;p<h.length;++p){var d=h[p],g=d[1^f];n(e[t],e[r],e[s],e[g])>0&&(o=d,s=g,l=f)}return i||o&&c(o,l),s}function f(t,r){var i=a[r][t][0],o=[t];c(i,r);for(var s=i[1^r];;){for(;s!==t;)o.push(s),s=u(o[o.length-2],s,!1);if(a[0][t].length+a[1][t].length===0)break;var l=o[o.length-1],f=t,h=o[1],p=u(l,f,!0);if(n(e[l],e[f],e[h],e[p])<0)break;o.push(t),s=u(l,f)}return o}function h(t,e){return e[1]===e[e.length-1]}for(o=0;o<r;++o)for(var p=0;p<2;++p){for(var d=[];a[p][o].length>0;){a[0][o].length;var g=f(o,p);h(0,g)?d.push.apply(d,g):(d.length>0&&l.push(d),d=g)}d.length>0&&l.push(d)}return l};var n=t("compare-angle")},{"compare-angle":132}],513:[function(t,e,r){"use strict";e.exports=function(t,e){for(var r=n(t,e.length),i=new Array(e.length),a=new Array(e.length),o=[],s=0;s<e.length;++s){var l=r[s].length;a[s]=l,i[s]=!0,l<=1&&o.push(s)}for(;o.length>0;){var c=o.pop();i[c]=!1;var u=r[c];for(s=0;s<u.length;++s){var f=u[s];0==--a[f]&&o.push(f)}}var h=new Array(e.length),p=[];for(s=0;s<e.length;++s)if(i[s]){c=p.length;h[s]=c,p.push(e[s])}else h[s]=-1;var d=[];for(s=0;s<t.length;++s){var g=t[s];i[g[0]]&&i[g[1]]&&d.push([h[g[0]],h[g[1]]])}return[d,p]};var n=t("edges-to-adjacency-list")},{"edges-to-adjacency-list":178}],514:[function(t,e,r){"use strict";e.exports=function(t,e){var r=c(t,e);t=r[0];for(var f=(e=r[1]).length,h=(t.length,n(t,e.length)),p=0;p<f;++p)if(h[p].length%2==1)throw new Error("planar-graph-to-polyline: graph must be manifold");var d=i(t,e);var g=(d=d.filter((function(t){for(var r=t.length,n=[0],i=0;i<r;++i){var a=e[t[i]],l=e[t[(i+1)%r]],c=o(-a[0],a[1]),u=o(-a[0],l[1]),f=o(l[0],a[1]),h=o(l[0],l[1]);n=s(n,s(s(c,u),s(f,h)))}return n[n.length-1]>0}))).length,m=new Array(g),v=new Array(g);for(p=0;p<g;++p){m[p]=p;var y=new Array(g),x=d[p].map((function(t){return e[t]})),b=a([x]),_=0;t:for(var w=0;w<g;++w)if(y[w]=0,p!==w){for(var T=(q=d[w]).length,k=0;k<T;++k){var M=b(e[q[k]]);if(0!==M){M<0&&(y[w]=1,_+=1);continue t}}y[w]=1,_+=1}v[p]=[_,p,y]}v.sort((function(t,e){return e[0]-t[0]}));for(p=0;p<g;++p){var A=(y=v[p])[1],S=y[2];for(w=0;w<g;++w)S[w]&&(m[w]=A)}var E=function(t){for(var e=new Array(t),r=0;r<t;++r)e[r]=[];return e}(g);for(p=0;p<g;++p)E[p].push(m[p]),E[m[p]].push(p);var C={},L=u(f,!1);for(p=0;p<g;++p)for(T=(q=d[p]).length,w=0;w<T;++w){var I=q[w],P=q[(w+1)%T],z=Math.min(I,P)+":"+Math.max(I,P);if(z in C){var O=C[z];E[O].push(p),E[p].push(O),L[I]=L[P]=!0}else C[z]=p}function D(t){for(var e=t.length,r=0;r<e;++r)if(!L[t[r]])return!1;return!0}var R=[],F=u(g,-1);for(p=0;p<g;++p)m[p]!==p||D(d[p])?F[p]=-1:(R.push(p),F[p]=0);r=[];for(;R.length>0;){var B=R.pop(),N=E[B];l(N,(function(t,e){return t-e}));var j,U=N.length,V=F[B];if(0===V){var q=d[B];j=[q]}for(p=0;p<U;++p){var H=N[p];if(!(F[H]>=0))if(F[H]=1^V,R.push(H),0===V)D(q=d[H])||(q.reverse(),j.push(q))}0===V&&r.push(j)}return r};var n=t("edges-to-adjacency-list"),i=t("planar-dual"),a=t("point-in-big-polygon"),o=t("two-product"),s=t("robust-sum"),l=t("uniq"),c=t("./lib/trim-leaves");function u(t,e){for(var r=new Array(t),n=0;n<t;++n)r[n]=e;return r}},{"./lib/trim-leaves":513,"edges-to-adjacency-list":178,"planar-dual":512,"point-in-big-polygon":516,"robust-sum":553,"two-product":582,uniq:597}],515:[function(t,e,r){arguments[4][243][0].apply(r,arguments)},{dup:243}],516:[function(t,e,r){e.exports=function(t){for(var e=t.length,r=[],a=[],s=0;s<e;++s)for(var u=t[s],f=u.length,h=f-1,p=0;p<f;h=p++){var d=u[h],g=u[p];d[0]===g[0]?a.push([d,g]):r.push([d,g])}if(0===r.length)return 0===a.length?c:(m=l(a),function(t){return m(t[0],t[1])?0:1});var m;var v=i(r),y=function(t,e){return function(r){var i=o.le(e,r[0]);if(i<0)return 1;var a=t[i];if(!a){if(!(i>0&&e[i]===r[0]))return 1;a=t[i-1]}for(var s=1;a;){var l=a.key,c=n(r,l[0],l[1]);if(l[0][0]<l[1][0])if(c<0)a=a.left;else{if(!(c>0))return 0;s=-1,a=a.right}else if(c>0)a=a.left;else{if(!(c<0))return 0;s=1,a=a.right}}return s}}(v.slabs,v.coordinates);return 0===a.length?y:function(t,e){return function(r){return t(r[0],r[1])?0:e(r)}}(l(a),y)};var n=t("robust-orientation")[3],i=t("slab-decomposition"),a=t("interval-tree-1d"),o=t("binary-search-bounds");function s(){return!0}function l(t){for(var e={},r=0;r<t.length;++r){var n=t[r],i=n[0][0],o=n[0][1],l=n[1][1],c=[Math.min(o,l),Math.max(o,l)];i in e?e[i].push(c):e[i]=[c]}var u={},f=Object.keys(e);for(r=0;r<f.length;++r){var h=e[f[r]];u[f[r]]=a(h)}return function(t){return function(e,r){var n=t[e];return!!n&&!!n.queryPoint(r,s)}}(u)}function c(t){return 1}},{"binary-search-bounds":515,"interval-tree-1d":460,"robust-orientation":548,"slab-decomposition":565}],517:[function(t,e,r){
/*
 * @copyright 2016 Sean Connelly (@voidqk), http://syntheti.cc
 * @license MIT
 * @preserve Project Home: https://github.com/voidqk/polybooljs
 */
/*!
 * repeat-string <https://github.com/jonschlinkert/repeat-string>
 *
 * Copyright (c) 2014-2015, Jon Schlinkert.
 * Licensed under the MIT License.
 */
        });
        require(['plotly'], function(Plotly) {
            window._Plotly = Plotly;
        });
        }
        </script>




<div>                            <div id="08736711-e694-482a-9357-d4e3d6237dd7" class="plotly-graph-div" style="height:525px; width:100%;"></div>            <script type="text/javascript">                require(["plotly"], function(Plotly) {                    window.PLOTLYENV=window.PLOTLYENV || {};                                    if (document.getElementById("08736711-e694-482a-9357-d4e3d6237dd7")) {                    Plotly.newPlot(                        "08736711-e694-482a-9357-d4e3d6237dd7",                        [{"close": [25859.36428638706, 25948.197964470794, 25749.106735136127, 25753.95929850106, 25725.087827734977, 26387.74791739874, 25905.63785593694, 25900.10190570366, 25857.257728995824, 25140.138898899415, 25979.21538462445, 26234.18982796697, 26615.532123428224, 26792.60882462043, 26566.033844441456, 26468.617801591503, 26867.0605755984, 27200.83584839815, 27110.600552890646, 26589.232106802505, 26582.589416632578, 26575.52911690974, 26503.235602590674, 26287.076366997982, 26151.495531909033, 26288.209341200014, 27013.05810967051, 26896.650032793077, 27007.09435594733, 27958.086080312773, 28301.572097802455], "high": [25898.432073032756, 26054.793419062265, 25998.296229842043, 25829.364772941324, 25835.942668563916, 26387.74791739874, 26355.95434081812, 25907.292127847395, 25889.67163888094, 25836.14289431529, 26288.334884466993, 26304.01546518303, 26751.79664567292, 26792.60882462043, 26704.25388242849, 26605.36747233914, 27394.588104693972, 27289.4248902988, 27318.242557709546, 27115.846446970816, 26688.33796153136, 26615.098925655053, 26657.753582685626, 26357.55015326377, 26347.306498337617, 26805.628892226956, 27146.515346023432, 27151.16450461917, 27075.965613822682, 27958.086080312773, 28301.572097802455], "low": [25791.936056022405, 25836.905638144235, 25659.620573078173, 25652.30731623389, 25576.564268541297, 25647.715450955635, 25764.72345705586, 25813.384607397376, 25682.08207006774, 25023.24918499984, 25133.303106566527, 25843.107804557887, 26193.031945995655, 26251.615685201057, 26471.09371981062, 26462.58323203275, 26456.81769925053, 26682.841448803098, 26936.571052710085, 26418.52778477277, 26534.177936540287, 26536.561163334205, 26447.45930249158, 26059.043074839537, 26111.574712349553, 26166.382102431195, 26344.99309446877, 26836.0656620818, 26895.989846752356, 26969.876144072576, 27902.79035419223], "open": [25794.334274999826, 25853.65684277757, 25959.596311463454, 25829.364772941324, 25770.129054916044, 25752.958418589413, 26192.333433090567, 25907.228137249735, 25889.67163888094, 25834.8856281802, 25133.303106566527, 25850.322299629544, 26222.013303986474, 26531.39556626326, 26610.403126161622, 26557.768691994646, 26520.988254783886, 26741.461110948952, 27213.18465907596, 27115.846446970816, 26561.133454198716, 26581.967576018324, 26573.9234797301, 26257.58376993293, 26296.92231737691, 26204.75759083597, 26350.146895428057, 27009.01375072488, 26917.199101637976, 26969.876144072576, 27967.510579087113], "type": "candlestick", "x": ["2023-09-02", "2023-09-03", "2023-09-04", "2023-09-05", "2023-09-06", "2023-09-07", "2023-09-08", "2023-09-09", "2023-09-10", "2023-09-11", "2023-09-12", "2023-09-13", "2023-09-14", "2023-09-15", "2023-09-16", "2023-09-17", "2023-09-18", "2023-09-19", "2023-09-20", "2023-09-21", "2023-09-22", "2023-09-23", "2023-09-24", "2023-09-25", "2023-09-26", "2023-09-27", "2023-09-28", "2023-09-29", "2023-09-30", "2023-10-01", "2023-10-02"]}],                        {"template": {"data": {"bar": [{"error_x": {"color": "#2a3f5f"}, "error_y": {"color": "#2a3f5f"}, "marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "bar"}], "barpolar": [{"marker": {"line": {"color": "#E5ECF6", "width": 0.5}}, "type": "barpolar"}], "carpet": [{"aaxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "baxis": {"endlinecolor": "#2a3f5f", "gridcolor": "white", "linecolor": "white", "minorgridcolor": "white", "startlinecolor": "#2a3f5f"}, "type": "carpet"}], "choropleth": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "choropleth"}], "contour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "contour"}], "contourcarpet": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "contourcarpet"}], "heatmap": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmap"}], "heatmapgl": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "heatmapgl"}], "histogram": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "histogram"}], "histogram2d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2d"}], "histogram2dcontour": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "histogram2dcontour"}], "mesh3d": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "type": "mesh3d"}], "parcoords": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "parcoords"}], "pie": [{"automargin": true, "type": "pie"}], "scatter": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter"}], "scatter3d": [{"line": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatter3d"}], "scattercarpet": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattercarpet"}], "scattergeo": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergeo"}], "scattergl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattergl"}], "scattermapbox": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scattermapbox"}], "scatterpolar": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolar"}], "scatterpolargl": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterpolargl"}], "scatterternary": [{"marker": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "type": "scatterternary"}], "surface": [{"colorbar": {"outlinewidth": 0, "ticks": ""}, "colorscale": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "type": "surface"}], "table": [{"cells": {"fill": {"color": "#EBF0F8"}, "line": {"color": "white"}}, "header": {"fill": {"color": "#C8D4E3"}, "line": {"color": "white"}}, "type": "table"}]}, "layout": {"annotationdefaults": {"arrowcolor": "#2a3f5f", "arrowhead": 0, "arrowwidth": 1}, "autotypenumbers": "strict", "coloraxis": {"colorbar": {"outlinewidth": 0, "ticks": ""}}, "colorscale": {"diverging": [[0, "#8e0152"], [0.1, "#c51b7d"], [0.2, "#de77ae"], [0.3, "#f1b6da"], [0.4, "#fde0ef"], [0.5, "#f7f7f7"], [0.6, "#e6f5d0"], [0.7, "#b8e186"], [0.8, "#7fbc41"], [0.9, "#4d9221"], [1, "#276419"]], "sequential": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]], "sequentialminus": [[0.0, "#0d0887"], [0.1111111111111111, "#46039f"], [0.2222222222222222, "#7201a8"], [0.3333333333333333, "#9c179e"], [0.4444444444444444, "#bd3786"], [0.5555555555555556, "#d8576b"], [0.6666666666666666, "#ed7953"], [0.7777777777777778, "#fb9f3a"], [0.8888888888888888, "#fdca26"], [1.0, "#f0f921"]]}, "colorway": ["#636efa", "#EF553B", "#00cc96", "#ab63fa", "#FFA15A", "#19d3f3", "#FF6692", "#B6E880", "#FF97FF", "#FECB52"], "font": {"color": "#2a3f5f"}, "geo": {"bgcolor": "white", "lakecolor": "white", "landcolor": "#E5ECF6", "showlakes": true, "showland": true, "subunitcolor": "white"}, "hoverlabel": {"align": "left"}, "hovermode": "closest", "mapbox": {"style": "light"}, "paper_bgcolor": "white", "plot_bgcolor": "#E5ECF6", "polar": {"angularaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "radialaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "scene": {"xaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "yaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}, "zaxis": {"backgroundcolor": "#E5ECF6", "gridcolor": "white", "gridwidth": 2, "linecolor": "white", "showbackground": true, "ticks": "", "zerolinecolor": "white"}}, "shapedefaults": {"line": {"color": "#2a3f5f"}}, "ternary": {"aaxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "baxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}, "bgcolor": "#E5ECF6", "caxis": {"gridcolor": "white", "linecolor": "white", "ticks": ""}}, "title": {"x": 0.05}, "xaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}, "yaxis": {"automargin": true, "gridcolor": "white", "linecolor": "white", "ticks": "", "title": {"standoff": 15}, "zerolinecolor": "white", "zerolinewidth": 2}}}, "title": {"text": "Bitcoin Candlestick Chart Over Past 30 Days"}, "xaxis": {"rangeslider": {"visible": false}, "title": {"text": "Date"}}, "yaxis": {"title": {"text": "Price (USD $)"}}},                        {"responsive": true}                    ).then(function(){

var gd = document.getElementById('08736711-e694-482a-9357-d4e3d6237dd7');
var x = new MutationObserver(function (mutations, observer) {{
        var display = window.getComputedStyle(gd).display;
        if (!display || display === 'none') {{
            console.log([gd, 'removed!']);
            Plotly.purge(gd);
            observer.disconnect();
        }}
}});

// Listen for the removal of the full notebook cells
var notebookContainer = gd.closest('#notebook-container');
if (notebookContainer) {{
    x.observe(notebookContainer, {childList: true});
}}

// Listen for the clearing of the current output cell
var outputEl = gd.closest('.output');
if (outputEl) {{
    x.observe(outputEl, {childList: true});
}}

                        })                };                });            </script>        </div>


**Watson Speech to Text API**  
(Note this may fail if API has been deleted from IBM Cloud accoint)  


```python
#install require library 

!pip install PyJWT==1.7.1 ibm_watson wget
```

    Collecting PyJWT==1.7.1
      Using cached PyJWT-1.7.1-py2.py3-none-any.whl (18 kB)
    Requirement already satisfied: ibm_watson in c:\users\ajdpi\anaconda3\lib\site-packages (5.0.2)
    Requirement already satisfied: wget in c:\users\ajdpi\anaconda3\lib\site-packages (3.2)
    Requirement already satisfied: websocket-client==0.48.0 in c:\users\ajdpi\anaconda3\lib\site-packages (from ibm_watson) (0.48.0)
    Requirement already satisfied: requests<3.0,>=2.0 in c:\users\ajdpi\anaconda3\lib\site-packages (from ibm_watson) (2.26.0)
    Requirement already satisfied: python-dateutil>=2.5.3 in c:\users\ajdpi\anaconda3\lib\site-packages (from ibm_watson) (2.8.2)
    Requirement already satisfied: ibm-cloud-sdk-core==1.7.3 in c:\users\ajdpi\anaconda3\lib\site-packages (from ibm_watson) (1.7.3)
    Requirement already satisfied: six in c:\users\ajdpi\anaconda3\lib\site-packages (from websocket-client==0.48.0->ibm_watson) (1.16.0)
    Requirement already satisfied: idna<4,>=2.5 in c:\users\ajdpi\anaconda3\lib\site-packages (from requests<3.0,>=2.0->ibm_watson) (3.2)
    Requirement already satisfied: certifi>=2017.4.17 in c:\users\ajdpi\anaconda3\lib\site-packages (from requests<3.0,>=2.0->ibm_watson) (2021.10.8)
    Requirement already satisfied: urllib3<1.27,>=1.21.1 in c:\users\ajdpi\anaconda3\lib\site-packages (from requests<3.0,>=2.0->ibm_watson) (1.26.7)
    Requirement already satisfied: charset-normalizer~=2.0.0 in c:\users\ajdpi\anaconda3\lib\site-packages (from requests<3.0,>=2.0->ibm_watson) (2.0.4)
    Installing collected packages: PyJWT
      Attempting uninstall: PyJWT
        Found existing installation: PyJWT 2.1.0
        Uninstalling PyJWT-2.1.0:
          Successfully uninstalled PyJWT-2.1.0
    Successfully installed PyJWT-1.7.1
    


```python
# import SpeechToTextV1 from ibm_watson

from ibm_watson import SpeechToTextV1 
import json
from ibm_cloud_sdk_core.authenticators import IAMAuthenticator
```


```python
# The service endpoint is based on the location of the service 
# instance, we store the information in the variable URL
# URL is obtained from IBM cloud services Speech to Text

url_s2t = "https://api.eu-gb.speech-to-text.watson.cloud.ibm.com/instances/da244606-73f7-4718-8c1c-2c5466754e50"
```


```python
# a key is required for the service, this is essentially a password for the API service

iam_apikey_s2t = "p9l8ngfN9jLWN3F_j7yayZroRXEN-d0QMLIhbVKKTpGC"
```


```python
# create a Speech to Text Adapter object

authenticator = IAMAuthenticator(iam_apikey_s2t)
s2t = SpeechToTextV1(authenticator=authenticator)
s2t.set_service_url(url_s2t)
s2t
```




    <ibm_watson.speech_to_text_v1_adapter.SpeechToTextV1Adapter at 0x19ab7fdfcd0>




```python
# install package to be able to use wget when running jupyter through anaconda

!conda install -c anaconda wget
```

    Collecting package metadata (current_repodata.json): ...working... done
    Solving environment: ...working... failed with initial frozen solve. Retrying with flexible solve.
    Collecting package metadata (repodata.json): ...working... done
    Solving environment: ...working... failed with initial frozen solve. Retrying with flexible solve.
    

    
    PackagesNotFoundError: The following packages are not available from current channels:
    
      - wget
      - as
    
    Current channels:
    
      - https://conda.anaconda.org/anaconda/win-64
      - https://conda.anaconda.org/anaconda/noarch
      - https://repo.anaconda.com/pkgs/main/win-64
      - https://repo.anaconda.com/pkgs/main/noarch
      - https://repo.anaconda.com/pkgs/r/win-64
      - https://repo.anaconda.com/pkgs/r/noarch
      - https://repo.anaconda.com/pkgs/msys2/win-64
      - https://repo.anaconda.com/pkgs/msys2/noarch
    
    To search for alternate channels that may provide the conda package you're
    looking for, navigate to
    
        https://anaconda.org
    
    and use the search bar at the top of the page.
    
    
    


```python
# download audio file to use to convert to text

# -O outputs to specified document and will overwrite 
# exsiting if run multipul times

!wget -O PolynomialRegressionandPipelines.mp3 https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%205/data/PolynomialRegressionandPipelines.mp3
```

    'wget' is not recognized as an internal or external command,
    operable program or batch file.
    


```python
# assign path of file we want to convert to text to variable

filename='PolynomialRegressionandPipelines.mp3'
```


```python
# create file object 'wav' and open in binary mode
# use method 'recognize' to return recognized text
# parameter 'audio' is the file object
# parameter ' content_type' is format of file

with open(filename, mode="rb")  as wav:
    response = s2t.recognize(audio=wav, content_type='audio/mp3')
```


    ---------------------------------------------------------------------------

    FileNotFoundError                         Traceback (most recent call last)

    ~\AppData\Local\Temp/ipykernel_3300/3508802217.py in <module>
          4 # parameter ' content_type' is format of file
          5 
    ----> 6 with open(filename, mode="rb")  as wav:
          7     response = s2t.recognize(audio=wav, content_type='audio/mp3')
    

    FileNotFoundError: [Errno 2] No such file or directory: 'PolynomialRegressionandPipelines.mp3'



```python
# attribute 'result' contains a dictionary with the recognized text

response.result
```


```python
# normalize semi-structured JSON data into a flat table

pd.json_normalize(response.result['results'],"alternatives")
```


```python
# obtain recognized text and assign to variable

recognized_text=response.result['results'][0]["alternatives"][0]["transcript"]
type(recognized_text)
```


```python
recognized_text
```

**Watson Language Translator**
(Note this may fail if API has been deleted from IBM Cloud accoint)


```python
# import 'LanguageTranslatorV3' from ibm_watson library

from ibm_watson import LanguageTranslatorV3
```


```python
# The service endpoint is based on the location of the service 
# instance, we store the information in the variable URL

url_lt='https://api.eu-gb.language-translator.watson.cloud.ibm.com/instances/81c2ebf3-d09f-41f5-85fa-68260a27bac0'
```


```python
# a key is required for the service, this is essentially a password for the API service

apikey_lt='D1479Mx2sctIc6L_8EAO7jCBUe2tzRSzNtnqqeaHwq4q'
```


```python
# API requests require a version parameter that takes a date in the format version=YYYY-MM-DD

version_lt='2018-05-01'
```


```python
# create a Language Translator object 'language_translator'

authenticator = IAMAuthenticator(apikey_lt)
language_translator = LanguageTranslatorV3(version=version_lt,authenticator=authenticator)
language_translator.set_service_url(url_lt)
language_translator
```


```python
# get a Lists the languages that the service can identify. The method Returns the language codes

pd.json_normalize(language_translator.list_identifiable_languages().get_result(), "languages")
```


```python
# method translate this will translate the text

# parameter text is the text, model_id is the type of model we 
# would like to use, here set to 'en-es' or English to Spanish

# we get a detailed response object 'translation_response'

translation_response = language_translator.translate(text=recognized_text, model_id='en-es')
translation_response
```


```python
# The 'result' is a dictionary

translation = translation_response.get_result()
translation
```


```python
# can obtain the actual translation as a string

spanish_translation =translation['translations'][0]['translation']
spanish_translation 
```


```python
# can translate back to English

translation_new = language_translator.translate(text=spanish_translation ,model_id='es-en').get_result()
```


```python
# obtain string from dictionary

translation_eng=translation_new['translations'][0]['translation']
translation_eng
```

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)

---

**HTTP protocol**:
* General protocal for transferring information through the web  
* Rest APIs communicate via HTTP messages which usually contain a JSON file  
* When a client uses a webpage, browser sends a HTTP request to server and the server will try to find the desired resource, by default this will be index.html. If request is successful, the server will send the object to the client in a HTTP response. This will include type of resource, length of resource and other info  
* URL **Uniform Resource Locator** is one of the most popular ways to find resources on the web. This can be broken into 3 parts:
    1.  **Scheme** - This is the protocol, e.g. **`http://`**  
    2.  **Internet address or Base URL** - Used to find the location of web server, e.g. **`www.webaddress.com`**  
    3.  **Route** - Location on the web server, e.g. **`/images/IDSNlogo.png`**  

---

## <center>Notes;</center>


```python

```


```python

```


```python

```


```python

```


```python

```

[<p style="text-align: right;">**⬆ Table of Contents ⬆**</p>](#Python-Basics!)


```python

```