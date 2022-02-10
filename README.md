# Web Stack Implementation- LEMP
WEB STACK IMPLEMENTATION (LEMP STACK)

### What is LEMP STACK?
LEMP is a variation of the ubiquitous LAMP stack used for developing and deploying web applications. Traditionally, LAMP consists of Linux, Apache, MySQL, and PHP. Due to its modular nature, the components can easily be swapped out. With LEMP, Apache is replaced with the lightweight yet powerful Nginx.

* LEMP  stands for Linux, Nginx, MySQL, PHP or Python, or Perl.

**Linux**  
Linux is the operating system. It is popular in part because it offers more flexibility and configuration options than some other operating systems. Two of the most commonly used Linux distributions in LEMP stacks are Debian and Ubuntu.

**Nginx**  
Nginx is an open source reverse proxy server for HTTP, HTTPS, SMTP, POP3, and IMAP protocols. It also functions as a load balancer, HTTP cache, and web server (origin server). It has a strong focus on high concurrency, high performance and low memory usage. 

**MySQL**  
MySQL is an open source relational database management system for storing application data. It is also suitable for running even large and complex websites.

**PHP**  
PHP is the programming language.  It is an open source scripting language that works with Apache to help developers create dynamic web pages.

### Prerequisites

As the tittle indicates, this project will be deploy in the AWS Cloud platform.  An AWS account and a virtual server with Ubuntu Server OS must setup.
AWS is one the major Cloud Service Providers, and it provides a free virtual server called EC2 stands for Elastic Computer Cloud.  
These screenshots below will show the followings:

Create an AWS account

![](pics/aws.png)

![](pics/aws-console.png)

Search for EC2

![](pics/ec2.png)


Select the AMI: Ubuntu Server 20.25 LTS

![](pics/ec2-ami.png)

![](pics/ec2-type.png)

Select a key pair: No need to create a new key pair, use the existing key pair from Project 1. Remember, one key pair can be used for multiple EC2 instances.

![](pics/ec2-keypair-sel.png)

![](pics/ec2-summary.png)


Connect EC2 to your local machine
![](pics/GitBash.png)

![](pics/ec2-to-local-m.png)


### Installing Nginx Web Server

* The Nginx is a high performance web server which will help to display web pages. The use of apt package is crucial to install the Nginx web server. 

Execute the following commands to install Nginx

![](pics/nginx-install.png)

![](pics/nginx-install1.png)

To verify that nginx was successfully installed and is running as a service in Ubuntu, run the following command:
![](pics/nginx-succ-install.png)

If it is green and running, meaning the Web Server has launched successfully.

![](pics/nginx-green.png)

In order to receive and traffic by our Web Server, it is important to open TCP port 80 which is that default part that web browsers use to access web pages in the internet. 

![](pics/inbound-rule1.png)

![](pics/inbound-rule2.png)

![](pics/inbound-rule3.png)

To test how our Nginx server can respond to requests from the Internet. Open a web browser of your choice and try to access following url: 

![](pics/welcome0-nginx.png)

![](pics/welcome-nginx.png)

### Installing MySql

Now that the Nginx web server is up and running, you need to install a Database Management System (DBMS). MySQL is an open source relational database management system for storing application data. This particular database system is very suitable for this project.  

![](pics/mysql.png)
![](pics/mysql1.png)

Start the interactive script by running this command:
![](pics/mysql2.png)

![](pics/mysql3.png)


Request for the VALIDATE PASSWORD PLUGIN configuration.

![](pics/mysql4.png)

For the rest of the questions, press Y and hit the ENTER key at each prompt.

![](pics/mysql5.png)


test if you’re able to log in to the MySQL console by typing:

![](pics/mysql6.png)