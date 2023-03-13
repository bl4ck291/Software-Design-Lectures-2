# Lecture 1

## Event Sourcing

## Linearization

### Linearizability

- Helps understanding CAP theorem
- Used in analysis of competitive systems

### Histories

- FIFO

- enqueue(x) : add x to the end of the queue
- dequeue(x) : remove x from the beginning of the queue

- History — finite sequence of the operations. The one single execution of some code is a history.

![image](./images/lecture1/1.jpg)
![image](./images/lecture1/2.jpg)

### Sequential specification

![image](./images/lecture1/3.jpg)

- Circled in red in the photo is not possible, we need to dequeue Y before X.

- Beginning moment - invocation of the first operation
- Result moment - end of the last operation

### Happens-before

![image](./images/lecture1/4.jpg)

### Parallel operations

![image](./images/lecture1/5.jpg)

### Sequential histories
![image](./images/lecture1/6.jpg)

- All operations happened sequentially, not just in one thread.

### Linearizability

![image](./images/lecture1/7.jpg)

![image](./images/lecture1/8.jpg)

![image](./images/lecture1/9.jpg)

![image](./images/lecture1/10.jpg)

### Interesting fact

![image](./images/lecture1/11.jpg)

- Atomicity here is not the same atomocity as in ACID.

- Linearizability is one of the guarantess in parallel programming (The strongest).

## CAP-Theorem

![image](./images/lecture1/12.jpg)

- 3 Properties: Consistency, Availability, Partition Tolerance

- Brewer's theorem: It is impossible to have all 3 properties at the same time. (2 out of 3)

![image](./images/lecture1/13.jpg)

- Consistency: All nodes see the same data at the same time.

- Availability: Every request receives a response.

- Partition Tolerance: The system continues to operate despite an arbitrary number of messages being dropped (or delayed) by the network between nodes.

![image](./images/lecture1/14.jpg)

![image](./images/lecture1/15.jpg)

![image](./images/lecture1/16.jpg)

![image](./images/lecture1/17.jpg)

![image](./images/lecture1/18.jpg)