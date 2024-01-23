# Python

```python
print("hello world ")
```

## Indentation

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Indentation refers to the spaces at the beginning of a code line.Where in other programming languages the indentation in code is for readability only, the indentation in Python is very important.</span>

## <span>Comments</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Comments starts with a </span>`#`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">, and Python will ignore them:</span>

```python
#This is a comment
print("Hello, World!")
```

### <span style="font-size: 17px">Multiline Comments</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">you can add a multiline string (triple quotes) in your code, and place your comment inside it:</span>

```python
"""
This is a comment
written in
more than just one line
"""
print("Hello, World!")
```

## <span>Variables</span>

### Creating Variables

<span style="font-size: 15px">Python has no command for declaring a variable.A variable is created the moment you first assign a value to it.</span>

```python
x = 4       # x is of type int
x = "Sally" # x is now of type str
print(x)
```

### Casting

<span style="font-size: 15px">Specify the data type of a variable, this can be done with casting.</span>

```python
x = str(3)    # x will be '3'
y = int(3)    # y will be 3
z = float(3)  # z will be 3.0
```

### Get the Type

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Get the data type of a variable with the </span>`type()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> function.</span>

```python
x = 5
y = "John"
print(type(x))
print(type(y))
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">String variables can be declared either by using single or double quotes & Variable names are case-sensitive</span>

### Variable Names :

- <span style="font-size: 15px">A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and \_ )</span>
- <span style="font-size: 15px">A variable name must start with a letter or the underscore character</span>
- <span style="font-size: 15px">A variable name cannot start with a number & </span><span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">variable names are case-sensitive</span>

```python
# illegal Variable Names
2myvar = "John"
my-var = "John"
my var = "John"
```

### <span>Assign Multiple Values :</span>

<span style="font-size: 15px">Python allows you to assign values to multiple variables in one line:</span>

```python
x, y, z = "Orange", "Banana", "Cherry"
print(x)
print(y)
print(z)
```

### Unpack a Collection

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">If you have a collection of values in a list, tuple etc. Python allows you to extract the values into variables. This is called </span>*unpacking*<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">.</span>

```python
fruits = ["apple", "banana", "cherry"]
x, y, z = fruits
print(x)
print(y)
print(z)
```

### Output Variables :

`print()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> function, you output multiple variables, separated by a comma,You can also use the </span>`+`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> operator to output multiple variables.</span>

```python
x = "Python"
y = "is"
z = "awesome"
print(x, y, z)  #Output: Python is awesome

x = "Python "
y = "is "
z = "awesome"
print(x + y + z)  #Output: Pythonisawesome
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">For numbers, the </span>`+`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> character works as a mathematical operator:</span> 

```python
x = 5
y = 10
print(x + y)  #Output: 15
```

```python
x = 5
y = "John" 
print(x, y)  #Output: 5 John (Concatenation)
```

```python
x = 5
y = "John"
print(x + y) #Output: error (since x is a int and y is a string)
```

### Global Variables

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Variables that are created outside of a function are known as global,Global variables can be used by everyone, both inside of functions and outside.</span>

```python
x = "awesome"

def myfunc():
  print("Python is " + x)

myfunc()
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">If you create a variable with the same name inside a function, this variable will be local, and can only be used inside the function. The global variable with the same name will remain as it was, global and with the original value.</span>

```python
x = "awesome"

def myfunc():
  x = "fantastic"
  print("Python is " + x)

