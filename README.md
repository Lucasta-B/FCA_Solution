# FCA - DevOps Program


**Reference Implementations (Model Answers)**

- [Project 1 - Python, Flask, MYSQL](project1-python-flask/README.md)
- [Project 2 - jenkins-docker](project2-jenkins-docker/README.md)
- [Project 3 - SpringBoot MicroService](project3-springboot/README.md)
- [Project 4 - Jenkins CI/CD](project4-cicd-pipeline/README.md)
- [Project 5 - AWS Design and Deploy](project5-aws-design-deploy/README.md)

---

## Introduction
The program revolves around a case study of developing Automation that will be deployed to AWS.  The program consists of three dedicated project lab stages that mimic a DevOps life cycle from Application Development, CI/CD and Deploying to the Cloud.

![](./docs/images/project-plan.png)
<figcaption><b>Fig.1 - Project Plan</b></figcaption>

---

**Project 0**
This is equivalent of the set-up sprint and will be part of the GIT exercises by setting up a GIT repository that will be used by rest of the projects for source and version management.

**Project 1**
Project 1 involves building an automation process for archive files that can be controlled by REST API using Flask, Python and MYSQL that can be invoked from a remote machine.

**Project 2**
This consist of building and dockerising the Python application from project 1

**Project 3**
Design AWS infrastructure for the deployment of Project 1 Python Application to AWS that can  access from the WEB. 

---

## Case Study - Remote Backup Automation
The project will be based on the creation of a manual backup auditing and reporting system with the following features:


### FEATURE: RUN BACKUP
>**Scenario: Required Folder Exists**  
Given the specified folder exists  
Given the flask automation application is up and running  
When the backup/{folder_name} command is sent to the relevant flask http endpoint  
Then the folder is copied into the user backup folder on the remote machine  
And an ‘Action: Backup’ record with a status of “SUCCESS” is stored in the DB  

>**Scenario: Required Folder does not Exist**
Given the specified folder does not exist  
When backup for the specified folder command is invoked  
Then an error status is returned with an “No such directory” error message

### FEATURE: DISPLAY LOGS
>**Scenario: user request logs with no criteria**   
When {get_logs} command is invoked  
Then message displayed to user that logs have been cleared  
And record with clear data displayed to user  

Scenario: user request most Recent Reset 
When {most_recent_reset} command invoked
Then top record of the table extracted and displayed

Scenario: user request logs for a date range
        Given a date range parameter is specified 
When {get_logs} command is invoked
Then all the records within the date range (inclusive start and end date) is returned 


FEATURE: DISPLAY STATISTICS
Scenario: User requests stats
When {get_stats} command is invoked
Then the total number of backups, successes and failures are returned


---

## Minimal Viable Product

- **Manage Seller**
    - Register a new seller
    - Display all sellers

- **Manage Properties**
    - Add properties
    - Display all properties
    - Find and display properties with given search criteria on price, bedrooms, bathroom and garden
    - Withdraw a property
    - Resubmit a property

- **Manage Buyer**
    - Register new buyer
    - Display all buyers
