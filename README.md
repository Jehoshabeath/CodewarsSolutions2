* https://www.codewars.com/kata/create-phone-number/train/javascript

```javaScript```

Create Phone Number

function createPhoneNumber(numbers){
  let formatPhone = [];
  for(let i=0; i<numbers.length; i++){
    if(i === 0){
      formatPhone.push('(' + numbers[i]);
    } else if(i === 2){
      formatPhone.push(numbers[i] + ')');
    } else if(i === 3){
      formatPhone.push(' ' + numbers[i]);
    } else if(i === 5){
      formatPhone.push(numbers[i] + '-');
    } else {
      formatPhone.push(numbers[i]);
    }
}
return formatPhone.join('');
}   

* https://www.codewars.com/kata/credit-card-issuer-checking/train/javascript

 ```javaScript```
 
 Credit card issuer checking
 
 function getIssuer(number) {
   if (/^3[4|7]\d{13}$/.test(number)) return 'AMEX'
   if (/^6011\d{12}$/.test(number)) return 'Discover'
   if (/^5[1-5]\d{14}$/.test(number)) return 'Mastercard'
   if (/^4(\d{12}|\d{15})$/.test(number)) return 'VISA'
   return 'Unknown'
 }
 
 *https://www.codewars.com/kata/remove-string-spaces/train/javascript
 
 ```javaScript```
 
  Remove String Spaces
  
  function noSpace(x){
   return x.replace(/\s/g, ''); 
  }
  
  * https://www.codewars.com/kata/get-list-sum-recursively/train/javascript/5d158f3306317c0022af2122
  
  ```javaScript```
  
  Get list sum recursively
  
  function sumR(x) {
    if(x.length === 0){
    return 0;
    }else{
    return x.shift () + sumR(x);
    }
  }
  
  * https://www.codewars.com/kata/do-i-get-a-bonus/train/javascript
  
  ```javaScript```
  
  Do I get a bonus?
  
  function bonusTime(salary, bonus) {
    return bonus ? `£${10 * salary}` : `£${salary}`;
  }
  
  * https://www.codewars.com/kata/initialize-my-name/train/javascript/5d182fca0fb98b001c583d46
  
  ```javaScript```
  
  Initialize my name
  
  function initializeNames(name){
    let arr = name.split(' ');
     for (let i = 1; i < arr.length - 1; i++) 
         arr[i] = arr[i].charAt(0) + '.';
     return arr.join(' ');
  }
  merge branch 
  
  * https://www.codewars.com/kata/returning-strings/train/javascript
  
  ```javaScript```
  
  Returning Strings
  
  function greet(name){
    return `Hello, ${name} how are you doing today?`;
  }
  
  * https://www.codewars.com/kata/string-ends-with/train/javascript/5d22c23d3c70c00021be4fd1
  
  ```javaScript```
  
  String ends with?
  
  function solution(str, ending){
   return str.endsWith(ending);
  }
  
  * https://www.codewars.com/kata/spongebob-meme/train/javascript
  
  ```javaScript```
  
  sPoNgEbOb MeMe
  
  function spongeMeme(s) {
    let str = '';
    for(let i = 0; i < s.length; i++){
      if(i % 2 == 0){ str += s[i].toUpperCase();
      }else{ str += s[i].toLowerCase();
      }
  }
  return str;
  }
  
  * https://www.codewars.com/kata/print-a-rectangle-using-asterisks/train/javascript
  
  ```javascript```
  
  Print a Rectangle Using Asterisks
  
  function getRectangleString(w, h) {
    if (w === 1&&h === 1) return '*\r\n'
    if (w === 1&&h === 2) return '*\r\n*\r\n'
      let start = '*' . repeat(w) + '\r\n'
      let mid = '*'+' '.repeat(w - 2) +'*'+'\r\n'
      let end = mid.repeat(h - 2)
    return start + end + start;
  }
  * https://www.codewars.com/kata/maximum-triplet-sum-array-series-number-7/train/javascript
  
  ```javaScript```
  
  Maximum Triplet Sum (Array Series #7)
  
  function maxTriSum(numbers){
    let sum = 0;
      let res = numbers.sort((a, b) => b - a);
      let arr = [];
      for(let i = 0; i < res.length; i++){
        if (arr.length >= 3){
          break
          }
          if(!arr.includes(res[i])){
            arr.push(res[i]);
            sum += res[i];
            }
          }
         return sum;
         
  }
  
  *https://www.codewars.com/kata/string-average/train/javascript
  
  ```javaScript```
  
  String average
  
  function averageString(str) {
    let num = 'zero,one,two,three,four,five,six,seven,eight,nine'.split(',');
    let arr = str.split(/\s/);
    let all = arr.map(s =>num.indexOf(s));
    let avg = all.reduce((a,b) => a + b,0)/arr.length;
    let na = 'n/a';
    return all.some(n =>n<0) ? na : num[Math.floor(avg)] || na;
    
  }
  
  *https://www.codewars.com/users/Favor/completed_solutions
  
  ```javaScript```
  
  Ordering the words!
  
  function orderWord(s){
   return !s||s.length==0?"Invalid String!":s.split('').sort().join('')
  }
  
  * https://www.codewars.com/kata/numerical-palindrome-number-5-1/train/javascript
  
  ```javaScript```
  
  Numerical Palindrome #5
  
  function palindrome(num) { 
    if(typeof num !== 'number' || num < 0) return "Not valid";
    if(num < 10) return false;
    num = num.toString().split('').sort();
    console.log(num);
    let count = 0;
    for(let i = 0; i < num.length - 1; i){
     if(num[i] === num[i + 1]){
      count = count + 2;
      i = i + 2;
     }else i++;
    }
    if(num.length === count || num.length === count +1){
    return true;
    }else return false;
    
  }
  
  *https://www.codewars.com/kata/are-we-alternate/train/javascript
  
  ```javaScript```
  
  Are we alternate?
  
  function isAlt(word) {
    let vowels = ['a','e','i','o','u'];
    let letters = word.split('');
    for(let i = 0; i < letters.length - 1; i++) {
      if(vowels.includes(letters[i])) {
          if(vowels.includes(letters[i+1])) {
             return false;
         }
      }
      else {
        if(!vowels.includes(letters[i+1])) {
          return false;
          }
       }
     }
      return true;
  }
  