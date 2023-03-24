# Object Question

### Q 1.Write a function that takes an object as an input and returns a new object with the same keys and values, but with all the string values capitalized.
~~~
let obj = {
   name : "hassan",
   address : "merta",
   village : "karakwal",
   pincode : 1233455666
}
 
function test(obj){
let newObj = {};
for(let arr of Object.entries(obj)){
    if(typeof arr[1] === "string"){
      newObj[arr[0]] = arr[1].charAt(0).toUpperCase().concat(arr[1].slice(1));
    }
}
console.log(newObj)
}
test(obj);
~~~

### Q 2. Write a function that takes two objects as inputs and returns a new object that contains only the keys that are present in both objects, along with their corresponding values from the first object.
~~~
function takeObj(...objArr){  
    let newObj = {};
    for(let val1 of Object.entries(objArr[0])){
      for(let i=1; i < objArr.length; i++){
         for(let val2 of Object.entries(objArr[i])){
            if(val1[0] === val2[0]){
               newObj[val1[0]] = val1[1];
            }
         }
      }
    }
   console.log(final);
}

takeObj({name : "hassan", city : "merta", villge : "karakwal"},{name1 : "Abbas", city : "merta", villge : "karakwal", pincode : 1234567},{name:"fvee",city:"fwefwf"});
~~~

### Q 3. Write a function that takes an array of objects as an input and returns a new array that contains only the objects that have unique values for a specified key. For example, if the input array contains objects with a "name" key, the function should return an array of objects with unique names.
~~~
function takeObj(objArr){
    let newObj = {};
    objArr.forEach((obj)=> {
      if(obj.name){
         newObj[obj.name] = obj
      }
    });
    console.log(Object.values(newObj));
}

takeObj([{name:"sher mohammad", city : "merta", villge : "karakwal"},{name : "hassan", city : "merta", villge : "karakwal", pincode : 1234567},{name:"sher mohammad",city:"jaipur"}])
~~~

### Q 4. Write a function that takes an object as an input and returns an array of all the keys in the object, sorted alphabetically.
~~~
function orderBy(obj){
   let obj1 = Object.keys(obj).sort();
    console.log(obj1)
}
orderBy({name:"hassan",mobile:43434,address:"jaipur"})
~~~

### Q 5. Write a function that takes an object and a string as input and returns a new object with all the keys that start with the specified string. The original object should not be modified.
~~~
function objStr(obj,str){
   let obj1 = Object.entries(obj);
   let newObj = {}
    obj1.forEach((val)=>{
     if(val[0].startsWith(str)){
        newObj[val[0]] = val[1];
     }
 });
    console.log(newObj);
}
objStr({name:"hassan",mobile:43434,address:"jaipur"},"mobile")
~~~

# Array Questions

### Q 1. Write a function that takes an array of strings as an input and returns a new array where each string has been capitalized (i.e. the first letter of each word is capitalized).
~~~
function capString(arrStr){
   return arrStr.reduce((str,val)=> {
      return str += val.charAt(0).toUpperCase().concat(val.slice(1), " ");
   },"")
}
console.log(capString(["hello","wecode","academy"]));
~~~

### Q 2. Write a function that takes an array of numbers as an input and returns the highest product of any three numbers in the array.
~~~
function pruNum(arrNum){
   let fhN = arrNum[0];
   let shN = 0;
   let thN = 0;
   for(let val of arrNum){
     if(fhN < val){  
      let tmp = fhN;
      let tmp1 = shN;
      fhN = val;
      shN = tmp;
      thN = tmp1;
   }else if(shN < val && val < fhN){
         shN = val;
   }else if(thN < val && val < shN){
         thN = val;
    } 
}
console.log(fhN * shN * thN);
}
pruNum([1,2,3,4,5,6,7,8,8,6,9,12,10,9]);
~~~

### Q 3. Write a function that takes two arrays as inputs and returns a new array that contains only the elements that are present in both arrays, with no duplicates.
~~~
function uniqueEle(arr1, arr2){
   let newArr = [];
   arr1.forEach((val1)=>{
      for(let val2 of arr2){
         if(val1 === val2){
           if(!newArr.includes(val1) && !newArr.includes(val2)){
            newArr.push(val1);
           }   
         }
          }
   });
   console.log(newArr);
}
uniqueEle([1,2,3,4,1,2,3],[7,6,5,4,3,2,1]);
~~~

### Q 4. Write a function that takes an array of strings as an input and returns a new array that contains only the strings that are palindromes (i.e. they are the same forwards and backwards).
~~~
function palindrom(arrStr){
   return arrStr.filter((str,ind,arr) => [...str].reverse().join("") === arr[ind]);
}
console.log(palindrom(["ababa","dd","fefeee","fvgre","madam"]))
~~~

### Q 5. Write a function that takes an array of numbers as an input and returns a new array where each number has been multiplied by 2 if it is even, or by 3 if it is odd.
~~~
function multiple(arrNum){
   return arrNum.map((num)=>{
      if(num % 2 === 0){
         return num * 2;
      }else{
         return num * 3;
      }
      });
}
console.log(multiple([1,2,3,4,5,6,7]));
~~~

# Set Questions
 
### Q 1. Write a function that takes an array of Sets as an input and returns a new Set that contains only the elements that are present in all of the Sets.

~~~
let set1 = new Set([1,2,3,4,5]);
let set2 = new Set([2,3,4,5,6]);
let set3 = new Set([3,4,5,6]);
let arr = [set1,set2,set3];

