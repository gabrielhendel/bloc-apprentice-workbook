# Module 1 Review Questions and Exercises

## Instructions

1. Click "edit" at the top of the page.
2. Fill in your answers below each question.
3. Save your changes and send a link to your mentor!

## HTML

### Questions

1. What is HTML and what is it used for?
HTML (hypertext markup language) is a markup language used by browsers to render webpages. It defines a site's text/content, layout, and style (though that last one is mostly handled by CSS).

2. What is the difference between an ID and a class?
An id typically refers to just one element (a unique HTML element you want to refer to in CSS), while class is a type that can apply to many individual elements.

3. What does it mean to write "semantic" HTML?
HTML that conveys the semantic meaning of what's being written. For example, using some of the new HTML5 elements like <header>, <footer> and <nav> is more semantic than using more generic elements like <li> <div> and <p> with classes.

### Exercises

1. Write a paragraph tag with a class of "highlight" and content "Watch out!".
<p class="highlight">Watch out!</p>

2. Write an HTML image tag to show an image called `profile-picture.jpg`.
<img src=`profile-picture.jpg`>

3. Write a link tag that links to http://google.com.
<a href='http://google.com'>Google</a>

5. Write an complete standard HTML document outline (including a DOCTYPE, and `<html>`, `<head>`, and `<body>` tags).

<!DOCTYPE html>

<head> 
  <script type="text/javascript" src="main.css"></script>
  <link rel="stylesheet" type="text/css" href="main.css">
</head>

<body>
  //body elements
</body>

6. Inside of the code for the previous exercise, write the appropriate tag to link to a script file called `main.js`.
See above

7. Inside of the code for the previous exercise, write the appropriate tag to link to a stylesheet file called `main.css`.
See above

8. Write a numbered list in HTML and list three of your favorite books.
<ul>
  <li>When Breath Becomes Air</li>
  <li>The Unbearable Lightness of Being</li>
  <li>Frankenstein</li>
</ul>
9. Fix the indentation of the following HTML sample:

  ```html
  <div>
    <ul>
      <li>Item 1</li>
      <li>Item 2</li>
      <li>Item 3</li>
    </ul>
  </div>
  ```

## CSS

### Questions

1. What is CSS and what is it used for?
Cascading Style Sheets are used to define the style (fonts, weights, colors, borders, margins, etc) and layout (box model) of a webpage. Refers to the HTML elements of the webpage.

2. What is the CSS box model?
The area that a specific element takes up on a webpage when rendered in the browser is shaped like a box, with content surrounded by padding, surrounded by a border, surrounded by margins. The magnitude of each of these attributes can be defined in CSS.

3. What's the difference between margin and padding?
Padding is between border and content. Margin is outside the border, and defines where this box ends and the box of neighboring elements begins.

### Exercises

1. Write a CSS rule to make the text of all `h1` tags red.
h1 {
  color: red;
}

2. Write a CSS rule to make the background color of the link with `class="btn"` blue:

  ```html
  <a href="#" class="btn">Learn more</a>
  ```
.btn {
  background-color: blue;
}


3. Write a CSS rule to give the first paragraph in the following HTML a font size of `20px`, but not the second paragraph.

  ```html
  <header class="jumbotron">
    <p>Hello, World!</p>
  </header>

  <p>Welcome to this awesome website!</p>
  ```
  
  header.p {
    font-size: 20px;
  }

## JavaScript

### Questions

1. What is a function? What are they used for?
A function is a modular bit of code that can be called from elsewhere in the code in order to perform a basic task/functionality. It can optionally take in parameters (arguments) and return output.

2. What is the difference between `==` and `===`?
The latter is more strict. It checks that data types are equal as well (since it doesn't convert types).

3. What is the difference between global and local scope variables?
global variables can be referenced from anywhere in the program (since they're defined outside a particular function/object). 
Local variables are defined in a specific function/object and can only be referenced inside that particular function/object.

4. What is a boolean value?
A binary true/false

5. What is an array?
An ordered list of elements (e.g. [3, 10, "Hello"]

### Exercises

1. Write a line that declares a variable called `myName` and set its value to your name.
var myName = 'Gabe Hendel';

2. Write a loop that logs the numbers 1 through 10 to the console.
for (var i = 1; i <= 10; i++) {
  console.log(i);
}

3. Translate the following pseudocode into JavaScript: if `score` is greater than `3` and `lives` is greater than `0`, alert "You win!".
if (score > 3 && lives > 0) {
  alert("You win!");
}

4. Write a function `sayHello` that takes one argument, a name, and logs "Hello, <name>!" to the console. Then, call the function below the function definition and pass in your name as the argument.
function sayHello(name) {
  console.log("Hello, " + name + "!");
}


5. What would the following script log to the console?
"Friday, Friday"

  ```javascript
  var currentSong = "Call Me Maybe";

  function setSong(song) {
    currentSong = song;
  }

  setSong("Friday, Friday");

  console.log(currentSong);
  ```

6. What would the following script log to the console?
10

  ```javascript
  var add = function(a, b) {
    return a + b;
  }

  var result = add(3, 7);

  console.log(result);
  ```

7. What would the following script log to the console?
Hello Sarah ! Goodbye Sarah !

  ```javascript
  var helloGoodbye = function(name) {
    return sayHello(name) + " " + sayGoodbye(name);
  }

  var sayHello = function(name) {
    return "Hello " + name " !";
  }

  var sayGoodbye = function(name) {
    return "Goodbye " + name " !";
  }

  console.log(helloGoodbye("Sarah"));
  ```

8. Write a function `findLongestWord()` that takes an array of words and returns the length of the longest one.


9. Define a function `sum()` that sums all the numbers in an array of numbers. For example, `sum([1,2,3,4])` should return 10.
function sum(numbers) {
  var currentSum = 0;
  for (var i = 0; i < numbers.length; i++) {
    currentSum = currentSum + numbers[i];
  }
  return currentSum;
}


10. Write a function that takes a character (i.e. a string of length 1) and returns true if it is a vowel, false otherwise.
function vowelChecker (character) {
  if (character == 'a' || character == 'e' || character == 'i' || character == 'o' || character == 'u') {
    return true;
  }
  else {
    return false;
  }
}

11. Write the correct line to make `"Woof!"` show up in the console based on this script:
pet.speak();

  ```javascript
  var pet = {
    name: "Charles",
    goodDog: true,
    speak: function() {
      console.log("Woof!");
    }
  };
  ```

12. Using the same script as above, write the correct line to log the dog's name to the console.
console.log(pet.name());

## Command Line

### Questions

1. What is the command line and what is it used for?
Lets a computer user interact with their computer via text input as opposed to a GUI/mouse

2. What does the command `ls` do?
Lists files/directories in the current directory

3. What does the command `pwd` do?
Writes path of current directory

4. What does the following command do: `cd my-cool-project`
goes into that directory called "my-cool-project"

### Exercises

1. Write the command to make a new directory called "my-cool-project".
mkdir my-cool-project

2. Write the command to create a file called "index.html".
touch index.html

3. Write the command to delete a file called "main.css".
-d main.css

## Git

### Questions

1. What is Git and what is it used for?
A system for tracking a history of changes to a project. Allows people to navigate history of changes, do version control and revert to a past version, and collaborate on work on a project in separate branches and merge changes and identify differences.

2. What's the difference between a local repository and a remote repository?
Local repository is on the user's local server. Remote repository is on a cloud server, often on some service like github.

### Exercises

1. Write the command that you would use to create a new local Git repository.
git init

2. Write the command to stage a file called `index.html` to be committed.
git add index.html

3. Write the command to view the current status of the git repository.
git status
