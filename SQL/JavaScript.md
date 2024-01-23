**<span style="font-size: 17px">JavaScript</span>** 

JavaScript is a Programming language for the Web.

JavaScript **getElementById("Name of the ID")** : 

getElementById("id name") is used to Search for the id name in HTML.

**Example:** Create a Button Based JS using getElementByI():

```javascript
<html>
<body>
<h1>This is the Heading</h1>
<p id = "demo">Js getElementById("demo") usecase.</p>
<button type="button" onclick='document.getElementById("demo").innerHTML = "H3110 J5 !"'>Click Me</button>
</body>
</html>
```

JavaScript **Scripting &lt;script&gt;&lt;/script&gt; :**

**Example:** Using Scripting to Print Some thing :

```javascript
<html>
<body>
<h1>This is the Heading</h1>
<p id = "demo">Replaceing text</p>
<script>
document.getElementById("demo").innerHTML="JS Text is Replaced"
</script>
</body>
</html>
```

JavaScript **function function_name(param) :**

**Example :** Using JS Function for Button :

```javascript
<html>
<head>
<script>
function myFunction(){
 document.getElementById("demo").innerHTML = "Replaced by Function"
}
</script>
</head>
<body>
<h1>This is the Header</h1>
<p id = "demo">Replace this with the Function</p>
<button type="button" onclick="myFunction()">Replace</button>
</body>
</html>
```

Using External Source File :

```javascript
<script src="myScript.js"></script>
```

Placing Script file outside the main file has some advantages :

1. Seperate Code 
2. Easy to Read and Maintain 
3. Speed Up the Load time.

External Source: Using Website to import a Script with full file path.

```javascript
<script src="https://mywebsite/js/myScript.js"></script>
```

**Displaying Data** in JavaScript 

1. Writing into an HTML element using innerHTML
2. Writing into the HTML output using document.write()
3. Writing into an alert Box using window.alert()
4. Writing into the Browser console , using console.log()

Using **document.write(**"Text to be Printed on the Screen"**) :**

**Example :** Using the document.write() to directing print in Output: 

```javascript
<html>
<body>
<h1>This is the Heading</h1>
<p>This example is not any demo id bytheway</p>
<script>
document.write("Sujal")
</script>
</body>
</html>
```

Using document.write() after an HTML document is loaded will **delete all the Existing HTML.** Should be Used for only Testing.

```javascript
<html>
<body>
<h1>This is the Heading</h1>
<p id="demo">This is why you should use document.write()</p>
<button type="button" onclick="myfunc()">try</button>
<script>
function myfunc(){
document.write("Sujal")
}
</script>
</body>
</html>
```

Using **window.alert()** :

```javascript
<html>
<body>
<h1>This is the Heading</h1>
<p>Using window.alert()</p>
<script>
window.alert(1+2)
</script>
</body>
</html>
```

Using window in window.alert() is not manditory since windows is a Global object in the JS library

Using the **windows.print()** to print the entire page :

```javascript
<html>
<body>
<h1>This is the heading</h1>
<p>Using the window.print() to print the page.</p>
<button type="button" onclick="Function()">Try</button>
<script>
function Function(){
window.print()
}
</script>
</body>
</html>
```

In JavaScript **Programming Instructions** are called **Statements**.

**Assigning variables :**

```javascript
let a,b,c;
a = 1;
b = 2;
c = a+b; 
let person = "Sujal";
```

<table>
<tbody><tr><th colspan="1" rowspan="1"><p>Keyword </p></th><th colspan="1" rowspan="1"><p>Description</p></th></tr><tr><td colspan="1" rowspan="1"><p>var</p></td><td colspan="1" rowspan="1"><p>Declare a Variable </p></td></tr><tr><td colspan="1" rowspan="1"><p>let</p></td><td colspan="1" rowspan="1"><p>Declare a Block Variable </p></td></tr><tr><td colspan="1" rowspan="1"><p>const </p></td><td colspan="1" rowspan="1"><p>Declares a Block constant </p></td></tr><tr><td colspan="1" rowspan="1"><p>if </p></td><td colspan="1" rowspan="1"><p>Condition Execution </p></td></tr><tr><td colspan="1" rowspan="1"><p>function </p></td><td colspan="1" rowspan="1"><p>Declaring a Function </p></td></tr><tr><td colspan="1" rowspan="1"><p>for </p></td><td colspan="1" rowspan="1"><p>Declaring a Conditional Loop</p></td></tr><tr><td colspan="1" rowspan="1"><p>try</p></td><td colspan="1" rowspan="1"><p>Implementing error handling to a block of statment.</p></td></tr></tbody>
</table>

