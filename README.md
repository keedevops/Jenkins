# Jenkins Installation on EC2 Instance
Create an Ubuntu EC2 Instance 

![Screenshot Capture - 2024-01-24 - 13-04-13](https://github.com/keedevops/Jenkins/assets/155215036/8d160fee-530a-46d3-877a-3372885df1ce)

Connect the instance through **EC2 instance connect**

![Screenshot Capture - 2024-01-24 - 13-07-44](https://github.com/keedevops/Jenkins/assets/155215036/d11bec73-fc2a-4315-816a-20abd913de83)

Update the package lists in the instance
```
sudo apt update -y
apt list --upgradable

```
Install the **Open Java Development** Kit with the specified version either java 8 or java 11
```
sudo apt install openjdk-8-jdk
sudo apt update (Update the java package)

```
Check the java version that you have installed with this command
```
java -version

```
To install the Jenkins follow this website **https://pkg.jenkins.io/debian/**
This is the Debian package repository of Jenkins to automate installation and upgrade. To use this repository, first add the key to your system
```
  sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
    https://pkg.jenkins.io/debian/jenkins.io-2023.key

  echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]     https://pkg.jenkins.io/debian binary/ | sudo tee     /etc/apt/sources.list.d/jenkins.list > /dev/null
```
  
Now update the system and start the jenkins service by following these commands
```
     sudo apt-get update
     sudo systemctl start jenkins
     sudo systemctl enable jenkins
     sudo systemctl status jenkins

```
Now that the service has started copy the public ip address of your instance and add 8080 port number when it throws an error check the security details whether the custom tcp has 8080 port number in it

![Screenshot Capture - 2024-01-24 - 13-21-22](https://github.com/keedevops/Jenkins/assets/155215036/d55f34d7-011a-408e-8ac5-2ec66cda1503)

When the port number is defined it should reflect this page
![Screenshot (9)](https://github.com/keedevops/Jenkins/assets/155215036/1b0ee072-21c5-4f6b-900c-30c962e3a62d)

To check the credentials in the CLI type this command
```
sudo cat /var/lib/jenkins/secrets/initialAdminPassword

```
Then the site is ready to download the necessary plugins for the jenkins and configure the user details 

![Screenshot (10)](https://github.com/keedevops/Jenkins/assets/155215036/65607f5e-2ac5-467b-b330-d4d06c64da00)
