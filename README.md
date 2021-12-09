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
- Run playbook with environment variable if you want to change the default remote_user (root) in ansible.cfg
    ```
    cd transtats-ansible
    ansible-playbook --extra-vars "REMOTE_USER=remote_user" 	provision.yml
- By default this playbook download Transtats latest released tar.gz file for deployment. For different transtats version deployment, one can use environment variables
release_testing (false|default) and test_target_url (https://github.com/transtats/transtats/archive/refs/heads/devel.zip|default).
   ```
   cd transtas-ansible
       ansible-playbook --extra-vars "TEST_TARGET_URL=https://github.com/transtats/transtats/archive/refs/heads/r085.zip RELEASE_TESTING=true" provision.yml
- Run playbook with environment variable if you want to change the db name..etc

    ```
    cd transtats-ansible
	ansible-playbook --extra-vars "DATABASE_NAME=db_name DATABASE_USER=db_user DATABASE_PASSWD=db_pass  DATABASE_HOST=db_host" provision.yml 
	``` 

	Replace the value in place of db_name, db_user, db_pass and db_host. 


