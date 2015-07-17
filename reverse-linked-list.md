## Reverse Linked List 

> https://leetcode.com/problems/reverse-linked-list/

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
 * @return {ListNode}
 */
var reverseList = function(head) {
    // First Solution
    if(head === null){return null}
    while(true){
        if(head.next === null){break}
        head.next.prev = head
        head = head.next
    }
    var result = head
    while(true){
        if(head.prev === undefined){
            head.next = null
            break;
        }
        head.next = head.prev
        delete head.prev
        head = head.next
    }
    return result
    // Second Solution
    // var result = null
    // while(true){
    //     if(head === null){break}
    //     var tmp = new ListNode(head.val)
    //     tmp.next = result
    //     result = tmp
    //     head = head.next
    // }
    // return result
};
```