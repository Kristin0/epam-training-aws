## WordPress automation with Ansible  
--tested on Debian(host), Ubuntu20.04_core(remote)

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
```
├── ansible.cfg
├── group_vars
│   └── myservers.yml
├── inventory
├── README.md
├── roles
│   ├── mysql
│   │   ├── defaults
│   │   │   └── main.yml
│   │   ├── files
│   │   ├── handlers
│   │   │   └── main.yml
│   │   ├── tasks
│   │   │   └── main.yml
│   │   ├── templates
│   │   └── vars
│   │       └── main.yml
│   ├── nginx
│   │   ├── defaults
│   │   │   └── main.yml
│   │   ├── files
│   │   ├── handlers
│   │   │   └── main.yml
│   │   ├── tasks
│   │   │   └── main.yml
│   │   ├── templates
│   │   │   └── wordpress.j2
│   │   └── vars
│   │       └── main.yml
│   └── wordpress
│       ├── defaults
│       │   └── main.yml
│       ├── files
│       ├── handlers
│       │   └── main.yml
│       ├── tasks
│       │   └── main.yml
│       ├── templates
│       │   ├── index.j2
│       │   └── wp-config.php.j2
│       └── vars
│           └── main.yml
├── Vagrantfile
└── wordpress.yml
```
![image](https://user-images.githubusercontent.com/44585557/111031212-c4784100-841f-11eb-8e91-9837066b7318.png)
![image](https://user-images.githubusercontent.com/44585557/111031234-cfcb6c80-841f-11eb-8856-e5fff37a52f9.png)


