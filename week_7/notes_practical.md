# Notes (Practical)

Below, I explore some of the fundamental constructs of the JavaScript programming language. 


## Comments 
In javascript there are two ways to create comments 

**Block Comments**

```javascript
	/* This is a block comment, we can run 
		over multiple lines 
	*/
```
**Inline Comments**

```javascript
	// This is a inline comment, it can only take up one line
```


* Add comments for the purpose of making the source code easier to understand
* Comments are not displayed in the browsers
* It is also a good practice to "hide" scripts from browsers without support for it


## Variables

Computer programs use variables to store information.

### Rules for JavaScript Variables

* Variable names are case sensitive 
  e.g. y and Y are different
* \`Variable names must begin with a letter or underscore
  e.g. year, \_month

### Declaring JavaScript Variables

In JavaScript variables can be declared in the following ways:

* `var x;`
* `var x=5;`
* `var firstNumber,secondNumber,number1,number2,sum;`

### Javascript is Dynamically Typed

JavaScript is dynamically typed. This means you don't have to declare the type of variable in advanced. The value you assign to the variable determines the type.

```javascript
var  myNumber = 42;    // is a Number
var  myString = "bar"; // is a string
var  myBoolean = true;  // is a boolean
```

### Performing Maths

You can apply mathematic operations to numbers using some basic operators like:

```
 var x = 5;  
 var y = 20;  
 var result = x + y; // result will equal 25
 var result = x * y; // result will equal 100 
 var result = y/x;  //  result will equal 5
```



## The Document Object - Accessing HTML

Javascript becomes really interesting when we start to perform  actions on HTML elements. We can use `properties` and `attributes` attached to the `document` object to achieve this. 

Consider the demo below:

* We use `document.getElementById("name").value` to get the value of the input box with the id attribute `name` and assign it to a variable `nameValue`

* We can then use  `document.getElementById("demo").innerHTML =  "Hello " +  nameValue;` to display a message within a `<p>` element with an id of `demo`

* Notice how the code block to perform the above operations is wrapped in `  function showName()`. This function is invoked (run) when the button is clicked. The button element is given the attribute `onClick="showName()` in order to achieve this. 
```html


<html>
 <head>
  
     <title>JavaScript Page</title>
     
     <!--
        This script in included in the head so we need to call it
     -->
     <script type="text/javascript">
         //This is a function
         function showName(){
            // create a variable called name and assign it the value of the name input box 
            var nameValue =  document.getElementById("name").value;

            /* we can now print the name. The . allows us to append to a string */
            document.getElementById("demo").innerHTML =  "Hello " +  nameValue;
        } //end function 
    </script>
 </head>
 <body>
  
  
    <p> <input type="text" placeholder="enter name" id="name">  </p>   
    
     <!-- 
        Notice the onClick attribute. This will call the function showName()
     -->
     
    <p> <button onClick="showName()">Click Me</button> </p>     

    <!-- 
      
      We will display our output below 

     -->
     
    <p id="demo"></p>
    
 </body>
</html>
```
