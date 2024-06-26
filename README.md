# Steps:
1. Edit ansible.cfg and set a path for a log file
	This must be unique otherwise it overwrites past logs so switch it to like a site ID involved with what is thes cript will be upgrading or something.
3. Edit inventory.ini and add the hostnames of the routers that you want to upgrade. Just list them line-by-line like I've shown below:
`
[target]
gw-foo.msln.net
gw-bar.msln.net
`
2. Stop editing the inventory file and run the following:
	
	`ansible-playbook upgrade.yml -i inventory.ini`
	
	**Make sure you run this exactly as shown and not from a different directory. We need ansible.cfg to be in your current working directory**
