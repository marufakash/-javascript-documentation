# JavaScript documentation

## 1.1 Introduction to Javascript

- A programming language for web.
- it can be used in front-end and back-end

## 1.2 Output and comment

- Writing into an HTML element, using `innerHTML`
- Writing into the HTML output using `document.write()`
- Writing into the browser console, using `console.log()`

```JavaScript
// single line comment
document.write("Welcome to JavaScript");
document.write("<h1>Welcome to JavaScript</h1>");
console.log("Hello programmer");

/*
This is a multiple line comment.
In this section nothing to be executed in main file.
To readable, this is good practice to use coment.
*/
alert("welcome to js program");
```

## 1.3 Tokens

- Keywords: javascript reserved words for specific reasons.

  - Example - abstract, break, char, double, export, import, try, catch, finally, throw, throws, if, else, switch, case, break, default, continue,for, while, do, var, let, const, class, extends, implements, public, private, protected, new, static, this, true, false, boolean, string, number, function, instanceof

- puncuators

  - () round brackets / parentheses
  - {} curly brackets / braces
  - [] square brackets / brackets
  - <> angle brackets / chevrons

- Data types
  
  - JavaScript Datatypes (String, Number, Boolean, Null, Symbol)
  - The Object Datatype (An object, An array, A date)

    ```JavaScript
    // Numbers:
    let length = 16;
    let weight = 7.5;

    // Strings:
    let color = "Yellow";
    let lastName = "Johnson";

    // Booleans
    let x = true;
    let y = false;

    // Object:
    const person = {firstName:"John", lastName:"Doe"};

    // Array object:
    const cars = ["Saab", "Volvo", "BMW"];

    // Date object:
    const date = new Date("2022-03-25");
    ```

- Variables

  - Varibale is a placeholder for storing data.   

    ```JavaScript
    let name = "Maruf Akash";
    var price = 129.66
    const title = "Learning Point"
    ```

  - variables naming rules (collected from w3school)
    - The general rules for constructing names for variables (unique identifiers) are:
    - Names can contain letters, digits, underscores, and dollar signs.
    - Names must begin with a letter
    - Names can also begin with $ and _ (but we will not use it in this tutorial)
    - Names are case sensitive (y and Y are different variables)
    - Reserved words (like JavaScript keywords) cannot be used as names

  - 3 most popular variable naming style
    - Underscore: first_name, last_name
    - Upper Camel Case (Pascal Case): FirstName, LastName
    - Lower Camel Case: firstName, lastName
 
  - var vs let vs const
    - 2 important things: reassign, scope - block, function, global
    - var variable can be reassigned and function scoped.
      ```JavaScript
      var name = "alex";
      name = "robin"; // reassign allowed for var variables

      if (true) {
        var age = 32;
      }

      console.log(name);
      console.log(age); //  allowed as var variable is function scoped
      ```
    - let variable can be reassigned but blocked (a set of curly braces) scoped.
        
        ```JavaScript
        let name = "alex";
        name = "robin"; // reassign allowed for let variables

        if (true) {
            let age = 32;
        }

        console.log(name);
        console.log(age); // not allowed as let variable is block scoped
        ```
    
    - const variable can not be reassigned but blocked (a set of curly braces) scoped.

      ```JavaScript
      const name = "alex";
      name = "robin"; // reassign is not allowed for const variables

      if (true) {
        const age = 32;
      }

      console.log(name);
      console.log(age); //  not allowed as const variable is blocked scoped
      ```

- Operators

  - Arithmetic operators : +, -, *, /, %
  - Assignment operators: +=, -=, *=, /=, %=
  - Unary operators: ++, --
  - Comparision / Relational operators: >, >=, <, <=, ==, !=, ===, !==
  - Logical operators: &&, ||, !
  - Ternary Operator: `condition ? expression1 : expression2;`
  - Bitwise operators: &, |, ^, ~, >>, <<

## 1.4 Prompt & Data Type conversion

- prompt() can help us to take user input. Though it is not recommended but for testing purpose we can use it instead of a form.
- Number(), toString(), pasreInt(), parseFloat(), parseDouble()

## 1.5 Math methods

- max(), min(), sqrt(), pow(), ceil(), floor(), round(), random()

    ```JavaScript
    console.log(Math.max(20, 30));
    console.log(Math.min(20, 30));
    console.log(Math.floor(3.4));
    console.log(Math.ceil(3.4));
    console.log(Math.round(3.4));
    console.log(Math.random());

    const randomNumber = Math.floor(Math.random() * 5) + 1;
    ```

