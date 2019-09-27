Role Details: 
========= 

Role used for installing the mediawiki in docker containers

The only requirement in the this role is that it should be deployed onto the machine already having docker yum repository.
  
No variable dependencies though few important variables already defined and must be used in the same way written after the playbook is executed.

mysql user - wiki_user
mysql database - mediawiki_db
mysql password - mediawiki

NOTE: The user is allowed granted privileges from every IP.

No other dependencies except the managed host must be centos or rhel.

License
-------

BSD
