# 290. Word Pattern
  
<br>**Problem:** https://leetcode.com/problems/word-pattern/<br>

**Difficulty:** Easy<br>
**Topics:** Hash Table, String<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-07-03 16:59 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 12.3 MB (beats 91.9346%)


<!-- leetgit:submissionId=2054599287 codeHash=13cb35aae4c4793c3af0e3d5b25f2e02615305c3235b7010dee1fb7564da8ce0 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
class Solution(object):
    def wordPattern(self, pattern, s):
        """
        :type pattern: str
        :type s: str
        :rtype: bool
        """
        words = s.split()

        # Number of pattern characters and words must match
        if len(pattern) != len(words):
            return False

        char_to_word = {}
        used_words = set()

        for i in range(len(pattern)):
            char = pattern[i]
            word = words[i]

            if char in char_to_word:
                # Existing mapping must match
                if char_to_word[char] != word:
                    return False
            else:
                # Word is already mapped to another character
                if word in used_words:
                    return False

                char_to_word[char] = word
                used_words.add(word)

        return True

                

        
```
