# Script to install apache and launch webserver on EC2 Instance using User Data as text
# Launch instance normally, and in advanced details paste following script 


#!/bin/bash
sudo su 
yum update -y
yum install -y httpd.x86_64
systemctl start httpd.service
systemctl enable httpd.service
echo "Displaying automated website using EC2 User Data  $(hostname-f)" > /var/www/html/index.html
