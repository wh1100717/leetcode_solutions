## Remove Duplicates from Sorted List 

> https://leetcode.com/problems/remove-duplicates-from-sorted-list/

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
     m[point.val] = true
     while(true){
        if(point.next === null){break}
        if(m[point.next.val]){
            point.next = point.next.next
        }else{
            m[point.next.val] = true
            point = point.next
        }
     }
     return head
};
```