## Excel Sheet Column Number

> https://leetcode.com/problems/excel-sheet-column-number/

```javascript
/**
 * @param {string} s
 * @return {number}
 */
var titleToNumber = function(s) {
    len = s.length
    result = 0
    for(var i = 1; i <= len; i++){
        var c = s[len - i]
        result += (c.charCodeAt() - 64) * Math.pow(26, i-1)
    }
    return result
};
```