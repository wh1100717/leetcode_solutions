## ZigZag Conversion 

> https://leetcode.com/problems/zigzag-conversion/

```javascript
/**
 * @param {string} s
 * @param {number} numRows
 * @return {string}
 */
var convert = function(s, numRows) {
    // Memory Limit Exceeded
    // var result = ""
    // var indexes = []
    // var i = 0
    // while(true){
    //     var index = (numRows - 1) * 2 * i
    //     if(s[index] === undefined){break}
    //     indexes.push(index)
    //     i++
    // }
    // for(var row = 0; row < numRows; row++){
    //     for(var m = 0; m < indexes.length; m++){
    //         var index = indexes[m]
    //         if(row === 0){
    //             result.push(s[index])
    //             continue;
    //         }
    //         if(row === numRows - 1){
    //             if(s[index + row] !== undefined){
    //                 result.push(s[index + row])
    //             }
    //             continue;
    //         }
    //         if(s[index - row] !== undefined){
    //             result.push(s[index - row])
    //         }
    //         if(s[index + row] !== undefined){
    //             result.push(s[index + row])
    //         }
    //     }
    // }
    // return result

    // WTF... also Memory Limit Exceeded
    // var result = "",
    //     d = (numRows - 1) * 2
    // for(var row = 0; row < numRows; row++){
    //     var index = 0
    //     while(true){
    //         var c
    //         if(row === 0){
    //             c = s[index * d]
    //             if(c === undefined){break}
    //             result += c
    //         }else if(row === numRows - 1){
    //             c = s[index * d + row]
    //             if(c === undefined){break}
    //             result += c
    //         }else {
    //             if(index * d - row > 0){
    //                 c = s[index * d - row]
    //                 if(c === undefined){break}
    //                 result += c
    //             }
    //             c = s[index * d + row]
    //             if(c === undefined){break}
    //             result += c
    //         }
    //         index++
    //     }
    // }
    // return result
    
    //泪奔....一致 Memory Limit Exceeded 的原因是少了当numRows为1的判断
    if(numRows === 1){return s} 
    var result = "",
        d = (numRows - 1) * 2,
        len = s.length
    for(var row = 0; row < numRows; row++){
        var index = 0
        while(true){
            var t = index * d
            if(row === 0){
                if(t >= len){break}
                result += s[t]
            }else if(row === numRows - 1){
                if(t + row >= len){break}
                result += s[t + row]
            }else {
                if(t - row > 0){
                    if(t - row >= len){break}
                    result += s[t - row]
                }
                if(t + row >= len){break}
                result += s[t + row]
            }
            index++
        }
    }
    return result
    
};
```