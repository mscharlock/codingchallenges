# Queues
Basically a line! Similar to a linked list

## Queue Constructor
```
const Queue = module.exports = class {
  Constructor() {
    this.head = null
    this.tail = null
  }
}
```

## Methods for a Queue
Enqueue - add something to the line
Dequeue - decrease from the line

## Enqueue
```
enqueue(val) {
  let node = new Node(val)
  if (!this.head) {
    this.head = this.tail = node
    return node
  }
  this.tail.next = node
  this.tail = node
  return this.tail
}
```

## Dequeue () {
```
  if (!this.head) return null
  if (this.head == this.tail) {
    this.head = this.tail = null
  } else {
    let tmp = this.head
    this.head = tmp.next
    tmp.next = null
    return tmp
    }
  }
```


}
