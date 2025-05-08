---
layout: post
title: Compilers
description: A course only offered once every 2 years at the University of Pennsylvania.
---

This semester, I had the chance to take [CIS 4521: Compilers](https://www.seas.upenn.edu/~cis5521/), a course offered only once every 2 years here at Penn. The course is taught by [Steve Zdancewic](https://scholar.google.com/citations?user=19kNRU0AAAAJ&hl=en), Schlein Family President’s Distinguished Professor of Computer and Information Science, who has research interests in programming languages and computer security. As an aside, I served as teaching assistant under Steve for [CIS 1200](https://www.seas.upenn.edu/~cis120/current/) my sophomore spring, and have always quietly admired his proficiency for PL.

On the course: it was taught in [OCaml](https://ocaml.org/), starting with subsets of x86 and LLVM IR, building up to the compilation of a bootstrapped language called Oat. We got the chance to implement the various moving parts of a compiler, from lexing, to parsing, to typechecking, analysis, and finally to optimization. My takeaway: a compiler takes some text, verifies that it's gramatically correct, and then turns it to another gramatically correct piece of text. If you think about it this way, LLMs are just glorified compilers, except much less deterministic than the ones we learned about and implemented in the course. I really enjoyed all the homework assignments, especially the last few on typechecking, analysis and optimization. OCaml is also incredibly lightweight and elegant, and the provided build environment with [dune](https://dune.build/) was such a comfy experience.

On the difficulty: either this kind of content comes more naturally to me, or the course is not as bad as many make it out to be. If you've been following along with the course content, the assignments are really quite accessible. Code files are well annotated and the assignments are well-documented. That being said, this will probably still be one of your harder courses this semester due to the volume of work that it demands. Despite being easy, writing the code can be somewhat tedious and difficult to debug. There's no better way to spend a Sunday evening reading a few hundred lines of assembly...

Highly recommend for the CIS majors at Penn! Take it while you still can, and you'll learn a lot about the cool optimizations compilers do under the hood to make your code run fast.


