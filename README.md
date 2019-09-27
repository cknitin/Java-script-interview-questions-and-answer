# Java script interview questions and answer

## 1. var vs let vs const

### Use of var

    function show(){
      var num =10;
        console.log(num);  // num =  10
      if(true){
       var num = 20;
        console.log(num); // num =  20
      }
      console.log(a);  // num = 20
    }


### Use of let

    function show(){
      let num =10;
        console.log(num);  // num =  10
      if(true){
       var num = 20;       // error
        console.log(num); 
      }
      console.log(a);  // num = 20
    }

### Use of const

    function show(){
      const num =10;
        console.log(num);  // num =  10
      if(true){
       var num = 20;       // error
        console.log(num); 
      }
      console.log(a);  // num = 20
    }
    
 ## 2. What is global namespace

var name = 'nitin': --> Hit enter

now, it can be access like

window.name; ---> it will show nitin

## 3. What is IIFE function?

### Answer: An IIFE (Immediately Invoked Function Expression) is a JavaScript function that runs as soon as it is defined.

syntax - (()=> {.....})()

        (function () {
            var name = "Barry";
        })();

        // Variable name is not accessible from the outside scope
        
        name // throws "Uncaught ReferenceError: aName is not defined"
      
 next, 
 
        var result = (function () {
            var name = "James"; 
            return name; 
        })(); 
        // Immediately creates the output: 
        result; // "James"

## 3. What is the use of "this" in javascript?

        this === window --> true

        var objMy = {
            name: 'nitin',
            sayHello :function() { return 'Hello,'+ this.name; }
        }
        
        objMy.sayHello();  ---> Hello, Nitin


## 4. Object creation in JavaScript

        var person = function(name, city) {
            this.name = name;
            this.city = city;
        };
        
        var nitin = new person('nitin', 'newyork');

