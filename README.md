Ansible project for Deploying Transtats


### How to use

- Install ansible on your computer (`sudo pip install ansible` should do the
  trick).
- Clone this project.
- Edit the `transtats-ansible/hosts` file and enter the IP address of the server you are
	deploying to and edit the path to the private key file.
- Run the playbook:

	```
	cd transtats-ansible
	ansible-playbook provision.yml
	```	
