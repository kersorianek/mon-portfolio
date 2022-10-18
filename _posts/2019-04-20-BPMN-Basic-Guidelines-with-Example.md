---
layout: post
title: BPMN Basics for Business Analyst
subtitle: Business Process Model and Notation Quick Guidelines  
tags:
  [
    business system analysis,
    system analysis,
    business analysis,
    bpmn,
  ]
image: /assets/img/diary.png
bigimg: /assets/img/back.gif
thumbnail-img: /assets/img/diary.png
share-img: /assets/img/diary.png
cover-img: /assets/img/cover.jpg
---

BPMN stands for Business Process Modeling Notation. It is a graphical notation style; In other word, a visual language. BPMN is a flow chart based modeling language.
It describes processes as flow of activities, or actions, arranged in swimming lanes, representing activity performers

_Qucik Link to Specific Topic:_

- [What is BPMN?](#what-is-bpmn)
- [Benefits of Using BPMN:](#benefits-of-using-bpmn)
- [Basic Components of BMPN:](#basic-components-of-bmpn)
	- [Activity:](#activity)
- [About Content Creator:](#about-content-creator)
- [All Posts on Business Analysis:](#all-posts-on-business-analysis)

Business Process Modeling Notation (BPMN) 2.0 Model

# What is BPMN?

BPMN (Business Process Modeling and Notation) is the global standard for modeling business processes, which is a critical component of business process management. 

BPMN diagrams enable many stakeholders to view business processes, making it simpler to improve workflow effectiveness and efficiency.

Everyone from business analysts to developers to company managers may "speak the same language" and confidently adjust to changing conditions.

 
 BPMN was created in 2004 by the Business Process Management Initiative (BPMI). BPMI collaborated with the Object Management Group (OMG) in 2005.

# Benefits of Using BPMN:
- All stakeholders can understand how a process works
- IT and business analysts can work together on a consistent, accurate process design 
- Everyone can understand how a technical process lives within the bigger business picture

BPMN Allow you to GAP Analysis during requirement analysis and model 
1.  Current state: “as-is”
2.  Future state: “to-be”

# Basic Components of BMPN: 
	1. Swimming Lane: Independent Process (Divider between processes)
	2. Lane:  Functionality or Activity within a Swimming Lane
	3. Event:  Mark start and end of a process. 
	4. Gateway: Control process flow, Can test a decision.
	5. Activity: Process or Sub process. Naming convention should use verb and noun
	6. Sequence Flow: A solid arrow that connects Event, Activity, and Gateway


## Activity: 
A BPMN Activity is simply "Work" that a company or organization performs in a business process. An Activity is can be atomic (Tasks) or decomposable (Sub-Processes). There are basically three BPMN activity types:

	1. BPMN Task
	2. BPMN Sub-Process
	3. BPMN Call Activity


A BPMN task is an atomic activity within a process flow. You create a task when the activity cannot be broken down to a finer level of detail. Generally, a person or applications will perform the task when it is executed.

In BPMN 2.0, there are different types of tasks identified for use in representing more specific behavior that tasks might represent. Here is a list of BPMN 2.0 task type:
	• Service Task
	• Send Task
	• Receive Task
	• User Task
	• Manual Task
	• Business Rule Task
	• Script Task



Service Task
A Service Task is a Task that uses a Web service, an automated application, or other kinds of service in completing the task.

Service Task
The example below shows the process of answering a question in a forum. A Service Task is used to represent the publishing of answer on Twitter, through the web service they provided.

Send Task
A Send Task is represents a task that sends a Message to another pool. The Task is completed once the Message has been sent.

Receive Task
A Receive Task indicates that the process has to wait for a message to arrive in order to continue. The Task is completed once the message has received.

User Task
A User Task represents that a human performer performs the Task with the use of a software application.

Manual Task
A Manual Task is a Task that is performed without the aid of any business process execution engine or any application.

Business Rule Task
Business Rule Task is newly added in BPMN 2.0. It provides a mechanism for a process to provide input to a Business Rules Engine and then obtain the output provided by the Business Rules Engine.

Script Task
A Script Task is executed by a business process engine. The task defines a script that the engine can interpret. When the task begin, the engine will execute the script. The Task will be completed when the script is completed.


BPMN Sub-Processes
In BPMN, a sub-process is a compound activity that represents a collection of other tasks and sub-processes. Generally, we create BPMN diagrams to communicate processes with others. To facilitate effective communications, we really do not want to make a business process diagram too complex. By using sub-processes, you can split a complex process into multiple levels, which allows you to focus on a particular area in a single process diagram.

BPMN Sub-Processes
BPMN specifies five types of markers for Sub-Processes. We will go cover each of them in the sections below.

BPMN Sub-Processes Example
Loop
A Sub-Process with loop marker indicates that the sub-process repeats itself in sequence.

Loop
Multi-instance
A Sub-Process with Multi-Instance marker indicates that the sub-process can run with other identical sub-processes simultaneously.

Multi-instance
Compensation
A Sub-Process with Compensation marker, or simply called a compensation sub-process, represents a collection of tasks that describe some part of the compensation method.

Compensation
Ad hoc
A Sub-Process with Ad-Hoc marker represents a collection of tasks that exist solely for handling a specific case.

Ad hoc
BPMN Call Activities
A BPMN Call Activity references an Activity defined in a process that is external to the current process definition. It allows you to create a reusable process definition that can be reused in multiple other process definitions.

The figure below shows a BPMN Call Activity example. It consists of a Call Activity Register that references the Register task defined in a global process.

BPMN Call Activities



 


----------------------------------------------------------------------
----------------------------------------------------------------------

# About Content Creator: 


Hi, This is **Rafayet Hossain**, a seasoned Business System Analyst (BSA), Project Manager, and SQA Engineer. He acts as a change agent to enable digital changes to your organization.

For Any Query or Assigment Contact: 

[![Linkedin](https://img.shields.io/badge/-LinkedIn-blue?style=flat&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/rafayethossain/)
[![Gmail](https://img.shields.io/badge/-Gmail-c14438?style=flat&logo=Gmail&logoColor=white)](mailto:rafayet13@gmail.com)


----------------------------------------------------------------------
----------------------------------------------------------------------



 
# All Posts on Business Analysis:  

Click on any of the desired links to directly access the information.

- [x]  [**An Introduction to Business Analysis and the Business Analyst**](https://rafayethossain.github.io/2019-01-22-Introduction-to-Business-Analysis/)
- [x]  [**Project Initiation Activities as a Business Analyst**](https://rafayethossain.github.io/2019-02-07-Project-Initiation-Business-Analysis-Activities/)
- [x]  [**Project Inititation Activities**](https://rafayethossain.github.io/2019-02-25-How-to-Prepare-Business-Case-Business-Analyst/)
- [x]  [**How to Prepare a Business Case for Project**](https://rafayethossain.github.io/2019-02-25-How-to-Prepare-Business-Case-Business-Analyst/)
- [x]  [**How to Manage Your Project Stakeholder Using RACI Matrix**](https://rafayethossain.github.io/2019-02-27-Stakeholder-Management-Business-Analyst/)  
- [x]  [**Everything You Need to Kow About Software Requirements**](https://rafayethossain.github.io/2019-03-03-What-is-Software-Requirements/)
- [x]  [**Requirements Elicitation Techniques You Must Learn**](https://rafayethossain.github.io/2019-03-30-Requirement-Elicitation-Complete-Guidelines/)
- [x]  [**How a Pro BA Analyze Software Requirements**](https://rafayethossain.github.io/2019-04-04-Requirement-Analysis-Guidelines/)
- [x]  [**BPMN Basics for Business Analyst**](https://rafayethossain.github.io/2019-04-20-BPMN-Basic-Guidelines-with-Example/)
- [x]  [**Requirements Specification Techniques**](https://rafayethossain.github.io/2019-05-01-Requirement-Specification-Techniques/)
- [x]  [**Preparing a Software Requirement Specification (SRS) Document That Works**](https://rafayethossain.github.io/2019-05-07-How-to-Write-SRS-Document/)
- [x]  [**Software Requirements Approval to Kick off Development**](https://rafayethossain.github.io/2019-06-06-Requirement-Approval-Process/)
- [x]  [**Change Control Process in SDLC**](https://rafayethossain.github.io/2019-07-07-Change-Control-Process-in-SDLC/)
- [x]  [**Agile Project Managment with Srum Roles and Responsibilites**](https://rafayethossain.github.io/2022-10-10-Agile-Scrum-in-a-Nutshell/)




{: .box-success}
Enjoy !!!
**See Yaaa, Next.**

![Diary](/assets/img/diary.png "Diary")
