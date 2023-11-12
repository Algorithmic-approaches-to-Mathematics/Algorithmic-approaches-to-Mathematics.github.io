---
title: "Help guide"
date: 2023-06-23T19:44:49+01:00
draft: false
order: 1
description: "How to help yourself when stuck"
summary: '![image](https://imgs.xkcd.com/comics/unsolved_math_problems_2x.png)'
---


# What to do when I encounter problems?

## By Paweł Piekarz and Enrico Caprioglio (TAs on the course)
# What to do when I encounter problems?

![image](https://as1.ftcdn.net/v2/jpg/02/51/39/64/1000_F_251396412_Me2JAC075fZGVFFW4UQjCRuwd0d9VsSi.jpg)

At various times during the course, you will encounter different problems while working on the notebooks. That’s absolutely normal! You aren’t expected to already know and be able to do everything. Otherwise, why would you even be doing the course? Encountering challenges and making mistakes is a natural part of learning; however, to learn, you must overcome those obstacles. And sometimes it's hard to figure out how to do it, all by yourself.

## Obtaining help

![image](https://media.istockphoto.com/id/691703496/photo/group-of-students-at-the-university-using-a-laptop-computer.jpg?s=612x612&w=0&k=20&c=vfg5LK876DiVQOZfl5g_rFwlsI9BKYI3NK95d1V95lg=)

The easiest way of getting some support is **discussing the problem with your peers**. You all have different strengths and weaknesses. Some other students might have already solved your problem or might be struggling with something you’ve done. Talk with people around you and help each other! Even if you don’t find a solution, discussing and brainstorming about it will help you understand it better.

Another easy way of obtaining guidance is going through the notebook before the labs, and **coming to the labs with prepared questions and problems.** Tutors are there to help you with any problems related to the topic. Asking them some prepared questions and presenting them with defined problems will also help them with helping you and allow you to spend more time on the labs focusing on other content. You can also **ask questions** about any challenges **during the labs** as you encounter them.

## Helping yourself

Problems during this module may come in different types. Sometimes the code might be giving you errors, doing things you weren’t expecting, and sometimes you might not know what to write or won’t understand what you’re meant to do on a conceptual level. If you can’t get help from others, it might often seem confusing and overwhelming. To make it easier, first, break down and identify what exactly is the problem you are having.

If you are **confused** about what’s going on **conceptually**, whether it’s about **writing code in Julia**, or about **mathematical foundations** of the material, you might need a review of the basics.  The [Mathematics Preliminaries](https://algorithmic-approaches-to-mathematics.github.io/prerequisites/mathematics-preliminaries/) page in [Prerequisites](https://algorithmic-approaches-to-mathematics.github.io/prerequisites/) tab contains references to courses covering most of the mathematical foundations of what’s going on, mostly on [Khan Academy](https://www.khanacademy.org/math), as well as some computational courses. Enrico lists the most course-relevant topics and videos on that page. When it comes to Julia, [Think Julia](https://benlauwens.github.io/ThinkJulia.jl/latest/book.html) is a free book that explains the basics pretty well in the first 3 chapters. The official [Julia Academy](https://juliaacademy.com/) contains many courses covering all topics from the basics to any advanced topics you would need. For any of you struggling with more advanced problems, [Introduction to Computational Thinking](https://computationalthinking.mit.edu/Fall23/) course is an excellent resource.
![image](https://previews.123rf.com/images/fbatista72/fbatista721401/fbatista72140100275/25434903-formula-advanced-math-equation.jpg)

Sometimes you know what you want to do on a theoretical level, but you may find it difficult to **translate your ideas into code**. The easiest way is to break down what you are planning to do in small steps. Take a pen and some paper, and write down or draw a flowchart - your inputs, array sizes and so on. Plan out what you want to do with them, how to process which values, with which iterators or indices, step by step. Then following your schematics, write code to follow them step by step. Analogically, if your **code isn't doing what you think it should**, you can write down your inputs, and following your code step by step, manually check what the code is doing and where it gets wrong. You can automate this process by **debugging** - use *print* function to return values you want to check to see if they are what you expect, or when they go wrong.
![image](https://prepbytes-misc-images.s3.ap-south-1.amazonaws.com/assets/1679044531720-1-01%20%2813%29.png)
**Attribution:** [Prepbytes blog](https://www.prepbytes.com/blog/)

Often, you will know what you want to do, but it won’t work – the code will throw **errors** or will do **something else than you expected**. In those cases, **Live docs** are your best friend. You can access them by clicking on them in the bottom right corner of your notebooks. Any in-built function or keyword you type or select will be explained there in real-time, with examples of its usage. Read how it works and compare the examples to how you have used it – should it work as you intended it to, or should you apply it differently? If you are looking for a function to do something, try typing what you think it's called - Live docs might suggest the actual name!
![image](https://miro.medium.com/v2/resize:fit:1400/1*FkxX64sbBjQXqmYf6Zzy_A.gif)
**Attribution:** [Towards Data Science](https://towardsdatascience.com/)

If knowledge of Julia, its syntax, and Live docs aren’t enough to help with errors, it might be time to check **online communities** for help. [Stack Overflow](https://stackoverflow.com/questions/tagged/julia), the official [Julia Discourse](https://discourse.julialang.org/) forum, and [r/Julia](https://www.reddit.com/r/Julia/) subreddit are very active and helpful. Most of the common problems you will encounter have already been discussed there and you should find the solutions just by searching for them. Generally, using Google or other search engine to look for a specific error message or describing the problem you are facing, should be enough to lead you to a thread with a detailed explanation of the solution.

### More on errors

Arguably, much of coding consists of interpreting errors. If you have already copy-pasted online your error output but the answers on the forums are even harder to interpret is there anything else you can do?
Most likely, the answer is going to be annoyingly simple. Here are a few tricks that may be helpful:

- `MethodError`
This is a sign that you may have called a function but the arguments of the function are of the wrong type.
If you are using Pluto notebooks, the error message should indicate at what line the error was encountered.
**Note:** if you have called another function defined previously in the notebook this may not always be in the cell you have just evaluated. Pluto should automatically redirect you there. To solve this error, you should start by making sure all the arguments of the function are of the correct type. You may find useful to rerun the cell, but add before the error a line that prints the type of all the arguments of the function. Then, by checking via the live docs what the correct arguments types should be for the function you are using, you should easily spot what causes the error.

- `Multiple expressions in one cell` or `syntax: invalid syntax (incomplete #<julia: "incomplete: "begin"`
This indicates that you have multiple lines of code in a cell but you forgot to add `begin` and `end` or the line containing `end` is ending another expression such as and `if` statement or a loop. A simple way to prevent this, is to make sure you follow standard indentation practices. Choose an indentation style such as from this [wiki](https://en.wikipedia.org/wiki/Indentation_style) or (better choice) follow the indentation style used in the notebooks. This will help you idetify exactly where a cell, a loop, or an if statement begins and end.

- `BoundsError: attempt to access 4-element Vector{Int64} at ...`
This is another common error that anyone who codes encounters daily. Basically, at some point you are trying to access a vector or matrix at some elements that does not exist. There are two things you should do to fix this error:
	- make sure you are using matrix splicing correctly: `mat[start:step:end, start:step:end]`
	- make sure that the matrix or vector you are accessing is of the correct size. Before performing the operation, add a line such as: `println(size(mat))` to check it is indeed the correct size.

- `Multiple definitions for`
This is an error specific for Pluto notebooks. It indicates that the same variable has been assigned a value in multiple cells. If this happend while debugging, you may want to use `let` `end` rather than `begin` `end`. This will let all the variables in the cell that starts with `let` be defined as **local variables**. You won't be able to use these variables anywhere else in the notebook, but at the same time they won't mess with variables already defined if you are just dong a quick check.

### Other general tricks

Everyone has different coding styles, as you code you will develop your own. By `style` I actually mean that different people tend to make different mistakes! Naturally, there will be many different ways to try to avoid making these mistakes. Here are a few tricks that TA's have put together:

- Use `println()` at any point in your code to check if you the code is doing the operations you expect. For instance, let's say you are running a large simulation, or performing different operations using matrices. At some point, you perform a dot product between two vectors and use the result to update another variable. However, at the end of you simulation you result is `inf` or `NaN`. Is the result of the dot product what you would expect? Just add a line with `println(dot_prod_result)` to make sure everything is going as you'd expect!

- If your cell is quite long and it has become hard to spot where the error(s) occurs (and all the above tricks haven't really worked out) try to split the cell into multiple cells, together with the addition of multiple `println()` to check if every operation is performing what you would expect. Once everything is working correctly, comment out or delete the `println()` functions and recombine the cells. It will be much easier to spot the source of the errors this way.

- (This is quite a personal trick and may not apply to everyone) When answering a question, or before writing any function, write a piece of code using a simple example. It is quite hard to write a general function immediately and then spot errors. Instead, it is much easier to write a short piece of code performing the operations you want to do using a simple example. For instance, let's say you want to write a function that performs a matrix operation. Rather than starting with a general function that accepts any matrix size as an input, first perform the matrix multiplication using two `2 x 2` matrices. Once everything is working as you'd expect, use `3 x 3` matrices. Once you fix the errors you encounter, use more complex inputs such as a `50 x 50` matrix and a `60 x 50` matrix. Any errors this time? Once you fix all the errors and add the relevant conditions required to perform the matrix multiplication you are ready to write the function. Once the function is written, keep testing new inputs. New errors will come up but it will be much easier to spot where the errors arise.

- Write comments! We forget things all the time, even the most obvious things. Luckly, comments require a very little amount of memory so add as many as you like in your notebooks. It will be much easier in December to go back to notebook 1 and revise for the exam if you have added your personal comments in the notebook. **However**, in general, there exists some [common practices](https://stackoverflow.blog/2021/12/23/best-practices-for-writing-code-comments/) to write comments if other people need to read your code (such as examiners in this case!). Comments will be helpful to show the examiners that you have a good indea of what the mistakes could be, even if you haven't really managed to solve the issue. As also mentioned [here](https://stackoverflow.blog/2021/12/23/best-practices-for-writing-code-comments/), it is important to add the source of pieces of your code if you have taken bits from the internet. This is important for you to remember where something came from (if later on that piece of code is causing you some trouble), as well as for the examiners.

