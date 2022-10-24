---
layout: post
title: What is Software Requirements
subtitle: Everything You Need to Kow About Software Requirements
tags:
  [business system analysis, system analysis, business analysis, requirement]
image: /assets/img/diary.png
bigimg: /assets/img/back.gif
thumbnail-img: /assets/img/diary.png
share-img: /assets/img/diary.png
cover-img: /assets/img/cover.jpg
---

A requirement is a detailed description of the service that software must provide. A requirement can range in complexity from a high-level abstract declaration of the user's need to comprehensive mathematical functional requirement specifications.

A software requirement is a functional or non-functional need that must be implemented in a system. The term functional refers to the provision of a certain service to the user.

In the context of a banking application, for example, when a customer clicks "View Balance," they must be able to view their most recent account balance.



A non-functional software requirement might also be a performance requirement. A non-functional requirement can be that every page of the system be viewable to consumers within 5 seconds.

_Quick Links to Topic:_

- [Overview of Software Requirement](#overview-of-software-requirement)
	- [What is Software Requirement?](#what-is-software-requirement)
	- [Category of Software Requirements](#category-of-software-requirements)
	- [Functional Requirements:](#functional-requirements)
		- [Functional Requirements Example:](#functional-requirements-example)
	- [Non-Functional Requirements:](#non-functional-requirements)
		- [Non-Functional Requirements Example:](#non-functional-requirements-example)
	- [Product Constraints:](#product-constraints)
		- [Product Constraint Example:](#product-constraint-example)
	- [What Makes a Good Requirements?](#what-makes-a-good-requirements)
	- [SMART Requirement](#smart-requirement)
		- [What is a SMART Requirement?](#what-is-a-smart-requirement)
- [Guidelines for Creating Valid Requirements](#guidelines-for-creating-valid-requirements)
	- [Checklist for Producing Valid Requirement:](#checklist-for-producing-valid-requirement)
- [Terms to Avoid while writing requirements :](#terms-to-avoid-while-writing-requirements-)
	- [Phase of the Requirements Process:](#phase-of-the-requirements-process)
- [Business Rules](#business-rules)
	- [Business Rules Explained](#business-rules-explained)
	- [Business Rules Vs Business Requirement](#business-rules-vs-business-requirement)
	- [Business Rules Best Practices:](#business-rules-best-practices)
- [About Content Creator:](#about-content-creator)
- [All Posts on Business Analysis:](#all-posts-on-business-analysis)

# Overview of Software Requirement

Why Do We Need Requirements?
- Guides the design of the eventual solution.
- Without correct requirements, you cannot design or build the correct product.

**About 60% of project failures originate with the requirements.**

## What is Software Requirement?

Something a product must do or a quality it must have. Software requirement is a functional or non-functional need to be implemented in the system.

## Category of Software Requirements 

Requirements are categorized as follows:
    1. Function Requirements:
    	a. Things the product must do.
    	b. Action the product must take.
    2. Non-Functional Requirements:
    	a. Properties or qualities the product must have.
    	b. How the product will behave.
    3. Constraints
    	a. Global Requirement:
    		i. Purpose of the project
    		ii. Users of a product

## Functional Requirements:

- **Scope of the Product** – defines the boundaries and connections to other products
- **Functional and Data Requirements** – Things the product must do and data manipulated by the functions

### Functional Requirements Example:
- The product must track recipes down the ingredient and quantity level
- The recipes must be editable by an administrator
- The product must display the orders that need to be completed
- The product must display the recipes to make the orders
- The product must track ingredients including their cost, vendors, and quantity in inventory
- The product must interact with the current Point of Sale system

## Non-Functional Requirements:

    • Look and Feel Requirements – intended appearance
    • Usability Requirements – based on the intended users
    • Performance Requirements – how fast, big, accurate, safe, reliable, etc.
    • Operational Requirements – product’s intended operating environment
    • Maintainability and Portability Requirements – how changeable product must be
    • Security Requirements – security, confidentiality, and integrity of the product
    • Cultural and Political Requirements – human factors
    • Legal Requirements – conformance to applicable laws

### Non-Functional Requirements Example:

- The product shall use the company colors and logos
- The product shall be intuitive, even to first time users
- The product shall only allow bakers and administrators to view recipes
- The product shall be easily upgraded for future business needs
- The product shall be scalable to multiple bakery locations

## Product Constraints:

    • Purpose of the Product – reason for building the product
    • Client, Customer, and Stakeholders – people that interact with the product'
    • Users of the Product – intended end-users and how they affect product usability
    • Requirements Constraints – limitations of the project and restrictions on design
    • Naming Conventions and Definitions – vocabulary of the product
    • Relevant Facts – outside influences that make a difference to this product
    • Assumptions – assumptions developers are making

### Product Constraint Example:

- The product budget must not exceed $50,000
- The product shall run on the company’s existing machines
- Implementation of the product cannot interrupt daily business
- The last 5 years of historical data needs to be made available in the product

## What Makes a Good Requirements?

We may create a long list of words such as:

	✅ Accountable ✅ Understandable, ✅ Attainable, ✅ Modifiable,
	✅ Testable, ✅ Traceable, ✅ Measurable, ✅ Feasible,
	✅ Allocable, ✅ Concise, ✅ Consistent, ✅ Complete, 
	✅ Correct, ✅ Feasible, ✅ Design Independent, 
	✅ Necessary, ✅ Organized, ✅ Unambiguous, 
	✅ Prioritized, and so on.

But we will use SMART formula like setting goal.

## SMART Requirement

**SMART** = Specific, Measurable, Attainable, Reasonable, Traceable

### What is a SMART Requirement?

    1. Specific:
    Overall:
    	○ Clear, no ambiguity
    	○ Consistent, same terminology throughout
    	○ Simple

    Question to Ask:
    	○ What?
    	○ Why?
    	○ Who ?
    	○ Where?

    Guidelines:
    	○ Avoid "Some", "Several", "Many"
    	○ State pronouns clearly "A calls B it is updated".
    	○ Specify units all with numbers
    	○ Use pictures to clarify understanding
    	○ Provide explanations for terms like "Transmitted", "Sent", "Downloaded", and "Processed"

    2. Measurable:
    	Overall:
    		○ Measure progress towards goal
    		○ Indicators should be quantifiable

    	Question to Ask:
    		○ How much?
    		○ How many?
    		○ How will I know when it is accomplished?

    	Guidelines:
    		○ Ensure measurable during requirement elicitation
    		○ Validate unequivocal success can be proven with that requirement
    		○ Determine tests that will need to be used to verify the requirement was met.
    3. Attainable :
    	Overall:
    		○ Validate requirement is feasible
    			□ Within technical expertise
    			□ Within scope of project
    			□ Within budget
    		○ Sanity check of the project

    	Question to Ask:
    		○ Is there a theoretical solution to the problem?
    		○ Has it been before?
    		○ Are there any known constraint (environment, political, etc.)?

    	Guidelines:
    		○ Determine who has responsibility for satisfying the requirement and validate they can deliver
    		○ Ensure sufficient time, resources, and budget
    		○ Reuse pieces from previous projects.
    4. Reasonable:
    	Overall:
    		○ Validate the effort is worth the requirement

    	Question to Ask:
    		○ Is this worthwhile?
    		○ Is the timing right?
    		○ Does this match our other effort/ needs

    	Guidelines:
    		○ Run all requirements through a "sanity check'
    		○ Ensure the requirement makes sense in context
    5. Traceable:
    	Overall:
    		○ Trace requirement through design, implementation, and testing

    	Question to Ask:
    		○ Can I ensure this requirement has been met in the design solution?
    		○ Can I ensure this requirement has been met in the implementation?
    		○ Can I ensure this requirement has been met in during testing?

    	Guidelines:
    		○ Requirement should include:
    			□ Originators
    			□ Assumptions
    			□  Business justifications
    			□ Dependencies on other requirements
    			□ Importance

# Guidelines for Creating Valid Requirements

## Checklist for Producing Valid Requirement:
- [x] Should use the word shall
- [x] Only one shall per requirement
- [x] Written in short, simple sentences
- [x] Consistent terminology
- [x] Stated positively
- [x] Accompanied by notes and comments to support and clarify
- [x] Stated imperatively
- [x] Don’t use will and should
  Tips for Producing Valid Requirement:
- [x] Or – Select one of the options
- [x] Can, should – Expresses desire or suggestion instead of requirement
- [x] Must – 100% reliability
- [x] Are, is, will – Descriptive part to lead into the requirement
- [x] Support, and/or – Confusing
- [x] But not limited to, etc. – Incomplete requirement/thought
- [x] Shall – dictates specification and functional capability

# Terms to Avoid while writing requirements :
	❌ Adequate ❌ Approximately ❌ Better than ❌ Comparison
	❌ Easy ❌ Maintainable ❌ Maximize ❌ Minimize 
	❌ Normally ❌ Optimize ❌ Quality product ❌ Quick 
	❌ Rapid ❌ Substantial ❌ Sufficient ❌ Timely

## Phase of the Requirements Process:
1. Requirement Elicitation
2. Requirement Analysis
3. Requirement Specification
4. Requirements Approval


#  Business Rules
- What are Business Rules?
- Business Rules vs Business Requirements
- Best Practices

## Business Rules Explained

**Definition:** A business rule is a rule that specifies or constrains a business component and always resolves to true or false.

Rules imply that the system must or must not perform something. There are just two options: black or white. Either "yes" or "no". Not both.

**Example:**
- You must be home by curfew.
- Entered email addresses must appear valid (contain @ and .)
- Each class must have at least one instructor
- Customers must have a valid driver’s license to rent a vehicle
- A quote must be completed prior to an invoice being generated

Then business requirement will help you to fulfill that rule. Like _Wearing a watch that alarm before 30 minutes of curfew._

**Purpose:** Business rules are intended to assert business structure or to control or influence the behavior of the business.

## Business Rules Vs Business Requirement

**Rule:** Entered email addresses must appear valid (contain @, then later .)

**Possible Requirements:**
- Capability to enter email address
- Alert agent when the email doesn’t appear to be valid
- Allow for correction of email if invalid email format is entered

**Rule:** Each course must have at least one instructor

**Possible Requirements:**
- Capability for Dean to assign instructor to course
- Course registration cannot be opened until an instructor is assigned

**Rule:** Customers must have a valid driver’s license to rent a vehicle

**Possible Requirements:**
- Employee to inspect driver’s license
- Ability for employee to validate driver’s license

**Rule:** A quote must be completed prior to an invoice being generated

**Possible Requirements:**
- Capability to enter a quote
- Details from quote must automatically flow to the invoice
- Ability to tie the quote and invoices together for reporting

## Business Rules Best Practices:
- [x] When documenting business rules, keep it simple.
- [x] Business requirements are used to comply with business rules. Keep them both in same document
- [x] Each business rule may need multiple requirements
- [x] Business rules should not be changed
- [x] Changes can cause major constraints down the road


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
