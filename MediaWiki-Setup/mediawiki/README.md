Role Details: 
========= 

This Role is used for installing required softwares and confiruring setup

1) The playbook used for the first task is bare_play.yml which uses a role named mediawiki. 
2) To analyze this play go for tasks/main.yml. The Mysql database user name is "wiki_user" with password "mediawiki". 
3) You can change the value of the user and password in vars/main.yml user_name and user_pass variable.
4) The name of the database in mysql is mediawiki_db you can change the same in vars/db_name. 
5) This user is granted privileges for localhost only.


