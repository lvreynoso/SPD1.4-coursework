```
First we create a temporary variable to store the most recent node. Set it to NULL.
For each node in the linked list,
  If we need to keep track of the next node to keep iterating through the linked list, set this node's next to a temp variable.
  If this node's next is NULL, set the list's HEAD to point to this node.
  We set the node's "next" to point to the location in our temp variable.
  We set our temp variable equal to the current node (as a reference).
Return the list.
```
