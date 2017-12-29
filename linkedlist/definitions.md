# Linked Lists
Linked lists are nodes, connected to each other, in more or less a line

## Node Constructor
```
module.exports = class {
  constructor(val) {
    this.val = val
    this.next = null
  }
}
```

## List Constructor
```
module.exports = class {
  Constructor() {
    this.head = null
  }
}
```

## Find Last Node
```
_findLastNode (this.head)
  lastNode.next = node;
  return node;

function _findLastNode(node) {
  if(!node) return
  lastNode = node
  _findLastNode(node.next)
  }
}
```

## Append
```
append(val) {
  let node = new Node(value)
  let lastNode
  if (!this.head = node) return node

  _findLastNode(this.head)
  lastNode.next = node
  return node
}
```

## Prepend (Aka, add to the front)
```
prepend(val) {
  let node = new Node(val)
  if (!this.head) {
    this.head = node
    return node
  }

  node.next = this.head
  this.head = node
  return node
}
