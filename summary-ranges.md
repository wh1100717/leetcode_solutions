## Summary Ranges 

> https://leetcode.com/problems/summary-ranges/

```javascript
/**
 * @param {number[]} nums
 * @return {string[]}
 */
var summaryRanges = function(nums) {
    if(nums.length === 0){return []}
    var result = []
    var first_num = nums[0]
    for(var i=0; i< nums.length; i++){
        if(nums[i+1] != nums[i] + 1 || i === nums.length -1){
            if(first_num === nums[i]){
                result.push(first_num.toString())
            }else{
                result.push(first_num + "->" + nums[i])
            }
            first_num = nums[i+1]
        }
    }
    return result
};
```