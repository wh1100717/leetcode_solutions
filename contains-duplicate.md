## Contains Duplicate 

> https://leetcode.com/problems/contains-duplicate/

```javascript
/**
 * @param {number[]} nums
 * @return {boolean}
 */
var containsDuplicate = function(nums) {
    var m = {}
    var len = nums.length
    for(var index=0; index < len; index++){
        m[nums[index]] = 1
    }
    return Object.keys(m).length !== len
};
```