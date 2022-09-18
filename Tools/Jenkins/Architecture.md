# Jenkins Architecture

![Jenkins architecture](https://www.jenkins.io/images/developer/architecture/jenkins-dataflow.png)

- Follows Master-Slave Architecture
- Developers commit changes to the source code, found in the repository.
- The Jenkins CI server checks the repository at regular intervals and pulls any newly available code.
- The Build Server builds the code into an executable file. In case the build fails, feedback is sent to the developers.
- Jenkins deploys the build application to the test server. If the test fails, the developers are alerted.
- If the code is error-free, the tested application is deployed on the production server.


### Jenkins Master-Slave Architecture
![Jenkins Master-Slave Architecture](https://www.simplilearn.com/ice9/free_resources_article_thumb/jenkins-master-slave-architecture.jpg)



References:
- https://www.jenkins.io/doc/developer/architecture/
- https://www.simplilearn.com/tutorials/jenkins-tutorial/what-is-jenkins#development_before_jenkins
- 