## Excel Sheet Column Title

> https://leetcode.com/problems/excel-sheet-column-title/

```javascript
/**
 * @param {number} n
 * @return {string}
 */
var convertToTitle = function(n) {
    var result = ""
    while(n > 26){
        var m = n % 26
        n = Math.floor(n / 26)
        if(m === 0){
            m = 26
            n -= 1
        }
        result = String.fromCharCode(64 + m) + result
    }
    return String.fromCharCode(64 + n) + result
};
```