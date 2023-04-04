**How to run ansible playbook **


## In case you need to run the palybook using cli, using WSL

### Install Ansible, sshpass and password store (used in some roles)


```
sudo apt-get install ansible sshpass  pass python3-pip -y
sudo pip install shyaml
```

### clone repo to your wsl

```

git clone git@github.com:harinderjits-git/ansible-db-tls.git
cd ansible-db-tls
```

### run the playbook

ansible_runner is wrapper being used

```
./ansible_runner
Usage: ${0##*/} [ playbook  stackBu   stackInstName tags(optional)]
            playbook: playbook  name without ".yml"
            stackInstName: stackInstName like orclqa2 or a hostname in case stackService is a host
            tags: list of tags in "abc,def,ghi"
```

Examples 

1. example : you want to run config_db_tns playbook for db on node1 of sit

```
 ./ansible_runner config_db_tns sit-db01
```
2. example : you want to run oracle_cert_rotation playbook for db on node1 of sit

```
 ./ansible_runner oracle_cert_rotation sit-db01
```
