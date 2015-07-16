## Maximum Depth of Binary Tree

>https://leetcode.com/problems/maximum-depth-of-binary-tree/

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
 * @return {number}
 */
var maxDepth = function(root) {
    // One Line Answer
    return root == null ? 0 : (1 + Math.max(root.left == null ? 0 : maxDepth(root.left), root.right == null ? 0 : maxDepth(root.right)))
    // Normal Answer
    // if(root == null){return 0}
    // var leftDepth = root == null ? 0 : maxDepth(root.left)
    // var rightDepth = root == null ? 0 : maxDepth(root.right)
    // return 1 + Math.max(leftDepth, rightDepth)
};
```