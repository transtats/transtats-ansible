Ansible project for Deploying Transtats


### How to use

- Install ansible on your computer (`sudo pip install ansible` should do the
  trick).
- Clone this project.
- Edit the `ansible/hosts` file and enter the IP address of the server you are
	deploying to and edit the path to the private key file.
- Edit the `ansible/vars.yml` file and enter values appropriate for your project.
- Run the playbook:

	```
	cd ansible
	ansible-playbook -i hosts provision.yml
	```	
