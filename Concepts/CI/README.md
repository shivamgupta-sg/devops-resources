# Continuous integration (CI)

- It is a DevOps software development practice where developers regularly merge their code changes into a central repository, after which automated builds and tests are run.
- Most often refers to the build or integration stage of the software release process and entails both an automation component (e.g. a CI or build service) and a cultural component (e.g. learning to integrate frequently).
- It refers to the build and unit testing stages of the software release process. Every revision that is committed triggers an automated build and test.

###Goals (Why Continuous Integration is needed?):
- Improves Deveploer Productivity
- To find and address bugs quicker
- Improve software quality
- Reduce the time it takes to validate and release new software updates (Deliver Updates Faster).

###How does Continuous Integration Work?
- Developers frequently commit to a shared repository using a version control system such as Git. 
- Prior to each commit, developers may choose to run local unit tests on their code as an extra verification layer before integrating with main code
- CI service automatically builds and runs unit tests on the new code changes to immediately surface any errors.

![Continuous Integration and Continuous Delivery](https://d1.awsstatic.com/product-marketing/DevOps/continuous_integration.4f4cddb8556e2b1a0ca0872ace4d5fe2f68bbc58.png)

- After CI we have CD stage i.e Continuous Delivery or Continuous Deployment

References:
- [What is Continuous Integration? - Amazon Web Services](https://aws.amazon.com/devops/continuous-integration/)