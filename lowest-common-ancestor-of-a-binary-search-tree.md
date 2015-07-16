## Lowest Common Ancestor of a Binary Search Tree 

> https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-search-tree/

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
 * @param {TreeNode} p
 * @param {TreeNode} q
 * @return {TreeNode}
 */
var lowestCommonAncestor = function(root, p, q) {
    if(root === null) {return null}
    leftAncestor = root.left === null ? null : lowestCommonAncestor(root.left, p, q)
    if(leftAncestor !== null) {return leftAncestor}
    rightAncestor = root.right === null ? null : lowestCommonAncestor(root.right, p, q)
    if(rightAncestor !== null) {return rightAncestor}
    if(isAncestor(root, p) && isAncestor(root, q)) {return root}
    return null
};

var isAncestor = function(root, p) {
    if(root === null) {return false}
    if(root === p) {return true}
    if(root.left === p || root.right === p){return true}
    return isAncestor(root.left, p) || isAncestor(root.right, p)
}
```