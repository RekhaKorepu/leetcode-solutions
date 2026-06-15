# 2216. Delete the Middle Node of a Linked List
  
<br>**Problem:** https://leetcode.com/problems/delete-the-middle-node-of-a-linked-list/<br>

**Difficulty:** Medium<br>
**Topics:** Linked List, Two Pointers<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-06-15 10:23 local time

**Runtime:** 97 ms (beats 18.324200000000022%)
**Memory:** 91.5 MB (beats 40.05200000000001%)


<!-- leetgit:submissionId=2033443589 codeHash=b16876bfcccff1ad25a25cbd393ff4e50897f1ff5cc94d6831ab937983ccf93d notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution(object):
    def deleteMiddle(self, head):
        """
        :type head: Optional[ListNode]
        :rtype: Optional[ListNode]
        """
        if not head:
            return head
           
        length=0
        temp=head
        while temp:
            length+=1
            temp=temp.next
        if length == 1:
            head=None
            return head
        
        middle_node= (length/2)

        num=0
        temp=head
        prev=temp
        while(num<middle_node):
            num+=1
            prev=temp
            temp=temp.next

        prev.next=temp.next
        return head
        


        
        


        
```