- Traditional function vs Arrow function
  ```JavaScript
  // demo1 - must use parenthesis for no parameters, but for one parameter its optional
  function display1() {
    console.log("I am display 1");
  }

  const display2 = () => {
    console.log("I am display 2");
  };

  display1();
  display2();

  // demo2 - no need to use curly braces if returning or dealing with single statement
  function display3() {
    console.log("I am display 3");
  }

  const display4 = () => console.log("I am display 4");

  display3();
  display4();

  // returning value in arrow function - no need to use curly braces if returning or dealing with single statement
  function display5() {
    return "I am display 5";
  }

  const display6 = () => "I am display 6";

  console.log(display5());
  console.log(display6());

  // parameters in arrow function
  function add1(x, y) {
    return x + y;
  }

  const add2 = (x, y) => x + y;

  console.log(add1(10, 20));
  console.log(add2(20, 30));
  ```

## 1.6 Control statement

- Conditional control statement: if, else if, else, switch

  - if, else if, else related programss
    - positive / negative / zero program
      ```JavaScript
      let num1 = parseInt(prompt("Enter first numebr : "));
      let num2 = parseInt(prompt("Enter second numebr : "));

      if(num1 > num2){
        console.log("Large Number is : " + num1);
      } else if(num2 > num1){
        console.log("Large Number is : " + num2);
      } else{
        console.log("Equal numbers");
      }
      ```

    - Vowel / consonant program
      ```JavaScript
      let letter = prompt("Enter a letter : ");

      // convert any uppercase input into lower cause we set only lowercase letter in condition
      letter = letter.toLowerCase();

      // Now check the condition
      if(letter == 'a' || letter == 'e' || letter == 'i' || letter == 'o' || letter =='u'){
        console.log('Vowel');
      } else{
        console.log('Consonant');
      }
      ```

  - switch
    - 4 keywords: switch, case, break, default
      ```JavaScript
      // Vowel Consonent using switch
      let letter = prompt("Enter any letter : ");
      letter = letter.toLowerCase();

      switch(letter) {
        case 'a':
        case 'e':
        case 'i':
        case 'o':
        case 'u':
            console.log("Vowel");
            break;
        default:
            console.log("Consonent");
      }
      ```

- Loop control statement: for, while, do while loop

  - for loop
    ```JavaScript
    // sum of numbers 1+2+..+10
    let sum = 0;

    for(let i=1; i<10; i++){
        sum = sum + i;
    }

    console.log("Summation is : " + sum);
    ```

  - while loop
    ```Javascript
    // sum of numbers 1+2+..+10
    let sum = 0;

    let i = 1;
    while(i<10){
        sum = sum + i;
        i++;
    }

    console.log("Summation is : " + sum);
    ```
  - do while loop
    ```Javascript
    // sum of numbers 1+2+..+10
    let sum = 0;

    let i = 1;
    do{
        sum = sum + i;
        i++;
    }while(i<10)

    console.log("Summation is : " + sum);
    ```

## 1.7 Object 
- object is one type of variable that can store differnt types of variables

  ```JavaScript
  // declaring objects 
  const student1 = {
    name: "Maruf Akash",
    age: 22,
    cgpa: 3.92,
    language: ["Bangla","English"]
  }

  const student2 = {
    name: "Gazi Mahabuba",
    age: 23,
    cgpa: 3.36,
    language: ["Hindi","Arbi","English"]
  }

  // printing object
  console.log(student1);

  // printing object property's value
  console.log(student1.name);

  // adding a constructor
  function student(name, age, cgpa, language){
    this.name = name;
    this.age = age;
    this.cgpa = cgpa;
    this.language = language;

    // adding function inside a constructor
    this.display = function(){
        console.log(this.name);
        console.log(this.age);
        console.log(this.cgpa);
        console.log(this.language);
    }
  }

  let student1 = new student("Maruf Akash",22,3.87,["Bangla","English","Hindi"]);
  let student2 = new student("Gazi Mahabuba",23,3.99,["Arbi","English","Hindi"]);

  console.log(student1);
  console.log(student2);

  student1.display();
  student2.display();
  ```

