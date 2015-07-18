## Reverse Bits

> https://leetcode.com/problems/reverse-bits/

```javascript
/**
 * @param {number} n - a positive integer
 * @return {number} - a positive integer
 */
var reverseBits = function(n) {
    var bit = (n).toString(2)
    var len = bit.length
    while(len !== 32){
        bit = "0" + bit
        len++
    }
    return Number.parseInt(bit.replace(/(.)/g, "$1,").split(",").reverse().join(""), 2)
};
```