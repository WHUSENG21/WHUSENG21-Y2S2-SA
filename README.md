<!-- START: HEADER -->
<div align="center">
<div align="center">
  <img width="200px" src="./assets/images/Logo.png" alt="Logo.png"/>
  <img width="192px" src="./assets/images/Selenium_Logo.png" alt="Selenium Logo"/>
  </div>
  <h1>Selenium</h1>
  <h3>The Selenium Browser Automation Project</h3>
  
  **Version 3.6**
  
  **Contributors**

2021326660029 - Alba, Nelson Jr.

2021326660024 - Lauron, John Albert

2021326660023 - Plongkaew, Chaiwat

2021326660027 - Akaaboune, Sifeddine

Instructor and Lecturer 梁鹏老师 Peng Liang Laoshi

<!-- END: HEADER -->

---

  <!-- START: ABSTRACT -->

  <h1>Abstract</h1>  
  <p>This research paper is all about analysing the Software Architecture of the famous open-source project called Selenium. Also known as "The Selenium Browser Automation Project", this open-source project is an umbrella project that creates a wide set of tools, libraries, and extensions for browser automations and tests catering to different environments, domains, and platforms. This research paper would focus on the architecture of one of its known tool - the Selenium WebDriver.</p>
  <p><b>Acknowledgments: </b>We would like to thank Peng Liang Laoshi for giving us consistent and useful feedback and guidance in the process of formulating and in completion of this Software Architecture document for the Selenium Project.</p>
</div>

 <!-- END: ABSTRACT -->

---

<!-- START: REVISION LOG -->
<div align="center">
  <h1>Revision Log</h1>  
<table>
  <tr>
    <th>#</th>
    <th>Version</th>
    <th>Date</th>
    <th>Logs</th>
  </tr>
  <tr>
    <td>1</td>
    <td>1.1</td>
    <td>3/1/23</td>
    <td>
      <ul>
        <li><a href="#1---introduction">Description</a>,</li> 
        <li><a href="#1---introduction">Business Context</a>,</li> 
        <li><a href="#1---introduction">Key Quality Concerns</a></li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>2</td>
    <td>2.2</td>
    <td>3/8/23</td>
    <td>
      <ul>
        <li><a href="#1---introduction">Description</a>,</li> 
        <li><a href="#1---introduction">Business Context</a>,</li> 
        <li><a href="#1---introduction">Key Quality Concerns</a></li>
      </ul
    </td>
  </tr>
  <tr>
    <td>3</td>
    <td>2.3</td>
    <td>3/15/23</td>
    <td>
      <ul>
        <li><a href="#2---stakeholder-analysis">Stakeholder Analysis</a></li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>4</td>
    <td>2.4</td>
    <td>3/22/23</td>
    <td>
      <ul>
        <li><a href="#2---stakeholder-analysis">Stakeholder Analysis</a></li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>5</td><td>2.5</td><td>3/29/23</td>
<td>
      <ul>
        <li><a href="#2---stakeholder-analysis">Stakeholder Analysis</a></li>
        <li><a href="#3---viewpoints-analysis">Viewpoints Analysis</a></li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>6</td><td>3.6</td><td>4/5/23</td>
    <td>
      <ul>
        <li><a href="#2---stakeholder-analysis">Stakeholder Analysis</a></li>
        <li><a href="#3---viewpoints-analysis">Viewpoints Analysis</a></li>
        <li><a href="#4---perspectives-analysis">Pespectives Analysis</a></li>
      </ul>
    </td>
  </tr>
  <tr><td>7</td><td>3.7</td><td>4/12/23</td><td></td></tr>
  <tr><td>8</td><td>3.8</td><td>4/26/23</td><td></td></tr>
  <tr><td>9</td><td>3.9</td><td>4/19/23</td><td></td></tr>
  <tr><td>10</td><td>4.10</td><td>5/3/23</td><td></td></tr>
  <tr><td>11</td><td>4.11</td><td>5/10/23</td><td></td></tr>
