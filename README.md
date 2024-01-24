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