**Comments :**

```javascript
// for Single line Comment 
/* Is used to create a Multi-Line Comment */
```

Always use const for declaring values that doesnt Change, Use let for Changeable Values.

JavaScript **let :**

JS let have a Block Scope , Because of which it must be declared before use and can cannot be Redeclared.

JavaScript **var :**

Javascript var have a global Scope , Because of which you can redeclare the var variable.

JavaScript **typeof :**

To Return the Type of data of the variable suplied.

**JavaScript Functions() :**

```javascript
<html>
<body>
<h1>Website</h1>
<button type="button" onclick="myfunc(1,2,3)">try</button>
<script>
function myfunc(a,b,c){
  window.alert(a*b+c)
}
</script>
</body>
</html>
```

Accessing a function with () results in returning the value of the return while accessing a function without () results in returning the entire function LOL ;0

**JavaScript Objects :**

```javascript
const car = {type:"Fiat", model:"500", color:"white"};
let x  = car.model
```

To Access the Object Properties. [objectName.property](http://objectName.property)Name 

Methods : Methods are actions that can be performed on object.methods are stored in properties as function definitions.

```javascript
const person = {
  firstname = "John",
  lastname = "Doe",
  id = 5566,
  fullname = function(){
     return this.firstname + " " + this.lastname;
  }
};
```

**this** is used to refer the firstname and lastname of the Object .

**Common HTML Events :** 

<table>
<tbody><tr><th colspan="1" rowspan="1"><p>Events</p></th><th colspan="1" rowspan="1"><p>Descriptions</p></th></tr><tr><td colspan="1" rowspan="1"><p>onchange</p></td><td colspan="1" rowspan="1"><p>HTML element has changed </p></td></tr><tr><td colspan="1" rowspan="1"><p>onclick</p></td><td colspan="1" rowspan="1"><p>The Users Click an HTML elements</p></td></tr><tr><td colspan="1" rowspan="1"><p>onmouseover</p></td><td colspan="1" rowspan="1"><p>The user moves the mouse over the HTML Element.</p></td></tr><tr><td colspan="1" rowspan="1"><p>onmouseout</p></td><td colspan="1" rowspan="1"><p>The user moves the mouse away from an HTML element.</p></td></tr><tr><td colspan="1" rowspan="1"><p>onkeydown</p></td><td colspan="1" rowspan="1"><p>The user pushes a keyboard key.</p></td></tr><tr><td colspan="1" rowspan="1"><p>onload</p></td><td colspan="1" rowspan="1"><p>The Browser has finished loading the page.</p></td></tr></tbody>
</table>

**Example :** Using onmouseover and onmouseout Events :

```javascript
<html>
<body>
<h1>Trend</h1>
<button onmouseover="visible()" onmouseout="invisible()">Cat</button>

<script>
function visible(){
    document.getElementById("demo").innerHTML = "Chipi Chipi Chapa Chapa Dubi Dubi Daba Daba";
}
function invisible(){
   document.getElementById("demo").innerHTML = "Magicomi Dubi Dubi Boom Boom Boom ;0";
}
</script>
<p id ="demo"></p>
</body>
</html>
```

**JavaScript String :**

To find the length of the string **length** can be use .

```javascript
let text = 'sujal machhale';
let length= text.length;
```

JavaScript **Escape Characters :**

In Javascript **\\** is the Escape Character .

```javascript
let car = "car names \"BMW\" is Awesome"
```

<table>
<tbody><tr><th colspan="1" rowspan="1"><p>\b</p></th><th colspan="1" rowspan="1"><p>backspace</p></th></tr><tr><td colspan="1" rowspan="1"><p>\f</p></td><td colspan="1" rowspan="1"><p>form feed</p></td></tr><tr><td colspan="1" rowspan="1"><p>\n</p></td><td colspan="1" rowspan="1"><p>New Line </p></td></tr><tr><td colspan="1" rowspan="1"><p>\r</p></td><td colspan="1" rowspan="1"><p>Carriage Return</p></td></tr><tr><td colspan="1" rowspan="1"><p>\t</p></td><td colspan="1" rowspan="1"><p>Horizontal tabulator</p></td></tr><tr><td colspan="1" rowspan="1"><p>\v</p></td><td colspan="1" rowspan="1"><p>Vertical tabulator</p></td></tr></tbody>
</table>

**JavaScript String Methods :**

To Return a Character at Specific Index we can use **charAt() , at() , \[ \] .**

```javascript
let text = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
let len = text.length; //return 26
let index1 = text.charAt(0); //return A
let index2 = text.at(1); //return B
let index3 = text[3]; //return D
```

To Extract certian Part of the String we can use :

**slice(start,end) , substring(start, end) , substr(start, length)**

```javascript
let string = "apple, bannana, kiwi";
let part1 = string.slice(7,13); //return bannana 
let part2 = string.sunstring(7,13); //return bannana
let part3 = string.substr(7,6);  //return bannana
```

JavaScript **String to Upper and Lower Case** : 

To Convert a string to upper case we use **toUpperCase()** and for Lower Case **toLowerCase()** .

```javascript
let x = "Hello World!";
let upper = x.toUpperCase(); //HELLO WORLD  
let lower = x.toLowerCase(); //hello world 
```

**JavaScript join() :**

join() method is used to join arrays in js with some seperator.

```javascript
const fruit = ["bannana","orange","apple"]
const joinArray = fruit.join("*")
```

**JavaScript push and pop** :

**push()** is used to add element to array at the end . **pop()** is used to remove array element from the end .

```javascript
fruits = ["bannana","Apple"]
fruit.pop()
fruits.push("Orange")
// [bannana , orange]
```

**JavaScript shift()  & unshift():**

**shift()** is used to remove the first element of the array a re-set the index of the array . 

**unshift()** is  used to add element to the start of the array and re-set the index of the array .

```javascript
const fruits = ["bannana","orange"]
fruit.shift()
fruit.unshift("apple")
//[apple,orange]
```

**JavaScript Concatinating Arrays :**

```javascript
const array1 = ["one" , "two"];
const array2 = ["three","Four"];
const array3 = ["five" , "six"];
const merge_array = array1.concat(array2,array3);
```

**JavaScript splice() :**

splice() method is used to add new items to an array at a speific location.

```javascript
const fruits = ["Bannana","Orange","Apple,Mango"];
fruit.splice(2,0,"lemon","kiwi")
```

(2) parameter is used to start adding the element from the specified index.

(0) parameter is used tell how many elements to remove from the array.

**JavaScript slice() :**

slice() method is used to peice out a peice of an array into a new array .

```javascript
const fruit = ["bannana","orange","Lemon"];
const array = fruit.slice(1,3);
//orange , lemon
```

**JavaScript indexOf() :**

JavaScript indexOf() is used to search of a element in an array . it finds and return the index of the array.

```javascript
const fruits = ["apple","orange","mango"];
let position  = fruits.indexOf("apple");
```

**JavaScript find() in array :**

find() in array search for first element of the array .

```javascript
<html>
<body>
<p id = "demo"></p>
<script>
const number = [1,3,19,10,24,25];
let greatest = number.find(myfunc);
document.getElementById("demo").innerHTML = greatest
function myfunc(value){
 return value > 10 }
</script>
</body>
</html>
```

JavaScript Sort()  and Reverse():

**sort()** and **reverse()** is used to sort an array alphabetically and reverse of alphabetic order. it creates an new array .

While toSorted() sorts in array without the new to create a new array .

```javascript
const fruits = ["bannana","orange","Apple"]
fruits.sort()
fruits.reverse()
```