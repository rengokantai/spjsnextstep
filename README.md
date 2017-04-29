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
functions area reference types, and are passed or returned by reference to one shared original, instead of being passed by value
