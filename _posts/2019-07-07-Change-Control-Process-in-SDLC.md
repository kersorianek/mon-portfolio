---
layout: post
title: Change Control Process in SDLC
subtitle: Change Control Process in Software Project
tags:
  [
    business system analysis,
    system analysis,
    business analysis,
    requirement elicitation,
    change management,
    change control,
  ]
image: /assets/img/diary.png
bigimg: /assets/img/back.gif
thumbnail-img: /assets/img/diary.png
share-img: /assets/img/diary.png
cover-img: /assets/img/cover.jpg
---
Change management is critical because it establishes parameters for enhanced responsibility and structure. It also improves decision-making by offering complete visibility of all project changes.

_Qucik Link to Specific Topic:_

- [Change Control in Software:](#change-control-in-software)
  - [What is Change Control?](#what-is-change-control)
  - [Why Change Control?](#why-change-control)
  - [Few questions to be considered:](#few-questions-to-be-considered)
  - [Different aspects of the Change Control process](#different-aspects-of-the-change-control-process)
  - [Process of Change Control](#process-of-change-control)
  - [Steps for Change Control Action:](#steps-for-change-control-action)
  - [Change Management Vs Change Control](#change-management-vs-change-control)
- [Impact Analysis in Software Change](#impact-analysis-in-software-change)
  - [Why is Change Impact Analysis performed??](#why-is-change-impact-analysis-performed)
  - [What is Impact Analysis Document?](#what-is-impact-analysis-document)
  - [Elements of Impact Analysis Document.](#elements-of-impact-analysis-document)
  - [Questions to Consider When Conducting Impact Analysis](#questions-to-consider-when-conducting-impact-analysis)
  - [Best practices for change Impact Analysis](#best-practices-for-change-impact-analysis)
  - [Summary](#summary)
- [All Posts on Business Analysis:](#all-posts-on-business-analysis)

# Change Control in Software: 

## What is Change Control?

Change Control is the process through which a company documents, identifies, and authorizes changes to its IT environment. It reduces the chance of illegal changes, interruption, and faults in the system.

## Why Change Control?

When new or different modifications to the system are sought, especially by stakeholders, they are neither optional nor ignorable. It must be done without disrupting other system components. 

This is where the change control comes into play. It enables project teams to change the scope of the project by implementing defined controls and regulations. When a project is not proceeding as expected, change control is used.

To maintain control over change requests, a formal document for each change request must be created and evaluated.

## Few questions to be considered: 
A number of questions may arise when studying Change Control, such as:

  - Who will approve the change?
  - Does it require to run through a change control board?
  - How much time will be required to research and implement the change?
  - What are the impacts of changes to other components of the system (schedules, cost, resources, etc.)?
  - Is there any threshold under which the project management can approve it?

## Different aspects of the Change Control process

A Change Control procedure should take into account a number of elements.

Change Control Process Steps Action taken in Change Control:

- Change request initiation and Control
- Request for changes should be standardized and subject to management review
- Change requestor should be kept informed
- Impact Assessment
- Make sure that all requests for change are assessed in a structured way for analyzing possible impacts
- Control and Documentation of Changes 
- A change log should be maintained that tells the date, person details who made changes and changes implemented
- Only authorized individual should be able to make changes
- A process for rolling back to the previous version should be identified
- Documentation and Procedures 
- Whenever system changes are implemented the procedures and associated document should update accordingly
- Authorized Maintenance 
- System access right should be controlled to avert unauthorized access
- Testing and User signoff 
- Software should be thoroughly tested
- Version Control
- Control should be placed on production source code to make sure that only the latest version is updated
-  Emergency Changes
-  A verbal authorization should be obtained, and the change should be documented as soon as possible

## Process of Change Control

Before we look at what is involved in the Change Control process, we will become acquainted with the papers that are utilized in Change Control. There are primarily two papers involved in Change Control.

- **Change Log:** A change log is a document that contains information about all Change Requests, such as the project ID, PCR (project change request) ID, priority, Owner details, Target date, status and status date, raised by, date when raised, and so on.

- **Change Request Form:** It is used to document details needed to support the decision-making process, such as 
  - The type of change, 
  - The benefits of the change, 
  - The name of the resource requesting the change,
  - The time and estimated cost, the priority of the change, 
  - The authorized person's details, 
  - The change request status, and so on.
  - 

Change Process Flow-Diagram
  
To deploy changes in a product or system, the Change Process follows a predefined pattern. We presented the steps involved in the Change Process using a flow diagram.

## Steps for Change Control Action: 

- Change request identification
- Identify the need for a change and describe it on the project change request form
- Change request assessment
- If the change is not valid, it has to be deferred or rejected
- Determine appropriate resources required to analyze the change request
- Perform quick assessment of the potential impact and update the change request form
- At this stage, rejected change request should stopped
- Change request analysis 
- For analysis assign the change request to an authorized member
- Deferred change re-enter this analysis step
- At this stage, rejected change request should stopped
- Change request approval 
- Identify change risk and complexity level before approval
- Identify the impact level of the change before approval
- Review impact of Change Request to authorized person for approval
- At this stage, rejected change request should stopped
- Change request implementation 
- Update project procedure and management plans
- Inform about the changes to the team
- Monitor progress of change request
- Record the completion of change request
- Close change request

_NOTE: The approval for Change Control may be done by Project Manager, Lead IT or Lead Developer, Stakeholder._

## Change Management Vs Change Control

- Change management is in charge of managing and regulating change requests to make changes to the IT infrastructure or any component of IT services in order to reduce the risk of service interruption and promote business advantage.
  
- Change control operations involve submitting, documenting, assessing, and approving changes in order to enhance the overall performance of the system or product.

# Impact Analysis in Software Change

- What is Impact Analysis?
- Impact Analysis is defined as analyzing the impact of changes in the deployed product or application. It gives the information about the areas of the system that may be affected due to the change in the particular section or features of the application.
- 
The impact on requirements, design and architecture, testing, and timeline is examined.
With the inclusion of new features into an application or product, it becomes critical to assess the impact of these new features or modifications on system performance. As a result, Impact Analysis is carried out.

## Why is Change Impact Analysis performed??

- It is done to understand the possible outcome of implementing the change. Inducing too much functionality into a product can reduce the overall performance of the product.
- To identify all the files, documents and models that might have to be modified if a team decides to implement the change in product
- To estimate the effort needed behind implementing the change
- To identify the task required to implement the change
- It will list the dependencies on a specific element

## What is Impact Analysis Document?

The Impact Analysis document can be used as a checklist. It is used to assess modification requests before proceeding with them. The Impact Analysis document should include information such as:

- Brief description of an issue
- Explain or show an example of how the defect is causing failure and/or inefficiency
- Include an estimate of complexity
- Include an estimate of cost and time for a fix
- Functionality to be tested
- List down the new test cases created for the change
- Reference document- Mention the reference document, technical specification, etc.

## Elements of Impact Analysis Document.

1. Change Request ID:
2. Title:
3. Description:
4. Date Prepare:
5. Prioritization estimate:
   o Relative Benefit
   o Relative Penalty
   o Relative cost
   o Relative risk
6. Estimated total effort: …..hours
7. Estimated lost effort: ……..hours
8. Estimated schedule Impact:……days
9. Quality Impacted;
10. Other Requirement affected:
11. Other tasks affected:
12. Integration issues:
    How to present Impact Analysis influence level
    Impact Analysis can be marked as per the color code to represent the criticality of the changes or impact of the changes over the system. The color code could be anything as shown below.
    - **Red** - Strong
    - **Yellow** - Moderate
    - **Green**- Weak

The above list explains the impact of the implemented changes



## Questions to Consider When Conducting Impact Analysis

- What are the adverse side effects or risks of making the proposed change?
- Does any tool be acquired in order to implement and test the change?
- If the change is accepted how much effort will be lost that is already been invested?
- Does a proposed change adversely affect performance requirements?
- To verify the proposed change does other user input be required?
- Does the change increase the product cost?
- Does the proposed change is something the current staff has knowledge and skills?
- Does the proposed change place any unacceptable demand on any computer resource?
  
## Best practices for change Impact Analysis
- Before initiating with Impact Analysis, make sure testing request contained no information about those part of the project that was influenced by changes
- Continue communication between developer and tester is must, not to miss any change needed to implement in the final product
- Identify if any user interface changes, deletions or additions are required.
- Estimate the number of acceptance, system or integration test cases that will be required
- Identify any impact of the proposed change to another project plan, configuration management plan or quality assurance plan.

## Summary
- The impact analysis will assure what part of an application need to be changed
- The impact on the system is analyzed on Requirements, Design & Architecture, impact on Test, etc.
- It helps to analyze what level of regression testing is required




For Any Query or Assigment Contact 
**Rafayet Hossain**

✅ Business Analyst | Project Manager | SQA | Writer ✅


[![Linkedin](https://img.shields.io/badge/-LinkedIn-blue?style=flat&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/rafayethossain/)
[![Gmail](https://img.shields.io/badge/-Gmail-c14438?style=flat&logo=Gmail&logoColor=white)](mailto:rafayet13@gmail.com)




 
# All Posts on Business Analysis:  

Click on any of the desired links to directly access the information.

- [x]  [**An Introduction to Business Analysis and the Business Analyst**](https://rafayethossain.github.io/2019-01-22-Introduction-to-Business-Analysis/)
- [x]  [**Project Inititation Activities**](https://rafayethossain.github.io/2019-02-21-Project-Initiation-Business-Analysis-Activities/)
- [x]  [**How to Prepare a Business Case**](https://rafayethossain.github.io/2019-02-25-How-to-Prepare-Business-Case-Business-Analyst/)
- [x]  [**Stakeholder Management and Stakeholder Analysis**](https://rafayethossain.github.io/2019-02-27-Stakeholder-Management-Business-Analyst/)  
- [x]  [**Everything You Need To Know About Software Requirements**](https://rafayethossain.github.io/2019-03-03-What-is-Software-Requirements/)
- [x]  [**Requirement Elicitiation Techniques You Must Know**](https://rafayethossain.github.io/2019-03-30-Requirement-Elicitation-Complete-Guidelines/)
- [x]  [**Complete Requirement Analysis Guidelines**](https://rafayethossain.github.io/2019-04-04-Requirement-Analysis-Guidelines/)
- [x]  [**Complete Requirement Specification Techniques**](https://rafayethossain.github.io/2019-05-01-Requirement-Specification-Techniques/)
- [x]  [**Requirements Approval Process You Should Follow**](https://rafayethossain.github.io/2019-06-06-Requirement-Approval-Process/)
- [x]  [**Change Control Process in SDLC**](https://rafayethossain.github.io/2019-07-07-Change-Control-Process-in-SDLC/)


{: .box-success}
Enjoy !!!
**See Yaaa, Next.**

![Diary](/assets/img/diary.png "Diary")
