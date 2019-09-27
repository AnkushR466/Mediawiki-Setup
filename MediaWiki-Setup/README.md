# MediaWiki

The complete setup is divided in two parts: 
 * The first part is for the bare-metal or virtual machine in which the mysql database as well as the mediawiki front-end is configured on the host.
 * The second part includes the desired task which was to launch two docker containers one for the front-end mediawiki web page and the second for the mysql database server.

There are three prerequisites for these task: 
 * Remote Machine must have predefined yum repo for docker installation 
 * Remote machine must be a redhat linux or centos 
 * ssh keys must be configured for password less login or the name of the user and password must be written in the hosts file and accordingly proper entry in sudoers as well as remote_user and become_user in ansible.cfg files if the become_user is not root.
 [I personally configure ansible on a another user and gave it the root powers and permissions by register it into /etc/sudoers file]

There are two roles created particularly for the above tasks.
 * First task 
   A) To perform the first task add the IP of the virtual machine or the remote machine in the bare group in the hosts file. 
   B) Run the following command inside this folder only 
       # ansible-playbook bare_play.yml
   C) The further details of the playbook and role architecture is explained in mediawiki/README.md
 * Second task
   A) Same as above.
   B) Run the following command inside this folder only
       # ansible-plaaybook dokcer_play.yml
   C) The further details of the playbook and role architecture is explained in mediawikipart2/README.md


The req.yml is file to handle all the prerequisites other then the mentioned above. You need not to run it seperately, it is imported in both plays.
