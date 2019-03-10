# Practical

## Task 1 - Our First JavaScript Program

Let's go ahead and create our first JavaScript program:

#### Including JavaScript

There are 2 main way's to include a JavaScript code in our HTML pages:


> **In the head - executed when called** 

```javascript
<html>
<head>
  <script type="text/javascript">
     JavaScript code
      … …
  </script>
</head>
<body>
    … …
</body>
</html>
```


> **In the body - executed when the page loads** 

```javascript
<html>
<head>
  … …
</head>
<body>
  <script type="text/javascript">
   JavaScript code
   … …
  </script>
</body>
</html>
```
 

Create a new file called `myFirstJavaScript.html` and type in the below code:

```javascript
<html>
 <head>
  <title>JavaScript Page</title>
 </head>
 <body>
  <script type="text/javascript">
    //simple code to demonstrate output
    document.write("Hello World!");
    document.write("<h1>This is a heading</h1>");
    document.write("<p>This is a paragraph.</p>");
  </script>
 </body>
</html>
```

Save your file and open up the page in your browser and see what happens. 


## Task 2 -  Reading Values
We're going to expand on the first exercise and use variables. Pay close attention on how the  `+` is used to concatenate(join together) text with variables. 

e.g. `document.write("<p> Your name:" + name  + "</p>" );`

Create a new file called `ex2.html` and type in the below code:

```javascript
	<html>
	 <head>
	  <title>JavaScript Page</title>
	 </head>
	 <body>
		 <script type="text/javascript">
	    //set up our variables
	    var name;
	    var age;
	    var yourLocation;
	    
	    //assign values 
	    name = "Joe";
	    
	    //age is an integer so we don't use ""
	    age = 33
	    
	    yourLocation = "Brighton"
	 
	    //simple code to demonstrate output
	    document.write("<p> Your name:" + name  + "</p>" );
	    document.write("<p> Your age:" + age + "</p>" );
	    document.write("<p> Your location:" + yourLocation  + "</p>" );  
	   
	   </script>
   
 </body>
</html>

```


Save your file and open up the page in your browser and see what happens. 

## Task 3  - Summing Numbers

This is the main exercise for this week, you're going to be creating a javaScript application that sums 3 numbers together entered by the user. This is going to be a good opportunity to practice the key points we've covered in this weeks session

* Create a new file called exercise3.html and save it in your session 11 folder

* Using a valid HTML structure place 3 input boxes on the page. You'll need to give each input boxes a unique id. Here's what input box one should look like:

```html
  <p> <input type="number" placeholder="enter number 1" id="number1">  </p>   
```

* Next, create a button that will invoke a javascript function. Notice the attribute `onClick="calculateNumber()`. `calculateNumber\(\)` is the javascript function that will be called when the button is pressed. We'll define this function in the next section. 

```html
<p> <button onClick="calculateNumber()">Click Me</button> </p>     
```

* In the head section of you document create the javaScript function calculateNumber

```html
    <head>  
     <!--
        This script in included in the head so we need to call it
     -->
     <script type="text/javascript">
         // This is a function
         function calculateNumber(){
             //your code will go here
         } //end function 
    </script>
```

* We now need to assign each number entered into the textbooks to a variable. The first number has been assigned for you. See if you can grab the other two.

```html
    <head>  
     <!--
        This script in included in the head so we need to call it
     -->
     <script type="text/javascript">
         // This is a function
         function calculateNumber(){
                var number1 =  parseInt(document.getElementById("number1").value);
          } //end function 
    </script>
```

* Now you've got the numbers stored in variables, go ahead and see if you can add them together and assign the sum to a variable called `result`

* Finally we need to actually display our result, you'll need to use a statement along the lines of:

```html
document.getElementById("result").innerHTML = result;
```

Where `result` corresponds to an element such as a `<p>` with and `id` of `result`



## Task 4 - Advanced optional task

- Create a firebase chat application, users should be able to log-in using Facebook oAuth.

- You will need to set up a firebase account [https://firebase.google.com/](https://firebase.google.com/)

- Use the [firebase documentation](https://firebase.google.com/docs/) and my [sample app](https://github.com/joeappleton18/firebase_chat_app) as a starting point

- Work out how to set up authentication, so you can use Facebook/Google to login

- When complete, publish to firebase hosting or GitHub pages and send me the link