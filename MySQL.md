Installing MySQL
----
sudo apt update
sudo apt install mysql-server
sudo mysql_secure_installation

CREATE USER 'username'@'host' IDENTIFIED WITH authentication_plugin BY 'password';

CREATE USER 'sammy'@'localhost' IDENTIFIED BY 'password';

CREATE USER 'sammy'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

ALTER USER 'sammy'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

GRANT PRIVILEGE ON database.table TO 'username'@'host';

GRANT CREATE, ALTER, DROP, INSERT, UPDATE, DELETE, SELECT, REFERENCES, RELOAD on *.* TO 'sammy'@'localhost' WITH GRANT OPTION;

GRANT ALL PRIVILEGES ON *.* TO 'sammy'@'localhost' WITH GRANT OPTION;

FLUSH PRIVILEGES;

------
systemctl status mysql.service
----
sudo mysqladmin -p -u [username] version
-------
SELECT user,authentication_string,plugin,host FROM mysql.user;
ALTER USER 'root'@'localhost' IDENTIFIED WITH caching_sha2_password BY 'password';
FLUSH PRIVILEGES;
SELECT user,authentication_string,plugin,host FROM mysql.user;
mysql -u root -p
sudo mysql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
FLUSH PRIVILEGES;
SELECT user,authentication_string,plugin,host FROM mysql.user;


SHOW VARIABLES LIKE 'validate_password%';
