## Rotate Array 

> https://leetcode.com/problems/rotate-array/

```javascript
/**
 * @param {number[]} nums
 * @param {number} k
 * @return {void} Do not return anything, modify nums in-place instead.
 */
var rotate = function(nums, k) {
    var tmp = nums.splice(nums.length - k)
    while(k !== 0){
        var t = tmp[k - 1]
        if(t !== undefined){nums.unshift(t)}
        k--
    }
};
```