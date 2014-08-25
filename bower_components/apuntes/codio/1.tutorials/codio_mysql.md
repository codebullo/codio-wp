## Información que muestra la instalacion MYSQL

To do so, start the server, then issue the following commands:

	/home/codio/.parts/packages/mysql/5.6.15/bin/mysqladmin -u root password 'new-password'
	/home/codio/.parts/packages/mysql/5.6.15/bin/mysqladmin -u root -h mailbox-spoon password 'new-password'

Alternatively you can run:                                                                        

	/home/codio/.parts/packages/mysql/5.6.15/bin/mysql_secure_installation


which will also give you the option of removing the test                                          
databases and anonymous user created by default.  This is                                         
strongly recommended for production servers.                                                      
                                                                                                  
See the manual for more instructions.                                                             
                                                                                                  
You can start the MySQL daemon with:

	cd . ; /home/codio/.parts/packages/mysql/5.6.15/bin/mysqld_safe &
    
You can test the MySQL daemon with mysql-test-run.pl
	
    cd mysql-test ; perl mysql-test-run.pl

Please report any problems with the `./bin/mysqlbug script!`                                    
                                                                                                  
The latest information about MySQL is available on the web at http://www.mysql.com                                                                            
                                                                                                  
Support MySQL by buying support/licenses at http://shop.mysql.com                                 
                                                                                                  
WARNING: Found existing config file /home/codio/.parts/packages/mysql/5.6.15/my.cnf on the system.
Because this file might be in use, it was not replaced,                                           
but was used in bootstrap (unless you used --defaults-file)                                       
and when you later start the server.                                                              
The new default config file was created as /home/codio/.parts/packages/mysql/5.6.15/my-new.cnf,   

============ mysql ============

To start the server:                                                                              

	$ parts start mysql

To stop the server:

	$ parts stop mysql

To connect to the server:                                                                         
	
    $ mysql







please compare it with your file and take the changes you need. 