myfunc()                   #Output: Python is fantatastic
print("Python is " + x)    #Output: Python is awesome
```

#### <span style="font-size: 15px">global Keyword :</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To create a global variable inside a function, you can use the </span>`global`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> keyword.</span>

```python
def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
```

---

## <span>Data Types</span>

### Built-in Data Types

<table>
<tbody><tr><td colspan="1" rowspan="1"><p>Text Type:</p></td><td colspan="1" rowspan="1"><p><code class="hljs" spellcheck="false">str</code></p></td></tr><tr><td colspan="1" rowspan="1"><p>Numeric Types:</p></td><td colspan="1" rowspan="1"><p><code class="hljs" spellcheck="false">int</code>, <code class="hljs" spellcheck="false">float</code>, <code class="hljs" spellcheck="false">complex</code></p></td></tr><tr><td colspan="1" rowspan="1"><p>Sequence Types:</p></td><td colspan="1" rowspan="1"><p><code class="hljs" spellcheck="false">list</code>, <code class="hljs" spellcheck="false">tuple</code>, <code class="hljs" spellcheck="false">range</code></p></td></tr><tr><td colspan="1" rowspan="1"><p>Mapping Type:</p></td><td colspan="1" rowspan="1"><p><code class="hljs" spellcheck="false">dict</code></p></td></tr><tr><td colspan="1" rowspan="1"><p>Set Types:</p></td><td colspan="1" rowspan="1"><p><code class="hljs" spellcheck="false">set</code>, <code class="hljs" spellcheck="false">frozenset</code></p></td></tr><tr><td colspan="1" rowspan="1"><p>Boolean Type:</p></td><td colspan="1" rowspan="1"><p><code class="hljs" spellcheck="false">bool</code></p></td></tr><tr><td colspan="1" rowspan="1"><p>Binary Types:</p></td><td colspan="1" rowspan="1"><p><code class="hljs" spellcheck="false">bytes</code>, <code class="hljs" spellcheck="false">bytearray</code>, <code class="hljs" spellcheck="false">memoryview</code></p></td></tr><tr><td colspan="1" rowspan="1"><p>None Type:</p></td><td colspan="1" rowspan="1"><p><code class="hljs" spellcheck="false">NoneType</code></p></td></tr></tbody>
</table>

### <span style="font-size: 19px">Numbers</span>

```python
x = 1    # int
y = 2.8  # float
z = 1j   # complex
```

**<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Int</span>**<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">, or integer, is a whole number, positive or negative, without decimals, of unlimited length.</span>

**<span style="font-size: 15px">Float</span>**<span style="font-size: 15px">, or "floating point number" is a number, positive or negative, containing one or more decimals.</span>

**<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Complex</span>** <span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">numbers are written with a "j" as the imaginary part:</span>

#### <span style="font-size: 17px">Random Number:</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Python does not have a </span>`random()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> function to make a random number, but Python has a built-in module called </span>`random`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> that can be used to make random numbers.</span>

```
import random

print(random.randrange(1, 10))
```

**Specify a Variable Type :**

```python
x = int(1)   # x will be 1
y = int(2.8) # y will be 2
z = int("3") # z will be 3
w = float("4.2") # w will be 4.2
y = float(2.8)   # y will be 2.8
z = str(3.0)  # z will be '3.0'
```

---

### <span style="font-size: 19px">Strings</span>

#### <span style="font-size: 15px">Strings are Arrays : </span>

<span style="font-size: 15px">Strings in Python are arrays of bytes representing unicode characters.</span><span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Square brackets can be used to access elements of the string.</span>

```python
a = "Hello, World!"
print(a[1])   #Output: e
```

#### <span style="font-size: 15px">String Length :</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To get the length of a string, use the </span>`len()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> function.</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To</span> **<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">check</span>** <span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">if a certain phrase or character is </span>**<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">present in a string</span>**<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">, we can use the keyword </span>`in`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">.</span>

```python
txt = "The best things in life are free!"
print("free" in txt)
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To </span>**<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">check</span>**<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> if a certain phrase or character is </span>**<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">NOT present in a string</span>**<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">, we can use the keyword </span>`not in`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">.</span>

```python
txt = "The best things in life are free!"
print("expensive" not in txt)
```

#### <span style="font-size: 17px">Slicing :</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Return a range of characters by using the slice syntax,</span><span style="font-size: 15px">Specify the start index and the end index, separated by a colon, to return a part of the string.</span>

```python
#characters from position 2 to position 5 (not included)
b = "Hello, World!"
print(b[2:5]) 
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">By leaving out the start index, the range will start at the first character:</span>

```python
b = "Hello, World!"
print(b[:5])
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">By leaving out the </span>*end* <span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">index, the range will go to the end:</span>

```python
b = "Hello, World!"
print(b[2:])
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Use negative indexes to start the slice from the end of the string</span>

```python
b = "Hello, World!"
print(b[-5:-2])  #Output: orl
```

#### <span style="font-size: 17px">Upper Case :</span>

<span style="font-size: 17px"> </span><span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`upper()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method returns the string in upper case</span>

```python
a = "Hello, World!"
print(a.upper())
```

#### <span style="font-size: 17px">Lower Case :</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`lower()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method returns the string in lower case:</span>

```python
a = "Hello, World!"
print(a.lower())
```

