---
layout: essay
type: essay
title: "ESLint: Helpful Guide or Nitpicky Enforcer?"
# All dates must be YYYY-MM-DD format!
date: 2025-09-24
published: true
labels:
  - ESLint
  - Typescript
  - Technical Essay
---

## Introduction
ESLint is like an extension that you add onto your IDE so that while you are coding it will show you errors with your code, not necessarily errors that make the code nonfunctional but that it should be formatted differently. The major purpose of ESLint is to make sure that you’re following coding standards so that future bugs can be avoided as well as the fact that other coders can look at your code without getting confused as to what you’re doing. 

## Readability Conventions
To some degree I think that some coding standards do help you learn a programming language or at the very least make it easier to understand what the code is doing. For example putting new line after a “{“ and before a “}” when dealing with functions or if statements, etc. is helpful like so: 
```
If (num == 10) {
num++;
return true;
}
```
Instead of something like below which is harder to read in my opinion but technically should function the same:
```
If (num == 10) { num++; return true; }
```

## Nitpicky Rules and Frustrations
After the first week of using ESLint with VSCode, if I’m being completely honest, I despise it because there are some formatting rules that I don’t agree with and in my opinion are too nit picky. For example, having to use single quotes instead of double quotes for strings:
```
const name = ‘Kate’ // correct way
const name = “Kate” // incorrect way
```
I think that this is counterintuitive in my opinion because previously we’ve learned that Java makes the distinction between strings and characters with double quotes for strings and single quotes for characters. Even though I know that the quotes don’t matter in typescript it’s just irritating having errors popping up because of my muscle memory of putting double quotes. However, I do agree with why this rule was implemented since you don’t want to use both single and double quotes because it might confuse other coders as to if there’s a difference between them since you used them in different places. But I would instead of picking single quotes, I would pick double quotes instead.

Another example of ESLint being nitpicky that I hate is when you have a space at the end of a line of code and it freaks out saying that you can’t do that when it shouldn’t even matter because it’s not like anyone can see the extra space at the end of a line. 
```
const idk = ‘test’;_
const idk = ‘test’;
```

## When ESLint is Actually Helpful
On the other hand, something like an indentation difference where it can look different depending on how long it is which can make it look confusing which I can understand why it would be important to remind coders to implement that. 
Example:
```
// bad example
const sum = 0;
for (const i = 0; i < array.length; i++) {
sum = array[i] + sum;
console.log(array[i]); }
return sum;

// good example
const sum = 0;
for (const i = 0; i < array.length; i++) {
sum = array[i] + sum;
console.log(array[i]);
}
return sum;
```
In the good example you can see that “sum = array[i] + sum;” and “console.log(array[i]);” are a part of the for loop and not “return sum;” while the bad example makes it look like the for loop includes the “return sum;” statement. 

## Conclusion:
All in all, I think ESLint can be useful for any tool that has errors that are basically reminders to format your code so that it’s readable for other people as well as preventing bugs from small errors. However, it shouldn’t be too overbearing and strict in the sense that there should be options where both can be correct. For example with the double quotes vs single quotes, the syntax rule should be to make it so that the error only occurs if it sees that there’s both instances in the code otherwise it should be found. Which is the whole point of that rule to be consistent right? I think that ESLint can be useful for beginners in coding who have never learned how to format code yet. However for those that have already done a lot of projects and understand that readability of code is important then it’s not as useful.

