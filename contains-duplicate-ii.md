## Contains Duplicate II 

> https://leetcode.com/problems/contains-duplicate-ii/

```javascript
/**
 * @param {number[]} nums
 * @param {number} k
 * @return {boolean}
 */
var containsNearbyDuplicate = function(nums, k) {
    var m = {}
    var len = nums.length
    for(var index=0; index < len; index++){
        var num = nums[index]
        if(m[num] === undefined){
            m[num] = [index]
        }else{
            m[num].push(index)
        }
    }
    keys = Object.keys(m)
    for(var i=0; i < keys.length; i++){
        var key = keys[i]
        t = m[key]
        if(t.length === 1){
            continue;
        }
        for(var n=0; n < t.length - 1; n++){
            if(t[n + 1] - t[n] <= k){
                return true
            }
        }
    }
    return false
};
```