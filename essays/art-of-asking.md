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

```
Why is processing a sorted array faster than processing an unsorted array?

In this C++ code, sorting the data (before the timed region) makes the primary loop ~6x faster:

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

- Without std::sort(data, data + arraySize); , the code runs in 11.54 seconds.
- With the sorted data, the code runs in 1.93 seconds.

(Sorting itself takes more time than this one pass over the array, so it's not actually worth doing if we needed to calculate this for an unknown array.)
```

First things first, the header: “Why is processing a sorted array faster than processing an unsorted array?”
This is a good header because it’s clear, concise, and specific as in, they could’ve said “Why is my code slow?” but instead chose the header above. Not only that but it also invites explanation and is search friendly so that if someone else has the same question, which is likely, they would also be able to get their answer from there.

Within the body of the question, the asker is clear and gives the measured timings of the processing times “11.54 seconds” and “1.93 seconds” and clearly asks why the difference exists. This shows that the asker has an interest in understanding the background hardware stuff that’s happening that they don’t know about, which helps get people to answer their question. 

```
A: datetime and the datetime.timedelta classes are your friend.

1. find today
2. use that to find the first day of this month.
3. use timedelta to backup a single day, to the last day of the previous month.
4. print the YYYYMM string you're looking for.

Like this:

 >>> import datetime
 >>> today = datetime.date.today()
 >>> first = datetime.date(day=1, month=today.month, year=today.year)
 >>> lastMonth = first - datetime.timedelta(days=1)
 >>> print lastMonth.strftime("%Y%m")
 201202
 >>>

```
 
The asker received six possible answers, and he or she was successful in inciting discussion from multiple users. The answers themselves were clear and were devoid of the rumored sarcasm and hostility of “hackers.” Since I myself have referenced this page and found it useful, I can confidently say that it is a good question.

## The foolproof way to get ignored.

While there are decent questions that benefit everyone, there are those one can ask to create an entirely different effect. In the following example, a user asks how he would, in short, create a desktop application with Facebook.

```
Q: Facebook Desktop Notifier

I am a beginner programmer that have never used anything other than what's included in a language.

I am trying to create a desktop application that notifies me anytime I get an update onfacebook. 
How should go about doing this? Thanks in advance.

edit Sorry I was not clear. Is there any way to make a DESKTOP application with facebook?
```

A simple “yes” would have answered the question, but we know that’s not the sort of answer he or she is looking for. Fortunately, someone kindly responded with a link to Facebook’s developer website. The asker should have done more research on his or her potential project. Then further down the road, he or she could have asked more specific and detailed questions that wouldn’t require a thousand-paged response for a sufficient answer.

## Conclusion

When we rely on others’ generosity and expertise to provide answers to our questions, it should hold that the question we ask should be one that leads to efficient and effective help that not only benefits us, but also the people we ask and others who might ask the same question in the future. Thus, if you have a question… make it a smart one! Asking questions may not always get you the best answer, but asking them in a way that will make others want to answer them will increase the success of finding a good solution and make it a positive experience on all sides.
