# Modern Future 

### Q1 Write a function that takes a string and returns a new string with all the words reversed using the spread operator.

~~~
function revstr([...str]){
  return str.reverse().join("");
}
console.log(revstr("WeCode Academy"))
~~~

### Q2 Create a function that takes in an array and uses the rest operator to remove the first element from the array and finally return the array without first element.

~~~
function resArr(arr){
  let [,...a] = arr;
  return a;
}
console.log(resArr([1,2,3,4,5]));
~~~

### Q3 Create a function that takes an unknown number of arrays and uses the rest operator to flatten them into a single array.

~~~
function faltArr(...arr){
 return arr.flat();
}
console.log(faltArr([1,2,3,4,5],[6,7,8,9],[10,1,12,13,14,15]));
~~~

### Q4 Write a function that takes an object as a parameter and returns the value of its "x" property if it exists, otherwise it returns null. Hint : (Use optional chaining)

~~~
function obj(obj){
 return obj?.x || null;
}
console.log(obj({name : "hello",x:10}));
~~~

### Q5 Write a function which takes in an array and create two separate arrays for odd numbers and even numbers and finally merge them in the order that all odd numbers will move to the left of the array and all even numbers to right of the array.

~~~
function oddEven(arr){
  let newArr = [];
  arr.forEach((val) => val % 2 === 0 ? newArr.push(val) : newArr.unshift(val));
  return newArr;
}
console.log(oddEven([1,2,3,4,5,6,7,8]));
~~~

### Q6 Create an array of numbers. Now change the position of each element with their next element.

~~~
function posiChange(arr){
  let newArr = [];
  for(let i = 0; i < arr.length; i++){
    if(!newArr.includes(arr[i])){
      if(arr[i+1]){
        newArr.push(arr[i+1]);
     }
        newArr.push(arr[i])
   }
}
  return newArr;
}
console.log(posiChange([1,2,3,4,5,6,7]));
~~~

### Q7 Ask user below questions
What is your age  : 12
What is your mobile : 9581894461
What is your address : Jaipur
Now create an object and use enhanced object literal property computation to create below object


~~~
  let age = Number(prompt('What is your age ?'));
  let mobileNumber = Number(prompt('What is your mobile number ?'));
  let address = prompt('What is your address ?');
  let obj = {
    ['age'+age] : age,
    [mobileNumber] : 'mobileNumber',
    [address+age+'address'] : address
  }
console.log(obj) 
~~~

### Q8 Using enhanced object literal function, create a function sum which takes an array as parameter and return sum of all the numbers in the array.

~~~
function sum(arr){
    return arr.reduce((total,val)=> total+val)
}
console.log(sum([1,2,3,4,5]))
~~~

### Q9 Take a number and check if number is greater than 80 or not. If yes then assign 100 to number else assign 200. Use short circuiting whereever possible.

~~~
let num  = 40;
num = num > 80 && 100 || num < 80 && 200
console.log(num)
~~~

### Q10 Create an array of 10 numbers. Now create a new array of 0 and 1 using Array destructring based on if number is odd then 1 else 0

~~~
let arr = [1,2,3,4,5,6,7,8,9,10];
let newArr = [];
for(let val of arr){
   val % 2 === 0 ? newArr.push(0) : newArr.push(1); 
}
console.log(newArr)
~~~

### Q11 Given an array of price, use map function to return a new array where each price is converted to new price including tax, which is the price with a 10% tax added.

~~~
let arr = [1,2,3,4,5,6,7,8,9,10];
let newArr = arr.map((val)=> val + val / 10)
console.log(newArr)
~~~

### Q12 Given an array of strings, use reduce to return the total number of characters in all the strings.

~~~
let str = "WeCode Academy";
let newArr = str.split(" ").reduce((total,val)=> total + val.length,0);
console.log(newArr)
~~~

### Q13 Given an array of strings, use map and reduce to return the total number of characters in all the strings with a length less than 5.

~~~
let str = "Hell WeCode Academy rr";
let sum = 0;
str.split(" ").map((val)=> val.length < 5 ? sum += val.length : val);
console.log(sum)
~~~

### Q14 Given an array of numbers, use map, filter, and reduce to return the sum of all the odd numbers multiplied by 3

~~~
let arr = [1,2,3,4,5,6];
let sumMultiple = arr.filter((val)=> val % 2 !== 0).map((val)=>  val*3).reduce((total,val)=>total+val)
console.log(sum)
~~~

### Q15 Given a string, reverse the order of the words in the string. For example, "the quick brown fox" becomes "fox brown quick the".

~~~
let str = "the quick brown fox";
let revStr = str.split(" ").reverse().join(" ");
console.log(revStr);
~~~
