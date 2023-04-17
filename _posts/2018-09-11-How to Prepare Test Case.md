---
layout: post
title: How to Write Test Cases for Software
subtitle: Best Practices for Preparation of Test Case
tags: [sqa, software testing]
image: /assets/img/diary.png
thumbnail-img: /assets/img/diary.png
bigimg: /assets/img/cover.jpg
share-img: /assets/img/diary.png
cover-img: /assets/img/cover.jpg
---

Consider any of your software systems in testing to be a Disneyland Park that you might wish to visit. Of course, you may just buy tickets and visit the park whenever you want. While this is enjoyable, there is a strong risk you will miss out on great locations.

In this instance, all you can do is gather a park map. The same is true for your project; you need maps to know what to test, what you already tested, and what you don't need to test. And thus the concept of creating a test case is born. One of the most significant aspects of software testing is test cases. It is utilized by the quality assurance team, development, and middle management executives.

_Qucik Link to Specific Topic:_

- [What is a Test Case](#what-is-a-test-case)
- [How to write test case for software:](#how-to-write-test-case-for-software)
  - [Use a clear title](#use-a-clear-title)
  - [Include a strong description](#include-a-strong-description)
  - [Include estimates and prerequisites](#include-estimates-and-prerequisites)
  - [Keep test steps clear and concise](#keep-test-steps-clear-and-concise)
  - [Make it reusable](#make-it-reusable)
- [Do's for Writing Test Case](#dos-for-writing-test-case)
- [Dont's for Writing Test Case](#donts-for-writing-test-case)
- [A Complete Checklist to Check Web Application:](#a-complete-checklist-to-check-web-application)
- [Checklist During Test Execution Phase:](#checklist-during-test-execution-phase)
- [About Content Creator:](#about-content-creator)
- [All Posts on Software Testing:](#all-posts-on-software-testing)

# What is a Test Case
A **Test Case** is a document artifact consisting of certain actions or sequences of events for testing the software product against a specific requirements. 

When it comes to quality, the test case is the condition that ensures the tested product is functional up to a specific degree and ready to go live.
From the perspective of a tester, test cases give the settings under which a tester conducts the task of confirming the authenticity of a specific function or feature of a system.

# How to write test case for software:

## Use a clear title

A good test case begins with a clear and compelling title. It is best practice to name the test case after the module that is being tested. If you examine the login page, for example, include "login page" in the title of the test case.

## Include a strong description

Read the description so the examiner knows what they are testing. Other pertinent information, such as the test environment, test data, and prerequisites/assumptions, may be included in this area at times. Test descriptions should be simple to read and understand the test's high-level goals and objectives right away.

## Include estimates and prerequisites

Any applicable assumptions and conditions must be met before the test may be executed. Depending on the test environment and the necessity for a special configuration before running the test, this information may include the page the user should start the test on.

## Keep test steps clear and concise

Remember that the person who authored the test case may not be the one who runs the test. The test steps should include the relevant data as well as instructions on how to carry out the test. This is most likely the most crucial aspect of every test case. Write the test case so that anyone can follow it and test it.
- Include anticipated outcomes.
- Expected Results In contrast to their test processes, tell the examiner what outcomes should be produced.
 
The examiner uses this to evaluate whether the test case "passed" or "failed."

## Make it reusable

A good test case gives the software testing team with reusable and long-term value. Remember this while creating a test case. Instead of redoing the test case, you can save a lot of time by reusing it.


The ideal technique for novices when writing test cases is to read the software requirements document several times until the needs are clear, and then begin writing by determining the circumstance based on the information supplied in the needed documents. A test case template is given for practical convenience in test case preparation.


{: .box-success}
# Do's for Writing Test Case

- [x] It should be simple, precise, and concise.
- [x] User perspective must be taken into consideration.
- [x] Use of the tracebility matrix
- [x] Assign an ID to each of the test cases 
- [x] Try to write independent, reusable, and repeatable test cases. 
     


{: .box-warning}
# Dont's for Writing Test Case

- [x] Do not write unnecessary or redundant test execution steps.
- [x] Do not consider or assume any sort of requirement on your own without consulting the SRS or BRS.
- [x] Do not write reptitive test cases. 
- [x] Do not forget to get the test cases reviewed by the development team.
     

# A Complete Checklist to Check Web Application:

- [x] Is the proper template being used?
- [x] Have the following information been accurately entered? Reference to a requirement, Description of the test script, Name of the author, Created date, Procedure for Installation, Where appropriate, prerequisites
- [x] Have the Test conditions (scenarios) and, if appropriate, the Risk factor been identified?
- [x] Have all explicit and implicit scenarios provided in the requirement been translated into Test conditions?
- [x] Have the linked areas that may be affected by the requirement's implementation been identified and included in the test cases? (Determine the impact areas and cross-check them with the test scenarios.)
- [x] Is equivalence partitioning used? Have all of the domain's classes been accurately identified?
- [x] Is the test data set, if required, properly generated?
- [x] Have you recognized and included the boundary values, special values, and incorrect values in the Test data set?
- [x] Has the Test data been embedded into the test cases?
- [x] Have the required negative scenarios been identified in the test conditions?
- [x] Have the steps been correctly given in appropriate sequence for each test scenario? Steps/Actions should state very clearly the sequence of actions to be carried out on the system by the user. All statements should be definite. Ensure that terms like “If”, “In case” etc are not used.
- [x] "Have the Expected Results been identified correctly? Expected Results should clearly state how the system should respond to the user actions given in each step/action.
- [x] Ensure that too many things are not included to be verified under one expected output.
- [x] Ensure that separate cases are written for multiple verifications of the application’s behavior.
- [x] Vague statements like “Appropriate message/value/screen” etc, should not be part of expected result. Every detail should be clearly spelt out."
- [x] Are all the statements free from grammatical errors?

# Checklist During Test Execution Phase:

- [x] Have the Actual Results been updated for each of the steps? Has the actual result been documented for a failed step and for its subsequent re-runs?
- [x] Have all the steps been executed successfully? Every failed step should have retest details or some disposition if it is not fixed.
- [x] Have the defect details like Defect id, description etc. been given for a failed step?
- [x] Has the reason for the failure been recorded? (For example, invalid input data, new functionality not tested before, existing problem)
- [x] Did a peer recreate the defect before logging it in the Defects database? Have these details been documented?
- [x] Has the defect been retested and if so, have the retest details and the result documented along with the date on which the retest was done?
- [x] Have the Execution details like executed by and executed date, been filled up correctly
- [x] Have the results from different environments (Browsers, for example) been recorded? (If applicable)
- [x] Have the metrics related to the test cases been updated in all applicable metrics documents? (Number of Test cases prepared, executed, Number of test case executions with defects, Total Number of defects etc.)
- [x] Are all the statements free from grammatical errors?





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



# All Posts on Software Testing:  

Click on any of the desired links to directly access the information.

- [x]  [**Introduction to Software Testing**](https://rafayethossain.github.io/2018-08-05-Introduction-to-Software-Testing/)
- [x]  [**Software Testing Glossary**](https://rafayethossain.github.io/2018-08-12-Software-Testing-Terms-of-Glossary/)
- [x]  [**Software Testing Types**](https://rafayethossain.github.io/2018-08-22-Software-Testing-Types/)
- [x]  [**Activities in Software Testing**](https://rafayethossain.github.io/2018-09-01-Test-Activities-You-Must-Know/)
- [x]  [**How to Prepare Test Case**](https://rafayethossain.github.io/2018-09-11-How-Prepare-Test-Case/)
- [x]  [**Introduction to Software Testing**](https://rafayethossain.github.io/2018-08-05-Introduction-to-Software-Testing/)
- [x]  [**How to Write a Bug Report**](https://rafayethossain.github.io/2018-09-20-How-to-Write-a-Bug-Report/)
- [x]  [**Bug Life Cycle**](https://rafayethossain.github.io/2018-09-23-Life-Cycle-of-a-Bug/)
- [x]  [**Front End Testing Basic**](https://rafayethossain.github.io/2018-09-30-Basic-GUI-Testing/)
- [x]  [**Mobile Application Testing Basic**](https://rafayethossain.github.io/2018-10-05-Mobile-App-Testing-Basic/)
- [x]  [**Software Testing Toolkit**](https://rafayethossain.github.io/2018-10-10-Software-Testing-Toolkit/)
- [x]  [**Introduction to Software Testing**](https://rafayethossain.github.io/2018-08-05-Introduction-to-Software-Testing/)
- [x]  [**How to Install Python**](https://rafayethossain.github.io/2018-12-31-how-install-python-on-windows/)
- [x]  [**Begineer Tips to Learn Python by Yourself**](https://rafayethossain.github.io/2019-01-03-Beginner-Tips-for-Learning-Python/)
- [x]  [**Free Resource for Python Learning**](https://rafayethossain.github.io/2019-01-04-Python-Resource-Books-and-Recipe/)
- [x]  [**Python Basic Coding for Newbie**](https://rafayethossain.github.io/2019-01-05-Basic-Python-Coding/)
- [x]  [**Python 30 Secondes Recipe**](https://rafayethossain.github.io/2019-01-07-Python-Easy-Trick-Collected/)
- [x]  [**How to Install Selenium with Python**](https://rafayethossain.github.io/2019-01-08-How-To-Install-Selenium-Python-Webdriver/)
- [x]  [**First Selenium Python Script**](https://rafayethossain.github.io/2019-01-09-My-First-Python-Selenium-Script/)


 

{: .box-success}
Enjoy !!!
**See Yaaa, Next.**

![Cover](/assets/img/cover.jpg "Cover")