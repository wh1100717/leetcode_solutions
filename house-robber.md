## House Robber 

> https://leetcode.com/problems/house-robber/

```javascript
/**
 * @param {number[]} nums
 * @return {number}
 */
var rob = function(nums) {
    // Recursive solution is too slow..
    // if(nums.length === 0){return 0}
    // if(nums.length === 1){return nums[0]}
    // if(nums.length === 2){return Math.max.apply(this, nums)}
    // return Math.max(nums[0] + rob(nums.slice(2)), rob(nums.slice(1)))
    var result = 0
    var m = 0
    for(var index = 0; index < nums.length; index++){
        var num = nums[index]
        var tmp = result
        result = Math.max(result, num + m)
        m = tmp
    }
    return result
};
```