# spjsnextstep
## 3. Closure and Hoisting
### 1 What is
```
var publicFunction = function(){
  var pri = 1;
  return pri;
}
cosole.log(pri); //error
```
but functions can return values, and primitive types (such as Strings) are passed by value.
```
var p = publicFunction();
console.log(p);
```
functions area reference types, and are passed or returned by reference to one shared original, instead of being passed by value.

#### what is a closure
A function defined within another function, and then returned by outer function, retains access to any variables that were the inner function was defined, even after the outer function has terminated.

### 3 Surprising Closure Behavior
```
var counter;
var functions = []
var values = [];
var makeReturner = function(value){
  return function(){
    return value;
  }
};

for(counter=0;counter<5;counter++){
  values[counter]=counter;
  functions[counter]=makeReturner(counter);
}
```