#### <span style="font-size: 17px">Remove Whitespace :</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`strip()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method removes any whitespace from the beginning or the end:</span>

```python
a = " Hello, World! "
print(a.strip()) # returns "Hello, World!"
```

#### <span style="font-size: 17px">Replace String :</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`replace()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method replaces a string with another string</span>

```python
a = "Hello, World!"
print(a.replace("H", "J"))
```

#### <span style="font-size: 17px">Split String :</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`split()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method returns a list where the text between the specified separator becomes the list items.</span>

```python
a = "Hello, World!"
print(a.split(",")) # returns ['Hello', ' World!']
```

#### <span style="font-size: 17px">String Format:</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">We can combine strings and numbers by using the </span>`format()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method,The </span>`format()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method takes the passed arguments, formats them, and places them in the string where the placeholders </span>`{}`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> are:</span>

```python
age = 36
txt = "My name is John, and I am {}"
print(txt.format(age))

quantity = 3
itemno = 567
price = 49.95
myorder = "I want {} pieces of item {} for {} dollars."
print(myorder.format(quantity, itemno, price))
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">You can use index numbers </span>`{0}`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> to be sure the arguments are placed in the correct placeholders</span>

```python
quantity = 3
itemno = 567
price = 49.95
myorder = "I want to pay {2} dollars for {0} pieces of item {1}."
print(myorder.format(quantity, itemno, price))
```

#### <span style="font-size: 17px">Escape Character :</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">An escape character is a backslash </span>`\`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> followed by the character you want to insert</span>

```python
txt = "We are the so-called \"Vikings\" from the north."
```

<table>
<tbody><tr><th colspan="1" rowspan="1"><p>Code</p></th><th colspan="1" rowspan="1"><p>Result</p></th><th colspan="1" rowspan="1"><p></p></th></tr><tr><td colspan="1" rowspan="1"><p>\'</p></td><td colspan="1" rowspan="1"><p>Single Quote</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>\\</p></td><td colspan="1" rowspan="1"><p>Backslash</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>\n</p></td><td colspan="1" rowspan="1"><p>New Line</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>\r</p></td><td colspan="1" rowspan="1"><p>Carriage Return</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>\t</p></td><td colspan="1" rowspan="1"><p>Tab</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>\b</p></td><td colspan="1" rowspan="1"><p>Backspace</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>\f</p></td><td colspan="1" rowspan="1"><p>Form Feed</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>\ooo</p></td><td colspan="1" rowspan="1"><p>Octal value</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>\xhh</p></td><td colspan="1" rowspan="1"><p>Hex value</p></td><td colspan="1" rowspan="1"><p></p></td></tr></tbody>
</table>

---

### <span style="font-size: 21px">Booleans</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">You can evaluate any expression in Python, and get one of two answers, </span>`True`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> or </span>`False`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">.</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">When you compare two values, the expression is evaluated and Python returns the Boolean answer.</span>

```python
x = "Hello"
y = 15
print(bool(x))  #true
print(bool(y))  #true
```

<span style="font-size: 15px">The following will return False:</span>

```python
bool(False)
bool(None)
bool(0)
bool("")
bool(())
bool([])
bool({})
```

---

## <span>Operators :</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Operators are used to perform operations on variables and values.</span>

<table>
<tbody><tr><td colspan="1" rowspan="1"><p>+</p></td><td colspan="1" rowspan="1"><p>Addition</p></td><td colspan="1" rowspan="1"><p>x + y</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>-</p></td><td colspan="1" rowspan="1"><p>Subtraction</p></td><td colspan="1" rowspan="1"><p>x - y</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>*</p></td><td colspan="1" rowspan="1"><p>Multiplication</p></td><td colspan="1" rowspan="1"><p>x * y</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>/</p></td><td colspan="1" rowspan="1"><p>Division</p></td><td colspan="1" rowspan="1"><p>x / y</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>%</p></td><td colspan="1" rowspan="1"><p>Modulus</p></td><td colspan="1" rowspan="1"><p>x % y</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>**</p></td><td colspan="1" rowspan="1"><p>Exponentiation</p></td><td colspan="1" rowspan="1"><p>x ** y</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>//</p></td><td colspan="1" rowspan="1"><p>Floor division</p></td><td colspan="1" rowspan="1"><p>x // y</p></td><td colspan="1" rowspan="1"><p></p></td></tr></tbody>
</table>

#### <span style="font-size: 17px">Comparison Operators</span>

<table>
<tbody><tr><td colspan="1" rowspan="1"><p>==</p></td><td colspan="1" rowspan="1"><p>Equal</p></td><td colspan="1" rowspan="1"><p>x == y</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>!=</p></td><td colspan="1" rowspan="1"><p>Not equal</p></td><td colspan="1" rowspan="1"><p>x != y</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>&gt;</p></td><td colspan="1" rowspan="1"><p>Greater than</p></td><td colspan="1" rowspan="1"><p>x &gt; y</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>&lt;</p></td><td colspan="1" rowspan="1"><p>Less than</p></td><td colspan="1" rowspan="1"><p>x &lt; y</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>&gt;=</p></td><td colspan="1" rowspan="1"><p>Greater than or equal to</p></td><td colspan="1" rowspan="1"><p>x &gt;= y</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>&lt;=</p></td><td colspan="1" rowspan="1"><p>Less than or equal to</p></td><td colspan="1" rowspan="1"><p>x &lt;= y</p></td><td colspan="1" rowspan="1"><p></p></td></tr></tbody>
</table>

#### <span style="font-size: 17px">Logical Operators</span>

<table>
<tbody><tr><th colspan="1" rowspan="1"><p>Operator</p></th><th colspan="1" rowspan="1"><p>Description</p></th><th colspan="1" rowspan="1"><p>Example</p></th><th colspan="1" rowspan="1"><p></p></th></tr><tr><td colspan="1" rowspan="1"><p>and&nbsp;</p></td><td colspan="1" rowspan="1"><p>Returns True if both statements are true</p></td><td colspan="1" rowspan="1"><p>x &lt; 5 and&nbsp; x &lt; 10</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>or</p></td><td colspan="1" rowspan="1"><p>Returns True if one of the statements is true</p></td><td colspan="1" rowspan="1"><p>x &lt; 5 or x &lt; 4</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>not</p></td><td colspan="1" rowspan="1"><p>Reverse the result, returns False if the result is true</p></td><td colspan="1" rowspan="1"><p>not(x &lt; 5 and x &lt; 10)</p></td><td colspan="1" rowspan="1"><p></p></td></tr></tbody>
</table>

<table>
<tbody><tr><td colspan="1" rowspan="1"><p>is&nbsp;</p></td><td colspan="1" rowspan="1"><p>Returns True if both variables are the same object</p></td><td colspan="1" rowspan="1"><p>x is y</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>is not</p></td><td colspan="1" rowspan="1"><p>Returns True if both variables are not the same object</p></td><td colspan="1" rowspan="1"><p>x is not y</p></td><td colspan="1" rowspan="1"><p></p></td></tr></tbody>
</table>

#### <span style="font-size: 17px">Bitwise Operators</span>

<table>
<tbody><tr><th colspan="1" rowspan="1"><p>Operator</p></th><th colspan="1" rowspan="1"><p>Name</p></th><th colspan="1" rowspan="1"><p>Description</p></th><th colspan="1" rowspan="1"><p>Example</p></th><th colspan="1" rowspan="1"><p></p></th></tr><tr><td colspan="1" rowspan="1"><p>&amp;&nbsp;</p></td><td colspan="1" rowspan="1"><p>AND</p></td><td colspan="1" rowspan="1"><p>Sets each bit to 1 if both bits are 1</p></td><td colspan="1" rowspan="1"><p>x &amp; y</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>|</p></td><td colspan="1" rowspan="1"><p>OR</p></td><td colspan="1" rowspan="1"><p>Sets each bit to 1 if one of two bits is 1</p></td><td colspan="1" rowspan="1"><p>x | y</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>^</p></td><td colspan="1" rowspan="1"><p>XOR</p></td><td colspan="1" rowspan="1"><p>Sets each bit to 1 if only one of two bits is 1</p></td><td colspan="1" rowspan="1"><p>x ^ y</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>~</p></td><td colspan="1" rowspan="1"><p>NOT</p></td><td colspan="1" rowspan="1"><p>Inverts all the bits</p></td><td colspan="1" rowspan="1"><p>~x</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>&lt;&lt;</p></td><td colspan="1" rowspan="1"><p>Zero fill left shift</p></td><td colspan="1" rowspan="1"><p>Shift left by pushing zeros in from the right and let the leftmost bits fall off</p></td><td colspan="1" rowspan="1"><p>x &lt;&lt; 2</p></td><td colspan="1" rowspan="1"><p></p></td></tr><tr><td colspan="1" rowspan="1"><p>&gt;&gt;</p></td><td colspan="1" rowspan="1"><p>Signed right shift</p></td><td colspan="1" rowspan="1"><p>Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off</p></td><td colspan="1" rowspan="1"><p>x &gt;&gt; 2</p></td><td colspan="1" rowspan="1"><p></p></td></tr></tbody>
</table>

---

# <span style="font-size: 25px">Arrays</span>

- **<span style="font-size: 15px">List</span>**<span style="font-size: 15px"> is a collection which is ordered and changeable. Allows duplicate members.</span>
- [**<span style="font-size: 15px">Tuple</span>**](https://www.w3schools.com/python/python_tuples.asp)<span style="font-size: 15px"> is a collection which is ordered and unchangeable. Allows duplicate members.</span>
- [**<span style="font-size: 15px">Set</span>**](https://www.w3schools.com/python/python_sets.asp)<span style="font-size: 15px"> is a collection which is unordered, unchangeable\*, and unindexed. No duplicate members.</span>
- [**<span style="font-size: 15px">Dictionary</span>**](https://www.w3schools.com/python/python_dictionaries.asp)<span style="font-size: 15px"> is a collection which is ordered\*\* and changeable. No duplicate members.</span>

## <span style="font-size: 22px">Lists</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">List items are ordered, changeable, and allow duplicate values.</span>

```python
mylist = ["apple", "banana", "cherry"]
```

<span style="font-size: 15px">Lists are used to store multiple items in a single variable.Lists are one of 4 built-in data types in Python used to store collections of data, the other 3 are </span>[<span style="font-size: 15px">Tuple</span>](https://www.w3schools.com/python/python_tuples.asp)<span style="font-size: 15px">, </span>[<span style="font-size: 15px">Set</span>](https://www.w3schools.com/python/python_sets.asp)<span style="font-size: 15px">, and </span>[<span style="font-size: 15px">Dictionary</span>](https://www.w3schools.com/python/python_dictionaries.asp)<span style="font-size: 15px">, all with different qualities and usage.</span>

#### <span style="font-size: 17px">list() Constructor</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">use the </span><span style="font-family: Consolas, Menlo, courier new, monospace; color: crimson; font-size: 15.75px">list()</span><span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> constructor when creating a new list.</span>

```python
thislist = list(("apple", "banana", "cherry")) 
# note the double round-brackets
print(thislist)
```

### <span style="font-size: 17px">Access Items</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">List items are indexed and you can access them by referring to the index number</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">You can specify a range of indexes by specifying where to start and where to end the range.</span>

```python
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[2:5])
```

### <span style="font-size: 17px">Check if Item Exists</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To determine if a specified item is present in a list use the </span>`in`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> keyword:</span>

```python
thislist = ["apple", "banana", "cherry"]
if "apple" in thislist:
  print("Yes, 'apple' is in the fruits list")
