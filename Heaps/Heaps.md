**Definition**
- Complete binary tree with heap properties:
	- Min Heap: Parent $\leq$ children (root is minimum)
	- Max Heap: Parent $\geq$ children (root is maximum)
- Implemented as an array, not explicit tree nodes

```Python
import heapq

heap = []
heapq.heappush(heap, val)
min_val = heapq.heappop(heap)

min_val = heap[0]
heapq.heapify(arr)
```
- For max heap, negate values

**Common Operations**
- `heappush(heap, val)` - push to heap - $O (\log n)$ 
- `heappop(heap)` - pop heap - $O(\log n)$
- `heap[0]` - peek minimum - $O(1)$
- `heapify(arr)` - heapify existing list $O(n)$

**Patterns**
- Problems explicitly mention "top k"
- Running median (two heaps)
- Kth largest/smallest element





