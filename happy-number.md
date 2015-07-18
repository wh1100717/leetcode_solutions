## Happy Number 

> https://leetcode.com/problems/happy-number/

```javascript
/**
 * @param {number} n
 * @return {boolean}
 */
var isHappy = function(n) {
    var map = {}
    while(true){
        var r = cal(n)
        if(r === 1){return true}
        if(map[r]){return false}
        map[r] = true
        n = r
    }
};

var cal = function(n) {
    total = 0
    n.toString().replace(/(.)/g, "$1,").split(",").forEach(function(val){
        if(val !== ""){total += Math.pow(Number.parseInt(val), 2)}
    })
    return total
}
```