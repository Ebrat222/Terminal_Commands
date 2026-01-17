### Install Mariadb in Termux

```bash
# Update package repositories and upgrade existing packages
pkg update && pkg upgrade 

# Install MariaDB package
pkg install mariadb

# Initialize the MariaDB data directory
mysql_install_db

# Start MariaDB server in safe mode as root (background process)
mariadbd-safe  -u root &

# Run security configuration script
mysql_secure_installation

# Connect to MariaDB as root
mysql -u root -p
```
