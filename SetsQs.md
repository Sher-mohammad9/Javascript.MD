## Sets Questions

### Q 1. Create an empty set called mySet.
~~~
const mySet = new Set();
~~~

### Q 2. Add the values 1, 2, and 3 to mySet.
~~~
mySet.add(1).add(2).add(3);
~~~

### Q 3. Check if mySet contains the value 2.
~~~
console.log(mySet.has(2))
~~~

### Q 4. Remove the value 3 from mySet.
~~~
mySet.delete(3);
console.log(mySet)
~~~

### Q 5. Find the size of mySet.
~~~
console.log(mySet.size);
~~~

### Q 6. Create a new set called otherSet containing the values 2, 3, and 4.
~~~
const otherSet = new Set();
otherSet.add(2).add(3).add(4);
console.log(otherSet);
~~~

### Q 7. Find the intersection of mySet and otherSet.
~~~
const intOfSets = new Set();
otherSet.forEach((value)=>{
   if(mySet.has(value)){
      intOfSets.add(value);
   }
});
console.log(intOfSets);
~~~

### Q 8. Find the union of mySet and otherSet.
~~~
otherSet.forEach((val)=>{
      if(!mySet.has(val)){
            mySet.add(val)
      }
});
console.log(mySet)

let arr = [...mySet,...otherSet]
const newSet = new Set(arr)
console.log(newSet)
~~~

### Q 9. Find the difference of mySet and otherSet.
~~~
const diffOfSets = new Set()

if(otherSet.size >= mySet.size){
   otherSet.forEach((val)=>{
      if(!mySet.has(val)){
         diffOfSets.add(val);
      }
   })
}else{
   mySet.forEach((val)=>{
      if(!otherSet.has(val)){
         diffOfSets.add(val);
      }
   })
}

console.log(diffOfSets)
~~~

### Q 10. Find the symmetric difference of mySet and otherSet.
~~~
const symDiffOfSets = new Set()

otherSet.forEach((val1)=>{
   for(let val2 of mySet){
      if(!otherSet.has(val2)){
            symDiffOfSets.add(val2)
      }
      if(!mySet.has(val1)){
            symDiffOfSets.add(val1)  
      }
   }
});

console.log(symDiffOfSets)
~~~

### Q 11. Create an array called myArray containing the values 1, 2, 2, and 3.
 ~~~
 const myArray = [1,2,2,3];
~~~

### Q 12. Convert myArray to a set called mySet2.
 ~~~
 const mySet2 = new Set(myArray);
 ~~~

### Q 13. Check if mySet2 contains the value 2.
 ~~~
 console.log(mySet2.has(2))
 ~~~

### Q 14. Remove all duplicate values from myArray and store the result in a new array called uniqueArray.
~~~
const  newSet11 = new Set(myArray)
const uniqueArray = [...newSet11];
~~~

### Q 15. Convert uniqueArray to a set called uniqueSet.
~~~
const uniqueSet = new Set(uniqueArray);
~~~

### Q 16. Add the value 4 to uniqueSet.
~~~
uniqueSet.add(4);
~~~

### Q 17. Remove the value 3 from uniqueSet.
~~~
uniqueSet.delete(3);
~~~

### Q 18. Check if uniqueSet is a subset of mySet.
~~~
let subset = true;
uniqueSet.forEach((val)=>{
   if(!mySet.has(val)){
      subset = false;
   }
})
console.log(subset)
~~~

### Q 19. Check if mySet is a superset of uniqueSet.
~~~
let superSet = true;
uniqueSet.forEach((val)=>{
   if(!mySet.has(val)){
      superSet = false;
   }
})
console.log(superSet)
~~~
### Q 20. Find the difference between mySet and uniqueSet.
~~~
const mySet = new Set([1,2,3,4,5]);
const uniqueSet = new Set([1,2,3]);
const diff = [...mySet].filter((ele) => !uniqueSet.has(ele));
console.log(diff)
~~~
