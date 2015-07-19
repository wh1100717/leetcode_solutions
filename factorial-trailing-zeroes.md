## Factorial Trailing Zeroes 

> https://leetcode.com/problems/factorial-trailing-zeroes/

```javascript
/**
 * @param {number} n
 * @return {number}
 */
var trailingZeroes = function(n) {
    if(n === 0){return 0}
    var m = Math.floor(n / 5)
    return m + trailingZeroes(m)
};
```