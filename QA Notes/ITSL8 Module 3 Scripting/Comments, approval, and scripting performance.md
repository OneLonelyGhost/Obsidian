---
title: "Comments, approval, and scripting performance | ITS SQ | Lesson | QA Platform"
source: "https://app.qa.com/course/comments-approval-and-scripting-performance-itsl8-sq-a31-1698/how-add-comments-batch-scripts/?context_id=12176&context_resource=lp"
author:
  - "[[QA Platform]]"
published:
created: 2025-01-08
description: "How to add comments to batch scripts - Comments, approval, and scripting performance | ITS SQ | lesson from QA Platform. Start learning today with our digital training solutions."
tags:
  - "clippings"
---
## How to add comments to batch scripts

So, you have been asked to maintain someone else’s batch scripts or modify your own scripts written many months or years ago.

Unfortunately, scripts often lack documentation, contain unclear code, and show inconsistent styles over time.  

In this step, you will learn the best way to maintain your scripts, by using comments.

### Comments in batch scripts 

Larry Wall, the creator of the Perl programming language, said there are three great virtues of a programmer; laziness, impatience, and hubris. 

Now before you gleefully down tools, these are strictly tongue-in-cheek, true laziness requires hard work! 

So how do we achieve these virtues? 

**Laziness:** You should make your code easy to understand. Writing clear code reduces the need for many comments. 

**Impatience:** As you aim to avoid unnecessary delays in execution, you should avoid long, pointless comments. Keep comments helpful and quick to grasp. 

**Hubris:** Take pride in your code by making it as clean, organised, and understandable as possible. When commenting, this could mean making your work accessible and understandable to those who might be less familiar with the specifics of your project. 

### Comments by language 

Larry Wall may argue that a well written and simple program does not require comments, but in the real world, it is best practice to embed comments in your code.  

Most scripting languages support single line comments and some also support multi-line comments. Bash, Python, Perl, PowerShell, and JavaScript support single-line and multi-line comments with three main batch scripting languages (Bash, Python, and PowerShell) using a **\#** symbol for single-line comments.

#### Special and descriptive comments 

In UNIX and Linux scripting, start with a **#!** (Hash Bang or Shebang) followed by the interpreter's path to ensure your script runs correctly when called from the shell prompt. You only need the script’s name at the prompt. 

The hash bang line for a bash shell is **#! /bin/bash** and for a Python script is **#! /bin/python** (or possibly **#! /bin/env python3** for a specific version of Python). 

As illustrated in **Figure 1** below, it is good practice to follow a special comment (in all scripting languages) with descriptive comments on the author, version, and a clear description of what the script does (not how it does it).

## ![Diagram showing the hash bang line for a bash shell, as described in the text above. The author is JBloggs. The version is 1.0. The description says , ‘daily incremental backup of users home directories’.](https://assets.cloudacademy.com/bakery/media/uploads/entity/blobid1-a042b3ff-f11a-4768-8bbc-65eb0ecd96b0.png)

**Figure 1:** Script comments in UNIX and Linux.

When you’re ready, select **Next** to continue.