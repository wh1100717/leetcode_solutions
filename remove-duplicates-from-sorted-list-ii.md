## Remove Duplicates from Sorted List II

> https://leetcode.com/problems/remove-duplicates-from-sorted-list-ii/

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
var deleteDuplicates = function(head) {
     var m = {}
     if(head === null){return null}
     var point = head
     m[point.val] = 0
     while(true){
        if(point.next === null){break}
        if(m[point.next.val] !== undefined){
            m[point.next.val] = 1
            point.next = point.next.next
        }else{
            m[point.next.val] = 0
            point = point.next
        }
     }
     while(true){
         if(head === null){break}
         if(m[head.val] === 1){
             head = head.next
         }else{
             break;
         }
     }
     if(head === null){return null}
     point = head
     while(true){
         if(point.next === null){break}
         if(m[point.next.val] === 1){
             point.next = point.next.next
         }else{
             point = point.next
         }
     }
     return head
};
```