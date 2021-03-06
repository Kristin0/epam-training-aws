# What to do --- tested on Debian(host), Ubuntu(remote)

Do first
```
sudo apt-get install python3-pip && pip3 install ansible && export PATH=$PATH:~/.local/bin # export is for one session
git clone git@github.com:Kristin0/epam-training-ansible.git && cd epam-training-ansible/
vagrant up 
```

Then you need to copy your local ssh public key to your "remote" vagrant host and enter password *vagrant*. If you still don't have keys, see *ssh-keygen*

```
ssh-copy-id vagrant@192.168.111.111 
```
   
Check if you have a connection to your host
```
ansible  all -m ping
```
Then use existing playbook with command
```
ansible-playbook all playbook.yml
```
