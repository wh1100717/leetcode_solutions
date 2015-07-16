## Power of Two 

> https://leetcode.com/problems/power-of-two/

```javascript
/**
 * @param {number} n
 * @return {boolean}
 */
var isPowerOfTwo = function(n) {
    if(n <= 0){return false}
    if(n === 1){return true}
    while(true){
        if(n%2 === 1){return false}
        n = n / 2
        if(n === 1){return true}
    }
};
```