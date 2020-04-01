# RedBlackTree
A Red-Black binary search tree for the Crystal language

Deletion is not supported yet.

Functions :
  - initialize
      Create a new tree with default comparator <
  - initialize((V, V) -> Bool)
      Provide a comparator block to indicate a specific ordering
  - insert(V) or <<(V)
      Add item to the tree and restore properties
  - walk
      Yield each value in order
  - walk_ref
      Yield each node in order
  - enum
      Same as walk, but with a counter
  - enum_ref
      Same as walk_ref, but with a counter
  - empty?
      Test if tree is empty
  - empty!
      Delete all nodes
  - collect
      Return an array of all values in order
  - height(Node(V) | Leaf)
      Number of sons before a Leaf is reached
  - depth(Node(V))
      Number of parents before the root is reached
  - display
      Pretty-print tree

The following are available in three forms :
  - find(V)
      Find the first node with the required value. Error if value cannot be found.
  - max
      Find the rightmost node (with the biggest value)
  - min
      Find the lsfttmost node (with the smallest value)
  - succ(Node(V))
      Find node with the next bigger value
  - pred(Node(V))
      Find node with the next smaller value
  for any f of these functions,
    f raises an error is no node satisfies the required property
    f? returns nil if no node satisfies the required property
    f! returns a list of all nodes that satisfy the property
