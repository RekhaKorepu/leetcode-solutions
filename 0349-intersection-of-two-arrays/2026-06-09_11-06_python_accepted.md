# 349. Intersection of Two Arrays
  
<br>**Problem:** https://leetcode.com/problems/intersection-of-two-arrays/<br>

**Difficulty:** Easy<br>
**Topics:** Array, Hash Table, Two Pointers, Binary Search, Sorting<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-06-09 11:06 local time

**Runtime:** 17 ms (beats 20.588800000000003%)
**Memory:** 12.4 MB (beats 94.4512%)


<!-- leetgit:submissionId=2027086004 codeHash=8842b7848ad0fb6ca880aafeb9cea893a5bf3723c1b738746f4a02ff0b368171 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def intersection(self, nums1, nums2):
        """
        :type nums1: List[int]
        :type nums2: List[int]
        :rtype: List[int]
        """
        res=[]
        for x in nums1:
            if x in nums2 and x not in res:
                res.append(x)
        return res
        
```
