---
layout: post
title: How To Install Selenium Python Webdriver
subtitle: Software Test Automation with Selenium & Python
tags:
  [
    python tutorial,
    python tips,
    selenium,
    python,
    webdriver,
    python selenium webdriver,
  ]
image: /img/selenium-with-python.png
bigimg: /img/back.gif
thumbnail-img: /assets/img/selenium-with-python.png
share-img: /img/selenium-with-python.png
cover-img: /assets/img/cover.jpg
---

Selenium Python bindings provide a straightforward API for creating functional/acceptance tests with Selenium WebDriver. The majority of Python Selenium libraries are similar to Selenium.Net or Java packages.

Selenium Python bindings provide a straightforward API for developers and QA engineers to access Selenium WebDrivers such as Firefox, Internet Explorer, Chrome, Remote, and others.
Python versions `2.7, 3.4, 3.5, 3.6, and 3.10` are currently supported.

Python Selenium bindings require the installation of both the Python language and Python Selenium bindings. This article describes how to install Python Selenium bindings on Windows.

How to Setup the Selenium Python Webdriver:

# Step 1: 

Install Python 3.10 using the Windows binary installer package.

If you are using 32bit windows, download this package `"Python 3.10.0 Windows x86 MSI Installer"` and install it.
For 64 bit windows, download and install the package `"Python 3.10.0 Windows X86-64 MSI Installer".`

# Step 2:

python is installed at `C:\Python310` folder by default.
Start a command prompt using the "cmd.exe" program and run the "pip.exe" command as given below to install or upgrade selenium.

`C:\Python34\Scripts\pip.exe install -U selenium`
Alternatively, you can download the source distribution selenium-2.41.tar.gz , unarchive it, and run the command below:

python setup.py install

# Step 3:

test Python and Selenium library installation. Open Python 3.6.0 Shell and type the following command.
This code will launch Google page if Python and Selenium bindings are installed correctly.

```py
from selenium import webdriver
browser = webdriver.Firefox()
browser.get('http://www.google.com')
```

_More information can be found on Python Selenium site._



For Any Query or Assigment Contact 
**Rafayet Hossain**

✅ Business Analyst || SQA || Writer ✅


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
