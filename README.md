# Baby-Steps-for-Javascript-and-ES6
This repository is for latest ES6 helper methods and new function implemented in standard version of javascript 

#ES6 foreach(for better code)
```javascript 
//foreach loop 
let colors = ['red','green','blue'];
//for accessing element
colors.forEach(element = > {
console.log(element);}) 
//output 
// red
// green
//blue

//passing parameters element and index

colors.forEach((color,index)=>{
console.log(`${index} : ${color}`;)
})
//output
// 0 : red
// 1: green
// 2 : blue

//function can be reused when we use forEach 
//for eg:

//this function color1() canbe reused again in another steps
function color1(element)
{
console.log(element);}

colors.forEach(color1) ; // pass refrence of color1 function
```
