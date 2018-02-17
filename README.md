This is an role for maintaining the zabbix-agent compiled from sources.
---

If you have a large server farm with different kinds of distros you can build zabbix agent from source instead of wasting time dealing with madness of varying linux environment

How to use:
Install Python and Ansible
http://goo.gl/i9xDPS

Clone this repo
```
git clone https://github.com/unwashed-and-dazed/ansible-zabbix-agentd.git
cd ansible-zabbix-agentd
```

Edit the configuration file and change "Server" and "ServerActive" wit your zabbix server IP
```
vim roles/zabbix_agentd/files/zabbix_agentd.conf
```

Create a inventory with the linux box you want to target
```
echo "IP.XX.YY.ZZ" > inventory
```

Run the playbook
```
ansible-playbook -i inventory run.yml
```
