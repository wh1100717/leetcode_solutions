## Isomorphic Strings 

> https://leetcode.com/problems/isomorphic-strings/

```javascript
/**
 * @param {string} s
 * @param {string} t
 * @return {boolean}
 */
var isIsomorphic = function(s, t) {
    // First Solution
    // var s_len = s.length,
    //     t_len = t.length,
    //     s_done = {},
    //     t_done = {},
    //     s_array = [],
    //     t_array = []
    // if(s_len !== t_len){return false}
    // for(var m = 0; m < s_len; m++){
    //     var s_c = s[m]
    //     var t_c = t[m]
    //     if(s_done[s_c] === undefined){
    //         s_done[s_c] = [m]
    //     }else {
    //         s_done[s_c].push(m)
    //     }
    //     if(t_done[t_c] === undefined){
    //         t_done[t_c] = [m]
    //     }else{
    //         t_done[t_c].push(m)
    //     }
    // }
    // var s_keys = Object.keys(s_done)
    // var t_keys = Object.keys(t_done)
    // for(var x = 0; x < s_keys.length; x++){
    //     s_array.push(s_done[s_keys[x]])
    // }
    // for(var y = 0; y < t_keys.length; y++){
    //     t_array.push(t_done[t_keys[y]])
    // }
    // return JSON.stringify(s_array.sort()) === JSON.stringify(t_array.sort())
    
    // Second Solution
    if(s.length !== t.length){return false}
    var sm = {}, tm = {}
    for(var i = 0; i < s.length; tm[s[i]] = sm[t[i]] = i, i++){ if(tm[s[i]] !== sm[t[i]]){return false}}
    return true
};
```