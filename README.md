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
      console.log(num);  // num = 20
    }


### Use of let

    function show(){
      let num =10;
        console.log(num);  // num =  10
      if(true){
       var num = 20;       // error
        console.log(num); 
      }
      console.log(num);  // num = 20
    }

### Use of const

    function show(){
      const num =10;
        console.log(num);  // num =  10
      if(true){
       var num = 20;       // error
        console.log(num); 
      }
      console.log(num);  // num = 20
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

## 5. proptotype in javascript

    var employee = function(){};

    employee.prototype.name = "n/a"
    employee.prototype.age = "0"

    var nitin = new employee();

    console.log(nitin.city); -->  n/a

    nitin.name = 'Nitin';
    employee.prototype.sayHello = function() { return 'Hello '+ this.name};

    nitin.sayHello()  ---> Hi, Nitin

## 6. Call in javascript

    var myObj = {
	name: 'Nitin'
    }

    var sayHello = function() {
        return 'Hello ' + this.name;
    }

    sayHello();

    sayHello.call(myObj);	----> Hello Nitin

next example,


	var myObj = {
	num: 2
	}

	var myFunc = function (add) {

		return this.num + add;
	}

	myFunc()  ----> NaN

	myFunc(2) ----> NaN

	myFunc.call(myObj, 2); ----> 4

next example,

	var myObj = {
	num: 2
	}


	var myFunc1 = function (num1, num2) {

		return this.num + num1 + num2;
	}

	myFunc1.call(myObj, 2, 3);


## 7. apply in javascript

	var myObj = {
	num: 2
	}


	var myFunc1 = function (num1, num2) {

		return this.num + num1 + num2;
	}

	myFunc1.apply(myObj, [2, 3]);

## 8. bind in javascript

	var myObj = {
	num1: 2,
	num2: 3,
	}

	var myFunc = function () {
		return this.num1 + this.num2;
	}

	myFunc();

	var added = myFunc.bind(myObj);
	
	added();  ---> 5

## 9. class in javascript

	class person {
		constructor(name, age) {
			this.name = name;
			this.age = age;
		}

		sayHello() {
			return 'Hello, ' + this.name;
		}
	}

	var james = new person('James', 30);	
