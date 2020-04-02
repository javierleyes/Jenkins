# Install Jenkins on Docker step by step

#### You should have docker installed

Execute on powershell:

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

docker container exec -u 0 -it name bash
	wget http://updates.jenkins-ci.org/download/war/2.222.1/jenkins.war
	mv ./jenkins.war /usr/share/jenkins
	chown jenkins:jenkins /usr/share/jenkins/jenkins.war
	exit
	docker container restart jenkins