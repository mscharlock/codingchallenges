## Stacks
They are basically data structures that are like buffet plates - nodes stacked on top of nodes. First in is the first out (FIFO).

## Generic Node Constructor
Leaving this here in case I need to reference it
```
module.exports = class {
  Constructor(val) {
    this.val = val
    this.next = null
  }
}
```

## Stack Constructor
```
const Stack = module.exports = class {
  Constructor () {
    this.top = null
  }
}
```

## Methods we have on a stack:
Push, pop, peek

## Push
```
push(val) {
  let node = new Node(val)
  if (!this.top) {
    this.top = node
    return node
  }

  node.next = this.top
  this.top = node
  return this.top
}
```

## Pop
```
pop() {
  if (!this.top) return null
  let top = this.top.val
  this.top = this.top.next
  return top
}
```

## Peek
```
peek() {
  return this.top
  }
```
