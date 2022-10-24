---
layout: post
title: Requirements Specification Techniques
subtitle: Requirements Specification Techniques
tags:
  [
    business system analysis,
    system analysis,
    business analysis,
    requirement elicitation,
  ]
image: /assets/img/diary.png
bigimg: /assets/img/back.gif
thumbnail-img: /assets/img/diary.png
share-img: /assets/img/diary.png
cover-img: /assets/img/cover.jpg
---
The specification of requirements is an essential aspect of the Requirements Engineering process. It is the third step, following Requirements Capture and Analysis. The purpose is to generate a document, or Requirements Specification, with the appropriate amount of information.

_Qucik Link to Specific Topic:_

- [Activities of Requirement Specifications:](#activities-of-requirement-specifications)
- [Categorizing Requirements](#categorizing-requirements)
  - [Why Categorize Requirement?](#why-categorize-requirement)
  - [Category of Software Requirements:](#category-of-software-requirements)
- [Deriving Requirements](#deriving-requirements)
  - [Techniques for determining requirement include:](#techniques-for-determining-requirement-include)
    - [Parsing Requirements:](#parsing-requirements)
    - [Interpreting Requirements:](#interpreting-requirements)
    - [Focusing Requirements:](#focusing-requirements)
    - [Qualifying Requirements:](#qualifying-requirements)
- [Assigning Requirement Attributes](#assigning-requirement-attributes)
  - [Why Assign Requirement Attributes?](#why-assign-requirement-attributes)
  - [Typical Attributes:](#typical-attributes)
- [Prioritizing Requirement](#prioritizing-requirement)
  - [Why Prioritize Requirement:](#why-prioritize-requirement)
  - [Prioritize Factors:](#prioritize-factors)
  - [03  Step Prioritization Process:](#03--step-prioritization-process)
  - [Requirement Prioritization Best Practices:](#requirement-prioritization-best-practices)
- [Validate your requirement using **SMART** formula.](#validate-your-requirement-using-smart-formula)
- [Business Requirement Document (BRD) Basics:](#business-requirement-document-brd-basics)
  - [What is a Business Requirements Document?](#what-is-a-business-requirements-document)
  - [Who prepares BRD?](#who-prepares-brd)
  - [What is the use of BRD?](#what-is-the-use-of-brd)
  - [What is the standard format for BRD?](#what-is-the-standard-format-for-brd)
- [About Content Creator:](#about-content-creator)
- [All Posts on Business Analysis:](#all-posts-on-business-analysis)

# Activities of Requirement Specifications:
We learned about requirements elicitation in the previous section, where we worked through and extracted those needs from stakeholders and documents to understand what the as-is and to-be processes will look like.

We then went through requirement analysis, where we took those needs and articulated them in numerous ways so that parties, whether technical or business, could comprehend them, and we produced visual models to aid with that. This is the third step, requirement specification.

And essentially, what we're doing here is classifying and breaking down the criteria that we have. So, if one requirement is a little long or complex, what is pushing them to split it up into numerous needs so it's a little simpler to comprehend in plain and simple?


So we're categorizing, generating needs, and prioritizing those requirements. And it's critical that you prioritize requirements, that you assign a level of priority to them, because as the project progresses and you have a deadline for implementation, you don't want to be at the point where you're 90% through the project and realize you're not going to get every single requirement in and now trying to circle back to the business to figure out what, you know, based on what you haven't done, what you should do.


That is not the time to do it; you will go nowhere and face a lot of pushback. Prioritizing requirements is crucial at this point. 

Finally, as the final stage of this requirement formulation process, you acquire validation of those requirements. So you go back to the company and make certain that the requirements are supported by at least a few stakeholders. This is to guarantee that you're on the right track. This will be useful when you approach the final round of requirements approval.


# Categorizing Requirements

One of the first steps in the requirements definition process is to classify requirements, which essentially involves dividing the needs into functional, nonfunctional or supplementary, and constraint requirements. And this is beneficial in a variety of ways.

## Why Categorize Requirement?

  1. Aids in documentation
  2. Helps to prioritize
  3. Assist Estimating the system cost.
  4. Identifies areas that require further investigation.

## Category of Software Requirements:

    1. Functional Requirements:
    	a. Things the product must do.
    	b. Action product must take
    2. Non-Functional Requirements:
    	a. Properties or qualities the product must have
    	b. How the product will behave
    3. Constraints:
    	a. Global Requirements :
    		i. Purpose of the project
    		ii. Users of the project.

you've elicited and now you're going to go through in and categorize them all out.

# Deriving Requirements

Your captured requirement is a document that may require additional development through derivation. And deriving requirements is all about three things:

 1. Adding further details 
 2. Adding clarity to this requirement 
 3. Removing ambiguity.

## Techniques for determining requirement include:
    • Parsing Requirement
    • Interpreting Requirements
    • Focusing Requirements
    • Qualifying Requirements.

 ### Parsing Requirements:
- Breaking down requirements that are too broad.
- Removing "and" from requirements
  - Risk is high that only one of the conditions will be tested
  - Hard to trace the requirement bug/ failure

**Breaking Down Example:**
- Original Requirement:
    - “User-completed fields on tax forms shall be converted to electronic text documents.”

- Parsed Requirements:
  - “The system shall be able to convert handwriting to text.”
  - “The system shall be able to convert machine print to text.”
  - “The system shall be able to electronically correct user-completed fields.

### Interpreting Requirements:
- Reduce generalness and ambiguity of stated requirements .

**Interpreting Requirement Example:**

- Original Requirement:
  - “Each PC shall have state-of-the-art software installed.”

- Interpreted Requirement:
  - “Each PC shall have Microsoft Office 2013 and Windows 10 installed.”
- Parsed Requirements:
  - "Each PC shall have Microsoft Office 2013 installed.”
  - “Each PC shall have Windows 10 installed."

### Focusing Requirements:
- Combine overlapping requirements into one focused requirement.
  
** Focusing Requirements Example:** 

- Original Requirement:
  - “Each PC must have a standard spreadsheet tool installed that runs in Windows.”
- Focused Requirement:
  -  “Each PC on the LAN shall have Microsoft Office Excel 2013.”

### Qualifying Requirements:

- Add a requirement to provide a method of verification or compliance .
- 
** Qualifying Requirements Example:**
- Original Requirement:
  - “The xxx command must perform the following actions…”
- Qualified Requirement:
  - “Each command shall be executed during system testing to demonstrate its functionality.”

# Assigning Requirement Attributes
## Why Assign Requirement Attributes?
 1. **Clarification:** More details
 2. **Filtering:** Filter by type functional, non-functional, constraints, and priority. 
 3. **Validation:** Requirement met the business need.

## Typical Attributes:
-  **Unique Identifier:** A unique identifier means that that identifier is unique to that specific requirement. It never changes.
-  **Acceptance Criteria:** what is the criteria that's going to use to validate that that has been met?
-  **Author:** who's actually writing the requirements?
-  **Complexity:** how hard is this going to be to implement in scale of 1 to 10?
-  **Ownership:** a group, the department that's been affected by the requirement (Not the raiser).
-  **Performance:** If there is any performance attribute like how fast it should response.
-  **Urgency:** How quickly it is needed, in which iteration of agile approach?
-  **Business Value:** What business value it will add. 
-  **Status:** Started, Confirmed, Developed, Tested, etc.
-  **Type:** Functional, Non- Functional, Constraints.
-  **Priority:** High, Medium, Low
-  **Source:** Who raise this, in case any 
clarification is needed to whom to consult?

# Prioritizing Requirement

## Why Prioritize Requirement:
Generally there are too many functions and features to implement within the project schedule and budget.

## Prioritize Factors:
- Value to the business
- Value to the customer
- Minimize cost to develop
- Time to implement
- Ease of technical implementation
- Ease of business implementation
- Obligation to some external authority

## 03  Step Prioritization Process:
 1. Define usefulness to business (critical, important, nice to have) 
 2. Estimate cost (1-5 scale) 
 3. Determine timeframe (1-5 scale)

## Requirement Prioritization Best Practices:
 - ✅ Keep it simple
 - ✅ Business value reigns supreme
 - ✅ Remove prioritization away from politics
 - ✅ Prioritize (and re-prioritize) after each project iteration

# Validate your requirement using **SMART** formula.


# Business Requirement Document (BRD) Basics:

## What is a Business Requirements Document?

It's a document that houses all of the requirements, the business rules, the use cases, the version history, stakeholders, basically everything that you're eliciting as part of the requirements of the project are documented within here.

## Who prepares BRD?
Well it's pretty obvious. The business analyst is responsible for filling out the BRD and making sure that it's complete and accurate. And that's really what's utilized as you move into the next phases of the project to pass the requirements phase.

## What is the use of BRD?
Number one it houses all of the requirements for the specific project. That's the most critical use of the business requirements document is to house all of those requirements. Information of Stakeholder mapping, approvals, etc. will be kept here. Eventually the original system shall be design, implemented, and tested based on this document.

## What is the standard format for BRD?
No there is no standard but it is pretty obvious that every organization use a BRD format based on their needs. But most of the information are almost similar.

One question that comes up a lot is 'hey, when do I fill this out?', you'll see as we go through kind of an example template and format that it's a pretty formal document. You have your elicitation, then you have your analysis, then your specification, then your validation. So in the elicitation that's when you're meeting with everyone, that's when you're doing all your different elicitation activities and at that time I'm not documenting inside of a BRD, 

I'm trying to write good requirements, write SMART requirements because I don't want to rewrite them all later, is when I start to put a lot of the details into the BRD and also in the specification phases when I kind of finalize that.

If You Like This Post

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/rafayetanalyst/)






----------------------------------------------------------------------
----------------------------------------------------------------------

# About Content Creator: 


Hi, This is **Rafayet Hossain**

A seasoned Business System Analyst (BSA), Project Manager, and SQA Engineer.
He acts as a change agent to enable digital changes to your organization.

Provide Services on:

🎯 Software Project Managment 

🎯 Business System Analysis 

🎯 Software Testing 

🎯 Business Consulting

🎯 Technical Document Preparation 

🎯 Individual Training  


👉 For Any Query or Assigment Contact: 


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
