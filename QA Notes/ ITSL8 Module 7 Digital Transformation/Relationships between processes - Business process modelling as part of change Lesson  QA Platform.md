---
title: "Relationships between processes - Business process modelling as part of change Lesson | QA Platform"
source: "https://app.qa.com/course/business-process-modelling-part-change-1698/relationships-between-processes/?context_id=13677&context_resource=lp"
author:
  - "[[QA Platform]]"
published:
created: 2025-02-10
description: "Relationships between processes - Business process modelling as part of change lesson from QA Platform. Start learning today with our digital training solutions."
tags:
  - "clippings"
---
Here you can see that the organisation is the sum of it’s processes and the process is the sum of its tasks.

![The organisation chart starts with the organisation at the top, that is linked down to the organisation processes.  One of the process shows the variety of tasks that are needed to complete that process.](https://assets.cloudacademy.com/bakery/media/uploads/entity/blobid1-f18c8ab3-fa56-48aa-9cb3-397ca1d7a62f.png)

Figure 1: Relations between the processes

There should be minimum coupling, i.e., the only dependency should be at the end of a process or task and a process or task should be replaceable without affecting the others. 

In our At Home cinema example (detailed on the previous step), we should be able to replace a task or a process without affecting the next task or process or the one preceding it. (For example, we could choose to replace one film promotion process with a completely different process, and if result is the same then we will still sell tickets.) 

Identifying the relationships helps us to understand the processes as modular entities; that is, with a distinct start and end. 

We can also apply the same logic to tasks, as they too have a distinct start and end. 

For each process we need to understand the triggering event, outcomes and outputs, tasks, decisions and who is involved. 

### **Dependency vs Flow** 

- When we are considering our processes, we start at a high level with an organisation model of processes.
- At this top enterprise level, we are interested in the dependencies between processes.
- The output of one process may be used as input by another process – this is dependency.
- We should also be able to replace an entire process with another without impacting on any other process (as the start point and outcome should be the same – minimum coupling).

New analysts sometimes confuse dependency with flow.  Dependencies and the processes help to define the scope of the situation being examined.  The dependencies also help to contain the boundary of the process itself. 

Flow happens within a single process and describes the sequence of the tasks – this is the focus of this chapter. 

### **Process Dependencies** 

- One process is related to the next
- All the processes must complete to deliver the product or service being requested by the customer.
- Any exceptions that halt a process will be considered at the event-response level. We don’t need to know what these are in detail. We are interested in what should happen, not what could happen!

In our At Home Cinema, we have three core processes at the enterprise level: Promote film, Sell ticket, and Screen film. Dependencies exist between these three processes. 

Our customers need to be able to buy their tickets to see their chosen film and the Sell ticket process enables this.  

There could be many customers using the Sell ticket process at any time: 

- Fred is at the box office buying two full price tickets for the 7:30pm showing of the latest blockbuster.
- Anne is on the website booking two adult and two child tickets for the kids’ club showing this coming Saturday.
- Lucy has phoned the box office and is buying two student tickets for the new art house film on Sunday afternoon.

Whatever the different types of tickets, different times, and different films, Promote film must happen before a customer knows what’s on offer to allow us to sell tickets. We must sell tickets otherwise Screen film cannot happen – there would be no point screening a film if no one wanted to watch it.

![Flow chart showing how each process is linked: Promote film is linked to Sell ticket, which is linked to Screen film.](https://assets.cloudacademy.com/bakery/media/uploads/entity/blobid3-e3b3ba7c-70a5-402e-8b5c-223f6a922cad.png)

Figure 2:  Dependencies between processes 

The dependency occurs because there are many promotional activities which lead to many tickets being sold and many films are shown.  

But there is only one overall process for promoting a film, one process for selling a ticket and one process for screening a film. Within each of those many instances of a process there are specific sub-processes (or tasks) that flow in sequence. 

In the diagram, there are dependencies between the processes.  

- There are tasks within each of these processes which allow them to be decomposed further.
- Within each process there are a series of tasks that determine the flow from task to task.
- Each task will be an action towards completing the overall process and are performed in sequence.

In the previous step, we focused on the core processes and the dependencies that exist between them at an organisation level. In this step, we will be using process models to define the flows between the tasks. The flow determines the order of the tasks and the participation of actors that together make up the overall process. 

### **Modelling Notations** 

There are many notations in use for modelling processes, e.g.: 

- BPMN: gaining in popularity.
- UML: widely used worldwide and can show hierarchy.
- ARIS: popular in Europe.
- IDEF: popular in the States.

A good process model should show flow (sequence), branching (selection) and looping (iteration or repetition). It should also show us the process broken down into steps, so we can see:  

- Logic of the sequence
- Who (role) performs the step?
- Decisions taken and possible outcomes.

You have come to the end of this Lesson. In the next step you will test your learning and understanding by completing a Knowledge Check. Once completed, you will then move on to the next Lesson, External Factors.