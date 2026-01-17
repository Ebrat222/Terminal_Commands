### Install MySQL in UserLand

```bash
# Update package list to get latest versions and dependencies
sudo apt update

# Install MySQL server package
sudo apt install mysql-server

# Start the MySQL service
sudo service mysql start

# Launch MySQL command line interface as root
sudo mysql

# Check the version of mysql using command
mysql --version
```

#### Additional recommendations:

```bash
# Secure MySQL installation (recommended after installation)
sudo mysql_secure_installation

# Check MySQL service status
sudo service mysql status

# Enable MySQL to start on boot
sudo systemctl enable mysql
```

#### Common follow-up steps:

```bash
# Create a new MySQL user (run within MySQL CLI)
CREATE USER 'username'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON *.* TO 'username'@'localhost';
FLUSH PRIVILEGES;
```
