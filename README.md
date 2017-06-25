# ansible-playbooks

Steps required to configure a host from scratch:

**Before** execute anything, be sure you have not any old ssh key entry on ~/.ssh/known_hosts with the same IP.

1. Add it to know hosts: ssh root@37.247.52.181
2. ansible-playbook playbooks/pb_unboxing_host.yml -i 37.247.52.181, -u root -k
3. ssh apalau@37.247.52.181
4. 	sudo sed -i "s|#Port 22|Port 23033|g" /etc/ssh/sshd_config && sudo service sshd restart && exit
5. Check roles to be applied on groups/vps_server.yml
6. ansible-playbook master.yml