function stesAll(arr){
   let newSet = new Set();
   let peEleSte = new Set();
   for(let val1 of arr){
      newSet = new Set([...newSet, ...val1]);
   }
    newSet.forEach((val2)=>{
      let flag = true;
      for(let val3 of arr){
           if(!val3.has(val2)){
              flag = false;
           }
      }
           if(flag){
            peEleSte.add(val2)
           }
    })
console.log(peEleSte);
}
stesAll(arr)
~~~ 

### Q 2. Write a function that takes an array of numbers as an input and returns a new Set that contains only the numbers that are odd.

~~~
function setOdds(arr){
   let newSet = new Set();
   let newArr = arr.filter((num) => num % 2 !== 0);
   newSet = new Set(newArr)
   console.log(newSet);
}
setOdds([1,2,3,4,5,6]);
~~~

### Q3. Write a function that takes two Sets as inputs and returns a new Set that contains only the elements that are present in the first Set but not the second.

~~~
function towSet(set1, set2){
   let newSet = new Set([...set1]);
   console.log(newSet)
}
towSet(new Set([1,2,3,4,5], new Set([6,5,4,3,2,1])));
~~~

### Q 4. Write a function that takes an array of Sets as an input and returns a new Set that contains only the unique elements across all of the Sets.

~~~
let set1 = new Set([1,2,3,4,5]);
let set2 = new Set([2,3,4,5,6]);
let set3 = new Set([3,4,5,6]);
let arr = [set1,set2,set3];

function dd(arrSet){
   let newSet = new Set();
   arrSet.forEach((val)=> {
      newSet = new Set([...newSet, ...val])
   });
   console.log(newSet);
}
console.log(dd(arr))
~~~

### Q 5. Write a function that takes two Sets as inputs and returns a new Set that contains only the elements that are present in the first Set and the second Set, but not in both.

~~~
let set1 = new Set([1,2,3,4,5]);
let set2 = new Set([2,3,4,5,6]);
let set3 = new Set([1,2,3,4,5,6,7])
let arr = [set1,set2];

function checkSteEle(...sets){
   let newSet = new Set();
    sets[0].forEach((val1)=>{
         for(let val2 of sets){
           for(let val3 of val2){
            if(!val2.has(val1)){
               newSet.add(val1);
            }
            if(!sets[0].has(val3)){
               newSet.add(val3)
            }
         }
         }
    })
   console.log(newSet)
}
checkSteEle(set1,set2,set3)
~~~

# Map Questions

### Q 1. Write a function that takes two Maps as inputs and returns a new Map that contains only the keys that are present in both Maps, with the corresponding values from the first Map.

~~~
let map1 = new Map([[1,243],[3,433],[11,"hassan"]])
let map2 = new Map([[7,2],[6,4],[5,6],[11,"hassan"]]);
let map3 = new Map([[9,2],[8,4],[7,6],[5,8],[9,10],[11,"hassan"]])

function checkMap(...map){
   let newMap = new Map();
   for(let val1 of map[0].entries()){;
       for(let val2 of map){
         for(let val3 of val2.entries()){
            if(map[0].has(val3[0])){
               newMap.set(val1[0], val1[1]);
            }
         }
       }
   }
   console.log(newMap)
}
checkMap(map1,map2,map3);
~~~

### Q 2. rite a function that takes a Map of numbers as an input and returns a new Map where each key is the square root of the corresponding key in the input Map, and the value is the square of the corresponding value in the input Map.

~~~
let map = new Map([[1,1],[4,3],[9,5]])

function squareRoot(map){
   let newMap = new Map();
   [...map].forEach((arr) => {
      newMap.set(Math.sqrt(arr[0]), arr[1] * 2)
   })
   console.log(newMap);
}
squareRoot(map);
~~~

### Q 3. Write a function that takes two Maps as inputs and returns a new Map that contains only the keys that are present in both Maps, with the corresponding values from the second Map.

~~~
let map1 = new Map([[1,243],[3,433],[11,"hassan"]])
let map2 = new Map([[7,2],[6,4],[5,6],[11,"hassan"]]);
let map3 = new Map([[9,2],[8,4],[7,6],[5,8],[9,10],[11,"hassan"]])

function checkMap(...map){
   let newMap = new Map();
   for(let val1 of map[1].entries()){;
       for(let val2 of map){
         for(let val3 of val2.entries()){
            if(map[1].has(val3[0])){
               newMap.set(val1[0], val1[1]);
            }
         }
       }
   }
   console.log(newMap)
}
checkMap(map1,map2,map3);
~~~

### Q 4. Write a function that takes a Map of numbers as an input and returns the sum of the values of all of the even keys in the Map.

~~~
let map1 = new Map([[1,243],[3,433],[11,"hassan"]])

function checkMap(map){
   let sum = 0;
   [...map].forEach((val) => sum += val[0]);
   console.log(sum)
}
checkMap(map1);
~~~

### Q 5. rite a function that takes a Map of strings as an input and returns a new Map where each key is a letter and the value is the number of times that letter appears in the values of the input Map.

~~~
let map1 = new Map([["m","mohammad"],["k","khan"],["a","hassan"]])

function checkMap(map){
   let newMap = new Map();
   [...map].forEach((val1) => {
      let count = 0;
      for(let i = 0; i < val1[1].length; i++){
        if(val1[0] === val1[1][i]){
         count++
        }
      }
      newMap.set(val1[0],count);
   });
   console.log(newMap)
}
checkMap(map1);
~~~