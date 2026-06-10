# 6. Zigzag Conversion
  
<br>**Problem:** https://leetcode.com/problems/zigzag-conversion/<br>

**Difficulty:** Medium<br>
**Topics:** String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-06-10 14:54 local time

**Runtime:** 15 ms (beats 49.2547%)
**Memory:** 12.4 MB (beats 57.454899999999995%)


<!-- leetgit:submissionId=2028453988 codeHash=c42878df1129b3c748f3e9d1bbf93211cbff15f8a6a9db725acb15f9e8b512de notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def convert(self, s, numRows):
        """
        :type s: str
        :type numRows: int
        :rtype: str
        """
        res = [""] * numRows
        if(numRows==1 or numRows>=len(s)):
            return s
        current_row=0
        direction=1
        for letter in s:
            res[current_row]+=letter

            if(current_row==0):
                direction=1
            elif(current_row==numRows-1):
                direction=-1

            current_row=current_row+direction

        return "".join(res)
            
        

 



        
```
