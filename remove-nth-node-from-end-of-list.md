## Remove Nth Node From End of List

> https://leetcode.com/problems/remove-nth-node-from-end-of-list/

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
 * @param {number} n
 * @return {ListNode}
 */
var removeNthFromEnd = function(head, n) {
    var point = head
    var remove_point = null
    var index = 0
    if(point === null){return null}
    if(point.next === null && n === 1){return null}
    while(true){
        if(point === null){
            if(remove_point === null){
                head = head.next
            }else{
                remove_point.next = remove_point.next.next
            }
            return head
        }
        if(index === n){
            remove_point = head
        }
        if(index > n){
            remove_point = remove_point.next
        }
        point = point.next
        index++
    }
};
```