</table>
</div>
<!-- END: REVISION LOG -->

---

<!-- START: TABLE OF CONTENTS -->
<details open align="left">
  <summary><b>Table of Contents</b></summary>

- [**1 - Introduction**](#1---introduction)
  - [1.1 - Description](#11---description)
  - [1.2 - File Organisation](#12---file-organisation)
- [**2 - Stakeholder Analysis**](#2---stakeholder-analysis)
  - [2.1 - Stakeholders by Category](#21---stakeholders-by-category)
    - [2.1.1 - Acquirers](#211---acquirers)
    - [2.1.2 - Assessors](#212---assessors)
    - [2.1.3 - Communicators](#213---communicators)
    - [2.1.4 - Developers](#214---developers)
    - [2.1.5 - Maintainers](#215---maintainers)
    - [2.1.6 - Production Engineers](#216---production-engineers)
    - [2.1.7 - Suppliers](#217---suppliers)
    - [2.1.8 - Support Staff](#218---support-staff)
    - [2.1.9 - System Administrators](#219---system-administrators)
    - [2.1.10 - Testers](#2110---testers)
    - [2.1.11 - Users](#2111---users)
    - [2.1.12 - Competitors](#2112---competitors)
  - [2.2 - Stakeholder Influence](#22---stakeholder-influence)
  - [2.3 - Integrators](#23---integrators)
- [**3 - Viewpoints Analysis**](#3---viewpoints-analysis)
  - [3.1 - Context View](#31---context-view)
    - [3.1.1 - System Scope](#311---system-scope)
    - [3.1.2 - External Entities Involved](#312---external-entities-involved)
    - [3.1.3 - Context View Explanation](#313---context-view-explanation)
  - [3.2 - Functional View](#32---functional-view)
    - [3.2.1 - Capabilities](#321---capabilities)
    - [3.2.2 - Interfaces and Structure](#322---interfaces-and-structure)
  - [3.3 - Development View](#33---development-view)
    - [3.3.1 - Module Structure](#331---module-structure)
    - [3.3.2 - Module Dependencies](#332---module-dependencies)
    - [3.2.3 - Common Design](#323---common-design)
    - [3.2.4 - Codeline](#324---codeline)
      - [Source Code Structure](#source-code-structure)
      - [Build, Integration and Test Approach](#build-integration-and-test-approach)
      - [Release Process](#release-process)
  - [3.4 - Deployment View](#34---deployment-view)
  - [...](#)
- [**4 - Perspectives Analysis**](#4---perspectives-analysis)
  - [4.1 - Performance and Scalability Perspective](#41---performance-and-scalability-perspective)
  - [4.2 - Usability Perspective](#42---usability-perspective)
- [**5 - Technical Debt**](#5---technical-debt)
  - [5.1 - Code Quality](#51---code-quality)
  - [5.2 - Historical Debt](#52---historical-debt)
  - [5.3 - Test Coverage](#53---test-coverage)
  - [5.4 - Possible Improvements](#54---possible-improvements)
- [**5 - Conclusion**](#5---conclusion)
- [References](#references)

</details>
<!-- END: TABLE OF CONTENTS -->

---

<!-- START: MAIN CONTENT -->
# **1 - Introduction**

## 1.1 - Description 

Selenium is an open-source project that allows automated testing of web applications across various browsers and platforms. It provides a suite of tools for automating web browsers, including a browser automation framework, a WebDriver API, and a language-specific client library. With Selenium, developers and testers can write scripts to simulate user interactions with a website, such as clicking buttons, filling out forms, and navigating through pages. Selenium supports multiple programming languages, including Java, Python, and JavaScript, making it easy to integrate with existing testing frameworks. It is widely used in the industry for testing web applications, ensuring they work as expected across different browsers and operating systems. Additionally, Selenium is highly extensible, enabling developers to create custom plugins and integrations to extend its capabilities.

The Selenium Project is formed by a community of users and open source contributors who develop, use and promote the different Selenium projects (IDE, Grid, WebDriver) and other related things, with the end goal of benefiting the community as a whole. The Selenium Project wants as much as possible to operate using procedures that are fair, open, inviting, and ultimately good for the community. Selenium is primarily used for but not limited to automated testing of web applications. It helps developers and testers quickly identify and fix issues with applications, ensuring that they work as expected across different browsers (Firefox, Microsoft Edge, Chrome, etc) and platforms.

Their key quality concerns are: 

1. <b>Test Stability:</b> Selenium tests must be reliable and consistent, producing the same results each time they are run.
2. <b>Test Coverage:</b> Selenium tests should cover all essential features and functionalities of the application under test.
3. <b>Test Maintainability:</b> Selenium tests should be easy to maintain, update, and modify when the application changes.
4. <b>Test Performance:</b> Selenium tests must be efficient and not overly burden the system, as this can cause false test results.
5. <b>Test Scalability:</b> Selenium tests should be able to handle a large number of test cases and execute them quickly.

## 1.2 - File Organisation
This document is organised in the following manner:

1. Chapter 2: Stakeholder Analysis
2. Chapter 3: Viewpoints Analysis
3. Chapter 4: Perspectives Analysis
4. Chapter 5: Technical Debt

---

# **2 - Stakeholder Analysis**

In this chapter, we will analyse Selenium WebDriver's architecture can work with its stakeholders by creating an architecture that would meet their complex, overlapping, and sometimes, needs and concerns that conflict with each other.

## 2.1 - Stakeholders by Category

We classify stakeholders based on Rozanski and Woods according to their roles and concerns.
### 2.1.1 - Acquirers
*Oversee the procurement of the system or product*

This category includes software development firms, testing service providers, or enterprises that use Selenium for their testing needs. Acquirers are interested in evaluating the features, functionalities, and compatibility of Selenium with their existing systems and processes. They may also be involved in negotiating licensing agreements and pricing models for using the Selenium project.

1. Software development firms such as Microsoft or Google
1. Testing service providers such as Sauce Labs or BrowserStack
1. Enterprises that use Selenium for their testing needs, such as Amazon or Netflix

### 2.1.2 - Assessors
*Oversee the system’s conformance to standards and legal regulation*

This category of stakeholders is responsible for ensuring that the Selenium project adheres to industry standards, regulations, and legal requirements. Assessors may include standards bodies, compliance auditors, and legal regulators. They are interested in evaluating the quality, safety, and security of the Selenium project and may require compliance documentation, such as test reports or certification records.

1. Standards bodies such as the World Wide Web Consortium (W3C)

### 2.1.3 - Communicators
*Explain the system to other stakeholders via its documentation and training materials*

Technical writers, trainers, and instructional designers fall under this category. They are responsible for developing the documentation and training materials required to explain Selenium's features and functionalities to other stakeholders. Communicators work closely with the development team to understand the technical details of Selenium and translate them into user-friendly language. They may also conduct training sessions or webinars to educate users on how to use Selenium.

1. Technical writers such as those working for the Selenium documentation team
1. Instructional designers such as those creating Selenium training courses
1. Trainers such as those conducting Selenium webinars or workshops


### 2.1.4 - Developers
*Construct and deploy the system from specifications (or lead the teams that do this)*

Software engineers and developers who work on designing, coding, and deploying Selenium's framework, libraries, and APIs fall under this category. They are responsible for building and maintaining the Selenium project and contributing to the development of Selenium-based testing tools and plugins. Developers work closely with other stakeholders to understand their requirements and ensure that Selenium is compatible with different operating systems and web browsers.

1. The Selenium project's core development team, including Simon Stewart, Julian Harty, and Jim Evans
1. Open source contributors who contribute code, bug fixes, and enhancements to Selenium
1. Third-party developers who create Selenium-based testing tools or plugins, such as the Selenium IDE or Selenium Grid

### 2.1.5 - Maintainers
*Manage the evolution of the system once it is operational*

This category of stakeholders is responsible for managing the evolution of the Selenium project once it is operational. Maintainers may include software engineers, testers, or project managers. They are responsible for fixing bugs, adding new features, improving performance, and ensuring that Selenium remains compatible with other software and technologies. Maintainers work closely with developers to ensure that any changes or updates to Selenium are implemented smoothly.

1. Members of the Selenium project's core development team who maintain the codebase, fix bugs, and add new features
1. Community members who maintain Selenium-based testing tools or plugins
1. Project managers who oversee the maintenance of the Selenium project

### 2.1.6 - Production Engineers
*Design, deploy, and manage the hardware and software environments in which the system will be built, tested, and run*

Engineers who design, deploy, and manage the hardware and software environments in which Selenium is built, tested, and run fall under this category. This may include managing servers, databases, and cloud-based platforms. Production engineers work closely with developers and maintainers to ensure that Selenium is deployed in a secure and scalable environment.

1. Infrastructure engineers at cloud service providers such as Amazon Web Services (AWS) or Google Cloud Platform (GCP)
1. DevOps engineers who manage the deployment and scaling of the Selenium project
1. Database administrators who ensure that the Selenium project's data is secure and available

### 2.1.7 - Suppliers
*Build and/or supply the hardware, software, or infrastructure on which the system will run*

This category includes companies that build or supply the hardware, software, or infrastructure required to run Selenium. Suppliers may include hosting providers, cloud service providers, and tool vendors. They work closely with other stakeholders to ensure that their products and services are compatible with Selenium.

1. Hardware suppliers such as Dell or HP
1. Cloud service providers such as Amazon Web Services (AWS) or Google Cloud Platform (GCP)
1. Tool vendors such as JetBrains or Atlassian

### 2.1.8 - Support Staff
*Provide support to users for the product or system when it is running*

Support staff provides technical support and troubleshooting to users who encounter issues while using Selenium. This category includes customer support representatives, technical support engineers, and helpdesk personnel. They work closely with users to resolve any issues and may escalate more complex problems to developers or maintainers.

1. Technical support engineers at testing service providers such as Sauce Labs or BrowserStack
1. Customer support representatives at software development firms such as Microsoft or Google
1. Helpdesk personnel at enterprises that use Selenium for their testing needs

### 2.1.9 - System Administrators
*Run the system once it has been deployed*

This category of stakeholders is responsible for running and managing the Selenium system once it has been deployed. This includes installing updates, monitoring performance, and ensuring system availability. System administrators work closely with production engineers and maintainers to ensure that Selenium is running smoothly and that any issues are resolved quickly.

1. System administrators at cloud service providers such as AWS or GCP
1. IT administrators at enterprises that use Selenium for their testing needs
1. DevOps engineers who manage the deployment and scaling of Selenium-based testing environments

### 2.1.10 - Testers
*Test the system to ensure that it is suitable for use*

Testers are individuals or teams who test the Selenium project to ensure that it is suitable for use, that it meets user requirements, and that it is compatible with different operating systems and web browsers. This category includes software testers, quality assurance engineers, and testing service providers. Testers work closely with developers and maintainers to identify and report any bugs or issues that they encounter during testing.

1. Software testers at software development firms such as Microsoft or Google
1. Quality assurance engineers at enterprises that use Selenium for their testing needs
1. Testing service providers such as Sauce Labs or BrowserStack

### 2.1.11 - Users
*Define the system’s functionality and ultimately make use of it*

Users of Selenium are individuals or teams who define the system's functionality and ultimately make use of it. This category includes software developers, quality assurance teams, and automation engineers who use Selenium to test web applications. Users are interested in evaluating the features, functionalities, and compatibility of Selenium with their existing software development processes. They may also provide feedback on usability, performance, and other aspects of Selenium that are important to their testing needs.

1. Software developers who use Selenium to test web applications
1. Automation engineers who use Selenium to create automated test scripts
1. Quality assurance teams who use Selenium to ensure software quality and functionality

### 2.1.12 - Competitors
*Aim to put a similar or better competing system on the market.*

Competitors of Selenium are individuals or teams who aim to put a similar or better competing system to Selenium on the market. These stakeholders aim to develop a better system themselves to gain a competitive advantage over Selenium in the same automated testing tools market. 

Stakeholders which are categorised as competitors to Selenium include:
1. testRigor
2. Rapise 
3. Katalon Platform
4. Virtuoso
5. Subject7
6. Testim
7. etc.


## 2.2 - Stakeholder Influence
Another way to classify the stakeholders of Selenium is to classify them by the power or influence they have to be able to change the system and by their interest in the Selenium Project.

1. Official Selenium Members - The people who are officially associated with Selenium.
2. Selenium Community - The Selenium open-source community is the community that helps contribute to the Selenium open-source project in any way (ex: bug reports, feature requests, enhancing documentation, code contributions, etc. )
3. Developers Community - Community of developers that uses Selenium for their own projects and testing automations.
4. 


<!-- TODO: Create Power-Inrterest Grid for Selenium's Stakeholders -->


## 2.3 - Integrators

# **3 - Viewpoints Analysis**
## 3.1 - Context View
### 3.1.1 - System Scope
Selenium brings together browser vendors, engineers, and enthusiasts to further an open discussion around the automation of the web platform. Selenium has 3 main components to make itself communicate with a browser such as WebDriver, RemoteWebDriver, and Selenium Server or Selenium Grid. First, at the core of Selenium is WebDriver APIs, an interface to write instruction sets that can be run interchangeably in many browsers. It uses browser automation APIs provided by browser vendors to control the browser and run tests. Once you’ve installed everything, only a few lines of code get you inside a browser. The communication way of selenium can categorize into two types: Direct communication and Remote communication. In direct communication, WebDriver passes commands to the browser through the browser’s driver and receives information back via the same route. In addition, the driver is specific to the browser, such as ChromeDriver for Google’s Chrome/Chromium, GeckoDriver for Mozilla’s Firefox, etc.  In Remote communication, WebDriver will talk to RemoteWebDriver, then RemoteWebDriver will talk to the browser’s driver. Plus, RemoteWebDriver can also take place using Selenium Server or Selenium Grid.


### 3.1.2 - External Entities Involved
In terms of the relationship between developers and Selenium,  Selenium has role that is to test the framework of developers by using WebDriver. A test framework that is compatible with the language bindings is a bare minimum requirement for developers; examples include NUnit for.NET, JUnit for Java, RSpec for Ruby, etc. Their WebDriver and related actions in their tests should be run and executed by the test framework.

### 3.1.3 - Context View Explanation
...

## 3.2 - Functional View
The functional viewpoint of Selenium can be divided into three main components:
### 3.2.1 - Capabilities

1. Selenium WebDriver: This is the core component of Selenium. It is responsible for controlling the web browser and sending commands to it. WebDriver supports several different web browsers and allows testers to create automated tests for different web applications.

2. Selenium IDE: This is a graphical user interface that allows testers to record and replay their test scripts. It also provides advanced scripting capabilities, allowing testers to create more complex tests.

3. Selenium Grid: This component allows testers to distribute tests across multiple machines, making it easier to run tests in parallel. It also provides a way to manage the nodes on which tests are running.

### 3.2.2 - Interfaces and Structure
These components all interact with each other to provide a complete testing platform. WebDriver is responsible for controlling the web browser and sending commands to it. IDE is used to record and replay test scripts, and Grid is used to distribute tests across multiple machines. Together, all three components provide a powerful testing solution for web applications.

The functional viewpoint focusing on the WebDriver:

Selenium WebDriver is the core component of Selenium and is responsible for controlling the web browser and sending commands to it. It supports multiple web browsers such as Chrome, Firefox, Edge, and Safari, allowing testers to create automated tests for different web applications.

The WebDriver supports two types of commands: 
- Actions and assertions. Actions are commands that interact with the web browser, such as clicking on elements, entering text, and submitting forms. Assertions are commands that verify  that the web page contains the expected elements and values.

- The WebDriver also provides a number of APIs that allow testers to create more complex tests. These APIs include methods for finding elements, manipulating the DOM, and taking screenshots. WebDriver also provides support for JavaScript and AJAX, allowing testers to create more advanced tests.

- Finally, WebDriver supports various languages such as Java, Python, and JavaScript, allowing testers to create automated tests in the language of their choice. It also provides a number of features to help testers debug their tests, such as logging, breakpoints, and stack traces.






## 3.3 - Development View
### 3.3.1 - Module Structure
### 3.3.2 - Module Dependencies
### 3.2.3 - Common Design
### 3.2.4 - Codeline
#### Source Code Structure
#### Build, Integration and Test Approach
#### Release Process
...

## 3.4 - Deployment View

## ...

# **4 - Perspectives Analysis**

Selenium's architecture as a whole has a lot of benefits catering to the needs of their different stakeholders. The first benefit is that their architecture will inhibit or enable a system’s driving quality attributes. Another benefit of their architecture is that their architecture can be created as a transferable, reusable model that form the heart of a product line. Selenium’s architecture as an umbrella project to develop a wide range of tools and extensions for browser automation for testing purposes allows Selenium to be very modifiable, reusable, and scalable.

## 4.1 - Performance and Scalability Perspective

With the amount of different tools and extensions to use, as well as being able to use them in a wide range of programming languages, Selenium proves to be scalable as you can widely use selenium’s tools and extensions in different situations, and easily modify and reuse automated tests in different environments. With having one architecture with a wide range of application, development of applications could become scalable without having the need to go for other alternatives for doing automated testing in different environments or platforms.

Another benefit to note is that their documented architecture enhances communication among stakeholders. Selenium provides document pages for different interactions between the components and the browser such as, direct-communication, remote communication through RemoteWebDriver, and Remote communication through Selenium Grid.

Lastly, their architecture can provide the basis for evolutionary prototyping. Initially, they were developed as a solution in the form of a program using Javascript to address shortcomings of manual testing back in 2004, the creator of Selenium Jason Huggins realised the idea of the testing program could do much more and called their program from JavaScript TestRunner to Selenium Core and made it open-sourced. Their program turned into a big project with the goal to make automating of testing easier by overcoming domain-related issues by creating different tools and extensions and expanding from JavaScript to be able to be used also in different programming languages, making it more usable and wider in application and use by people. There is clear evolution in improving further their architecture as they develop and advance along the tools they develop, benefiting and increasing possibilities and usabilities for their different tools, extensions, and libraries undertaking the same architecture principles they have designed. With a clear sign of will to continue to evolve and develop to better cater for their stakeholders and their needs, Selenium's architecture keeps developing to the future on.

## 4.2 - Usability Perspective
 
Selenium is modifiable because you can assign different software tests using different tools or extensions, as well as different programming languages to conduct automated tests in different environments.

The wide range of tools and extensions under the Selenium Project allows people to create automated tests under one architecture, making automated tests reusable and easier to do by following the same architecture with provided support for different programming languages, and tools and extensions catering to different environments and platforms, lesser worry of domain-related issues to conduct automated testings and synchronisation for test driven developments.


# **5 - Technical Debt**
## 5.1 - Code Quality
## 5.2 - Historical Debt
## 5.3 - Test Coverage
## 5.4 - Possible Improvements
# **5 - Conclusion**

# References

<!-- END: MAIN CONTENT -->
