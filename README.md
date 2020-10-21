Ansible project for Deploying Transtats


### How to use

- Install ansible on your computer (`sudo pip install ansible` should do the
  trick).
- Clone this project.
- Edit the `transtats-ansible/hosts` file and enter the IP address of the server you are
	deploying to.
- If you want to deploy app on different platform just create platform ansible-distriution-name-vars.yml file in vars folder e.g RHEL-vars.yml. 	
oko- Run the playbook:

	```
	cd transtats-ansible
	ansible-playbook provision.yml
	```	
- Run playbook with environment variable if you want to change the db name..etc

    ```
    cd transtats-ansible
	ansible-playbook --extra-vars "DATABASE_NAME=db_name DATABASE_USER=db_user DATABASE_PASSWD=db_pass  DATABASE_HOST=db_host" provision.yml 
	``` 

	Replace the value in place of db_name, db_user, db_pass and db_host. 