## 1.8 Array
- Array is a collection of similar data type mostly.
- Array methods - push(), pop(), shift(), unShift(), slice(), splice(), sort(), reverse()
  ```JavaScript
  let names = ["Maruf", "Sumaya", "Oishi", "Mahabuba", "Urmi"];
  console.log(names);

  // Push() - add a new element in the end of array
  names.push("Tanzim","Sayma");
  console.log(names);

  // pop() - remove an element in the end of array
  names.pop();
  console.log(names);

  // shift() -remove an element in the front of array
  names.shift();
  console.log(names);

  // unshift() - add a new element in the front of array
  names.unshift("Akash");
  console.log(names);

  // splice(start, delete, add)
  names.splice(2,0,"Monisha","Riya");
  console.log(names);

  // sort()
  console.log(names.sort());

  // reverse()
  console.log(names.reverse());

  // numbers sorting
  let numbers = [6,9,0,72,1,-2];
  numbers = numbers.sort((a,b) => a-b);
  console.log(numbers);
  ```
- find(), findIndex()
  ```JavaScript
  // find(callback, value) return the value of the first element that pass certain condition

  const numbers = [11,7,5,28,9, 19,0];
  let firstEvenNumber = numbers.find((x) => x%2===0);
  console.log(firstEvenNumber);

  // findIndex(callback, value) return the index of the first element that pass certain condition

  let firstEvenNumberIndex = numbers.findIndex((x) => x%2===0);
  console.log(firstEvenNumberIndex);
  ```

- One-Dimensional Array
  ```JavaScript
  // 1D Array - Create a function called highestScore that will receive a 1D array called scores & return the highest score

  function highestScore(scores) {
    let max = scores[0];
    for(let i=1; i<scores.length; i++){
        if(max < scores[i]){
            max = scores[i];
        }
    }
    return max;
  }

  // Getting input from the user
  et scores = [];
  for(let i=0; i<5; i++){
    scores[i] = Number(prompt("Enter the scores : "));
  }
  console.log(scores);

  console.log("Highest score : " + highestScore(scores));
  ```

- Two-Dimensional Array
  ```JavaScript
  // 2D Array - create a function called highestRunScorer that will receive a 2D array called playersInfo. Based on highest score, return the name of player.

  function highestRunScorer(playersInfo) {
    let highestScorer = playersInfo[0][0];
    let highestScore = playersInfo[0][1];

    for(let i=0; i<playersInfo.length; i++){
        if(highestScore < playersInfo[i][1]){
            highestScore = playersInfo[i][1];
            highestScorer = playersInfo[i][0];
        }
    }

    return highestScorer;
  }

  let playersInfo =[
    ["Maruf Akash", 78],
    ["Gazi Mahabuba", 91],
    ["Sumaya Islam", 54],
    ["Urmi Akter", 99],
    ["Mariya Khan", 88]
  ]

  console.log("Highest Scorer : " + highestRunScorer(playersInfo));
  ```

## 1.9 Higher Order Array function

- map() higher order function
 
  - when we use loop we need to create an array but map returns an array
  - map() does not change the original array.
  - map() creates a new array from calling a function for every array element.
  - map() calls a function once for each element in an array.
  - map() does not execute the function for empty elements.
  - syntax and example
  
    ```JavaScript
    let numbers = [5,6,7,8,9,10];
    let squareNumbers = numbers.map((x) => {
      return x*x;
    })

    console.log(squareNumbers);
    ```
- filter() higher order function
 
  - filter() does not change the original array.
  - filter() creates a new array filled with elements that pass a test provided by a function.
  - filter() calls a function once for each element in an array.
  - filter() syntax and example
    
    ```JavaScript
    let numbers = [22, 31, 4, 5, 35, 26, 78];
    let newNumbers = numbers.filter(function (x) {
      return x > 10;
    });
    console.log(newNumbers);
    ```
  
- reduce() higher order function

  - sum of all numbers; when sum think reduce
  - it executes a reducer function for array element.
  - it returns a single value: the function's accumulated result.
  - it does not execute the function for empty array elements.
  - it does not change the original array.

    ```JavaScript
    const numbers = [10, 20, 30, 40, 50];
    // first call -> previous 10, current 20
    // 2nd call -> previous 30, current 30
    // 3rd call -> previous 60, current 40
    // 4th call -> previous 100, current 50

    const result = numbers.reduce((previous, current) => {
      return previous + current;
    });
    console.log(result);
    ```

- ES6 map, filter & Arrow function example
  ```JavaScript
  const students = [
    {
        name: "Maruf Akash",
        id: 392,
        email: "marufakash392@gmail.com",
        cgpa: 3.55
    },
    {
        name: "Gazi Mahabuba",
        id: 288,
        email: "gazimahabuba54@yahoo.com",
        cgpa: 3.92
    },
    {
        name: "Ummay Sayma",
        id: 218,
        email: "saymaislam6621@gmail.com",
        cgpa: 2.71
    },
    {
        name: "Tanzila Monisha",
        id: 181,
        email: "tanzilamonisha52@gmail.com",
        cgpa: 1.98
    }
  ]

  const studentNames = () => students.filter((student) =>  student.cgpa < 2.00).map((studentInfo) => studentInfo.name);


  console.log(studentNames());
  ```

