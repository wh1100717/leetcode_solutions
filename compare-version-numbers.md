## Compare Version Numbers 

> https://leetcode.com/problems/compare-version-numbers/

```javascript
/**
 * @param {string} version1
 * @param {string} version2
 * @return {number}
 */
var compareVersion = function(version1, version2) {
    var v1 = version1.split(".")
    var v2 = version2.split(".")
    var cmp = []
    for(var index = 0; index < Math.max(v1.length, v2.length); index++){
        var v1_val = v1[index] === undefined ? 0 : v1[index]
        var v2_val = v2[index] === undefined ? 0 : v2[index]
        cmp.push(v1_val - v2_val)
    }
    for(var i = 0; i < cmp.length; i++){
        if(cmp[i] > 0){return 1}
        if(cmp[i] < 0){return -1}
    }
    return 0
};
```