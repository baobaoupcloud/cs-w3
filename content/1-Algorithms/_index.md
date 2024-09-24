---
title : "Algorithms"
date :  "`r Sys.Date()`" 
weight : 1 
chapter : false
pre : " <b> 1. </b> "
---
**Algorithm** can be imagined as a black box that may take an input and creates an output. 

As we step into this week, we will consider how the way an algorithm works with a problem may determine the time it takes to solve a problem. Algorithms can be designed to be more and more efficient, to a limit. We will focus upon the design of algorithms and how to measure their efficiency. We will use the time complexity to evaluate following algorithms’ performance.

**Time Complexity** considers how many times each statement executes. It is not the actual time required to execute a particular code, since that depends on other factors like programming language, operating software, processing power, etc. 

To express the time complexity of an algorithm, we use the **Big O notation**. It expresses how quickly the times grow relative to the input called `n` . 

For example that the run time of an algorithm grows “on the order of the size of the input”, we would state that as `O(n)`.

Or the time complexity `O(log n)` means that the time is decreased at a magnitude that is inversely proportional to the input `n` . Its algorithm doesn’t have to go through all of the input, since they usually work by discarding large chunks of input each step.

Programmers are also interested in the best case of an algorithm with the symbol Omega. Such as `Ω(n)` means that the algorithm takes n steps in the best case.