```

### <span style="font-size: 17px">Change Item Value</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To change the value of a specific item, refer to the index number</span>

```python
thislist = ["apple", "banana", "cherry"]
thislist[1] = "blackcurrant"
print(thislist)
```

### <span style="font-size: 17px">Change a Range of Item Values</span>

```python
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
thislist[1:3] = ["blackcurrant", "watermelon"]
print(thislist)
```

### <span style="font-size: 17px">Insert Items</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`insert()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method inserts an item at the specified index:</span>

```python
thislist = ["apple", "banana", "cherry"]
thislist.insert(2, "watermelon")
print(thislist)
```

### <span style="font-size: 17px">Append Items</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To add an item to the end of the list, use the </span><span style="font-family: Consolas, Menlo, courier new, monospace; color: crimson; font-size: 15.75px">append()</span><span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method:</span>

```python
thislist = ["apple", "banana", "cherry"]
thislist.append("orange")
print(thislist)
# [apple,banana,cherry,orange]
```

### <span style="font-size: 17px">Extend List</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To append elements from </span>*another list*<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> to the current list, use the </span>`extend()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method.</span>

```python
thislist = ["apple", "banana", "cherry"]
tropical = ["mango", "pineapple", "papaya"]
thislist.extend(tropical)
print(thislist)
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`extend()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method does not have to append </span>*lists*<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">, you can add any iterable object (tuples, sets, dictionaries etc.)</span>

