Find the Middle of A Linked List (2 Ways)
```//Find the middle of a linked list: 
current = head; 
length = 0; 
middle = head; 

//While the current has a next, increment length and 
while(current.next) {
  length++; 
  
 //if the length as you increment is mod 2, then the middle "pointer" moves over to the next node. It's a bit like splitting the list in half and then counting one over as the middle?  
  if(length % 2 == 0) {
    middle = middle.next();
  }
  //similarly, the current pointer moves over to the next
  current = current.next(); 
  }
  return middle; 
}
```

Runtime: O(n), because we're iterating through once
Memory usage: We have to keep track of a couple of variables, including length

----------------
```//Another way 
fast = head; 
slow = head; 

let middleFinder = (head) => {
while (fast.next) {
  fast = fast.next.next;
  slow = slow.next;
  }
  return slow 
}
 ```
 
 This essentially does the same thing, but doesn't mod by 2, it counts over by 2
Runtime: O(n) - we're still iterating through only once
Memory usage: A little better because we don't keep track of length. First method is faster though! 
