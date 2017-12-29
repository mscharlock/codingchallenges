# Trees
What is a tree?
Similar to the file structure you might be used to if you've ever used Windows File Explorer or something similar, trees contain nodes which branch off from each other (i.e. have children).

[From Wikipedia:](https://github.com/mscharlock/codingchallenges) A tree is a data structure made up of nodes or vertices and edges without having any cycle. The tree with no nodes is called the null or empty tree. A tree that is not empty consists of a root node and potentially many levels of additional nodes that form a hierarchy.


## Big O for BSTs:
O(log n)
Logarithmic time

## Tree node
```
const TreeNode = module.exports = class {
  constructor(val) {
    this.val = val;
    this.children = [];
  }
}
```

## Insert into a tree
```
insert(newNode, parentVal) {
  if (!newNode instance TreeNode) throw new error ('Not a tree!')
  this.preOrder(node => {
    if(!node) return
    if(node.val === parentVal)
      node.children.push(newNode)
      return this
    })
}
```

## Prune
```
prune(val) {
  this.breadthFirst(node => {
    if(!node) return
    node.children = node.children.filter(child => child.val !== val)
    })
}
```

## Tree Traversals:
Methods of moving around/through a tree.

## Breadth First Traversal
```
breadthFirst(cb) {
  let q = [this]
  let current

  while(q.length) {
    current.q.shift()
    if(cb) cb(current)
    if(current.children.length) {
      q = [...q, ...current.children];
    }
  }
}
```

## In-Order Traversal
(Aka, Left then Root, then Right)
```
inOrder(cb) {
  _walk(this)

  function _walk(node) {
    cb(node)
    node.children.forEach(walk)
  }
}
```

## Pre-Order Traversal
(Aka Root then Left then Right)
```
preOrder(cb) {
  _walk(this)

  function _walk(node) {
    cb(node)
    node.children.forEach(_walk)
  }
}
```

## Post Order Traversal
```
postOrder(cb) {
  _walk(this)

  function _walk(node){
    node.children.forEach(_walk)
    cb(node)
  }
}
```
