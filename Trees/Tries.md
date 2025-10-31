**Definition**
- Prefix tree, that organizes strings based on common prefixes, allows fast searching of words
- Consists of nodes connected by edges where each node represents a character
- Root node doesn't store any character

```Python
class TrieNode:
	def __init__(self):
		self.children = {}
		self.endOfWord = False
```

**Algorithm Complexity**
- Insert: $O(m)$ where $m$ is the length of the word
- Search: $O(m)$
- Prefix Search: $O(m)$
- Space: $O(n \cdot m)$ where $m$ is length of word, $n$ is average word length

**Patterns**
- Multiple prefix queries
- Dictionary of words with common prefixes
- Need fast word lookup and prefix match up
- Problems mention "prefix", "autocomplete", "dictionary"

**Additional Notes**
- Each path from root to `endOfWord=True` represents a word
- Nodes share common prefixes
- Not all nodes are end of words