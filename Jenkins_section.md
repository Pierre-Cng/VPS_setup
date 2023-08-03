# Jenkins section:

## Set up Jenkins on a VPS:

Reference [here](https://www.jenkins.io/doc/book/installing/linux/#debianubuntu)  

### 1. Install Java:

Jenkins requires Java to run. Check if Java is installed with the command:  
`java -version`  
To install OpenJDK:  
`sudo apt update`  
`sudo apt install openjdk-17-jre`  
[See also](https://itslinuxfoss.com/install-java-debian-12-linux/#:~:text=Method%201%3A%20Using%20the%20Repository%20Package%201%20Step,...%204%20Step%204%3A%20Verify%20the%20Installation%20)  

### 2. Download and Install Jenkins:

Add the Jenkins repository to your system:  
`wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -`    
`sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'`  
Install Jenkins:  
`sudo apt update`  
`sudo apt install jenkins`  

### 3. Start Jenkins and Enable on Boot:

Start and enable Jenkins service:  
`sudo systemctl start jenkins`  
`sudo systemctl enable jenkins`  

### 4. Allow Jenkins service to pass firewall:

If UFW is used, to authorize Jenkins service, enter the command:  
`sudo ufw allow 8080`  
[See also](https://www.digitalocean.com/community/tutorials/how-to-install-jenkins-on-ubuntu-22-04#step-3-opening-the-firewall)  

### 5. Access Jenkins Web Interface:

Access the Jenkins web interface using the VPS's public IP address or domain name followed by port 8080. Open a web browser and enter the following URL:  
`http://your_vps_ip_or_domain:8080`  
During the initial setup, Jenkins will ask for an administrator password. The password is in the following file:  
`sudo cat /var/lib/jenkins/secrets/initialAdminPassword`  
Follow the instructions on the web interface to complete the installation and set up your Jenkins admin account.  

### 6. Configure Jenkins Security (Optional):

After the initial setup, it's essential to configure Jenkins security to protect your instance. You can enable security by installing the "Security Realm" and "Authorization Strategy" plugins, and then configuring them to suit your needs.  

### 7. Install Required Plugins:

Jenkins functionality can be extended through various plugins. Depending on the project needs, additional plugins from the Jenkins web interface can be installed.

### 8. Create Jenkins Jobs:

With Jenkins set up, Jenkins jobs can now be created to automate build, test, and deployment processes. Jenkins jobs are essentially tasks or projects that Jenkins can execute.  
Regularly update Jenkins and its plugins to keep the instance secure and up-to-date.

## Reference / tutorial:

<https://www.youtube.com/watch?v=f4idgaq2VqA>
<https://code.tutsplus.com/continuous-integration-workflow--CRS-200423c/jenkins-overview>
