## Valid Palindrome 

> https://leetcode.com/problems/valid-palindrome/

```javascript
/**
 * @param {string} s
 * @return {boolean}
 */
var isPalindrome = function(s) {
    //一行的代码
    //return s.replace(/[^a-zA-Z\w]/gi,"").toLowerCase() === s.toString().replace(/(.)/g, "$1,").split(",").reverse().join("")
    s = s.replace(/[^a-zA-Z\w]/gi,"").toLowerCase()
    return s === s.toString().replace(/(.)/g, "$1,").split(",").reverse().join("")
};
```