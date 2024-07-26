<!-- <img width=250 height=80 src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e3/Jenkins_logo_with_title.svg/2560px-Jenkins_logo_with_title.svg.png"> -->

## What is [Jenkins](https://medium.com/cloud-native-daily/jenkins-tutorial-basics-to-advanced-for-devops-engineer-27265e5ae67d)?
Jenkins is a open-source automation server written in __JAVA__ that facilitates __Continious Integration and Continious Deployment/Delivery(CI/CD)__ in software development. It automates the parts of software development related to building, testing, and deploying, allowing developers to focus on writing code and improving their applications. <br>

## Why Jenkins
Jenkins is used to build and test your software projects continuously make it easier for developers to integrate changes to the project, and make it easier for users to obtain a fresh build. It provides many plugins that help to support building, deploying and automating any project.

## Key Features of Jenkins
__1. Continious Integration and Continious Delivery (DI/CD):__ Jenkins automates the process of integrating code changes from multiple contributors into a shared repository several times a day (CI). It also automates the delivery of code changes to production environments (CD). <br>
__2. Extensible With Plugins:__ Jenkins has a rich ecosystem of plugins that allow it to integrate with various tools and platforms, such as Git, Maven, Gradle, Docker, Kubernetes, and more. Plugins extend Jenkins’ capabilities and enable custom workflows. <br>
__3. Distributed Builds:__ Jenkins can easily distribute work across multiple machines, elping in faster builds, test and deployments across multiple platforms. <br>
__4. Pipeline as Code:__ Jenkins uses a feature called Jenkins Pipeline, which allows developers to define their build, test, and deployment processes as code. This is usually done using a domain-specific language (DSL) based on Groovy. <br>
__5. Extensive Customization:__ Jenkins allows for extensive customization through its flexible configuration options and its support for scripting and custom plugins. <br>

## Why we used Jenkins?
__1. Continious Integration (CI):__ Jenkins facilitates continuous integration by automatically building and testing software whenever changes are made to the codebase. It helps identify issues and conflicts early in the development process, leading to faster feedback and easier bug resolution.
__2. Automated Testing:__ Jenkins allows the integration of automated testing frameworks into the build process. It can execute unit tests, integration tests, and other types of tests to ensure that the software functions as expected and meets the defined quality criteria.
__3. Continious Delivery/Deployment (CD):__ Jenkins enables continuous delivery and deployment by automating the steps involved in packaging, deploying, and releasing software. It streamlines the release process, reduces human error, and allows for frequent and reliable software deployments.
__4. Build and Release Management:__ Jenkins provides a centralized platform for managing build configurations, artifacts, and release versions. It tracks changes, manages dependencies, and ensures consistency across different builds and environments.
__5. Scalability and Flexibility:__ Jenkins is highly scalable and can support projects of various sizes and complexities. It can handle multiple builds concurrently and distribute work across multiple nodes for faster execution. Jenkins also offers extensive plugin support, allowing integration with a wide range of tools and technologies.
__6. Open Source and Cost-Effective:__  Jenkins is an open-source tool, it is freely available for use and can be customized as per project requirements. This makes it a cost-effective choice compared to commercial alternatives.


## Jenkins Workflow
<img src="https://user-images.githubusercontent.com/69889600/214857610-4fc3e64c-a262-4a6b-9e4d-b5b4eed057c6.png">

## How Jenkins Works
__1. Source Code Integration:__ Jenkins integrates with source control systems (Git) to pull code changes. <br>
__2. Build Automation:__ Jenkins triggers build processes using tools like Maven, Gradle, or Ant. The build scripts compile the code, resolve dependencies, and package the application. <br>
__3. Testing:__ Jenkins runs automated tests (unit tests, integration tests) to ensure the code changes do not break existing functionality. It can use testing frameworks like JUnit, TestNG, or others. <br>
__4. Deployment:__ After successful builds and tests, Jenkins can deploy the application to different environments (development, staging, production) using deployment tools and services. <br>
__5. Notification and Reporting:__ Jenkins provides detailed logs and reports for each build and test. It can notify developers of build results via email, Slack, or other communication tools. <br>

## Benefits of Using Jenkins
__1. Increased Developer Productivity:__ <br>
__2. Scalability:__ <br>
__3. Flexibility:__ The wide range of plugins and customization options makes jenkins adaptable to various workflows and development environments. <br>
__4. Handles errors:__ Continious integration ensures that code changes are tested frequently, allowing to gracefully handle failures and errors, and resume or retry failed tasks. <br>
__3. Faster Release Cycles:__


## Jenkins Architecture
* Developers modify the source code, committing changes to the repository, and Jenkins creates a new build in order to handle the new Git commit.
* Jenkins can work in “push” or “pull” mode. The Jenkins CI server is either triggered by an event such as a code commit, or it can regularly check the repository for changes.
* The build server builds the code and generates an artifact. If the build fails, the developer receives an alert.
* Jenkins deploys the built application/executable to the test server, which can execute continuous, automated tests. Developers receive alerts if their changes impact functionality.
* Jenkins optionally deploys the changes to the production server if the code has no issues.

## Jenkins Master-Slave Architecture

<img src="https://www.simplilearn.com/ice9/free_resources_article_thumb/jenkins-master-slave-architecture.jpg">
Jenkins follows Master-slave architecture to manage distributed builds. In this arcitecture, slave and master communicate through TCP/IP protocol.


## What is pipeline?


## Whata are plugins?
In __Jenkins__ plugins are small, independent program that can enhance the functionality of jenkins automation server to meet the need of specific user or organizations. They are used to enhance and customize Jenkins to support build, test, and deployment scenarios. Jenkins has vast ecosystem of plugins that provides integration with different tools, technologies, and services.
