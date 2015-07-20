## Remove Element 

> https://leetcode.com/problems/remove-element/

```javascript
/**
 * @param {number[]} nums
 * @param {number} val
 * @return {number}
 */
var removeElement = function(nums, val) {
    len = nums.length
    for(var i = 0; i < len; i++){
        var num = nums[i]
        if(num === val){
            nums.splice(i,1)
            i--
            len--
        }
    }
    return nums.length
};
```