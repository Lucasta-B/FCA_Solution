**&larr; [Back to Program README](../README.md)**
# Project 1 : Python, Flask, MySQL

<!-- TOC -->
* [Project 1 : Python, Flask, MySQL](#project-1--python-flask-mysql)
  * [Introduction](#introduction)
  * [API Design](#api-design)
  * [Tasks](#tasks)
  * [Minimal Viable Product](#minimal-viable-product)
<!-- TOC -->

## Introduction
Project 1 consist of building a Remote backup automation that can be invoked remotely using http.  The high level architecture is shown in figure 1 below.

![](./docs/images/project1.png)
<figcaption><b>Fig.1 - Project 1</b></figcaption>

A single table for recording logs is describe in figure 2 below:

![](./docs/images/db.png)  
<figcaption><b>Fig.2 - DB</b></figcaption>


## API Design
See [API Design](./docs/api.md)

## Tasks

The following lists the technical tasks required for Project 1.

>**Technical Tasks**
> Install docker
> Install mysql as docker image
> Create SQL schema

The following features is applicable to project 1 as outlined [program README](../README md/#case-study---remote-backup-automation)

This feature requires taking a command form a FLASK endpoint and executing the necessary logic in Python.
Each action will be recorded in the DB. 

- [RUN BACKUP](../README.md/#feature-run-backup)

![](./docs/images/execute-backup.png)  
<figcaption><b>Fig.3 - Backup Sequence</b></figcaption>

- [DISPLAY LOGS](../README.md/#feature-display-logs)
- [DISPLAY STATISTICS](../README.md/#feature-display-statistics)

These two features involves reading the actions table and returning the relevant result.  There is no logic to be performed with the Linux system 

![](./docs/images/get-logs.png)  
<figcaption><b>Fig.3 - Stats and Logs Sequence</b></figcaption>

## Minimal Viable Product
- **Remote backup**
  - Able to invoke remote backup from CURL

- **Display Logs**
  - ABle to display all logs
