---
layout: post
title: First Scipt With Selenium Python Webdriver
subtitle: Software Test Automation with Selenium & Python
tags: [python tutorial, selenium, python, webdriver, python selenium webdriver]
image: /assets/img/selenium-with-python.png
bigimg: /assets/img/back.gif
thumbnail-img: /assets/img/selenium-with-python.png
share-img: /assets/img/selenium-with-python.png
cover-img: /assets/img/cover.jpg
---


In this post, we will perform our first Selenium web testing using the Selenium Python web bindings.
If you already have the Selenium Python bindings installed, you can begin Web Automation Testing with your Python IDE.

**If Python and Selenium webdriver is not install, please follow the previous post.** 

```py 

from selenium import webdriver
from selenium.webdriver.common.keys import Keys

driver = webdriver.Firefox()
driver.get("http://www.python.org")
assert "Python" in driver.title
elem = driver.find_element_by_name("q")
elem.clear()
elem.send_keys("pycon")
elem.send_keys(Keys.RETURN)
assert "No results found." not in driver.page_source
driver.close()

```

* This code snippet is collected from official Selenium Python Document 

The above script can be saved into a file (eg:- python_org_search.py), then it can be run like this:

```
python python_org_search.py

```

## Example Explained
The selenium.webdriver module provides all the WebDriver implementations.
Currently supported WebDriver implementations are Firefox, Chrome, IE and Remote. 
The Keys class provide keys in the keyboard like RETURN, F1, ALT etc.

```py

from selenium import webdriver
from selenium.webdriver.common.keys import Keys

```
## Next, the instance of Firefox WebDriver is created.

```py
driver = webdriver.Firefox()

```
*You can change the browser from webdriver as you need*

The driver.get method will navigate to a page given by the URL.
WebDriver will wait until the page has fully loaded (that is, the “onload” event has fired) before returning control to your test or script.
It’s worth noting that if your page uses a lot of AJAX on load then WebDriver may not know when it has completely loaded.:

```py
driver.get("http://www.python.org")

```

## The next line is an assertion to confirm that title has “Python” word in it:

```py
assert "Python" in driver.title

```

WebDriver offers a number of ways to find elements using one of the find_element_by_* methods. For example,
the input text element can be located by its name attribute using find_element_by_name method.

```py

elem = driver.find_element_by_name("q")

```

Next, we are sending keys, this is similar to entering keys using your keyboard. Special keys can be sent using Keys class imported from selenium.webdriver.common.keys. 
To be safe, we’ll first clear any pre-populated text in the input field (e.g. “Search”) so it doesn’t affect our search results:

```py

elem.clear()
elem.send_keys("pycon")
elem.send_keys(Keys.RETURN)

```

After submission of the page, you should get the result if there is any.
To ensure that some results are found, make an assertion:

```py

assert "No results found." not in driver.page_source

```
Finally, the browser window is closed. You can also call quit method instead of close. 
The quit will exit entire browser whereas close` will close one tab, but if just one tab was open, by default most browser will exit entirely.:

```py

driver.close()

```
**I am sharing with you the below link to github repository to get know better about selenium python**
## Selenium Python

[**Selenium Python**](https://github.com/rafayethossain/Basic-Python-Script/tree/master/03.%20Selenium-Python)

## Selenium Python Crash Course

[**Selenium Python Crash Course**](https://github.com/rafayethossain/Basic-Python-Script/tree/master/04.%20Selenium%20Crash%20Course)




For Any Query or Assigment Contact 
**Rafayet Hossain**

✅ Business Analyst | SQA | Writer ✅


[![Linkedin](https://img.shields.io/badge/-LinkedIn-blue?style=flat&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/rafayethossain/)
[![Gmail](https://img.shields.io/badge/-Gmail-c14438?style=flat&logo=Gmail&logoColor=white)](mailto:rafayet13@gmail.com)




 
# All Posts on Testing:  

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
- [x]  [**How to Install Selenium with Python**](https://rafayethossain.github.io/2019-01-08-How-To-Install-Selenum-Python-Webdriver/)
- [x]  [**First Selenium Python Script**](https://rafayethossain.github.io/2019-01-09-My-First-Python-Selenium-Script/)



{: .box-success}
Enjoy !!!
**See Yaaa, Next.**

![Selenium with Python](/assets/img/selenium-with-python.png "Selenium with Python")
