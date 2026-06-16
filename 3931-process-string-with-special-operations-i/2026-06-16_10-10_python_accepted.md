# 3931. Process String with Special Operations I
  
<br>**Problem:** https://leetcode.com/problems/process-string-with-special-operations-i/<br>

**Difficulty:** Medium<br>
**Topics:** String, Simulation<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-06-16 10:10 local time

**Runtime:** 7 ms (beats 76.92309999999999%)
**Memory:** 17.1 MB (beats 92.3077%)


<!-- leetgit:submissionId=2034623431 codeHash=2d0065b1e48e714f341bdb4bee3777fca15b7d9a4291827fe2e55478694c4670 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def processStr(self, s):
        """
        :type s: str
        :rtype: str
        """
        res=""
        for index,char in enumerate(s):
            if char.isalpha():
                res+=char
            
            elif char == '*' and res.strip():
                res= res[:-1]
            elif char == "#":
                res= res*2
            elif char == "%":
                res= res[::-1]
        return res.strip()
            



        
```
