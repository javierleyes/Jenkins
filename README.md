# Install Jenkins on Docker step by step

#### You should have docker installed

Run on powershell:

```
docker pull jenkins/jenkins
```

```
docker run --name JenkinsTest -p 8080:8080 -p 5000:5000 -v {your_local_path}:/var/jenkins_home jenkins
```

Example:

```
docker run --name JenkinsTest -p 8080:8080 -p 5000:5000 -v C:\Jenkins:/var/jenkins_home jenkins
```

Finish process from web browser

# Update Jenkins to the last version

Execute on other powershell tab:

Run commands in docker container

```
docker container exec -u 0 -it JenkinsTest bash
```

You should specify version of jenkins:

```
wget http://updates.jenkins-ci.org/download/war/2.222.1/jenkins.war
```

Install new version

```
mv ./jenkins.war /usr/share/jenkins
```

```
chown jenkins:jenkins /usr/share/jenkins/jenkins.war
```

```
exit
```

```
docker container restart jenkins
```

Done!