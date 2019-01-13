# ansible-playbooks
## config-basic-host.yml - Setup a new server
Steps required to configure a host from scratch:
1. HOST=<ip> #hostname or host ip
2. ssh-keygen -R $HOST && ssh-keyscan -H $HOST >> ~/.ssh/known_hosts
3. git clone https://github.com/albpal/ansible-playbooks.git && cd ansible-playbooks
4. ansible-galaxy install -r roles/requirements.yml -p roles
5. ansible-playbook config-basic-host.yml -i $HOST, -u root -k

If all went OK, you should login to the host without enter the password.
  
`ssh apalau@$HOST -p 23033`

## install-portainer.yml - Install and configure Portainer (https://www.portainer.io)
1. HOST=<ip> #hostname or host ip
2. git clone https://github.com/albpal/ansible-playbooks.git && cd ansible-playbooks
3. ansible-galaxy install -r roles/requirements.yml -p roles
4. ansible-playbook install-portainer.yml -i $HOST, -u apalau -e ansible_ssh_port=23033

If all went OK, you should access Portainer at http://$HOST:9000
