<h3> 1. What is DevOps? </h3>
=> DevOps is a software development practice that aims to improve collaboration between devlopers and operations teams. The goal is to deliver software faster and more reliavle.

<h3> 2. What does DevOps engineers actually do? </h3>
=> DevOps simplify software development and deployment by automating tasks through different practices like, <br>
  - CICD using <b>GitLab</b> and <b>GitHub.</b> <br>
  - Creating and managng infrastructure programmatically using <b>Terraform</b> or <b>Ansible.</b> <br>
  - Monitoring systems or applications through <b>Prometheus</b> or <b>Grfana.</b> <br>
  - Hosting applications on <b>Cloud</b> or <b>On-premise.</b> <br>
And many other practices that ensures reliablity, security, and performance of your software applications. <br>
<br>
In Short the role of DevOps engineers is to deploy, troubleshoot, and make sure your applications or system are up and working.

<h3> 3. Benefits of DevOps? </h3>
<br><b> 1. increase productivity:</b>
<br><b> 2. Faster delivery:</b>
<br><b> 3. Better collaboration:</b>
<br><b> 4. Greater automation:</b> DevOps teams can use automation to speed up tasks like testing, code deployment, and incident management.
<br><b> 5. Easier maintenance:</b> DevOps can make it easier to maintain exixting deployment.
<br><b> 6. Decreases load:</b> 
<br><b> 7. Improved quality:</b> DevOps can help increase reliability and quality.

<h3> 4. DevOps Lifecycle: </h3>
<div>
  <img width=500 height=300 alt="DevOps lifecycle" src="https://miro.medium.com/v2/resize:fit:1024/0*u6zi1ux8N6qDQTha.png">
</div>
=> DevOps Lifecycle is a methodology software development teams use to bring products to market more quickly and efficiently. It's a way of managing the entire software lifecycle from development through release, focusing on collaboration between developers and IT operations professionals. Constant software creation, development, verification, release, and management are part of the DevOps lifecycle.

<br> **1. Plan:** Professional determine the commercial need and gather end-user opinions through this 
<br> **2. Code:** Developers will write code in accordance with the specifications outlined in the planning phase and will ensure that the code is created with the project’s operations in mind. DevOps tools and extexnsion like Git that assist them in preventing safety problems and bad coding standards.
<br> **3. Build:** After programmers have completed their tasks, they use tools suc as Maven and Gradle to submit the code to the common code source.
<br> **4. Test:** To assure software integrity, the product is first delivered to the test platform to execute various sorts of screening such as user acceptability testing, safety testing, integration checking, speed testing, and so on, utilizing tools such as JUnit, Selenium, etc. 
<br> **5. Release:** At this point, the build is prepared to be deployed in the operational environment. The DevOps department prepares updates or sends several versions to production when the build satisfies all checks based on the organizational demands.
<br> **6. Deploy:** At this point, Infrastructure-as-Code assists in creating the operational infrastructure and subsequently publishes the build using various DevOps lifecycle tools.
<br> **7. Operate:** This version is now convenient for users to utilize. With tools including Chef, the management department take care of server configuration and deployment at this point.
<br> **8. Monitor:** The DevOps workflow is observed at this level depending on data gathered from consumer behavior, application efficiency, and other sources. The ability to observe the complete surroundings aids teams in identifying bottlenecks affecting the production and operations teams' performance times
<br>

<h3> 5. DevOps Phases: </h3>
<div>
<img width=500 height=300 src="https://www.simform.com/wp-content/uploads/2022/01/devops-lifecycle-phases.png">
</div>

<br>**1. Continious Development (Planning & Coding):** This phase involves the planning and coding of the software. The vision of the project is decided during the planning phase. And the developers begin developing the code for the application. There are no DevOps tools that are required for planning, but there are several tools for maintaining the code.
<br>**2. Continious Integration:** Continuous integration is the most important stage of the DevOps lifecycle. At this phase, updated code or new functionality and features are developed and incorporated into the existing code. In addition, defects are spotted and recognized in the code at each level of unit testing during this phase, and the source code is updated accordingly. This stage transforms integration into a continuous process in which code is tested before each commit. In addition, the necessary tests are planned during this period.
<br>**3. Continious Testing:** 
<br>**4. Continious Deployment:**
<br>**5. Continious Feedback:**
<br>**6. Continious Monitoring:**
<br>**7. Continious Operations:**


<h4> Q) difference between monolithic architecture and microlithic architecture? </h4>
=>
<b>Monolithic Architecture:-</b>
Monolitic arcitecture is a traditional approach to designing software where an entire application is built as one large system and is usually one code-base. In this architecture, all the different components of the application, such as the user interface, business logic, and data access layer, are tightly integrated and deployed together. It extremely difficult to change technology or language or framework because everything is tightly coupled and depend on each other.
<br>
<b>Microlithic/Microservices Architecture:-</b>
Microservices architecture is built as small independent module based on business functionality. In microservices application, each project and services are independent from each other at the code level. Therefore it is easy to  configure and deploy completely and also easy to scale based on demand. <br>
- Each service is responsible for a single functionality or feature of the application and can be developed, deployed, and scaled independently. <br>
- The Microservice architecture has a significant impact on the relationship between the application and the database. <br>
- Instead of sharing a single database with other microservices, each microservice has its own database. It often results in duplication of some data, but having a database per microservice is essential if you want to benefit from this architecture, as it ensures loose coupling.

<table>
  <tr>
    <th>Sr. No.</th>
    <th>Key</th>
    <th>Monolithic architecture</th>
    <th>Microservices architecture</th>
  </tr>
  <tr>
    <td> 1 </td>
    <td> Basic </td>
    <td> Monolithic architecture is built as one large system and is usually one code-base </td>
    <td> Microservices architecture is built as small independent module based on business functionality </td>
  </tr>
  <tr>
    <td> 2 </td>
    <td> Scale </td>
    <td> It is not easy to scale based on demand </td>
    <td> It is easy to scale based on demand. </td>
  </tr>
  <tr>
    <td> 3 </td>
    <td> Database </td>
    <td> It has shared databse </td>
    <td> Each project/layer and module has their own database </td>
  </tr>
  <tr>
    <td> 4 </td>
    <td> Deployment </td>
    <td> Large code base makes IDE skiw and build time gets increase </td>
    <td> Each project is independent and small in size. So overall build and development time gets decrease. </td>
  </tr>
  <tr>
    <td> 5 </td>
    <td> Tightly Coupled and Loosely coupled </td>
    <td> It extremely difficult to change technology or language or framework because everything is tightly coupled and depend on each other </td>
    <td> Easy to change technology or framework because every module and project is independent </td>
  </tr>
</table>