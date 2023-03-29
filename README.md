<!-- START: HEADER -->
<div align="center">
  <img width="30%" src="./assets/images/Logo.png" alt="Logo.png"/>
  <h1>Selenium</h1>
  <h3>The Selenium Browser Automation Project</h3>
  <p>This research paper is all about analysing the Software Architecture of the famous open-source project called Selenium. Also known as "The Selenium Browser Automation Project", this open-source project is an umbrella project that creates a wide set of tools, libraries, and extensions for browser automations and tests catering to different environments, domains, and platforms. This research paper would focus on the architecture of one of its known tool - the Selenium WebDriver.</p>
</div>
<!-- END: HEADER -->

<!-- START: TABLE OF CONTENTS -->
<details open align="left">
  <summary><b>Table of Contents</b></summary>
  
- [**1 - Introduction**](#1---introduction)
  - [1.1 - Description](#11---description)
  - [1.2 - Business Context](#12---business-context)
  - [1.3 - Key Quality Concerns](#13---key-quality-concerns)
  - [1.4 - File Organisation](#14---file-organisation)
- [**2 - Stakeholder Analysis**](#2---stakeholder-analysis)
  - [2.2 Selenium's Architectural Benefits](#22-seleniums-architectural-benefits)
- [**3 - Viewpoints Analysis**](#3---viewpoints-analysis)
  - [3.1 - Context View](#31---context-view)
  - [3.2 - Development View](#32---development-view)
  - [3.3 - Deployment View](#33---deployment-view)
  - [...](#)
- [**4 - Perspectives Analysis**](#4---perspectives-analysis)
  - [...Coming Soon...](#coming-soon)
- [**5 - Conclusion**](#5---conclusion)
  - [...Coming Soon...](#coming-soon-1)
- [References](#references)


</details>
<!-- END: TABLE OF CONTENTS -->

---

<!-- START: MAIN CONTENT -->
# **1 - Introduction**
In this chapter, we will introduce what Selenium is, what is their business context, environment and significance, and the key quality concerns they would like to tackle and bring.

## 1.1 - Description

Selenium is an open-source project that allows automated testing of web applications across various browsers and platforms. It provides a suite of tools for automating web browsers, including a browser automation framework, a WebDriver API, and a language-specific client library. With Selenium, developers and testers can write scripts to simulate user interactions with a website, such as clicking buttons, filling out forms, and navigating through pages. Selenium supports multiple programming languages, including Java, Python, and JavaScript, making it easy to integrate with existing testing frameworks. It is widely used in the industry for testing web applications, ensuring they work as expected across different browsers and operating systems. Additionally, Selenium is highly extensible, enabling developers to create custom plugins and integrations to extend its capabilities.

## 1.2 - Business Context

The Selenium Project is formed by a community of users and open source contributors who develop, use and promote the different Selenium projects (IDE, Grid, WebDriver) and other related things, with the end goal of benefiting the community as a whole. The Selenium Project wants as much as possible to operate using procedures that are fair, open, inviting, and ultimately good for the community. Selenium is primarily used for but not limited to automated testing of web applications. It helps developers and testers quickly identify and fix issues with applications, ensuring that they work as expected across different browsers (Firefox, Microsoft Edge, Chrome, etc)  and platforms.

## 1.3 - Key Quality Concerns
1. <b>Test Stability:</b> Selenium tests must be reliable and consistent, producing the same results each time they are run.
2. <b>Test Coverage:</b> Selenium tests should cover all essential features and functionalities of the application under test.
3. <b>Test Maintainability:</b> Selenium tests should be easy to maintain, update, and modify when the application changes.
4. <b>Test Performance:</b> Selenium tests must be efficient and not overly burden the system, as this can cause false test results.
5. <b>Test Scalability:</b> Selenium tests should be able to handle a large number of test cases and execute them quickly.

## 1.4 - File Organisation
1. Chapter 2: Stakeholder Analysis
2. Chapter 3: Viewpoints Analysis
3. Chapter 4: Perspectives Analysis


---

# **2 - Stakeholder Analysis**
In this chapter, we will analyse Selenium WebDriver's architecture can work with its stakeholders by creating an architecture that would meet their complex, overlapping, and sometimes, needs and concerns that conflict with each other.

We classify stakeholders based on Rozanski and Woods according to their roles and concerns as in the following table:

<div align="center">

| Type                  | Description                                                                                                          |
| --------------------- | -------------------------------------------------------------------------------------------------------------------- |
| Acquirers             | Oversee the procurement of the system or product                                                                     |
| Assessors             | Oversee the system’s conformance to standards and legal regulation                                                   |
| Communicators         | Explain the system to other stakeholders via its documentation and training materials                                |
| Developers            | Construct and deploy the system from specifications (or lead the teams that do this)                                 |
| Maintainers           | Manage the evolution of the system once it is operational                                                            |
| Production Engineers  | Design, deploy, and manage the hardware and software environments in which the system will be built, tested, and run |
| Suppliers             | Build and/or supply the hardware, software, or infrastructure on which the system will run                           |
| Support Staff         | Provide support to users for the product or system when it is running                                                |
| System Administrators | Run the system once it has been deployed                                                                             |
| Testers               | Test the system to ensure that it is suitable for use                                                                |
| Users                 | Define the system’s functionality and ultimately make use of it                                                      |
</div>

**Stakeholders in more detail**
<table>
<tr>
<th>Type</th>
<th>Stakeholders</th>
<th>Description</th>
</tr>

<tr>
<td>
Acquirers
</td>
<td>
<ol>
<li>Software development firms such as Microsoft or Google</li>
<li>Testing service providers such as Sauce Labs or BrowserStack</li>
<li>Enterprises that use Selenium for their testing needs, such as Amazon or Netflix</li>

</ol>
</td>
<td>
This category includes software development firms, testing service providers, or enterprises that use Selenium for their testing needs. Acquirers are interested in evaluating the features, functionalities, and compatibility of Selenium with their existing systems and processes. They may also be involved in negotiating licensing agreements and pricing models for using the Selenium project.
</td>
</tr>
<tr>
<td>
Assessors
</td>
<td>
Standards bodies such as the World Wide Web Consortium (W3C)
</td>
<td>
This category of stakeholders is responsible for ensuring that the Selenium project adheres to industry standards, regulations, and legal requirements. Assessors may include standards bodies, compliance auditors, and legal regulators. They are interested in evaluating the quality, safety, and security of the Selenium project and may require compliance documentation, such as test reports or certification records.
</td>
</tr>

<tr>
<td>
Communicators
</td>
<td>
<ol>
<li>Technical writers such as those working for the Selenium documentation team</li>
<li>Instructional designers such as those creating Selenium training courses</li>
<li>Trainers such as those conducting Selenium webinars or workshops</li>

</ol>
</td>
<td>

</td>
</tr>

<tr>
<td>

</td>
<td>

</td>
<td>

</td>
</tr>

<tr>
<td>

</td>
<td>

</td>
<td>

</td>
</tr>

<tr>
<td>

</td>
<td>

</td>
<td>

</td>
</tr>

<tr>
<td>

</td>
<td>

</td>
<td>

</td>
</tr>

<tr>
<td>

</td>
<td>

</td>
<td>

</td>
</tr>

<tr>
<td>

</td>
<td>

</td>
<td>

</td>
</tr>

<tr>
<td>

</td>
<td>

</td>
<td>

</td>
</tr>

<tr>
<td>

</td>
<td>

</td>
<td>

</td>
</tr>

<tr>
<td>

</td>
<td>

</td>
<td>

</td>
</tr>
</table>


## 2.2 Selenium's Architectural Benefits
Selenium's architecture as a whole has a lot of benefits catering to the needs of their different stakeholders. The first benefit is that their architecture will inhibit or enable a system’s driving quality attributes. Another benefit of their architecture is that their architecture can be created as a transferable, reusable model that form the heart of a product line. Selenium’s architecture as an umbrella project to develop a wide range of tools and extensions for browser automation for testing purposes allows Selenium to be very modifiable, reusable, and scalable. 

1. **Modifiability:** It is modifiable because you can assign different software tests using different tools or extensions, as well as different programming languages to conduct automated tests in different environments.
2. **Reusability:** The wide range of tools and extensions under the Selenium Project allows people to create automated tests under one architecture, making automated tests reusable and easier to do by following the same architecture with provided support for different programming languages, and tools and extensions catering to different environments and platforms, lesser worry of domain-related issues to conduct automated testings and synchronisation for test driven developments.
3. **Scalability:** With the amount of different tools and extensions to use, as well as being able to use them in a wide range of programming languages, Selenium proves to be scalable as you can widely use selenium’s tools and extensions in different situations, and easily modify and reuse automated tests in  different environments. With having one architecture with a wide range of application, development of applications could become scalable without having the need to go for other alternatives for doing automated testing in different environments or platforms.

Another benefit to note is that their documented architecture enhances communication among stakeholders. Selenium provides document pages for different interactions between the components and the browser such as, direct-communication, remote communication through RemoteWebDriver, and Remote communication through Selenium Grid. 

Lastly, their architecture can provide the basis for evolutionary prototyping. Initially, they were developed as a solution in the form of a program using Javascript to address shortcomings of manual testing back in 2004, the creator of Selenium Jason Huggins realised the idea of the testing program could do much more and called their program from JavaScript TestRunner to Selenium Core and made it open-sourced. Their program turned into a big project with the goal to make automating of testing easier by overcoming domain-related issues by creating different tools and extensions and expanding from JavaScript to be able to be used also in different programming languages, making it more usable and wider in application and use by people. There is clear evolution in improving further their architecture as they develop and advance along the tools they develop, benefiting and increasing possibilities and usabilities for their different tools, extensions, and libraries undertaking the same architecture principles they have designed. With a clear sign of will to continue to evolve and develop to better cater for their stakeholders and their needs, Selenium's architecture keeps developing to the future on.

# **3 - Viewpoints Analysis**
...Coming Soon...

## 3.1 - Context View
...
## 3.2 - Development View
...
## 3.3 - Deployment View
...
---
# **4 - Perspectives Analysis**
...Coming Soon...
---
# **5 - Conclusion**
...Coming Soon...
---
# References




<!-- END: MAIN CONTENT -->

