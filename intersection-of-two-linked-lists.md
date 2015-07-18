## Intersection of Two Linked Lists 

> https://leetcode.com/problems/intersection-of-two-linked-lists/

```javascript
/**
 * Definition for singly-linked list.
 * function ListNode(val) {
 *     this.val = val;
 *     this.next = null;
 * }
 */

/**
 * @param {ListNode} headA
 * @param {ListNode} headB
 * @return {ListNode}
 */
var getIntersectionNode = function(headA, headB) {
    var sizeA = getListSize(headA)
    var sizeB = getListSize(headB)
    var m = sizeA - sizeB
    if(m > 0){
        while(m-- !== 0){
            headA = headA.next
        }
    }else{
        while(m++ !== 0){
            headB = headB.next
        }
    }
    while(true){
        if(headA === null || headB === null){
            return null
        }
        if(headA === headB){
            return headA
        }
        headA = headA.next
        headB = headB.next
    }
};

var getListSize = function(head){
    var size = 0
    while(true){
        if(head === null){
            return size
        }
        head = head.next
        size++
    }
}
```