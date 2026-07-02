# 3558. Find a Safe Walk Through a Grid
  
<br>**Problem:** https://leetcode.com/problems/find-a-safe-walk-through-a-grid/<br>

**Difficulty:** Medium<br>
**Topics:** Array, Breadth-First Search, Graph Theory, Heap (Priority Queue), Matrix, Shortest Path<br>
**Language:** python<br>
**Status:** Accepted<br>
**Submitted:** 2026-07-02 12:34 local time

**Runtime:** 93 ms (beats 94.7368%)
**Memory:** 12.7 MB (beats 15.789499999999999%)


<!-- leetgit:submissionId=2053175664 codeHash=c75f2099c96e94ae8de950e9b31a8a6b2052915dc81bc610266e5cee28994097 notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python
from collections import deque
class Solution(object):
    def findSafeWalk(self, grid, health):
        """
        :type grid: List[List[int]]
        :type health: int
        :rtype: bool
        """

        m= len(grid)
        n=len(grid[0])

        directions= [
            (1,0),
            (-1,0),
            (0,1),
            (0,-1)
        ]
        INF= float('inf')
        dist= [[INF]*n for _ in range(m)]
        dist[0][0] = grid[0][0]

        dq=deque()
        dq.append((0,0))

        while dq:
            row, col= dq.popleft()
            for dr,dc in directions:
                newRow = row + dr
                newCol= col + dc

                if(newRow<0 or newRow>=m or newCol<0 or newCol>=n):
                    continue
                
                newCost = dist[row][col] + grid[newRow][newCol]

                if newCost< dist[newRow][newCol]:
                    dist[newRow][newCol]= newCost

                    if grid[newRow][newCol]==0:
                        dq.appendleft((newRow, newCol))
                    else:
                        dq.append((newRow, newCol))

        return dist[m-1][n-1]<health

```
