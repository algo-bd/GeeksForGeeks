### [Sum the digits of a given number in single statement](http://www.geeksforgeeks.org/how-can-we-sum-the-digits-of-a-given-number-in-single-statement/)

### Javascript
```js
function sumDigits(no) {
    return no == 0 ? 0 : no % 10 + sumDigits(Math.floor(no / 10)); // Math.floor(x/y) for Integer Division
}
console.log(sumDigits(1352))
```
