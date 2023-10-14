---
layout: post
title: Data Science and Unit Testing: A Dynamic Duo for Reliable Analytics
subtitle: Data Science Excellence Through Unit Testing Strategies
cover-img: /assets/img/thunder.jpg
thumbnail-img: /assets/img/thunder.jpg
share-img: /assets/img/path.jpg
tags: [books, test]
---

Imagine the following scenario, Sam works as a data scientist. He collaborate with a team of peer data scientists. He is working on an analytical solution for a data science use case. He enthusiastically presents the solution he worked on to the client. The client likes Sam’s solution, but suggests a few improvements to his initial solution. Lisa, a peer data scientist who works in the same team as Sam, volunteers to make the number of modifications during the week he is away from work. After a break, Sam comes back to work, and is delighted to find Lisa has carried out the changes. However, he becomes increasingly doubtful whether the changes have broken the rest of the code. To quell his concerns, Sam devotes hours to testing each element of the downstream code, ensuring that the modifications did not undesirably impact the other parts the project. 

This is a very scary situation for any developer. Such situations will discourage collaboration and makes it very difficult to make changes in the code especially in fast-paced agile development. Sam wonders if he could position a gatekeeper so that he can keep faith in the code changes his fellow developers make. 

 Enter Unit Testing, which provides assurance to developers that their code performs as expected. The concept has its origins in software engineering where it is used to test if individual components function as expected. They check if a part of the code is fit to use. There are broadly two types of tests that can be used in data science and machine learning.
 
1.	Integration tests: These tests check if one part of the code works in cohesion with another part of the code. For example, testing if the model results are acceptable on a training set as well as on a testing set. Note that these tests are run as a part of the development process. 
2.	Unit tests: In unit tests, we check if individual components of the code work as expected. This involves testing certain parts of the code works as expected functionally. For example ensuring a resultant dataset contains figures within a specified boundary. These tests are often automated and will live in the production environment unlike integration tests. This is the subject of this article.

### The many uses of unit tests   
   
The unit tests are an integral part of the development of a data science project. With the right unit tests in place you will have confidence in the code that it is always operating within the boundaries that you have set. As a result, it fosters collaboration. In the above example, if Sam had the correct unit tests in place, he will always be willing to allow his colleagues to make the required changes to the code. He would not have to check every output as proper unit tests would have alerted any violations of the set boundaries. Not only it fosters collaboration, but it also helps data scientists and machine learling engineers in many ways. 

* The unit tests can be intelligently placed to detect edge cases. The required tests can be placed to alert when an abnormal behaviour surfaces. For example, regression involves adding multiple variables which could lead to unintended results. You can avoid grossly underfitting or overfitting models using these gatekeepers.
* Unit tests can work as living documentation of your code. For example, it will be difficult for a newly joined developer to understand how a data science usecase works without documentation. In fact, in some instances, even properly written documentation or code comments may not accurately say how a function is supposed to work. However, a well-written set of unit tests will allow a developer to understand easily how the code is intended to work and what are the boundaries within which the usecase is intended to operate.  
* They encourage the development of modular code. Placing unit tests requires developers to write functions in a testable manner. If there are large, unmanageable code, the developers are required to have smaller, more manageable code so that they can be tested. Therefore, unit tests promote the overall code health of the usecase. 

### Anatomy of a unit test

Unit test follows a very intuitive, easy to use format. You can conveniently use Pytest library in Python to write unit tests. There are many functionalities to Pytest which includes a detailed diagnosis of which tests passed and failed. However, we will look at how to first create a unit test.
•	Part1: Define the input and output datasets. We will type-out these two datasets with the scenarios we want to test. In this example, we are testing two scenarios of squarroot conversion.
•	Part 2: call the function on the input dataset.
•	Part 3: we have 2 datasets to test. The resultant dataset of the function and the expected dataset. We use the assert_data_frame_equal function within Pandas to test if the two datasets match.  
How to get the best out of your unit tests
These gatekeepers of your project should be intelligently placed to test strategic parts in your code. When writing a unit test, it is important that you test general situation and more rare occurrences. This will provide you the assurance that the code works in all scenarios. 


