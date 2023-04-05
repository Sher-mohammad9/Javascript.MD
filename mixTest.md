# Object Question

### Q 1.Write a function that takes an object as an input and returns a new object with the same keys and values, but with all the string values capitalized.
~~~
function test(obj){
let newObj = {};
Object.entries(obj).forEach((arr)=> typeof arr[1] === "string" ? newObj[arr[0]] = arr[1].charAt(0).toUpperCase().concat(arr[1].slice(1)) : arr[1]);
console.log(newObj)
}

test({name : "hassan", address : "merta", village : "karakwal", pincode : 1233455666});
~~~

### Q 2. Write a function that takes two objects as inputs and returns a new object that contains only the keys that are present in both objects, along with their corresponding values from the first object.
~~~
function takeObj(...objArr){  
   let newObj = {};
   Object.entries(objArr[0]).forEach((arr) => {
   Object.entries(objArr).forEach((val1)=>{
   Object.entries(val1[1]).forEach((val2)=>{
           if(arr[0] === val2[0]){
             newObj[arr[0]] = arr[1];
           }
         })
       })
    })
   console.log(newObj);
}

takeObj({name : "hassan", city : "merta", villge : "karakwal",},{name1 : "Abbas", city : "merta", villge : "karakwal", pincode : 1234567},{name:"fvee",city:"fwefwf",pincode:3453});

=======================================================================================

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
    objArr.forEach((obj)=> obj.name ? newObj[obj.name] = obj : obj);
    console.log(Object.values(newObj));
}

takeObj([
  { name: "Alice", age: 20 },
  { name: "Bob", age: 30 },
  { name: "Alice", age: 25 },
  { name: "Charlie", age: 35 },
  { name: "Bob", age: 40 }
])
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
    obj1.forEach((val) => val[0].startsWith(str) ? newObj[val[0]] = val[1] : val);
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
   let arr = [arrNum[0],0,0]
   for(let val of arrNum){
     if(arr[0] < val){  
      let tmp = arr[0];
      let tmp1 = arr[1];
      arr[0] = val;
      arr[1] = tmp;
      arr[2] = tmp1;
   }else if(arr[1] < val && val < arr[0]){
         arr[1] = val;
   }else if(arr[2] < val && val < arr[1]){
         arr[2] = val;
    } 
}
console.log(arr[0] * arr[1] * arr[2]);
}
pruNum([1,2,3,4,5,6,7,8,8,6,9,12,10,9]);
~~~

### Q 3. Write a function that takes two arrays as inputs and returns a new array that contains only the elements that are present in both arrays, with no duplicates.
~~~
function uniqueEle(arr1, arr2){
   let newArr = [];
   arr1.forEach((val1)=> arr2.includes(val1) && !newArr.includes(val1) ? newArr.push(val1) : val1);
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
   return arrNum.map((num)=> num % 2 === 0 ? num * 2 : num * 3);
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
    arr.forEach((val3)=> !val3.has(val2) ? flag = false : flag);
    flag ? peEleSte.add(val2) : peEleSte;
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
   let newSet = new Set();
   set1.forEach((val) => !set2.has(val) ? newSet.add(val) : val);
   console.log(newSet)
}
towSet(new Set([1,2,3,4,5,7,8,9]),new Set([6,5,4,3,2,1]));
~~~

### Q 4. Write a function that takes an array of Sets as an input and returns a new Set that contains only the unique elements across all of the Sets.

~~~
function uniqueSet(...arrSet){
   let newSet = new Set();
   arrSet.forEach((val)=> newSet = new Set([...newSet, ...val]));
   console.log(newSet);
}
console.log(uniqueSet(new Set([1,2,3,4,5]),new Set([2,3,4,5,6]),new Set([3,4,5,6])));
~~~

### Q 5. Write a function that takes two Sets as inputs and returns a new Set that contains only the elements that are present in the first Set and the second Set, but not in both.

~~~

function checkSteEle(...sets){
   let newSet = new Set();
    sets[0].forEach((val1)=>{
    sets.forEach((val2)=>{
    val2.forEach((val3)=>{
     !val2.has(val1) ? newSet.add(val1) : val1;
     !sets[0].has(val3) ? newSet.add(val3) : val3;
  }) 
    })
   console.log(newSet)
}
checkSteEle(new Set([1,2,3,4,5]), new Set([2,3,4,5,6]), new Set([1,2,3,4,5,6,7]))

~~~

# Map Questions

### Q 1. Write a function that takes two Maps as inputs and returns a new Map that contains only the keys that are present in both Maps, with the corresponding values from the first Map.

~~~
let map1 = new Map([[1,243],[3,433],[11,"hassan"]])
let map2 = new Map([[7,2],[6,4],[5,6],[11,"hassan"]]);
let map3 = new Map([[9,2],[8,4],[7,6],[5,8],[9,10],[11,"hassan"]])

function checkMap(...map){
   let newMap = new Map();
   map[0].forEach((val1,key)=>{
      map.forEach((val2)=>{
   val2.forEach((val3,key2)=> map[0].has(key2) ? newMap.set(key, val1) : val3)
       });
   });
   console.log(newMap);
}
checkMap(map1,map2,map3);
~~~

### Q 2. rite a function that takes a Map of numbers as an input and returns a new Map where each key is the square root of the corresponding key in the input Map, and the value is the square of the corresponding value in the input Map.

~~~
function squareRoot(map){
   let newMap = new Map();
   map.forEach((val,key) => newMap.set(Math.sqrt(key), val * 2));
   console.log(newMap);
}
squareRoot(new Map([[1,1],[4,3],[9,5]]));
~~~

### Q 3. Write a function that takes two Maps as inputs and returns a new Map that contains only the keys that are present in both Maps, with the corresponding values from the second Map.

~~~
let map1 = new Map([[1,243],[14,"hassan"],[3,433],[11,"hassan"]])
let map2 = new Map([[7,2],[6,4],[14,"Mo"],[5,6],[11,"hassan"]]);
let map3 = new Map([[7,6],[5,8],[9,10],[14,"hassan"],[11,"hassan"]])

function checkMap(...map){
   let newMap = new Map();
   map[1].forEach((val1, key1)=>{
   let flag = true;
   map.forEach((val2,key2)=> val2.has(key1) ? key1 : flag = false);
      flag ? newMap.set(key1, val1) : key1;
   })
   console.log(newMap)
}
checkMap(map1,map2,map3);

~~~

### Q 4. Write a function that takes a Map of numbers as an input and returns the sum of the values of all of the even keys in the Map.

~~~
let map1 = new Map([[1,243],[3,433],[11,"hassan"]])

function checkMap(map){
   let sum = 0;
   map.forEach((val,key) => sum += key);
   console.log(sum)
}
checkMap(map1);
~~~

### Q 5. rite a function that takes a Map of strings as an input and returns a new Map where each key is a letter and the value is the number of times that letter appears in the values of the input Map.

~~~
let map1 = new Map([['m,'mohammad'],['k,'khan'],["a","hassan"]]);

function checkMap(map){
   let newMap = new Map();
   map.forEach((val,key) => {
      let count = 0;
      for(let i = 0; i < val.length; i++){
        if(key === val[i]){
         count++
        }
      }
      newMap.set(key,count);
   });
   console.log(newMap)
}
checkMap(map1);
~~~