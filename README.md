- Jenkins Windows Automation

- url https://www.youtube.com/watch?v=JeXl60PbXXw

- Jenkins

```jenkins
docker run --name jenkins -w /var/jenkins_home -id -v jenkins:/var/jenkins_home -p 80:8080 -p 50000:50000 -v $(which docker):/usr/bin/docker -v /var/run/docker.sock:/var/run/docker.sock --restart unless-stopped jenkins/jenkins:lts
```

- jar as a service in windows

- https://github.com/winsw/winsw

- download this ---> WinSW.NET4.exe & sample-minimal.xml from releases

- jenkins connection
```connection
java -jar agent.jar -jnlpUrl http://172.31.88.230/computer/windows/jenkins-agent.jnlp -secret 3004fbe1e0882bb719c29959d6b20e11ad2d5d32b7edf0a0350f5799989813a2 -workDir ""
```

- command to run this as a service
WinSW.NET4.exe install

- windows delete a service
```delete
SC DELETE jenkins
```