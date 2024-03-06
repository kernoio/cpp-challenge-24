# Kerno's C++ Linux Engineering Challenge

Howdy 👋  You are here because you think you've got what it takes to join the ranks of an early-stage going into hyper-growth high-tech startup!
Now, shall put it to test?

We are in the lookout for beast-mode backend developers, mindful of architecture, data structures, performance and good engineering work — but whom always keep an eye on timely, customer-facing value delivery.

You are proficient in C++, you write clean but high-performance code and know how to take advantage of the internals of your compiler and your toolchain.


**But don't be shy!**
We place great value in education and experience; but we also recognize that talent is built on passion and hours dedicated to deliberate practice and learning... so don't shy away from applying if you feel you have what it takes!



## The challenge:
Write a C++ (linux) program "processor" that receives a stream of http "messages" (both inbound and outbound) via unix pipe.
The program maintains a minute by minute aggregation map by **request path** and **response code** dimensions.
Messages will not be ordered (you can receive 4 requests in a row, and subsequent responses), so you need to find a means to correlate them.
Every minute the map should be printed to a file indicated by the `-o <filepath>` argument received by your program.


### What we will be looking at?
- your code does what it's supposed to (duh!)
- your code is well organized and extensible (clean code practices)
- your code leverages adequately language features (C++20 and on)


### Some food for thought (a.k.a., nice to have's)
- What would happen if we added messages in another protocol / format?
- What would happen if the message rate exceeded your CPU capacity?
- What would happen if some messages never got a response?


### CPP is a very diverse universe
We do favor CLANG and BAZEL for most things -- but feel free to use whatever suites you best at this time. We prefer to see a good structured CMake project if that's more in your toolbelt than a half-baked Bazel one.


### Why THIS challenge?
Although algos and binary searches and whatnot are important in life... part of your job will be figuring out protocols and building highly efficient data transformation pipelines in resource constrained environments... so it will look a bit (likely quite more complex tho) like this challenge.

Was this too easy?... no worries... this is just a conversation starter.


## Clone this project to get started!
It contains a little go binary for linux (run it in a non-privileged docker please) that you can use to get the messages streaming:
```bash
$ ./generator | ./processor
```

### Deliverable
Please be kind to provide Dockerfile(s) to build and and test your code... setting C++ environments can be a bit painful and we have a lot of applications to review!