- forEach()
  
  ```JavaScript
  let sum = 0;
  const numbers = [65, 44, 12, 4];

  numbers.forEach((x) => {
    sum = sum + x;
  })

  console.log(`Summation : ${sum}`);
  ```

## 2.0 spread operator & destructure

- Destructure is a JavaScript expression that allows to unpack values from arrays, or properties from objects, into distinct variables

  ```JavaScript
  // Array destructuring
  const numbers = [10,20,30,40,50,60];
  const [num1,num2,num3,num4, ...num5] = numbers;
  console.log(num3);

  // Object destructuring
  const student = {
    name: "Maruf Akash",
    id: "19EEE047",
    session: 2019,
    cgpa: 3.92
  }

  const {name, id, session, cgpa} = student;
  console.log(`Name: ${name}, ID: ${id}, Session: ${session}, CGPA: ${cgpa}`);

  // destructuring function parameters
  const studentInfo = ({name,id,session,cgpa}) => {
    console.log(`Name: ${name}, ID: ${id}, Session: ${session}, CGPA: ${cgpa}`);
  }
  ```
- spread operator ( ... ) allows us to quickly copy all or part of an existing array or object into another array or object.
  ```JavaScript
  // concat two object
  let p1 = {
    name : 'Maruf Akash',
    ID : '19EEE047'
  }
  let p2 = {
    age : 23,
    Nationality : 'Bangladeshi'
  }

  let p = {...p1, ...p2}
  console.log(p);

  // concat two array
  let num1 = ["Maruf","Tanzim","Atik"];
  let num2 = ["Mim","Sumaya","Oishi"];

  let num = [...num1, ...num2];
  console.log(num);

  //push two array
  let numb = [1,4,5];
  let numb1 = [9, ...numb,7];

  console.log(numb1);
  ```

## 2.1 Document Object Model (DOM)

- The document object represents your web page.
- If you want to access any element in an HTML page, you always start with accessing the document object.
- Finding HTML Elements

  | Method | Description |
  | ---- | ---- |
  | document.getElementById(id) | Find an element by element id |
  | document.getElementsByTagName(name) | Find elements by tag name |
  | document.getElementsByClassName(name) | Find elements by class name |
  | document.querySelector(name) | find element by id class tag name |
  | document.querySelectorAll() | find element by id class tag name |

  - The `querySelectorAll()` method returns a static NodeList.

- Adding and Deleting Elements

  | Method | Description |
  | ---- | ---- |
  | document.createElement(element) | Create an HTML element |
  | element.removeChild(element) | Remove an HTML element |
  | element.appendChild(element) | Add an HTML element |
  | element.insertBefore(new, existing) | Add an HTML element |
  | document.write(text) | 	Write into the HTML output stream |

  - Add the html file
    ```HTML
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Find, create, add, remove html elements</title>
    </head>
        <body>
            <div class="my-div">
                <h1 class="heading1">This is heading 1</h1>
                <h1 class="heading2">This is heading 2</h1>
                <h1 class="heading3">This is heading 3</h1>
                <h1 class="heading4">This is heading 4</h1>
            </div>
        </body>
    </html>
    ```

  - Add the javascript file
    
    ```JavaScript
    // Create a new html element
    let heading5 = document.createElement("h1");
    let text = document.createTextNode("This is hesding 5");
    heading5.appendChild(text);

    let myDiv = document.querySelector(".my-div");
    myDiv.appendChild(heading5);

    // Remove a html element
    let heading3 = myDiv.children[2];
    myDiv.removeChild(heading3);

    // Add a new html element in first
    let heading0 = document.createElement("h1");
    let text1 = document.createTextNode("This is heading 0");
    heading0.appendChild(text1);

    let heading1 = myDiv.children[0];
    myDiv.insertBefore(heading0,heading1);
    ```
  



## 3.1 LocalStorage

- The localStorage object allows you to save key/value pairs in the browser.
- The localStorage object stores data with no expiration date.
- The data is not deleted when the browser is closed, and are available for future sessions.
- localStorage allow us to store, read, update & delete data.

1. setItem(key, value) - to store data

    ```JavaScript 
    localStorage.setItem("userName", "Maruf Akash");
    localStorage.setItem("userId", "19EEE047");
    localStorage.setItem("userEmail", "marufakash392@gmail.com");
    ```

