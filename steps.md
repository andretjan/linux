sudo apt install ufw
sudo ufw allow ssh
sudo ufw enable

sudo apt install mysql-server
sudo mysql
CREATE USER 'sammy'@'localhost' IDENTIFIED BY 'password';
FLUSH PRIVILEGES;
exit

GRANT ALL PRIVILEGES ON *.* TO 'sammy'@'localhost' WITH GRANT OPTION;

mysql -u sammy -p
systemctl status mysql.service

sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
sudo systemctl restart mysql

sudo ufw allow 3306
