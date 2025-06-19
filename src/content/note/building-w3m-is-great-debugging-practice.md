---
title: Building w3m is Great Debugging Practice
description: When I sat down to install and use w3m today, I didn't realize I would be embarking on the debugging odyssey that I am about to share with you.
publishDate: "2025-06-17T18:26:00Z"
---

Probably the number one gratification that will never get old for me as a developer and Linux user is building software from source. That little feeling that you get when you finally finish debugging a mountain of errors and get the code to compile is akin to putting the final piece of a puzzle into one of those stupid 1,000 piecers I hate. [1] You let your family build 90% of, while you finished the last 10% which was easy because they helped you figure your part out, even after solving the entire thing which took them the better part of the weekend (which is amazing considering they did it with a smile on their faces [2]), but also makes you feel like you are a super wizard of puzzles. Open source software developers who build tools that are dependencies for major software products like Node.js and major Python libraries truly are angels and that is a whole different story because sometimes I can hardly believe that somebody takes the time to build all these tools.

Back to my debugging experience, I was attempting to download a little tool called w3m and expected it to be a quick download of a compressed file, IYKYK like the ones on Linux you have to extract with the tar command and end in `.tar.gz`. Sure, the download was fast enough on my hotspot, but I wasn't expecting to spend the whole afternoon wrestling around with 53.5 megabytes of files and folders and bash commands and dependencies, etc. The first sign that I was getting myself into something that was more than a mere click and go install was right after the execution of basically the first command I ran in the process. I'll go ahead and show my exact walkthrough of what happened:

```bash
tar -xvzf w3m-0.5.3.tar.gz

Error: Can't untar the tar zip compression tardar bar tar gzzzzz 1
bleeehhhhhhheeerrrrpppppp
```

That just isn't supposed to happen when you're trying to extract a TAR archive - well, that is after you decompress the gzip of course. Well since that was pissing me off, I decided to jump into the documentation like a good problem solver to find out that I need to download some C and C++ garbage collector, which is no big deal right? Sounds cool to me and like another good rabbit hole to jump down another day, but as you'll soon see, this garbage collector is kind of a pain in the ass for anyone who is trying to use w3m. 

### `gc.h` Can't Be Found - After All ******* That?!?!?

...To be continued.....................

-----------------------------------------------------------------IN  PROGRESS----------------------

[1] That some asshole created out of a replica of Van Gogh's Starry Night or a cross of an Action Jackson and Picasso mash up painting that features every imaginable color and shape into a small frame

[2] This analogy is intentional - this really is how open source software is when you think about it. Some random guy builds all these crazy complex tools using C and whatever else godforsaken language they need to use for interacting with OS processes which probably takes them all of the free time they have outside of work to build, leaving them with exactly 4 hours each day to sleep, eat, raise children, have a social life, and anything not related to managing and moderating the open source software repository issues and pull requests, writing the code, and creating documentation. All of this work creating a C library that integrates your front end framework with a browser with WebAssembly, Deno, Rust, and all the frontend tools, blah, blah, yada, yada that runs a single process - only for you to be able to run your fart noises and glitter exploding task box checking animations for the half assed to do list application you built for your hackathon project. Thank your open source tool creators when you get the chance :)