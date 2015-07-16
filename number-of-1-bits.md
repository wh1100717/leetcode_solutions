## Number of 1 Bits

> https://leetcode.com/problems/number-of-1-bits/

```javascript
/**
 * @param {number} n - a positive integer
 * @return {number}
 */
var hammingWeight = function(n) {
    result = 0
    while(n !== 0){
        if(n % 2 === 1){result++}
        n = Math.floor(n / 2)
    }
    return result
};
```