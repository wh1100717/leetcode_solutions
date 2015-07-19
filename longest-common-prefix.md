## Longest Common Prefix 

> https://leetcode.com/problems/longest-common-prefix/

```javascript
/**
 * @param {string[]} strs
 * @return {string}
 */
var longestCommonPrefix = function(strs) {
    var prefix = ""
    var index = 0
    var cmpStr
    if(strs.length === 0){return ""}
    while(true){
        cmpStr = null
        for(var i = 0; i < strs.length; i++){
            var c = strs[i][index]
            if(c === undefined){
                return prefix
            }
            if(cmpStr === null){
                cmpStr = c
            }else{
                if(cmpStr !== c){return prefix}
            }
        }
        index++
        prefix += cmpStr
    }
};
```