# Jenkins Installation
source
```
https://www.jenkins.io/doc/book/installing/linux/
```
####  Installation of openJDK
## Amazon Linux
```
sudo dnf update -y
sudo yum install java-17-amazon-corretto-devel -y

sudo dnf install fontconfig java-21-openjdk -y
``` 

####  Installation of Jenkins
```
sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat/jenkins.io-2023.key
sudo dnf upgrade
# Add required dependencies for the jenkins package
sudo dnf install jenkins -y
```
####  Start Jenkins
```
sudo systemctl daemon-reload
sudo systemctl enable jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins
``` 

