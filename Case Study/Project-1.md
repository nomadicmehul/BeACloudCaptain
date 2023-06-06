You have been Hired Sr. DevOps Engineer in Abode Software. They want to implement DevOps Lifecycle in their company. You have been asked to implement this lifecycle as fast as possible.

ABC Software’s is a product-based company

Following are the specifications of the lifecycle:

1. Git Workflow has to be implemented
2. Code Build should automatically be triggered once commit is made to master branch or develop branch.
    a. If commit is made to master branch, test and push to prod
    b. If commit is made to develop branch, just test the product, do not push to prod
3. The Code should be containerized with the help of a Dockerfile. The Dockerfile should be built every time there is a push to Git-Hub. Use the following pre-built container for your application:
    a. The code should reside in '/var/www/html'
4. Once the website is built, you have to design a test-case, which will basically check if the website can be opened or not. If yes, the test should pass. This test has to run in headless mode, on the test server.
5. The above tasks should be defined in a Jenkins Pipeline, with the following Jobs Job 1
- Building Website
    a. Job 2 - Testing Website
    b. Job 3 - Push to Production
6. Since you are setting up the server for the first time, ensure the following file exists on both Test and Prod server in /home/ubuntu/config- management/status.txt. This file will be used by a third-party tool. This should basically have the info whether apache is installed on the system or not.
    a. The content of this file should be based on whether git is installed or not.
    b. If apache is installed => Apache is Installed on this System"
    c. If apache is not installed => "Apache is not installed on this System"

7. Create a Monitoring Service for the website on the Production server Architectural Advice:
    a. Create 3 servers on AWS "t2.micro"
    b. Server 1 - should have Jenkins Master, Puppet Master and Nagios Installed
    c. Server 2 - Testing Server, Jenkins Slave
    d. Server 3 - Prod Server, Jenkins Slave
