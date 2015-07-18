## Remove Linked List Elements

> https://leetcode.com/problems/remove-linked-list-elements/

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
 * @param {number} val
 * @return {ListNode}
 */
var removeElements = function(head, val) {
    point = head
    if(point === null){return null}
    while(true){
        if(point === null){return null}
        if(point.val === val){
            point = point.next
        }else{break}
    }
    head = point
    while(true){
        if(point === null){break}
        tmp = point.next
        while(true){
            if(tmp === null){break}
            if(tmp.val === val){
                tmp = tmp.next
            }else{break}
        }
        point.next = tmp
        point = point.next
    }
    return head
};
```