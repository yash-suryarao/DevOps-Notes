## What is CICD
__CI/CD__ stands for __Continuous Integration and Continuous Delivery/Deployment.__ It's a software development practice that automates the software release lifecycle to streamline and speed up the process. CI/CD is a key part of DevOps methodology, which aims to improve collaboration between development and operations teams. 

## Continious Integration
Continious integration is software development process in CICD pipeline where the members/developers are going to integrate their work or push their code on central repository systems where their code or their work going to be checked automatically (Tested).
<br><br>
[Continious Integration is a process in CI/CD pipeline where the developes are going to integrate/push their code on the center repository systems (GitHub) where their code is going to be checked automatically tested out.]
<br>

__Build__ ➡️(Auto)➡️ __Unit Tests__ ➡️(Auto)➡️ __Deploy to stage__ ➡️(Auto)➡️ __Acceptance Tests__

<img src="https://www.devopsschool.com/blog/wp-content/uploads/2020/05/CI-Process.png">


## Continious Delivery
Continious delivery is a software development practice where we compile the code that got from the repository and then create the build, test it out and be readily to deployed. Continious delivery is that the process of making sure the software is ready and it can be released anytime you want.

<img src="https://d274cmdd0goq94.cloudfront.net/wp-content/uploads/2020/12/qZ05Wx59htDXZgorhm29BWVT8KfUQDrwOIkX8tin.jpeg">


## Continious Deployment
Continuous Deployment is a software development process where code changes to an application are released automatically into the production environment.

![Continious-delivery](https://github.com/user-attachments/assets/56fab144-a448-4737-87db-8ffb4d87c62d)


## Stages in CICD pipeline

<img src="https://res.cloudinary.com/practicaldev/image/fetch/s--rZOYRHjZ--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_800/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/x2yeyhrxtk7d2c21mqcy.png">

__1. Source:__ Developers commit their code changes to a version control system like Git. Then the version control system triggers the pipeline when changes are detected in the repository to fo into next stage which is build stage. <br>

__2. Build:__ In build stage code is combined with dependencies and libraries to create a build or an artifacts that can be deployed in deployment platform. <br>

__3. Test:__ In test stage there are going to be automated tests to test your applications code and to check if it behaves correctly is there any issues to applications you can find them and in your test stage and also resolve them, once test stage is done it is going to move to the next stage which is deploy stage. <br>

__4. Deploy:__ Finally in the deploy stage application goes live because in this application will be deployed on the server after it has passes all the tests. <br>

[Reference Link for Stages in CICD](https://codefresh.io/learn/ci-cd-pipelines/ci-cd-process-flow-stages-and-critical-best-practices/#:~:text=The%20CI%2FCD%20pipeline%20combines,build%2C%20test%2C%20and%20deploy.)
  
## Benefits of using CICD

__1. Faster time to market:__ It shorter production cycles and allow teams to deliver more value in less time.<br>

[Using CICD we can automate the process, reduce manual intervention which allows us to deploy application faster and brings releases quicker.]  <br>

__2. Higher Software Quality:__ Automated testing in CICD can help us find bugs and issues early in the development process. <br>

__3. Reduce Risks:__ Automated tests can help reduce the chances of software bugs, which can make developers more confident in their code. <br>

__4. Collaboration:__ CI/CD can help align developers, operations teams, and other takeholders, which can lead to faster issue resolution and a more efficient software development process. <br>

__5. Improve Customer Satisfaction:__ Improved customer satisfaction: Faster release cycles, small updates, and better fault isolation can lead to a more positive customer experience.




