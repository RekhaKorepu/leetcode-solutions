# 8. String to Integer (atoi)
  
<br>**Problem:** https://leetcode.com/problems/string-to-integer-atoi/<br>

**Difficulty:** Medium<br>
**Topics:** String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-06-12 15:51 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.3 MB (beats 57.2239%)


<!-- leetgit:submissionId=2030695789 codeHash=d9f5e9fe1e6864106247970f9f2973d5a09e8e214fa9bf05d8c4cf996838bde9 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def myAtoi(self, s):
        """
        :type s: str
        :rtype: int
        """
        res = ""
        started = False

        for char in s:

            if char == " " and not started:
                continue

            if char.isdigit():
                started = True
                res += char

            elif (char == "+" or char == "-") and res == "":
                started = True
                res += char

            else:
                break

        if res == "" or res == "+" or res == "-":
            return 0

        num = int(res)

        INT_MIN = -(2 ** 31)
        INT_MAX = (2 ** 31) - 1

        if num < INT_MIN:
            return INT_MIN

        if num > INT_MAX:
            return INT_MAX

        return num


            
        
```
