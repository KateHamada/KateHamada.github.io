---
layout: essay
type: essay
title: "Reflect on Software Engineering"
date: 2025-12-17
published: false
labels:
  - Reflection
  - Functional Programming
  - Coding Standards
  - Software Engineering
---

<img width="300px" class="rounded float-end ps-4" src="../img/SE.png">

## Introduction
Software Engineering has many aspects to it other than just web application development like design patterns, agile project management, among others. Two of the aspects of software engineering that I found to be applicable to future projects are Functional Programming and coding standards.

## What is Functional Programming?
Functional programming is a declarative style of building software by composing pure functions. Unlike imperative programming, which focuses on how to do something (using loops and state changes), FP focuses on what something is.
An example of functional programming would be where we have a list of numbers and we want to filter out the odd numbers, square each of those numbers, and then sum the total. 

### The Functional Approach:
```
const numbers = [1, 2, 3, 4, 5];

const result = numbers
  .filter(n => n % 2 === 0)   // Step 1: Keep even numbers [2, 4]
  .map(n => n * n)            // Step 2: Square them [4, 16]
  .reduce((acc, n) => acc + n, 0); // Step 3: Sum them up (20)

console.log(result); // Output: 20
```

### Imperative Approach
While the imperative or common approach would include a for loop and an if statement like so:

```
const numbers = [1, 2, 3, 4, 5];
let result = 0; // Explicitly managing the state (accumulator)

for (let i = 0; i < numbers.length; i++) {
  const n = numbers[i];

  // Step 1: Filter (The "if" condition)
  if (n % 2 === 0) {
    
    // Step 2: Map (The transformation)
    const squared = n * n;

    // Step 3: Reduce (The manual accumulation)
    result += squared;
  }
}

console.log(result); // Output: 20
```

## Why would I use Functional Programming?
It may not be obvious but the reason why I would want to use functional programming is because it makes it easier to test code as you don’t need databases or other complex things as you can just pass the data in and just check the result because it should produce the same output for the same input.

## What are Coding Standards and why would I use it?
Coding standards are rules that agreed upon so that the code is readable by keeping naming schemes consistent or indentations, etc. I would use them in future projects that aren’t necessarily software development because they help speed up the process of working with other people so that no one is confused as to what a section of code is doing. 

## Conclusion
All in all, there are many concepts that you learn from Software Engineering that can be used in other areas of computer science. My focal takeaways are Functional Programming and Coding Standards.
