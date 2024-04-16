## Jenkins Sample Job
### Stages
1. Git Checkout
2. J-Unit test cases
3. Buid Stage
4. Code Analysis
5. Upload to artifact Manager
6. Deploy to Destination host/server

### Installation
#### JAVA
```
sudo apt-get update -y
sudo apt-get install openjdk-11-jdk-headless
vi ~/.bash_profile
   JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64/
   PATH=$PATH:$JAVA_HOME/bin
source ~/.bash_profile
java --version
```
#### Jenkins
```
Install in EC2 Ubuntu Server
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
sudo systemctl enable jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins
```
#### Maven
```
vi ~/.bash_profile
   M2_HOME=/opt/maven/maven
   PATH=$PATH:$JAVA_HOME/bin:$M2_HOME/bin
source ~/.bash_profile
# downloading maven version 3.9.1
wget [https://mirrors.estointernet.in/apache/maven/maven-3/3.9.1/binaries/apache-maven-3.6.3-bin.tar.gz](https://dlcdn.apache.org/maven/maven-3/3.9.1/binaries/apache-maven-3.9.1-bin.tar.gz)
tar -xvzf apache-maven-3.9.1-bin.tar.gz
mv apache-maven-3.9.1 /opt/maven
mvn –version
```
#### SonarQube
```
ref:
https://github.com/CHERUKURIPRAVEEN/sonarqube/blob/master/Installation.md
```
#### 
