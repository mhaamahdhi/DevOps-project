
![Screenshot_6](https://github.com/mhaamahdhi/DevOps-project/assets/12277830/5b1dea4f-4c0b-456e-9d83-5d780e71eacc)

We need 3 EC2 instances for the pipeline
  Jenkins
  SonarQube
  Docker

after the creation of the EC2 instances we have to loggin into the jenkins instance to configure the jenkins server 
  sudo apt update

  install the java runtime which is required to jenkins installation
    sudo apt install openjdk-11-jre -y

 * now we are going to install the Jenkins. I have took the installation script from this link(ubuntu) ==> https://www.jenkins.io/doc/book/installing/linux/#debianubuntu

    curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins


* we have to allow the port 8080 in the ec2 instance inbound rule at the security rule
* we can check weather the jenkins installed or not
    systemctl status jenkins
* after the installation of the jenkins we ahve to go to the jenkins server to configure the pipeline for the ci/cd
* createdt he new item as freestyle project
* and then we have to setup the github with jenkins
*  
  
