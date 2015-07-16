## Palindrome Number

> https://leetcode.com/problems/palindrome-number/

```javascript
/**
 * @param {number} x
 * @return {boolean}
 */
var isPalindrome = function(x) {
    return x === Number.parseInt(x.toString().replace(/(.)/g, "$1,").split(",").reverse().join(""))
};
```