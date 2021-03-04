# What to do

Do first
```
mkdir ansible && cd ansible
git clone git@github.com:Kristin0/epam-training-ansible.git
vagrant up 
```

Then you need to copy your local ssh public key to your "remote" vagrant host.
```
ssh-copy-id -i /home/<your_username>/.ssh/id_rsa.pub vagrant@192.168.111.111 
```
   
Check if you have a connection to your host
```
ansible -i inventory.yml all -m ping
```
