# ansible-playbooks
## config-basic-host.yml - Setup a new server
Steps required to configure a host from scratch:
1. HOST=<ip> #hostname or host ip
2. ssh-keygen -R $HOST && ssh-keyscan -H $HOST >> ~/.ssh/known_hosts
2. ansible-playbook config-basic-host.yml -i $HOST, --extra-vars -u root -k
3. ssh apalau@$HOST


