**Singly Linked Lists**
- Each node contains a value and reference field to link to next node

```Python
class Node:
	def __init__(self, val=0, next=None):
		self.val = val
		self.next = next
```

Properties
- Use the `head` node (first node) to represent the whole list
- Insert/Delete nodes in $O(n)$ time at specific position, since you need to traverse list
- Insert/Delete beginning is $O(1)$

**Tortoise-Hare Method** (two pointers)
- Moving slow pointer one step at a time while moving fast pointer two steps at a time

```Python
slow, fast = head, head
while fast and fast.next:
	slow = slow.next
	fast = fast.next.next
```
- Before doing `fast = fast.next.next`, we have to check both `fast` and `fast.next`
- Time: $O(n)$ 
- Use cases: Find middle node, detect cycle, find cycle start

**Reversing a Linked List**
- Two nodes to keep track, original head and new head
- Walk through original list and first save next node
- Make the current node point backwards to `prev` instead of forward
- Move both ptrs where `prev` becomes the current node and `curr` becomes next node

```Python
curr, prev = head, None

while curr:
	curr_next = curr.next
	curr.next = prev
	prev = curr
	curr = curr_next

return prev
```
- Time: $O(n)$, Space: $O(1)$ 

**Doubly Linked List**
- Has one more reference field which is known as `prev` where you know the previous node of the current node

```Python
class Node:
	def __init__(self, val=0, next=None, prev=None):
		self.val = val
		self.next = next
		self.prev = prev
```
- Can traverse in both directions
- Insert/Delete in $O(1)$ if you have reference to the node

**Dummy Node**
- A dummy node is a temporary placeholder node
- Usually used when your returning a new list or modifying head

```Python
dummy = Node(0)
dummy.next = head
```
