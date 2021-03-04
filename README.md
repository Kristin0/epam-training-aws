# What to do

First of all you need to copy your local ssh public key to your "remote" vagrant host. In my case
```
ssh-copy-id -i /home/<your_username>/.ssh/id_rsa.pub vagrant@192.168.111.111 
```
