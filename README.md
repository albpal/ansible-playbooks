# ansible-playbooks

Steps required to configure a host from scratch:

1. ansible-playbook playbooks/pb_unboxing_host.yml -i 37.247.52.181, -u root -k
2. ssh apalau@37.247.52.181
3. 	sudo sed -i "s|#Port 22|Port 23033|g" /etc/ssh/sshd_config && sudo service sshd restart && exit
4. Check roles to be applied on groups/vps_server.yml
5. ansible-playbook master.yml
