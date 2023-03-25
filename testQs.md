# Test Question
### Q 1.Write a JavaScript program to check whether a string "Code" presents at 5th (index 4) position in a given string, if "Code" presents in the string return the string without "Code" otherwise return the original one.
~~~
function string(str){
if(str.toLowerCase().indexOf("code") === 4){
    return str.substring(0,4).concat(str.slice(8))
}else{
    return str;
}   
}
console.log(string("Hellcode academy"));
~~~

### Q 2. Write a JavaScript program to capitalize the first letter of each word of a given string.
~~~
function string2(str){
   return str.split(" ").reduce((str, word)=>{
      return  str += word.charAt(0).toUpperCase().concat(word.slice(1)," ");
   },"");
}
console.log(string2('the quick brown fox'));
~~~

### Q 3. Write a JavaScript program to check whether all the digits in a given number are the same or not.
~~~
let num1 = 333;
let num2 = num1;
let num3 = "";
while(num1 > 0){
  num3 += num1 % 10;
  num1 = parseInt(num1/10);
}
num2 === +num3 ? console.log("yes") : console.log("no");
~~~

### Q 4. Write a JavaScript function that reverse a number.
~~~
let num4 = 123;
let revrseNum = "";
while(num4 > 0){
  revrseNum += num4 % 10;
  num4 = parseInt(num4/10);
}
console.log(+revrseNum)
~~~

### Q 5. Write a JavaScript function to extract unique characters from a string.
~~~
function uniqueStr(str){
   let newStr = "";
   for(let char of str){
      if(!newStr.includes(char)){
         newStr += char;
      }
   }
   return newStr;
}
console.log(uniqueStr("thequickbrownfoxjumpsoverthelazydog"));
~~~

### Q 6. Write a JavaScript function to chop a string into chunks of a given length. Test Data.
~~~
function string_chop(str, chop){
   let strToArr = [];
    if(str && !chop){
      strToArr.push(str);
    }else if(str && chop){
      for(let i = 0; i < str.length; i += chop){
         strToArr.push(str.substring(i, i + chop));
      }
    }
    return strToArr;
}
console.log(string_chop('w3resource'));
console.log(string_chop('w3resource',2));
console.log(string_chop('w3resource',3));
~~~

### Q 7. Write a JavaScript function to find a word within a string. Test Data.
~~~
function search_word(str, word){
 let count = 0;
 for(let i=0; i < str.length; i++){
   if(str[i] + str[i+1] === word || str[i] + str[i+1]+ str[i+2] === word){
      count++;
   }
 }
 return count;
}
console.log(search_word('The quick brown fox', 'fox'));
console.log(search_word('aa, bb, cc, dd, aa', 'aa'));
~~~

### Q 8. Create an array of numbers. Now filter out all the numbers from the array where number is in between 30-50. After filtering the numbers, add 20 to each number and finally print the sum of all numbers using reduce function.
~~~
function arrNum(arr){
   return arr.filter((num) => num >= 30 && num <= 50).map((num) => num + 20).reduce((total, num) => total + num);
}
console.log(arrNum([40,40,25,35,55]));
~~~

### Q 9. Convert below array
~~~
const arr1 = [[1,2], [3,4], [5,6], [7,8], [9,10]];
const arr2 = arr1.flatMap((arr)=> arr[0] + arr[1]);
console.log(arr2);
~~~

### Q 10. Print below pattern;
~~~
for(let i = 1; i <= 5; i++){
   let str = "";
   for(let j = 1; j <= i-1; j++){
      str += " ";
   }
   for(let l = i; l <= 5; l++){
      str += l + " ";
   }
   console.log(str);
}
~~~