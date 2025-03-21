A queue is a fundamental data structure in computer science that follows the First-In-First-Out (FIFO) principle. This means that the first element added to the queue will be the first one to be removed. Queues are widely used in various applications, such as scheduling processes in operating systems, handling requests in web servers, and managing tasks in multi-threading environments.
Queues are essential for managing tasks and resources efficiently in various computational scenarios.

## Key Operations in a Queue

1. **Enqueue**: This operation adds an element to the end of the queue.
2. **Dequeue**: This operation removes an element from the front of the queue.
3. **Front**: This operation retrieves the front element of the queue without removing it.
4. **Rear**: This operation retrieves the rear element of the queue without removing it.
5. **IsEmpty**: This operation checks whether the queue is empty.
6. **IsFull**: This operation checks whether the queue is full (if the queue has a fixed size).

## Implementations of a Queue

Queues can be implemented using various data structures, including arrays and linked lists. Below are examples of both implementations in Python.

### Array-Based Queue

```js
class Queue {
    constructor(capacity) {
        this.capacity = capacity;
        this.queue = new Array(capacity).fill(null);
        this.front = 0;
        this.rear = 0;
        this.size = 0;
    }
	
    isEmpty() {
        return this.size === 0;
    }
	
    isFull() {
        return this.size === this.capacity;
    }
	
    enqueue(item) {
        if (this.isFull()) {
            throw new Error("Queue is full");
        }
        this.queue[this.rear] = item;
        this.rear = (this.rear + 1) % this.capacity;
        this.size += 1;
    }
	
    dequeue() {
        if (this.isEmpty()) {
            throw new Error("Queue is empty");
        }
        const item = this.queue[this.front];
        this.front = (this.front + 1) % this.capacity;
        this.size -= 1;
        return item;
    }
	
    frontElement() {
        if (this.isEmpty()) {
            throw new Error("Queue is empty");
        }
        return this.queue[this.front];
    }
	
    rearElement() {
        if (this.isEmpty()) {
            throw new Error("Queue is empty");
        }
        return this.queue[(this.rear - 1 + this.capacity) % this.capacity];
    }
}

// Example usage
const queue = new Queue(5);
queue.enqueue(1);
queue.enqueue(2);
queue.enqueue(3);
console.log(queue.dequeue());  // Output: 1
console.log(queue.frontElement());  // Output: 2
console.log(queue.rearElement());  // Output: 3
```

### Linked List-Based Queue

```js

```

# Applications of Queues

1. **CPU Scheduling**: Queues are used to manage the order of processes waiting for CPU time.
2. **Disk Scheduling**: Queues are used to manage the order of I/O requests.
3. **Network Packets**: Queues are used to manage the order of packets in network routers.
4. **Breadth-First Search (BFS)**: Queues are used to explore nodes level by level in graph traversal algorithms.