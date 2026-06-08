# 2265. Partition Array According to Given Pivot
  
<br>**Problem:** https://leetcode.com/problems/partition-array-according-to-given-pivot/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Two Pointers, Simulation<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-06-08 14:06 local time

**Runtime:** 51 ms (beats 92.54380000000003%)
**Memory:** 29.4 MB (beats 60.526100000000035%)


<!-- leetgit:submissionId=2026148568 codeHash=f26bdeed2fb781c05cfce7aef1d0c409d98b47ed7594155bfc84d1dc1d5451d1 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def pivotArray(self, nums, pivot):
        """
        :type nums: List[int]
        :type pivot: int
        :rtype: List[int]
        """
        lesser=[]
        equal=[]
        greater=[]
        for x in nums:
            if(x<pivot):
                lesser.append(x)
            elif(x==pivot):
                equal.append(x)
            else:
                greater.append(x)
        return lesser+equal+greater



        

        
```
