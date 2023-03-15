# WHUSENG21-Y2S2-SA

# Project Topics Proposal (03/15/23 Wednesday)

<table>

  <tr>
    <th>#</th>
    <th>TOPIC</th>
    <th>DESCRIPTION</th>
  </tr>

  <!-- START: TOPIC#1: SPRING BOOT -->
  <tr>
    <td>1</td>
    <td><h2>Spring Boot</h2></td>
    <td>
      <h3>Description</h3>
      <p>The Spring Framework is a popular, open-source enterprise-level tool for creating production-grade applications and services that run on the Java Virtual Machine. Spring Boot simplifies the process of developing with Spring Framework by providing three key capabilities: autoconfiguration, an opinionated approach to configuration, and the ability to generate standalone applications. These elements work in concert to give developers a way to quickly and easily set up a Spring-based app with minimal configuration and setup.</p>
      <br/>
      <h3>Business Context</h3>
      <p>Spring Boot is an open-source Java-based framework used to create a micro Service and provides a streamlined, modular approach for creating apps. It is developed by Pivotal Team and is used to build stand-alone and production-ready spring web-applications. It is one specific module that is built as an extension of the Spring framework.Therefore, Spring can be used to develop applications for the web, desktop, mobile, and cloud. It is used by many organizations to build enterprise applications and web applications.</p>
      <br/>
      <h3>Key Quality Concerns</h3>
      <ol>
        <li><b>Security:</b> Spring Boot provides a range of security features, but the user must be aware of the specific security concerns that arise when developing a web application.</li>
        <li><b>Build and Deployment:</b> Spring Boot makes it easy to build and deploy applications, but it can be difficult to manage the complexity of the deployments.</li>
        <li><b>Performance:</b> Spring Boot has excellent performance characteristics, but it can be difficult to monitor and optimize the performance of a Spring Boot application. </li>
        <li><b>Scalability:</b> Spring Boot is designed to be scalable, but it can be difficult to scale an application to meet increased demand.</li>
        <li><b>Maintenance:</b> Spring Boot provides a range of features for maintaining applications, but it can be difficult to keep up with the maintenance tasks required to keep an application running.</li>
      </ol>
    </td>
  </tr>
  <!-- END: TOPIC#1: SPRING BOOT -->
  
  <!-- START: TOPIC#2: SELENIUM -->
  <tr>
    <td>2</td>
    <td><h2>Selenium</h2></td>
    <td>
      <h3>Description</h3>
      <p>Selenium is an open-source project that allows automated testing of web applications across various browsers and platforms. It provides a suite of tools for automating web browsers, including a browser automation framework, a WebDriver API, and a language-specific client library. With Selenium, developers and testers can write scripts to simulate user interactions with a website, such as clicking buttons, filling out forms, and navigating through pages. Selenium supports multiple programming languages, including Java, Python, and JavaScript, making it easy to integrate with existing testing frameworks. It is widely used in the industry for testing web applications, ensuring they work as expected across different browsers and operating systems. Additionally, Selenium is highly extensible, enabling developers to create custom plugins and integrations to extend its capabilities.</p>
      <br/>
      <h3>Business Context</h3>
      <p>The Selenium Project is formed by a community of users and open source contributors who develop, use and promote the different Selenium projects (IDE, Grid, WebDriver) and other related things, with the end goal of benefiting the community as a whole. The Selenium Project wants as much as possible to operate using procedures that are fair, open, inviting, and ultimately good for the community. Selenium is primarily used for but not limited to automated testing of web applications. It helps developers and testers quickly identify and fix issues with applications, ensuring that they work as expected across different browsers (Firefox, Microsoft Edge, Chrome, etc)  and platforms. </p>
      <br/>
      <h3>Key Quality Concerns</h3>
      <ol>
        <li><b>Test Stability:</b> Selenium tests must be reliable and consistent, producing the same results each time they are run.</li>
        <li><b>Test Coverage:</b> Selenium tests should cover all essential features and functionalities of the application under test.</li>
        <li><b>Test Maintainability:</b> Selenium tests should be easy to maintain, update, and modify when the application changes.</li>
        <li><b>Test Performance:</b> Selenium tests must be efficient and not overly burden the system, as this can cause false test results.</li>
        <li><b>Test Scalability:</b> Selenium tests should be able to handle a large number of test cases and execute them quickly.</li>
      </ol>
    </td>
  </tr>
  <!-- END: TOPIC#2: SELENIUM -->
  
   <!-- START: TOPIC#3: GGPO (GOOD GAME, PEACE OUT) -->
  <tr>
    <td>3</td>
    <td><h2>GGPO (Good Game, Peace Out)</h2></td>
    <td>
      <h3>Description</h3>
      <p>A middleware designed to help create a near-lagless online experience for various emulated arcade games and fighting games.

Rollback networking uses input prediction and speculative execution to send player inputs to the game immediately, providing the illusion of a zero-latency network. Using rollback, the same timings, reactions, visual and audio queues, and muscle memory your players build up playing offline will translate directly online. The GGPO networking SDK is designed to make incorporating rollback networking into new and existing games as easy as possible.
</p>
      <br/>
      <h3>Business Context</h3>
      <p>Relevant in multiplayer networking in the Video Game industry (Peer-to-Peer Network specifically).

Problem: Traditional techniques account for network transmission time by adding delay to a player's input, resulting in a sluggish, laggy game-feel.

Created in 2009, the GGPO networking SDK pioneered the use of rollback networking in peer-to-peer games. It's designed specifically to hide network latency in fast paced, twitch style games which require very precise inputs and frame perfect execution. GGPO is written in C, C++, and CMake.
</p>
      <br/>
      <h3>Key Quality Concerns</h3>
      <ol>
        <li><b>
Performance: </b> GGPO takes into consideration 2 or more players’ connection to the network. If the connection difference exceeds a certain threshold then even GGPO will be unable to solve the frame delays. 
E.g. Player A has 70ms, Player B has 900ms (very high ms causing noticeable lag); Player A will see Player B teleporting around.
</li>
        <li><b>Scalability:</b> GGPO only works in Peer-To-Peer network based games, therefore it cannot work with large multiplayer games.</li>
        <li><b>Bandwidth:</b> GGPO relies on a constant stream of input data from both players in order to accurately predict and roll back the game state. This means that games using GGPO may require more bandwidth than other online games. Developers will need to consider whether players with lower bandwidth connections will be able to effectively use GGPO without experiencing lag or other issues.
        </li>
        <li><b>Network Stability:</b> Because GGPO relies on a constant stream of input data from both players, any disruptions to the network connection can cause issues with the game’s synchronization. This means that network stability is particularly important when using GGPO, and developers will need to consider how to handle network disruptions and ensure that the game remains playable in the face of connection issues. </li>
      </ol>
    </td>
  </tr>
  <!-- END: TOPIC#3: GGPO (GOOD GAME, PEACE OUT) -->

</table>