### <span style="font-size: 17px">Remove Specified Item</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`remove()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method removes the specified item.</span>

```python
thislist = ["apple", "banana", "cherry"]
thislist.remove("banana")
print(thislist)
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`pop()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method removes the specified index.</span>

```python
thislist = ["apple", "banana", "cherry"]
thislist.pop(1)
print(thislist)
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">If you do not specify the index, the </span>`pop()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method removes the last item.</span>

<span style="font-size: 15px">The </span>`clear()`<span style="font-size: 15px"> method empties the list..The list still remains, but it has no content</span>

### <span style="font-size: 17px">Loop Through a List</span>

```python
thislist = ["apple", "banana", "cherry"]
for x in thislist:
  print(x)

thislist = ["apple", "banana", "cherry"]
for i in range(len(thislist)):
  print(thislist[i])

thislist = ["apple", "banana", "cherry"]
i = 0
while i < len(thislist):
  print(thislist[i])
  i = i + 1

thislist = ["apple", "banana", "cherry"]
[print(x) for x in thislist]
```

### <span style="font-size: 17px">Sort Lists</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">List objects have a </span>`sort()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method that will sort the list alphanumerically, ascending, by default:</span>

```python
thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]
thislist.sort()
print(thislist)
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To sort descending, use the keyword argument </span>`reverse = True`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">:</span>

```python
thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]
thislist.sort(reverse = True)
print(thislist)
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">By default the </span>`sort()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method is case sensitive, resulting in all capital letters being sorted before lower case letters.</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">So if you want a case-insensitive sort function, use str.lower as a key function:</span>

