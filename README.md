# Artifact Repository Manager with Nexus and Gradle

This project uses a premade application to showcase how to manage artifacts with a locally deployed instance of Nexus and an application using Gradle package manager.

## Purpose and Tasks

Apply DevOps Skills to properly manage artifacts with Nexus.

## Requirements

Ensure that Java 17 and Gradle 8.11 are installed on the remote server.
These are the versions I used to successfully configure and run this application without error. 
Using other versions may result in an incopatability between versions, resulting in a failure to build and deploy the application.

## Build and copy file to remote

```gradle
gradle build
```

```bash
scp <local jar file> <remote server>
```

## Start Application

```java
java -jar <.jar file>
```

Adding "&"  to the command will run the application in the background

## Stop or Kill application

[ctrl + c] will stop the application, but if you decided to run the application in the background with "&", there are some extra steps.

Locate only running java apps
```bash
ps aux | grep java
```

Take the PID column of the running application(process)
```bash
kill <pid of your app>
```
