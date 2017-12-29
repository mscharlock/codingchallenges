## Hash Tables
Commonly used in interviews! Essentially, they are sets of sorted data, put into an order. Think of a [bookshelf](https://medium.com/basecs/taking-hash-tables-off-the-shelf-139cbf4752f0).

## Constructor
```
class HashTable {
  constructor (size: 100) {
    this.size = size
    this.memory = [...Array(this.size)]
  }
}
```

## Hash
```
hash(key) {
  return key.split('').reduce((a, b) => a + b.charCode(0), 0) % this.size
}
```

## Set
```
set(key) {
  return this.memory[this.hashKey(key)] = value
}
```

## Get
```
get(key) {
  return this.memory[this.hashKey(key)]
}
```

## Remove
```
remove(key, searchTerm) {
  let address = this.hashKey(key)

  this.memory[address] ? delete this.memory[address] : 'new Error('key invalid')'
}
```
