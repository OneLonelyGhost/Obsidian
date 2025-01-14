---
title: "The levels of approval required for authorising batch scripts - Comments, approval, and scripting performance | ITS SQ | Lesson | QA Platform"
source: "https://app.qa.com/course/comments-approval-and-scripting-performance-itsl8-sq-a31-1698/levels-approval-required-authorising-batch-scripts/?context_id=12176&context_resource=lp"
author:
  - "[[QA Platform]]"
published:
created: 2025-01-08
description: "The levels of approval required for authorising batch scripts - Comments, approval, and scripting performance | ITS SQ | lesson from QA Platform. Start learning today with our digital training solutions."
tags:
  - "clippings"
---
Once you have written a script, how do you go about deploying it?

There is no simple answer to this question. Instead, it depends on what the script does, who is using it, where will it run, and whether it needs to run with higher privileges.

### Scope

If you are writing a script for yourself for fact-finding with your own or public data, then you may not need approval at all. However, if you were to write a tool that modifies your system, then it is likely that you will need to run the script with higher privileges (root or admin user account). In this case, you will need approval, likely from the system administrator or your line manager.  

It may help to think of the levels of approval as a sequence of nested bubbles or scopes, as illustrated in **Figure 1** below.

## ![Diagram showing the different levels of approval for various use cases: Local personal data - read only; Local System Config - read write; Server System Config/Production data - read/write; Network/System config/Customer data - read write; Cloud/System Config/Customer data - read write](https://assets.cloudacademy.com/bakery/media/uploads/entity/blobid1-be31a1ae-c2b9-407a-9755-05f71d0a0c74.png)

**Figure 1:** The levels of approval required for authorising batch scripts.

As you move towards the outer bubbles or scopes, your scripts may then interact with servers, networks, cloud instances, system data, production data, and customer data. It is likely that will need to get approval from the stakeholders of those systems and data. 

Once your scripts have been tested, you usually will need to gain approval/s before deploying on the production environment.  

If in doubt, you can always ask your line manager and the systems or data manager in your organisation.

### Testing 

One of the most important steps in software development is testing, which should be done before deployment, irrespective of which bubble/scope you are in.  

Testing should be done in a staging environment that acts as a near replica of the production environment.  

A virtual machine is often used by programmers to test, build, and deploy software in a safe environment. 

### Collaboration

If you are developing scripts in a team, you may find yourself using collaborative tools and online repositories such as GitHub, Gitlab, or Bitbucket. Most collaborative tools come equipped with version control, allowing programmers to track changes.  

Some programming tools can be configured to have rules for single or multiple approvals. This is useful when it comes to moving software through the development, testing and deployment stages.

When you’re ready, select **Next** to continue.