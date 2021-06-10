FROM jenkins/jenkins:lts-jdk11

RUN jenkins-plugin-cli --plugins maven-plugin sonar:2.13.1 dependency-check-jenkins-plugin:5.1.1

USER root
RUN apt-get update && apt-get install -y maven
USER jenkins
RUN mkdir -p /var/jenkins_home/.m2/
COPY ./settings.xml /var/jenkins_home/.m2/settings.xml