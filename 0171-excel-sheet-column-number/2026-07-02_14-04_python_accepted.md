# 171. Excel Sheet Column Number
  
<br>**Problem:** https://leetcode.com/problems/excel-sheet-column-number/<br>

**Difficulty:** Easy<br>
**Topics:** Math, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-07-02 14:04 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.4 MB (beats 52.91199999999999%)


<!-- leetgit:submissionId=2053264593 codeHash=f79c0db8c4fa2b8862fd2e4c37e36a5837cffd9a3cd5d2468a916bdd6a2086e7 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def titleToNumber(self, columnTitle):
        """
        :type columnTitle: str
        :rtype: int
        """
        result = 0
        for char in columnTitle:

            # ord() gets the ASCII value; subtracting ord('A') - 1 maps 'A' to 1
            result = result * 26 + (ord(char) - ord('A') + 1)
        return result
        
```
