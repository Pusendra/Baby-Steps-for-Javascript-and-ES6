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



#The 'map' Helper
```javascript
//'map' helper

let numbers = [2,3,4];
//double the numbers of array using map without creating new array

let doubled = numbers.map(number =>{
//map must have return keyword to operate
return number *2 ;
});
doubled; //output : [4,6,8]

//where to use map 
let cars = [{model : "audi" , price : "cheap"},{model:"tata", price : "expensive"}];
//how to get the price list of all cars?
//using map to solve this
let priced = map.cars(car =>{
return car.price;
})
priced; //output ["cheap", "expensive"]
```

# find helper
```javascript

let users = [{name : 'bob'}, {name : 'ram'}, {name : 'shyam'}];

//using find to find the particular username in array

users.find(user =>{
//output : {name : 'ram'}
return  user.name === 'ram';
})

//Drawbacks of find helper : find helper stops as soon as the value specied in the return statement is found,
//In the example below there are two name :'ram' but the find helper stops as soon as it found the name :'ram', id : 1 at user[1]
//and dosenot search for further expression

let users = [{name : 'bob'}, {name : 'ram' , id :1}, {name : 'shyam'},{name : 'ram'}];

users.find(user =>{
//output : {name : 'ram' , id :1} 
return  user.name === 'ram';
});


//complex example find helper

let posts = [{id : 1, title : "new post"},{id : 2 , title : "old post"}];
let  comment = {postId : 1 , content : "great post"};

function postForComment(posts,comment){
return posts.find(function(post){
return posts.id === comment.postId;
})
};
postForComment(posts,comment); //output : {id : 1, title : "new post"}


```