```python
thislist = ["banana", "Orange", "Kiwi", "cherry"]
thislist.sort(key = str.lower)
print(thislist)
```

### <span style="font-size: 17px">Reverse Order</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`reverse()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method reverses the current sorting order of the elements</span>

```python
thislist = ["banana", "Orange", "Kiwi", "cherry"]
thislist.reverse()
print(thislist)
```

### <span style="font-size: 17px">Copy Lists</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To make a copy, use the built-in List method </span>`copy()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">.Another way to make a copy is to use the built-in method </span>`list()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">.</span>

```python
thislist = ["apple", "banana", "cherry"]
mylist = thislist.copy()
print(mylist)
```

### <span style="font-size: 17px">Join Two Lists</span>

```python
list1 = ["a", "b", "c"]
list2 = [1, 2, 3]

list3 = list1 + list2
print(list3)

list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]

for x in list2:
  list1.append(x)

print(list1)

list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]

list1.extend(list2)
print(list1)
```

---

## <span style="font-size: 21px">Tuple</span>

<span style="font-family: Verdana, sans-serif; color: #101113; font-size: 15px">Tuples are used to store multiple items in a single variable,Tuple items are ordered, unchangeable, and allow duplicate values</span>

```python
mytuple = ("apple", "banana", "cherry")
```

### <span style="font-size: 17px">Change Tuple Values</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Tuples are </span>**<span style="font-size: 15px">unchangeable</span>**<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">, or </span>**<span style="font-size: 15px">immutable,</span>**<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">But there is a workaround. You can convert the tuple into a list, change the list, and convert the list back into a tuple</span>

```python
x = ("apple", "banana", "cherry")
y = list(x)
y[1] = "kiwi"
x = tuple(y)

print(x)
```

**Add tuple to a tuple**<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">. You are allowed to add tuples to tuples, so if you want to add one item, (or many), create a new tuple with the item(s), and add it to the existing tuple:</span>

```python
thistuple = ("apple", "banana", "cherry")
y = ("orange",)
thistuple += y

print(thistuple)
```

### <span style="font-size: 17px">Remove Items</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Tuples are </span>**unchangeable**<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">, so you cannot remove items from it, but you can use the same workaround as we used for changing and adding tuple items:</span>

```python
thistuple = ("apple", "banana", "cherry")
y = list(thistuple)
y.remove("apple")
thistuple = tuple(y)
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Python, we are also allowed to extract the values back into variables. This is called "unpacking</span>

```python
fruits = ("apple", "banana", "cherry")

(green, yellow, red) = fruits

print(green)
print(yellow)
print(red)
```

### <span style="font-size: 17px">Using Asterisk</span>`*`

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">If the number of variables is less than the number of values, you can add an </span>`*`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> to the variable name and the values will be assigned to the variable as a list:</span>

```python
fruits = ("apple", "banana", "cherry", "strawberry", "raspberry")

