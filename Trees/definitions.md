# Trees
What is a tree?
Similar to the file structure you might be used to if you've ever used Windows File Explorer or something similar, trees 


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

## Prune
```
prune(val) {
  this.breadthFirst(node => {
    if(!node) return
    node.children = node.children.filter(child => child.val !== val)
    })
}
```
