FROM jenkins/jenkins:lts-jdk11
# sonar:2.13.1 dependency-check-jenkins-plugin:5.1.1
RUN jenkins-plugin-cli --plugins pipeline-model-definition github-branch-source:1.8 maven-plugin

USER root
RUN apt-get update && apt-get install -y maven
USER jenkins

COPY settings.xml /var/jenkins_home/.m2