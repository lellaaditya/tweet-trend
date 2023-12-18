# Trend application

This is a small application that contains main and test folders.  
The Main contains the application code.  
The test contains test cases.  
It also contains pom.xml which has all dependencies and artifact name and version


# Tech Stack

# GitHub

# Jenkins
 Install Jenkins
  
  https://www.jenkins.io/doc/book/installing/linux/#debianubuntu
  
  https://pkg.jenkins.io/debian-stable/

  Steps to Install Jenkins

  ```
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
    https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
```

```
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
    https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
    /etc/apt/sources.list.d/jenkins.list > /dev/null
  ```

  ```
sudo apt-get update
```

```
sudo apt-get install fontconfig openjdk-17-jre
 ```
 
 ```
 sudo apt-get install jenkins
```

```
sudo systemctl enable jenkins
```

```
sudo systemctl start jenkins
```

```
sudo systemctl status jenkins
```

  Integrate GitHub with Jenkins

  Admin Password
  
  ```
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```
  
  Cred --> GitHub Username and Personal Access Token 
---
  Install maven

  https://maven.apache.org/download.cgi
  
  apache-maven-3.9.6-bin.tar.gz

  https://linuxhint.com/install_apache_maven_ubuntu/

  `
  --- NOTE:: Check Latest Maven Version ---
  `
  
Step 1: Install Java
First of all, make sure that Java is installed on your Ubuntu 22.04; if you do not have it, then utilize the given command for its installation:

```
sudo apt install default-jdk -y
```

Step 2: Download Apache Maven latest version
Next, write-out the below-given “wget” command for downloading the latest version of Apache Maven from the official website:

```
wget https://downloads.apache.org/maven/maven-3/3.9.6/binaries/apache-maven-3.9.6-bin.tar.gz -P /tmp
```

Step 3: Extract downloaded Apache Maven package
Now, move to the “/tmp” directory with the help of the “cd” command

```
cd /tmp
```

```
tar -xvzf apache-maven-3.9.6-bin.tar.gz
```

extracting the required package, copy it to the “/opt/” directory:

```
sudo cp -r apache-maven-3.9.6 /opt/maven
```

Step 4: Set up environment variables
In the next step, we will set up the environment variables by creating a maven script file “maven.sh” inside the “/etc.profile.d” directory:

```
sudo vim /etc/profile.d/maven.sh
```

In the opened “maven.sh” file, paste the follow code and press “CTRL+O” to save it:

```
export JAVA_HOME=/usr/lib/jvm/default-java
export M2_HOME=/opt/maven
export MAVEN_HOME=/opt/maven
export PATH=${M2_HOME}/bin:${PATH}
```

enabling the executable permission of the created Apache Maven script:
```
sudo chmod +x /etc/profile.d/maven.sh
```

load the environment variables with the help of the following “source” command:

```
source /etc/profile.d/maven.sh
```
Step 5: Check Apache Maven version

Lastly, verify the version of Apache Maven which you have installed on your Ubuntu 22.04:

```
mvn -version
```

GitHub Web Hook
```
https://www.blazemeter.com/blog/how-to-integrate-your-github-repository-to-your-jenkins-project
```

# GCP 
   GCP Instance

   Create VM and attach the below firewall
   
 
 Firewall

  <img width="715" alt="image" src="https://github.com/lellaaditya/tweet-trend/assets/139613275/219d845d-37fc-4d91-ad93-966cfb6b1187">


  
# SonarQube

Build Tool --> Maven Ant

```
https://github.com/ravdy/devops-workshop/tree/main/lab-docs
```

# JFrog

