---
layout: essay
type: essay
title: "[change]"
# All dates must be YYYY-MM-DD format!
date: 2025-09-10 [change]
published: false
labels:
  - [change]
  - Technical Essay
---

<img width="300px" class="rounded float-end ps-4" src="../img/smart-questions/rtfm.png">

# Title

I’ve had instructors address a whole class and say, “There’s no such thing as a stupid question.” I now know that is in fact not true because I’ve challenged the statement and received the appropriate dumb-stricken, annoyed look. There are definitely stupid questions, and along with that, usually unhelpful answers. Though we all might be guilty of being callous and making people victim to our poorly formed questions, there are steps we can take to ask smarter questions that hopefully don’t illicit the dreaded “rtfm” or “stfw” response.

## Header

Stack Overflow, a question and answer site for programmers, is a great resource for anyone who may have issues with code or who may simply want to learn new or different methods of doing something. There I found examples of good questions and bad questions, which could probably be improved.

In the following example, we examine the components of a decent question. In this case, the asker is trying to figure out a way to get the date of the previous month in Python.

```
if int(time.strftime('%m')) == 1:
    return '12'
else:
    if int(time.strftime('%m')) < 10:
        return '0'+str(time.strftime('%m')-1)
    else:
        return str(time.strftime('%m') -1)
```
