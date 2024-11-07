# Capstone Project - Introduction to Cloud Computing

## This is an E-Commerce Platform Deployment with Git, Linux, and AWS:

### Project Instruction:
I will be developing an e-commerce website for a new online marketplace named "MarketPeak." The platform will feature product listings, a shopping cart, and user authentication. 
I will utilise Git for version control, develop the platform in a Linux environment, and deploy it on an AWS EC2 instance. 

### Tasks 1: Implement Version Control with Git

### 1.1. Git Repository Initialization:
I created a new directory "MarketPeak_Ecommerce" with the mkdir command and Initialise it to git repository using the git init command. 


```
mkdir MarketPeak_Ecommerce
cd MarketPeak_Ecommerce
git init

```
![alt text](<Images/1.1 Mkdir.png>)



### 1.2. Local Website Development:
The website template was downloaded from [Here](https://www.tooplate.com/view/2130-waso-strategy) 

![alt text](<Images/1.2 Tooplate.png>)

### 1.3. Git Commit:
I successfully add and commit the changes with the git add . and git commit commands.

```
git add .
```
![alt text](<Images/1.3 git commit.png>)


After which i configured the global Git settings with git config --global and all was committed.

```
git config --global user.name "YourUsername"
git config --global user.email "youremail@example.com"
git commit -m "Initial commit with basic e-commerce site structure"

```

Then i linked my Local Repository to GitHub using the remote repository URL

```
git remote add origin https://github.com/Saxangel/MarketPeak_Ecommerce.git
git push -u origin main
```


### 2.1. EC2 Instance Setup:
I successfully logged-in to the AWS Management Console and launched an EC2 instance with Amazon Linux 2023 AMI. 
![alt text](<Images/2.1 Launch EC2 instance.png>)


### 2.2. File Transfer to EC2 (5 points):
Successful transfer of website files to the EC2 instance by cloning the repository

### 2.3. Web Server Installation:
I  installed an Apache webserver on the EC2 instance.
```
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
```
![alt text](<Images/2.3 Install web server.png>)

### 2.4. Server Configuration:
The web server was configured to serve the website from transferred files. 
```
cat /home/ubuntu/.ssh/id_rsa.pub
```
![alt text](<Images/2.4Generate Keygen.png>)


### 2.5. Website Access:
The website was fully accessed via a web browser using the EC2 instance public IP and file name.
![alt text](<Images/2.5 Web access.png>)


### 3.1. Development Branch:
I created a new branch called "development" in other to make changes to the website using the "checkout command"

```
git branch development
git checkout development
```
![alt text](<Images/3.1 Dev branch.png>)

### 3.2. Continued Development:
Few implementation were added to the website index.html file (Text and Colour was changed).

![alt text](<Images/3.2 Colour 2.png>)

### 3.3. Branch Merge (5 points):
The changes was merged to the master and redeployed on AWS ec2

![alt text](<Images/3.3 Change Merge.png>)


### 4.1. Challenges:
I encountered series of challenges during this projects