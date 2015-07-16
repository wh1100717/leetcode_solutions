## Delete Node in a Linked List 

> https://leetcode.com/problems/delete-node-in-a-linked-list/

```javascript
/**
 * Definition for singly-linked list.
 * function ListNode(val) {
 *     this.val = val;
 *     this.next = null;
 * }
 */
/**
 * @param {ListNode} node
 * @return {void} Do not return anything, modify node in-place instead.
 */
var deleteNode = function(node) {
    // One Line Anwser
    for(i in Object.keys(node)){node[Object.keys(node)[i]] = node.next[Object.keys(node)[i]]}
    // Two Line Anwser
    // node.val = node.next.val
    // node.next = node.next.next
};
```