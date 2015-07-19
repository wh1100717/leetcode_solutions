## Symmetric Tree 

> https://leetcode.com/problems/symmetric-tree/

```javascript
/**
 * Definition for a binary tree node.
 * function TreeNode(val) {
 *     this.val = val;
 *     this.left = this.right = null;
 * }
 */
/**
 * @param {TreeNode} root
 * @return {boolean}
 */
var isSymmetric = function(root) {
    if(root === null){return true}
    return isSym(root.left, root.right)
};

var isSym = function(left, right){
    if(left === null && right === null){return true}
    if(left === null || right === null){return false}
    if(left.val !== right.val){return false}
    return isSym(left.left, right.right) && isSym(left.right, right.left)
}
```