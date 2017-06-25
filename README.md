# ansible-playbooks

Steps required to configure a host from scratch:

1. ssh-keygen -R 37.247.52.181 && ssh-keyscan -H 37.247.52.181 >> ~/.ssh/known_hosts
2. ansible-playbook playbooks/pb_unboxing_host.yml -i 37.247.52.181, -u root -k
3. ssh apalau@37.247.52.181
4. 	sudo sed -i "s|#Port 22|Port 23033|g" /etc/ssh/sshd_config && sudo service sshd restart && exit
5. Check roles to be applied on groups/vps_server.yml
6. ansible-playbook master.yml
