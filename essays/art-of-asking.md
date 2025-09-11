---
layout: essay
type: essay
title: "The Art of Asking"
# All dates must be YYYY-MM-DD format!
date: 2025-09-10
published: false
labels:
  - Smart Questions
  - StackOverflow
  - Technical Essay
---

<img width="300px" class="rounded float-start pe-4" src="../img/smart-questions/rtfm.png">

## What Makes a Question Smart?

There’s a lot more than you would think when it comes to creating a smart question that will likely get you an answer on whatever problem you have with your code. In order to ask a smart question it requires you to do some work before you even go on a forum to ask otherwise you won’t get an answer and will likely get downvoted on StackOverflow. So before you ask, you should try to look for an answer on forums or the web or AI and make sure to include what you’ve tried and look up so far so that people know that this isn’t you just playing dumb in order to get someone else to do the work for you. Even though it seems tedious to do this, you should because at the end of the day you aren’t entitled to an answer from anyone else because you aren’t paying for it. Now onto creating the actual question, there are a lot of aspects of a smart question so I’ll show you an example of a smart question and then point out what was smart about it. Afterwards I’ll show you an example of a not so smart question that will lead you to not getting answers so that you’ll know what not to do.

In the example below, we will examine the components of a smart question. In this case the person asking is trying to figure out why a sorted array is processed faster than an unsorted. 

### Here’s the first half of the question from StackOverflow:

Header: Why is processing a sorted array faster than processing an unsorted array?

In this C++ code, sorting the data (before the timed region) makes the primary loop ~6x faster:

```
#include <algorithm>
#include <ctime>
#include <iostream>

int main()
{
    // Generate data
    const unsigned arraySize = 32768;
    int data[arraySize];

    for (unsigned c = 0; c < arraySize; ++c)
        data[c] = std::rand() % 256;

    // !!! With this, the next loop runs faster.
    std::sort(data, data + arraySize);

    // Test
    clock_t start = clock();
    long long sum = 0;
    for (unsigned i = 0; i < 100000; ++i)
    {
        for (unsigned c = 0; c < arraySize; ++c)
        {   // Primary loop.
            if (data[c] >= 128)
                sum += data[c];
        }
    }

    double elapsedTime = static_cast<double>(clock()-start) / CLOCKS_PER_SEC;

    std::cout << elapsedTime << '\n';
    std::cout << "sum = " << sum << '\n';
}
```
  - Without std::sort(data, data + arraySize); , the code runs in 11.54 seconds.
  - With the sorted data, the code runs in 1.93 seconds.

(Sorting itself takes more time than this one pass over the array, so it's not actually worth doing if we needed to calculate this for an unknown array.)

### First things first, the header: 

“Why is processing a sorted array faster than processing an unsorted array?”

This is a good header because it’s clear, concise, and specific as in, they could’ve said “Why is my code slow?” but instead chose the header above. Not only that but it also invites explanation and is search friendly so that if someone else has the same question, which is likely, they would also be able to get their answer from there.

Within the body of the question, the asker is clear and gives the measured timings of the processing times “11.54 seconds” and “1.93 seconds” and clearly asks why the difference exists. This shows that the asker has an interest in understanding the background hardware stuff that’s happening that they don’t know about, which helps get people to answer their question. 

### Here’s the second half of the question from StackOverflow:

Initially, I thought this might be just a language or compiler anomaly, so I tried Java:

```
import java.util.Arrays;
import java.util.Random;

public class Main
{
    public static void main(String[] args)
    {
        // Generate data
        int arraySize = 32768;
        int data[] = new int[arraySize];

        Random rnd = new Random(0);
        for (int c = 0; c < arraySize; ++c)
            data[c] = rnd.nextInt() % 256;

        // !!! With this, the next loop runs faster
        Arrays.sort(data);

        // Test
        long start = System.nanoTime();
        long sum = 0;
        for (int i = 0; i < 100000; ++i)
        {
            for (int c = 0; c < arraySize; ++c)
            {   // Primary loop.
                if (data[c] >= 128)
                    sum += data[c];
            }
        }

        System.out.println((System.nanoTime() - start) / 1000000000.0);
        System.out.println("sum = " + sum);
    }
}
```
With a similar but less extreme result.

My first thought was that sorting brings the data into the cache, but that's silly because the array was just generated.
  - What is going on?
  - Why is processing a sorted array faster than processing an unsorted array?
The code is summing up some independent terms, so the order should not matter.

### This shows that the asker attempted to figure it out themselves
This was demonstrated by showing both results in Java and C++ and suggesting that it might be due to the fact that sorting brings data into the cache but showed they do know something and said that thought was incorrect because the array was just generated. 

### Now onto a NOT smart example:

Header: Why is this bad?

Hi,
My program is slow. I tried doing stuff. It uses Java.
I have a list of numbers. When I sort them it's slower than when I don’t. But I thought sorting helps?
```
for(int i = 0; i < list.size(); i++) {
  if(list.get(i) > threshold) count++;
}
// etc.
```
What is going on? Please help ASAP!!

[something]

## Conclusion

Asking a smart question not only can be applied to coding questions but can also be applied to emailing professors, TA’s, or really anyone in order to get help with whatever it is you need help with. For non coding problems, I don’t think you have to go too in depth on what you’ve googled but to include the link to the assignment, your class plus your section number, and what you’ve attempted and are confused on does make the professor and/or TA more likely to help you in my past experience.