2. getItem(key) - to get data

    ```JavaScript
    const userName = localStorage.getItem("userName");
    const userEmail = localStorage.getItem("userEmail");
    console.log(`User-name: ${userName}, User-email: ${userEmail}`);
    ```

3. removeItem(key) - to remove data

    ```JavaScript
    localStorage.removeItem("userName");
    localStorage.removeItem("userEmail");
    localStorage.removeItem("userId");
    ```

4. Array store & read

    ```JavaScript
    const countries = ["Bangladesh","India","Pakistan","Japan","Sri Lanka"];
    localStorage.setItem("countries",JSON.stringify(countries));
    const countryList = JSON.parse(localStorage.getItem('countries'));
    console.log(countryList);
    ```
5. Object store & read

    ```JavaScript
    const studentInfo = {
      name: "Maruf Akash",
      email: "marufakash392@gmail.com",
      year: 2019,
      language: ["Bangla","English","Hindi"]
    }

    localStorage.setItem("studentInfo", JSON.stringify(studentInfo));
    const info = JSON.parse(localStorage.getItem("studentInfo"));
    console.log(info);
    ```
## 3.2 API Calling

- 4 ways to call api - XMLHttpRequest, fetch, axios, jquery

1. XMLHttpRequest

    ```JavaScript
    // event - onload(), onerror()
    // property - response, responseText, responseType, responseURL, status, statusText
    // function - open(), send(), setRequestHeader()
    // method - GET, POST, PUT, DELETE, PATCH

    const makeRequest = (method, url,data) =>{
        const xhr = new XMLHttpRequest();
        xhr.open(method, url);

        xhr.setRequestHeader('Content-Type', 'application/json');

        xhr.onload = () =>{
            let data = xhr.response;
            console.log(xhr.status);
            console.log(xhr.statusText);
            console.log(xhr.responseText);
            console.log(xhr.responseURL);
            console.log(JSON.parse(data));
        }

        xhr.onerror = () =>{
            console.log("Error is here");
        }

        xhr.send(JSON.stringify(data));
    }

    const getData = () => {
        makeRequest("GET", 'https://jsonplaceholder.typicode.com/posts');
    }
    //getData();

    const sendData = () => {
        makeRequest("POST", 'https://jsonplaceholder.typicode.com/posts', {
            title: 'foo',
            body: 'bar',
            userId: 1,
        });
    }
    //sendData();

    const updateData = () => {
        makeRequest("PUT", 'https://jsonplaceholder.typicode.com/posts/1', {
            id: 1,
            title: 'fooma',
            body: 'barma',
            userId: 1,
        });
    }
    //updateData();

    const updateSingleData = () => {
        makeRequest("PATCH", 'https://jsonplaceholder.typicode.com/posts/1', {
            title: 'This is changed',
        });
    }
    updateSingleData();

    const deleteData = () => {
        makeRequest("DELETE", 'https://jsonplaceholder.typicode.com/posts/1', {
        });
    }
    ```

2. fetch
 
    - fetch() has replaced XMLHttpRequest
    - fetch() - global method for making HTTP Request
    - 2 ways to call - then, async await

      ```JavaScript
      // method for making HTTP Request
      const makeRequest = async (url, config) => {
        const res = await fetch(url, config);
        if (!res.ok) {
          throw Error(`Error : ${res.status}`);
        }
        const data = await res.json();
        return data;
      };
        
      const deleteData = () => {
        makeRequest("https://jsonplaceholder.typicode.com/posts/1", {
          method: "DELETE",
      })
      .then((res) => console.log(res))
      .catch((err) => console.log(err));
      };
        
      deleteData();

      const updateData = () => {
        makeRequest("https://jsonplaceholder.typicode.com/posts/1", {
          method: "PATCH",
          body: JSON.stringify({
            title: "foomaraarrara",
          }),
          headers: {
            "Content-type": "application/json; charset=UTF-8",
          },
        })
        .then((res) => console.log(res))
          catch((err) => console.log(err));
      };
      
      updateData();
      
      const sendData = () => {
        makeRequest("https://jsonplaceholder.typicode.com/posts", {
          method: "POST",
          body: JSON.stringify({
            title: "foo",
            body: "bar",
            userId: 1,
          }),
          headers: {
            "Content-type": "application/json; charset=UTF-8",
          },
        })
        .then((res) => console.log(res))
        .catch((err) => console.log(err));
      };
      
      sendData();

      const getData = () => {
        makeRequest("https://jsonplaceholder.typicode.com/posts")
        .then((res) => console.log(res))
        .catch((err) => console.log(err));
      };
      
      getData();
      ```