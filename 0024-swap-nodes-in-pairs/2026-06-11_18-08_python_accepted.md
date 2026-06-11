# 24. Swap Nodes in Pairs
  
<br>**Problem:** https://leetcode.com/problems/swap-nodes-in-pairs/<br>

**Difficulty:** Medium<br>
**Topics:** Linked List, Recursion<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-06-11 18:08 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.4 MB (beats 39.64480000000001%)


<!-- leetgit:submissionId=2029733259 codeHash=258cbbe2b6b5dbcded1edf29eab612296d89de5c190381827e36b1ff557feab6 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution(object):
    def swapPairs(self, head):
        """
        :type head: Optional[ListNode]
        :rtype: Optional[ListNode]
        """
        if(head is None or head.next is None):
            return head
        current= head
        adjacent= current.next
        while current:
            temp= current.val
            if current.next is not None:
                   current.val=current.next.val
                   current.next.val= temp
                   current=current.next.next
            else:
                current=current.next
         
        return head



        

        
        
```
