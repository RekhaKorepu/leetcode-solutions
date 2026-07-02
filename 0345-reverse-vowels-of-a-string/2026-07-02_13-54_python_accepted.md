# 345. Reverse Vowels of a String
  
<br>**Problem:** https://leetcode.com/problems/reverse-vowels-of-a-string/<br>

**Difficulty:** Easy<br>
**Topics:** Two Pointers, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-07-02 13:54 local time

**Runtime:** 308 ms (beats 12.559300000000036%)
**Memory:** 13.6 MB (beats 74.2329%)


<!-- leetgit:submissionId=2053254375 codeHash=d8faddffff0607c32f5f242507dfbcf8b2b101877758b2edbb9d7ca368ab6ac2 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def reverseVowels(self, s):
        """
        :type s: str
        :rtype: str
        """
        n= len(s)
        result=list(s)
        print("result",result)
        vowels= ['a','e', 'i', 'o','u','A','E','I','O','U']
        left=0
        right=n-1
        if n==0 or n==1:
            return s
        while left<right and  left<n and  right>0:
            while result[left] not in vowels  and left<right:
                left+=1
            while result[right] not in vowels and left<right:
                right-=1
            temp=result[left]
            result[left]=result[right]
            result[right]=temp
            left+=1
            right-=1
        
        return "".join(result)
            
            



```
