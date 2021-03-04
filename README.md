# What to do

What you do first
```
mkdir ansible && cd ansible
git clone git@github.com:Kristin0/epam-training-ansible.git
vagrant up 
```

Then you need to copy your local ssh public key to your "remote" vagrant host. In my case
```
ssh-copy-id -i /home/<your_username>/.ssh/id_rsa.pub vagrant@192.168.111.111 
```
   
