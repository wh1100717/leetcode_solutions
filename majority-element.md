## Majority Element 

> https://leetcode.com/problems/majority-element/

```javascript
/**
 * @param {number[]} nums
 * @return {number}
 */
var majorityElement = function(nums) {
    var m = {}
    var len = nums.length
    for(var index = 0; index < len; index++){
        var num = nums[index]
        m[num] = m[num] === undefined ? 1 : m[num] + 1
    }
    var keys = Object.keys(m)
    for(var i = 0; i < keys.length; i++){
        var key = keys[i]
        if(m[key] > len / 2){return Number.parseInt(key)}
    }
    return 0
};
```