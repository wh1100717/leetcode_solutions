## Reverse Integer 

> https://leetcode.com/problems/reverse-integer/

```javascript
/**
 * @param {number} x
 * @return {number}
 */
var reverse = function(x) {
    var flag = true
    if(x < 0){flag = false}
    x = Math.abs(x)
    x = Number.parseInt(x.toString().replace(/(.)/g, "$1,").split(",").reverse().join(""))
    if(x > Number.parseInt("1111111111111111111111111111111", 2)){return 0}
    if(!flag){x = x * -1}
    return x
};
```