# Java script interview questions and answer

## 1. var vs let const

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
