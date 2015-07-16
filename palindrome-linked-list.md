## Palindrome Linked List 

> https://leetcode.com/problems/palindrome-linked-list/

```javascript
/**
 * Definition for singly-linked list.
 * function ListNode(val) {
 *     this.val = val;
 *     this.next = null;
 * }
 */
/**
 * @param {ListNode} head
 * @return {boolean}
 */
var isPalindrome = function(head) {
    if(head === null){return true}
    var vals = []
    while(head !== null){
        vals.push(head.val)
        head = head.next
    }
    return vals.toString() === vals.reverse().toString()
};
```