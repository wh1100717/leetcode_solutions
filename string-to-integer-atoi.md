## String to Integer (atoi) 

> https://leetcode.com/problems/string-to-integer-atoi/

```javascript
/**
 * @param {string} str
 * @return {number}
 */
var myAtoi = function(str) {
    str = str.trim()
    if(str === ""){return 0}
    var n = str.match(/^[+-]?\d+/)
    if(n === null){return 0}
    n = Number.parseInt(n[0])
    n = Math.min(n, 2147483647)
    n = Math.max(n, -2147483648)
    return n
};
```