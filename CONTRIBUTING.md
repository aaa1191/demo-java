# Adding Code To demo-java

**Working on your first Pull Request?** You can learn how from this *free* series [How to Contribute to an Open Source Project on GitHub](https://kcd.im/pull-request)

* Clone the repository

* Decide if your code example is an example or a framework

An **example** is some code that wants to demonstrate a feature. 
For example, parallelization with JUnit4, parallelization with
Junit5,
biometric authentication, simple Appium iOS test.

A **best-practice** is solution that shows off
how to use a specific technology combination in the optimal way
according to the Solution Architects team. You might have a
**best-practice** that shows how to correctly use Cucumber with Junit4
or Cucumber with Junit5 or maybe a data driven framework with
TestNg.
**best-practice** examples are not as common as code examples.

## Add relevant code

### Repository Structure

The correct repository structure is:

```text
Description
-----------------
It's basically Selenium/Appium/API... examples.
Followed by testRunnerVersion(which really only applies for Junit)
Most of the code is an "example".
There may be one or more "best-practice". Technically, there 
should only be a single "best-practice" implementation per our team.
However, we may choose to break this up into "best-practice" for web, mobile, api...

|-- demo-java
    |-- best-practice (Java module)
    |-- selenium-testRunnerVersion-examples (Java module)
    |-- selenium-testRunnerVersion-cucumber-examples (Java module)
    |-- appium-testRunnerVersion-examples (Java module)
    |-- appium-testRunnerVersion-cucumber-examples (Java module)
```

```text
Specific Structure With Examples
--------------------------------
|-- demo-java
    |-- best-practice (Java module)
            |-- src
            |-- main
            |-- test
                |-- java
                    |-- com.saucedemo
                        |-- VisualTests.java
                        |-- PerformanceTests.java
                        |-- FunctionalWebTests.java
                        |-- MobileWebTests.java
                        |-- ...
    |-- selenium-junit4-examples (Java module)
        |-- src
            |-- main
            |-- test
                |-- java
                    |-- com.saucedemo
                        |-- Junit4InParallelTests.java
                        |-- Junit4TestStatusUpdate.java
                        |-- Junit4DataDriven.java
                        |-- PerformanceTesting.java
    |-- selenium-testng-examples (Java module)
    |-- src
        |-- main
        |-- test
            |-- java
                |-- com.saucedemo
                    |-- TestNgTest.java
                    |-- W3CTest.java
                    |-- ParallelTest.java
                    |-- ...
    |-- selenium-testng-cucumber-examples (Java module)
        |-- ...
```

## FAQs

### Why is there only one best-practice folder?

With the evolution of Sauce, a true Best Practice is not only
Selenium automation. A true Best Practice shows customers
how to utilize all of the tools (Selenium, Appium, Visual, Performance, API...)
that Sauce has to offer in a cohesive framework
and test strategy.

### Why should I separate my code in this manner?

The key ideas behind this organization are visibility and 
reusability for the clients and the team. A mature customer may need
a performance testing code example using Junit5. On the other
hand, a less mature, but very valuable customer may need the 
same exact code sample but using Junit3. If we create
this code sample for one of the customers, wouldn't it
also be nice to make these visible to all other customers
that desire a specific combination of technologies?

But where would such code examples go? 

In the above structure that's easy for everyone to understand.

### Why does Cucumber get its own module?

Because the organization of the Cucumber source code is
different than the typical organization of a Maven project.
As a result, Cucumber needs it's own module where everything
is separated to meet Cucumber standards.

Also, Cucumber doesn't have a Best Practice as we don't
believe that it is one nor does our team have a Best Practice strategy
developed.

### But I don't want to create a code example for 10 different technologies!

There is no requirement to have a code **example** for every single tech combination.

Only create what's needed at the time. 
All we ask is that if you create a code example for one client
using a specific combination of technologies (ex Junit3 test status reporting), 
then make
that available to all customers, SAs, and SEs. 

Let your work be reusable and visible for the future instead
of being hidden somewhere in a private repository. It's highly
likely that there is a customer, or an engineer that's 
spending time recreating a code sample that you already 
created in your private repo.

### How will someone find my beautiful code sample?

There are code examples that are popular 
(Getting started samples) and there are code examples that
aren't so popular (using Junit3 to update test status).

If you feel that your code example needs to be front and
center then simply add it to the main [README](README.md).
We would be happy to see your excellent code there 😁