(green, yellow, *red) = fruits

print(green)
print(yellow)
print(red)
```

### <span style="font-size: 17px">Loop Through a Tuple</span>

```python
thistuple = ("apple", "banana", "cherry")
for x in thistuple:
  print(x)

thistuple = ("apple", "banana", "cherry")
for i in range(len(thistuple)):
  print(thistuple[i])

thistuple = ("apple", "banana", "cherry")
i = 0
while i < len(thistuple):
  print(thistuple[i])
  i = i + 1
```

---

## <span style="font-size: 25px">Sets</span>

<span style="font-size: 15px">Sets are used to store multiple items in a single variable </span><span style="font-size: 17px">, </span><span style="font-size: 15px">a set is a collection which is </span>*<span style="font-size: 15px">unordered</span>*<span style="font-size: 15px">, </span>*<span style="font-size: 15px">unchangeable\*</span>*<span style="font-size: 15px">, and </span>*<span style="font-size: 15px">unindexed</span>*<span style="font-size: 15px">., Duplicates are not allowed.</span>

```python
myset = {"apple", "banana", "cherry"}
```

### <span style="font-size: 17px">set() Constructor</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">use the </span><span style="font-family: Consolas, Menlo, courier new, monospace; color: crimson; font-size: 15.75px">set()</span><span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> constructor to make a set.</span>

```python
thisset = set(("apple", "banana", "cherry")) 
# note the double round-brackets
print(thisset)
```

### <span style="font-size: 17px">Add Items</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To add one item to a set use the </span>`add()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method.</span>

```python
thisset = {"apple", "banana", "cherry"}
thisset.add("orange")
print(thisset)
```

### <span style="font-size: 17px">Add Sets</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To add items from another set into the current set, use the </span>`update()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method, The object in the </span>`update()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method does not have to be a set, it can be any iterable object (tuples, lists, dictionaries etc.).</span>

```python
thisset = {"apple", "banana", "cherry"}
tropical = {"pineapple", "mango", "papaya"}

thisset.update(tropical)

print(thisset)
```

### <span style="font-size: 17px">Remove Item</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">To remove an item in a set, use the </span>`remove()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">, or the </span>`discard()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method.</span>

```python
thisset = {"apple", "banana", "cherry"}
thisset.remove("banana")
print(thisset)
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">If the item to remove does not exist, </span>`remove()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> will raise an error. But </span>`discard()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> will </span>**NOT**<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> raise any error.</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">You can also use the </span>`pop()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method to remove an item, but this method will remove a random item, so you cannot be sure what item that gets removed.</span>

<span style="font-size: 15px">The </span>`clear()`<span style="font-size: 15px"> method empties the set.</span>

### <span style="font-size: 17px">Join Two Sets</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">You can use the </span>`union()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method that returns a new set containing all items from both sets, or the </span>`update()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method that inserts all the items from one set into another:</span>

```python
set1 = {"a", "b" , "c"}
set2 = {1, 2, 3}

set3 = set1.union(set2)
set1.update(set2)
print(set3)
```

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Both </span>`union()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> and </span>`update()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> will exclude any duplicate items.</span>

`intersection_update()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method will keep only the items that are present in both sets.</span>

```python
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}

x.intersection_update(y)
print(x)
```

`symmetric_difference_update()`<span style="font-size: 15px"> method will keep only the elements that are NOT present in both sets.</span>

```python
x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}

x.symmetric_difference_update(y)
print(x)
```

---

## <span style="font-size: 23px">Dictionaries</span>

<span style="font-size: 15px">Dictionaries are used to store data values in key:value pairs.A dictionary is a collection which is ordered\*, changeable and do not allow duplicates.</span>

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
```

#### <span style="font-size: 17px">dict() Constructor</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">Use the </span><span style="font-family: Consolas, Menlo, courier new, monospace; color: crimson; font-size: 15.75px">dict()</span><span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> constructor to make a dictionary.</span>

```python
thisdict = dict(name = "John", age = 36, country = "Norway")
print(thisdict)
```

### <span style="font-size: 17px">Get Keys</span>

<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px">The </span>`keys()`<span style="font-family: Verdana, sans-serif; color: rgb(0, 0, 0); font-size: 15px"> method will return a list of all the keys in the dictionary.</span>

```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
x=thisdict.keys()
```