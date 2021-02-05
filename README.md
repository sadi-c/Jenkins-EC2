# Jenkins-EC2
How to set up Jenkins on AWS EC2 step by step 


> 1. Launch a EC2 on a public subnet and make sure that you have a SSH rule for yourself and also open up port 8080 on the server so that you can access Jenkins from the web.

<br>
<img src= "Imgs/sg.png">

> 2. SSH into your EC2 machine 

<br>
<img src= "Imgs/ssh.png">

> 3. Once you ssh into your EC2 machine, run the following commands:
* sudo yum update –y (This command updates the Linux operating system)
* sudo yum install java-1.8.0-openjdk-devel -y (This command installs the JAVA JDK which is use by Jenkins)
* sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat/jenkins.repo (This command pulls Jenkins repo to our machine)
* sudo rpm --import https://pkg.jenkins.io/redhat/jenkins.io.key (This command imports a key file from Jenkins-CI to enable installation from the package)
*  sudo yum install jenkins -y (installing jenkins)
* sudo systemctl start jenkins (starting jenkins service)
* sudo systemctl enable jenkins (enabling the jenkins service across server restarts)
* sudo systemctl status jenkins (ensuring jenkins service is up and running)


