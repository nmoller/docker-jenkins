# docker-jenkins
Jenkins slave to run docker

When trying to run a docker to run docker in jenkins, after trying you realise that 
you need java 1.8 (because the old one benhall/dind-jenkins-agent) uses 1.7 and the **fail message** is no clear about it.

This docker file offers basic fonctionnality. It is available in dockerhub as 

**nmolleruq/jenkins-docker-agent**

