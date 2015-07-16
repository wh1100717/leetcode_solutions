## Single Number

> https://leetcode.com/problems/single-number/

```
/**
 * @param {number[]} nums
 * @return {number}
 */
var singleNumber = function(nums) {
    var n = {}
    for(var index=0; index < nums.length; index++){
        var num = nums[index]
        if(n[num] == null){
            n[num] = 1
        }else{
            delete n[num]
        }
    }
    return Number(Object.keys(n)[0])
};
```