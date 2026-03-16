# jenkins-setup-aws-ec2
Deploying Jenkins CI/CD server on AWS EC2 instance
## Project Overview
This project demonstrates how to deploy Jenkins on an AWS EC2 instance to create a CI/CD automation server.

## Technologies Used
- AWS EC2
- Jenkins
- Linux (Ubuntu) WSL
- Java

## Steps Performed

1. Launch an Amazon EC2 instance in in AWS
2. Connected the EC2 instance to server using SSH
3. update the server
4. Install Java
5. Intalled jenkins(weekly)
6. Starting the jenkins device
7. checking the status of jenkins
8. Opened port 8080 in the security group (default port to jenkins is 8080)
9. Get the jenkins admin password
10. Accessed Jenkins through the public IP

## Commands Used

Update system
sudo apt update

Install Java
sudo apt install openjdk-17-jdk -y

Install Jenkins
wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
sudo apt install jenkins -y

Start Jenkins
sudo systemctl start jenkins

Check status
sudo systemctl status jenkins

Accessing jenkins in the browser
http://EC2-public-IP:8080

Get Jenkins admin password
sudo cat /var/lib/jenkins/secrets/initialadminpassword

## Output
Jenkins successfully running on:

http://EC2-PUBLIC-IP:8080
