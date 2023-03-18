## Array Question

### Q 1. Create an array called fruits that contains the following elements: "apple", "banana", "orange". Now check if "orange" is in the fruits array.
~~~
const fruits = ["apple", "banana", "orange"];
const checkfruits = fruits.includes("orange")
console.log(checkfruits);
~~~

### Q 2. Given an array of numbers, write a function that returns the sum of all the even numbers in the array.
~~~
const arrNum = [1,2,4,2,3,4,5,5,5,56,67,64,36];
const sum = arrNum.filter((val) => val % 2 === 0).reduce((total, val) => total + val)
console.log(sum)
~~~

### Q 3. Given two arrays of numbers, write a function that returns a new array that contains only the unique elements from both arrays.
~~~
const arr1 = [1,2,3,4,2,3];
const arr2 = [5,6,7,8,5,6];
const arr4 = [];
const arr3 = [];
for(let i = 0; i < arr1.length; i++){
      if(!arr3.includes(arr1[i]) && !arr4.includes(arr2[i])){
         arr3.push(arr1[i])
         arr4.push(arr2[i])
      }
}
const newArr = [...arr3,...arr4];
console.log(newArr);
~~~

### Q 4. Given an array of strings, write a function that returns the longest string in the array.
~~~
const arrStr = ["Hello", "wecode", "academy"];
let strLen = 0;
let longestStr = "";
arrStr.forEach((val) => {
   if(val.length > strLen){
      strLen =  val.length
      longestStr = val;
   }
})
console.log(longestStr)
~~~

### Q 5. Write a function that takes an array of numbers and returns the largest number in the array.
~~~
const arrNum1 = [1,2,4,5,4,5,6,565,67];
let largestNum = 0;
arrNum1.forEach((val)=>{
   if(largestNum < val){
      largestNum = val
   }
})
console.log(largestNum)
~~~

### Q 6. Write a function that takes an array of numbers and returns a new array that only contains the even numbers from the original array.
~~~
const arrNum2 = [1,2,4,5,4,5,6,565,67];
const evenNum1 = arrNum2.filter((val) => val % 2 === 0);
console.log(evenNum1);

function evenNum(arrNum){
   return arrNum.filter((val) => val % 2 === 0)
}
console.log(evenNum([1,2,4,5,4,5,6,565,67]))
~~~

### Q 7. Write a function that takes an array of strings and returns a new array that only contains strings with more than 5 characters.
~~~
function arrStr1(arrStr){
   return arrStr.filter((str) => str.length > 5)
}
console.log(arrStr1(["Hello","wecode","academy"]))
~~~

### Q 8. Write a function that takes two arrays of numbers and returns a new array that contains the intersection of the two arrays (i.e. only the numbers that appear in both arrays).
~~~
function intrOfArr(arrNum1, arrNum2){
   return arrNum1.filter((num) => arrNum2.includes(num));
}
console.log(intrOfArr([1,2,3,4],[9,8,7,3,2]))
~~~

### Q 9. Write a function that takes an array of numbers and returns a new array where each element is the square of the original element
~~~
function squareEle(arrNum){
   return arrNum.map((num) => num ** 2);
}
console.log(squareEle([1,2,3,4]))
~~~

### Q 10. Write a function that takes an array of numbers and returns the average of all the numbers in the array.
~~~
function averageArr(arrNum){
   return arrNum.reduce((total, val) => total + val) / arrNum.length;
}
console.log(averageArr([1,2,3,4,5]));
~~~

### Q 11. Write a function that takes an array of numbers and returns a new array that only contains numbers that are greater than 5. Use filter function.
~~~
function newArr1(arrNum){
   return arrNum.filter((num) => num > 5);
}
console.log(newArr1([1,2,3,4,5,6,7,8,9]));
~~~

### Q 12. Write a function that takes an array of numbers and returns a new array where each element is the original element plus 1. use map function.
~~~
function numPlus(arrNum){
   return arrNum.map((num) => num + 1);
}
console.log(numPlus([1,2,3,4,5,6,7,8,9]));
~~~

### Q 13. Write a function that takes an array of numbers and returns a new array that contains only the unique numbers using reduce.
~~~
function uniqueNum(arrNum){
   const newArr = [];
   arrNum.forEach((num)=>{
      if(!newArr.includes(num)){
         newArr.push(num)
      }
   })
   return newArr;
}
console.log(uniqueNum([1,2,3,4,5,6,7,1,2,3]));
~~~

### Q 14. Write a function that takes an array of strings and returns the total number of characters in all the strings using reduce.
~~~
function arrStr2(arrStr){
   return arrStr.reduce((total, str) => {
           return total + str.length;
   },0)
}
console.log(arrStr2(["Hello","wecode","academy"]));
~~~

### Q 15. Write a function that takes an array of strings and sorts them by their length in ascending order.
~~~
function sortStringsByLength(arrStr){
  return arrStr.sort((a,b)=> a.length - b.length);
}
console.log(sortStringsByLength(["apple", "banana", "cherry", "date"]));
~~~

### Q 16. Write a function that takes an array of numbers and returns the second highest number.
~~~
function secHighestNum(arrNum){
   let hNum = 0;
   let seNum = 0;
   for(let i = 0; i < arrNum.length; i++){
      if(hNum < arrNum[i]){
         seNum = hNum;
         hNum = arrNum[i];
      }else{
         seNum = arrNum[i]
      }
   }
return seNum;
}
console.log(secHighestNum([1,4,5,8,7,6,10,9,9]));
~~~

### Q 17. Write a function that takes an array of numbers and returns a new array with all the unique numbers.
~~~
function uniqueNum(arrNum){
   const newArr = [];
   arrNum.forEach((num) => {
      if(!newArr.includes(num)){
         newArr.push(num);
      }
   });
   return newArr;
}
console.log(uniqueNum([1,2,3,4,5,3,4,5]));
~~~

### Q 18. Write a function that takes an array of strings and returns a new array with only the strings that contain the letter "a".
~~~
function arrStr3(arrStr){
   return arrStr.filter((str) => str.includes("a"));
}
console.log(arrStr3(["Hello","wecode","academy"]));
~~~

### Q 19. Write a function that takes an array of numbers and returns a new array with the numbers sorted in ascending order.
~~~
function arrNum21(arrNum){
   return arrNum.sort((a,b) => a - b);
}
console.log(arrNum21([1,4,5,8,7,6,10,9,9]));
~~~

### Q 20. Write a function that takes an array of strings and flattens each string into an array of characters, then flattens the result into a single array.
~~~
function array(arr){
   return arr.flatMap((val) => val.split(""));
}
console.log(array(['hello', 'world']));
~~~