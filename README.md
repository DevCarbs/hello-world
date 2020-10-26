# hello-world
Simple hello-world website using an AWS EC2 Instance
EC2 Instance website: http://18.207.1.40/

# Workflow in commandline
# Log into CLI via terminal as root 
ssh -i EC2Tutorial.pem ec2-user@xx.xxx.x.xx                 # Look for permissions 0644 error if unable to ssh
sudo su

# Install Apache web server
# Start and enable http to be on - even across reboots
yum install -y httpd.x86_64
systemctl start httpd.service
systemctl enable httpd.service

# View webserver
curl localhost:80
go to ipaddress in browser                                  # If timeout, remember to open port 80 in sec group

# Edit webpage contents 
echo "text $(hostname-f)" > /var/www/html/index.html




