## What is Big O notation?
<p>
    Big O notation determines how fast a function or block of code can run. It refers to the time and memory usage to complete the function. In other words the "worst case scenario" for the code running. Its a benchmark for code.
</p>

## Contrast Big O with Omega and Theta...
<p>
    Big Omega is the least amount of time required ( the most efficient way possible, in other words best case) to run code. It is the opposite of Big O. Big Theta is defined as tightest bound and tightest bound is the best of all the worst case times that the algorithm can take.
</p>

## Code Example Of Linear Time Complexity
    console.log('Hello World!');

## Code Example Of Quadratic Time Complexity.
    for (let i = 0; i < 10; i++) {
        console.log(i);
    }