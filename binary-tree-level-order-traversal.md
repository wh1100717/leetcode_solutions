## Binary Tree Level Order Traversal 

> https://leetcode.com/problems/binary-tree-level-order-traversal/

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
 * @return {number[][]}
 */
var levelOrder = function(root) {
    var result = []
    var dept = 0
    var currentNodes = [root]
    while(true){
        if(currentNodes.length === 0){break}
        var tmpNodes = []
        var vals = []
        for(var index=0; index< currentNodes.length; index++){
            node = currentNodes[index]
            if(node !== null){
                vals.push(node.val)
                tmpNodes.push(node.left)
                tmpNodes.push(node.right)
            }
        }
        currentNodes = tmpNodes
        if(vals.length !== 0){
            result[dept++] = vals
        }
    }
    return result
};
```