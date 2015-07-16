## Product of Array Except Self

> https://leetcode.com/problems/product-of-array-except-self/

```javascript
/**
 * @param {number[]} nums
 * @return {number[]}
 */
var productExceptSelf = function(nums) {
    var len = nums.length, results = [nums[0]], apart = 1
    for(var index=1; index < len - 1; index++){results[index] = results[index - 1] * nums[index]}
    for(var index=len - 1; index > 0; apart *= nums[index--]){results[index] = results[index - 1] * apart}
    results[0] = apart
    return results
};
```