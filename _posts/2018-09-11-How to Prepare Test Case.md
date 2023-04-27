---
layout: post
title: How to Write Test Case for Software 
subtitle: A Comprehensive Guide for Writing Effective Test Case for Your Software Project
tags: [sqa, software testing]
image: /assets/img/diary.png
thumbnail-img: /assets/img/diary.png
bigimg: /assets/img/cover.jpg
share-img: /assets/img/diary.png
cover-img: /assets/img/cover.jpg
---

When testing software systems, think of it like visiting a Disneyland Park. Just like how you can miss out on great locations if you don't have a park map, you can miss critical elements in your project without a comprehensive testing plan. That's where test cases come in - they help you keep track of what you need to test, what you've already tested, and what you don't need to test.

As software complexity and the need for quality assurance increases, the importance of effective test cases grows. Test cases are a crucial part of any software testing process, and their quality can make or break the success of your project. In this guide, we will explore best practices for writing effective test cases, including essential elements, design techniques, and common pitfalls to avoid.


_Quick Link to Specific Topic:_

- [What is a Test Case](#what-is-a-test-case)
  - [Elements of a well-written test case](#elements-of-a-well-written-test-case)
    - [Test case ID:](#test-case-id)
    - [Test case name:](#test-case-name)
    - [Test case objective:](#test-case-objective)
    - [Preconditions:](#preconditions)
    - [Test steps:](#test-steps)
    - [Expected results:](#expected-results)
    - [Actual results:](#actual-results)
    - [Pass/fail criteria:](#passfail-criteria)
- [How to write test case for software:](#how-to-write-test-case-for-software)
  - [Use a clear title](#use-a-clear-title)
  - [Include a strong description](#include-a-strong-description)
  - [Include estimates and prerequisites](#include-estimates-and-prerequisites)
  - [Keep test steps clear and concise](#keep-test-steps-clear-and-concise)
  - [Make it reusable](#make-it-reusable)
  - [Different techniques for designing test cases](#different-techniques-for-designing-test-cases)
    - [Boundary value analysis:](#boundary-value-analysis)
    - [Equivalence partitioning:](#equivalence-partitioning)
    - [Decision table testing:](#decision-table-testing)
    - [State transition testing:](#state-transition-testing)
    - [Use case testing:](#use-case-testing)
  - [Importance of maintaining and updating test cases regularly](#importance-of-maintaining-and-updating-test-cases-regularly)
    - [Keeping test cases up to date with changes in the software:](#keeping-test-cases-up-to-date-with-changes-in-the-software)
    - [Removing redundant test cases:](#removing-redundant-test-cases)
    - [Adding new test cases:](#adding-new-test-cases)
    - [Re-executing test cases:](#re-executing-test-cases)
  - [Examples of how to write test cases for different types of software](#examples-of-how-to-write-test-cases-for-different-types-of-software)
    - [Web applications:](#web-applications)
    - [Mobile Application:](#mobile-application)
    - [Desktop software:](#desktop-software)
- [Do's for Writing Test Case](#dos-for-writing-test-case)
- [Dont's for Writing Test Case](#donts-for-writing-test-case)
- [A Complete Checklist to Check Web Application:](#a-complete-checklist-to-check-web-application)
- [Checklist During Test Execution Phase:](#checklist-during-test-execution-phase)
- [About Content Creator:](#about-content-creator)
- [All Posts on Software Testing:](#all-posts-on-software-testing)

# What is a Test Case
A Test Case is a document that outlines a specific set of actions or events designed to test a software product against a particular requirement. The primary purpose of a test case is to ensure that the product meets certain quality standards and is ready to be released.

Test cases provide testers with a set of conditions under which they can validate the accuracy of a specific feature or function of a system. By executing test cases, testers can identify and report any defects or issues in the software product, which can then be addressed by the development team.

Effective test cases are an essential component of any software testing process. They help ensure that the product functions as intended, is reliable, and meets the needs of its users. 


## Elements of a well-written test case

A well-written test case should be clear, concise, and easily understandable. It should contain the following elements:

### Test case ID: 
A unique identifier that allows easy reference to the test case.

### Test case name: 
A descriptive title that provides an overview of the test case.

### Test case objective: 
A statement that describes the purpose of the test case and what it aims to achieve.

### Preconditions: 
A list of conditions that must be met before the test case can be executed. This includes any hardware, software, or environmental requirements.

### Test steps: 
A detailed list of steps that need to be followed to execute the test case.

### Expected results: 
A clear and concise description of what should happen when the test case is executed successfully.

### Actual results: 
A record of the outcome of the test case when it is executed.

### Pass/fail criteria: 
A set of criteria that determines whether the test case has passed or failed.


# How to write test case for software:
 
Let's learn how to write test cases for your software project. 

## Use a clear title

A good test case begins with a clear and compelling title. It is best practice to name the test case after the module that is being tested. If you examine the login page, for example, include "login page" in the title of the test case.

## Include a strong description

Read the description so the examiner knows what they are testing. Other pertinent information, such as the test environment, test data, and prerequisites/assumptions, may be included in this area at times. Test descriptions should be simple to read and understand the test's high-level goals and objectives right away.

## Include estimates and prerequisites

Any applicable assumptions and conditions must be met before the test may be executed. Depending on the test environment and the necessity for a special configuration before running the test, this information may include the page the user should start the test on.

## Keep test steps clear and concise

It is essential to consider the target audience when writing a test case. Remember that, the person who authored the test case may not be the one who runs or executes the test. Therefore, it is crucial to ensure that the test steps are clear and concise and include all relevant data and instructions necessary to carry out the test.

To achieve this, it's best to use a step-by-step approach to writing test cases. Start by identifying the test objective and then write the test steps in a logical sequence. Make sure to use simple language and avoid technical jargon as much as possible. Write the test case so that anyone can follow it and test it.
- Include anticipated outcomes.
- Expected Results In contrast to their test processes, tell the examiner what outcomes should be produced.
 
The examiner uses this to evaluate whether the test case "passed" or "failed."

## Make it reusable


A good test case provides long-term value to the software testing team by being reusable. To save time, it is best to reuse test cases rather than redo them. 

As a beginner, the best approach to writing test cases is to thoroughly read the software requirements document multiple times to ensure a clear understanding of the needs before starting to write the test case. 

To begin, determine the scenario based on the information provided in the required documents. A test case template is available for practical convenience in preparing test cases.


## Different techniques for designing test cases

There are several techniques for designing test cases. Some of the most popular techniques include:

### Boundary value analysis: 
This involves testing values at the boundaries of the input domain, as they are most likely to cause errors.

### Equivalence partitioning: 
This involves dividing the input domain into equivalence classes and testing a representative value from each class.

### Decision table testing: 
This involves creating a table of inputs and outputs and testing each combination.

### State transition testing: 
This involves testing the software's response to changes in state or context.

### Use case testing: 
This involves testing the software's ability to meet the requirements of a specific use case.

## Importance of maintaining and updating test cases regularly

Maintaining and updating test cases regularly is essential to ensure that they remain relevant and effective. This includes:

### Keeping test cases up to date with changes in the software: 
As the software evolves, test cases need to be updated to ensure that they continue to test the software's functionality accurately.

### Removing redundant test cases: 
Over time, some test cases may become redundant, and they need to be removed to keep the test suite lean and efficient.

### Adding new test cases: 
New functionality or features may be added to the software, and new test cases need to be added to test these changes.

### Re-executing test cases: 
Regularly executing test cases ensures that the software remains stable and meets the desired functionality and quality requirements.


## Examples of how to write test cases for different types of software

Writing test cases for different types of software requires different approaches. Here are some examples of how to write test cases for different types of software:

### Web applications: 
Test cases for web applications should test the functionality and usability of the application on different browsers and operating systems. This includes testing the responsiveness of the web application, the accuracy of the data displayed, the performance of the application under different loads, and the security of the application against common attacks like SQL injection and cross-site scripting.

For example, a test case for a login functionality of a web application could be:

Test case ID: W1

Test case name: Login Functionality Test

Test case objective: To verify that the login functionality of the web application works as expected.

Preconditions: The web application is running on a supported browser and operating system.

Test steps:

Navigate to the login page.

Enter valid credentials.

Click on the login button.

Expected results: The user should be logged in successfully and redirected to the dashboard page.

Actual results: The user is logged in successfully and redirected to the dashboard page.

Pass/fail criteria: The test case passes if the user is logged in successfully and redirected to the dashboard page. Otherwise, the test case fails.

### Mobile Application:
Test cases for mobile apps should test the functionality and usability of the app on different devices, operating systems, and network conditions. This includes testing the performance of the app under different loads, the accuracy of the data displayed, and the user experience of the app.
For example, a test case for a weather app could be:

Test case ID: M1

Test case name: Weather Information Test

Test case objective: To verify that the weather information displayed in the app is accurate.

Preconditions: The mobile app is installed and running on a supported device and operating system.

Test steps:

Open the weather app.

Enter the name of a city in the search bar.

Click on the search button.

Expected results: The weather information for the city entered is displayed accurately.

Actual results: The weather information for the city entered is displayed accurately.

Pass/fail criteria: The test case passes if the weather information for the city entered is displayed accurately. Otherwise, the test case fails.

### Desktop software: 

Test cases for desktop software should test the functionality and usability of the software on different operating systems and hardware configurations. This includes testing the performance of the software under different loads, the accuracy of the data displayed, and the user experience of the software.
For example, a test case for a video editing software could be:

Test case ID: D1

Test case name: Video Editing Test

Test case objective: To verify that the video editing functionality of the software works as expected.

Preconditions: The desktop software is installed and running on a supported operating system.

Test steps:

Open the video editing software.

Import a video file.

Edit the video file by adding effects and transitions.

Export the edited video file.

Expected results: The edited video file is exported successfully and plays back correctly.

Actual results: The edited video file is exported successfully and plays back correctly.

Pass/fail criteria: The test case passes if the edited video file is exported successfully and plays back correctly. Otherwise, the test case fails.



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


 

In conclusion, writing effective test cases for software is a critical aspect of software development. It ensures that the software meets the desired functionality and quality requirements and is free of defects. By following the best practices for preparing test cases, including the elements of a well-written test case, different techniques for designing them, and the importance of maintaining and updating them regularly, software development teams can ensure that their software is of high quality and meets the needs of their users. Additionally, by avoiding common mistakes and using the examples provided for different types of software, teams can create effective and efficient test cases that contribute to the overall success of the software development project.





**[⬆ back to top](#what-is-a-test-case)**

---

---

Enjoyed this post!

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/rafayetanalyst/) [!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/rafayetanalyst/)

Your support helps me create more valuable content. Thank you!

---

---

# About Content Creator:

Hi, This is **Rafayet Hossain**

A Seasoned Business Systems Analyst, Project Manager, and SQA Engineer with experience in driving digital changes within organizations. I specialize in understanding business needs and developing software solutions to improve processes and drive growth. I am skilled in managing projects, analyzing data, and ensuring quality in the final product. I am passionate about using my expertise to help organizations reach their goals and succeed. Let's work together to improve your business and drive success. Contact me for any inquiries or projects.

👉 Contact Information :

[![Linkedin](https://img.shields.io/badge/-LinkedIn-blue?style=flat&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/rafayethossain/)
[![Gmail](https://img.shields.io/badge/-Gmail-c14438?style=flat&logo=Gmail&logoColor=white)](mailto:rafayet13@gmail.com)

---

---

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