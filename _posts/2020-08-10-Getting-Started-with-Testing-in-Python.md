---
title: Getting Started with Testing in Python
categories: ['porgramming']
tags: ['python', 'programming', 'unit-testing']
toc: true
---


<img src="https://miro.medium.com/max/4000/0*Ok0tm88hZLU5Prim">

Testing code is always wanted as a good habit. when you are working on a project, It’s really a good idea to check that every single unit/program is working perfectly. There is a lot of modules to test code in python. In this article, I’m going to share some basic with coding examples to getting started with python unit testing.

## Automated vs. Manual Testing

Testing is an integral part of any successful software project. Software Testing is categorized into two parts namely **Automation Testing** and **Manual Testing**.

### Manual Testing

Manual Testing is the process of testing the Software manually to find the defects before software goes live. This testing process is performed by a Quality Assurance engineer. In this process, testers execute test cases and generate reports manually without using any automation testing tools.

There is some kind of manual testing processes used by the testers.

* Black Box Testing

* White Box Testing

* Unit Testing

* System Testing

* Integration Testing

* Acceptance Testing

I’m not going deep in each type of Manual Testing on this basic learning. I will try to explain these types in my next article.

### Automation Testing

Automation Testing is the process of testing the software using an automation tool to find the defects. In this process, executing test scripts and generating reports are performed automatically. Some automation tools are:

* Selenium

* LoadRunner

* SilkTest

* IBM Functional Tester

![source: guru99](https://cdn-images-1.medium.com/max/2000/1*kj65XMPiH7-u0nAhFATI9A.png)*source: guru99*

This comparison doesn't mean that you can choose one over the other. In the software industry, both of them are used sequentially. There is still a lot to know about Automation and Manual Testing.

## Unit Testing vs. Integration Testing

When you are working on a team, you may contribute a small part of the software/project. The combined works become a successful project. When you write a simple function and test that code is working fine, then this type of test is called a **Unit test. **When all of the modules are integrated and then testing is required to check that everything is working as expected, that’s called **Integration Testing**. So, a unit testing is to identify that a small component is working or not whereas integrated testing is to identify that component operates with each other components on the application.

![unit test vs integration test](https://cdn-images-1.medium.com/max/2000/1*wLa_2P7D0coUth2vZ7iUiw.gif)*unit test vs integration test*

### Unit test:

* identify a small piece of code is working as expected or not

* checks a single component of the application/module

* It comes under the white box testing type

* test each unit separately and ensure that each unit is working as expected

### Integration Testing

* identify different modules are working as expected

* It checks the overall flow of the application

* comes under both white box and black box

* It’s performed after unit testing

In the 1st part, I have explained some basics of software testing and its purposes. In the 2nd part, I am giving some coding examples basis on unit testing in python.

In python programming, there are many test runners available. **unittest** is one of them which one is built into python standard library. Some other test runners are:

* **doctest**

* **pytest**

## unittest

**unittest** is a python built-in standard library. **unittest** contains both a testing framework and a test runner. To write and execute tests, it has some requirements. whiches are

1. You need to put your test cases inside a class as methods

1. You have to use assertion methods in the unittest class

![unittest assertion methods](https://cdn-images-1.medium.com/max/2000/1*9kSsBsn__CMQLEhRUcre6g.png)*unittest assertion methods*

To execute a test you have to:

1. import unittest library

1. create a class that inherits from unittest.TestCase

1. define test method with self as an argument

1. use self.assertion series to perform test execution

1. To generates the test results run unittest.main() inside the main function

That’s all, you will get OK if there is no error, see the below example.

{% gist a25cb22b0f328794c23e9fe0c6a6bf79 unittest.py %}

## Doctest

The **doctest **also a python built-in library. This module searches for pieces of text that look like interactive Python sessions in docstrings and then execute those sessions to verify that they work exactly as shown.

**Doctests** have a different use case than proper unit tests: they are usually less detailed and don’t catch special cases or obscure regression bugs. They are useful as expressive documentation of the main use cases of a module and its components. However, doctests should run automatically each time the full test suite runs.

A simple **doctest** in a function

{% gist cc53f9be64e6279395d14362c4c5716b doctest.py %}

While running this code, doctest will run and complain if the given description doesn't work as expected.

## pytest

**pytest** is an external tool for testing in python. It has some advantages compared to **unittest** . Since it is an external tool, so you have to install it first in your python interpreter. To install **pytest** run the following command:

    **pip install pytest**

following code to understand how it works:

{% gist e53d4b1e320bf00e01b318d6ed9b5d5f pytest.py %}

Run the following command in your project terminal:

    py.test pytest.py

![result of pytest](https://cdn-images-1.medium.com/max/2622/1*bMc8Y2mWYKznqjmwgIZRAw.png)*result of pytest*

You will get results like the above image.

We see that, **pytest** doesn’t need any TestClass, we can use simply assert to check test cases and execute the test cases directly from the terminal to generate reports.

You can use whatever you like and depending on your requirements. You can share with us which python module you are using currently.

![voting on unit test](https://www.pollsights.com/c/eLXRNd)

> Thanks for reading. Thumbs up if you like it. 
Also if you have any suggestion regarding this article, 
comments below.
