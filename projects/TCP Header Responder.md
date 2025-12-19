---
layout: project
type: project
image: img/tcp header.png 
title: "TCP Header Responder"
date: May 2025
published: false
labels:
  - C++
  - Visual Studio Code
summary: "Reads, writes, and manipulates binary data that are TCP headers."
---

<img class="img-fluid" src="/img/tcp header.png">
TCP Header Responder C++ Project

This project is a C++ project that I created in ICS 212 programming structure in spring 2025 that reads a 20 byte TCP header from a binary file. Once read, it extracts information like source and destination ports, sequence numbers, acknowledgement numbers, and active flags. Then it's printed so that the user can read understand what the file contains. The program is also able to create a response header by taking an existing request header and make modifcations like swapping the source and destination ports, etc.

I was also the sole developer for this project and so I implemented the read and write functions as well as the print and make header function. I wrote the logic to correctly discern the binary data into readable summary of the TCP head. I also wrote a function where I modified only specific bits within a bite. 

Somethings I learned from this project was how to use fstream in order to read binary files as well as bitwise operators in order to modify specific sections of the byte. I also learned how to interpret and convert multi-byte binary data into meaningful numbers.

Here is the project: <a href="https://github.com/KateHamada/TCP-Header-Responder.git">TCP Header Responder</a>
