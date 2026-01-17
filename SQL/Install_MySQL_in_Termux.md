### Install MySQL in Termux > Proot-distro > Ubuntu Linux

#### First, ensure you have Termux properly set up:

```bash
# Update packages
pkg update && pkg upgrade

# Install required dependencies
pkg install proot-distro -y

# List available distributions
proot-distro list

# Install Ubuntu
proot-distro install ubuntu

# Login to Ubuntu
proot-distro login ubuntu
```

#### Install MySQL in Ubuntu

#### Once inside the Ubuntu proot environment:

```bash
# Update package lists
apt update && apt upgrade -y

# Install MySQL Server
apt install mysql-server -y

# Initialize MySQL (Ubuntu 20.04+)
mysql_secure_installation
```
#### If You Got Error ?

```bash
# Create necessary run directory
mkdir -p /var/run/mysqld
chown mysql:mysql /var/run/mysqld

# Start MySQL server in the background
mysqld --user=mysql &

# Or use mysqld_safe for better stability
mysqld_safe --user=mysql &

# Try to connect to MySQL (no password initially)
mysql -u root
```

#### Now Add User Password

```sql
-- While in MySQL shell, set a password:
ALTER USER 'root'@'localhost' IDENTIFIED BY 'password';
FLUSH PRIVILEGES;

-- Then exit and reconnect with password
EXIT;
mysql -u root -p
```

