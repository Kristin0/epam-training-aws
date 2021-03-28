### user data for your ami
Please before using change inventory_aws_ec2.yml and group_vars to your own variables/credentials

```
#!/bin/bash -ex
apt update -y
apt install git -y
mkdir -p /home/ubuntu/ec2
cd /home/ubuntu/ec2
git init
git pull https://github.com/Kristin0/epam-training-ec2.git
chown -R ubuntu:ubuntu /home/ubuntu/ec2
runuser -l ubuntu -c 'cd ~/ec2/ansible && ansible-playbook wordpress.yml'
