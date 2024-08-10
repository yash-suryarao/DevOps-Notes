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
<img width=800 height=250 src="https://user-images.githubusercontent.com/69889600/214857610-4fc3e64c-a262-4a6b-9e4d-b5b4eed057c6.png">

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


## What is jenkins pipeline?
Jenkins pipelines is a collection of plugins that supports implementing and integrating continious integration and delivery pipelines into jenkins. A pipeline automated steps or stages required to build, test and depliver applications. Jenkins pipeline written in Declaritive and Scripted syntax. <br>
Jenkins pipelines are written using a domain-specific language called groovy which allows you to define complex workflows and automate any task in your software development process.

A pipeline typically consists of multiple stages, each representing a distinct phase in the software delivery process. These __stages__ can include: 

__1. Checkout:__ This stage involves retrieving the latest version of the source code from the version control system (such as Git) to begin the pipeline process. <br>
__2. Build:__ In this stage, the source code is compiled and built into executable artifacts or packages. It involves tasks like compiling code, resolving dependencies, and generating build artifacts.<br>
__3. Test:__ The test stage executes various types of tests, including unit tests, integration tests, and other automated tests, to ensure the software functions correctly and meets the specified quality criteria.<br>
__4. Static Code Analysis:__ This stage involves analyzing the codebase for potential issues, code style violations, security vulnerabilities, and other code quality concerns. Static code analysis tools are used to perform this analysis.<br>
__5. Deployment:__ The deployment stage involves deploying the built artifacts to the desired environment, such as staging or production. It may include tasks like configuring servers, setting up databases, and deploying the application or infrastructure.<br>
__6. Release:__ This stage handles the final steps required to release the software, such as generating release notes, updating version numbers, and notifying stakeholders about the new release.

## Declarative VS Scripted pipeline Syntax
### Declarative pipeline: 
Declarative Pipeline syntax in Jenkins is a more structured and simplified way of defining pipelines than the scripted pipeline syntax. It's based on the Groovy programming language, but uses a Groovy-based Domain-Specific Language (DSL) for pipeline configuration.

For Example:

```markdown
 pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Build the application
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                // Run the tests
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                // Deploy the application
                sh 'deploy.sh'
            }
        }
    }
 }
```

### Scripted pipeline:
Scripted Jenkins pipeline syntax runs on the Jenkins master with the help of a lightweight executor, and it is based on Groovy scripting language. In Scripted Pipeline, the entire workflow is defined in a single file called a Jenkinsfile. The Jenkinsfile is written in Groovy and is executed by the Jenkins Pipeline plugin. Scripted Pipeline provides a lot of flexibility and control over the workflow, but it can be more complex and verbose than Declarative Pipeline.

For Example:
``` console
node {
    stage('Build') {
        // Build the application
        sh 'mvn clean install'
    }
    stage('Test') {
        // Run the tests
        sh 'mvn test'
    }
    stage('Deploy') {
        // Deploy the application
        sh 'deploy.sh'
    }
}
```

<table>
<tr>
  <th> Scripted Pipeline </th>
  <th> Declarative Pipeline </th>
</tr>
<tr>
  <td> Scripted pipeline is based on Groovy scrpiting language </td>
  <td> Declarative pipeline is also based on Groovy, but it used a more structured and predefined format. </td>
</tr>
<tr>
  <td> Provides more flexibility and control over the pipeline wotkflow </td>
  <td> Declarative pipeline provides a flexibility and more structured syntax </td>
</tr>
<tr>
  <td> Scripted pipeline allows for more gragular error handling and recovery mechanisms. </td>
  <td> Declarative pipeline a simpler error handling mechanism that is more intuitive and easier to understand. </td>
</tr>
<tr>
  <td> Scripted Pipeline allows for more code reuse and modularity. </td>
  <td> Declarative Pipeline is designed to be more self-contained and less reliant on external scripts and libraries. </td>
</tr>
<tr>
  <td> Scripted Pipeline can be more complex and verbose. </td>
  <td> While Declarative Pipeline is designed to be more readable and easier to understand. </td>
</tr>
</table>



## Pipeline concepts

* __Pipeline:-__ A pipeline is a user-defined block of Continious delivery pipeline, which contains all the processes such as build, test, deploy, etc. it is a group of all the stages in a JenkinsFile. All the stages and steps are defined in this block. It is used in declarative pipeline syntax.

Also, a __pipeline__ block is a key part of __Declarative Pipeline syntax.__

* __Node:-__ A node is a machine which is part of the Jenkins environment and is capable of executing a Pipeline.

Also, a __node__ block is a key part of __Scripted Pipeline syntax.__

* __Stage:-__ A __stage__ block defines a conceptually distinct subset of tasks performed through the entire Pipeline (e.g. "Build", "Test" and "Deploy" stages), which is used by many plugins to visualize or present Jenkins Pipeline status/progress.

* __Steps:-__ A single task. Fundamentally, a step tells Jenkins what to do at a particular point in time (or "step" in the process). For example, to execute the shell command make, use the sh step: sh 'make'. When a plugin extends the Pipeline DSL, [1] that typically means the plugin has implemented a new step.


## Whata are plugins?
In __Jenkins__ plugins are small, independent program that can enhance the functionality of jenkins automation server to meet the need of specific user or organizations. They are used to enhance and customize Jenkins to support build, test, and deployment scenarios. Jenkins has vast ecosystem of plugins that provides integration with different tools, technologies, and services.
