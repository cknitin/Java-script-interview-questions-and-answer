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
