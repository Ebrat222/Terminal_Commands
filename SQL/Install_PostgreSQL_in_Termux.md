### Install PostgreSQL in Termux

```bash
# Install PostgreSQL package on Termux
pkg install postgresql

# Create the PostgreSQL data directory with parent directories if needed
mkdir -p $PREFIX/var/lib/postgresql

# Initialize the PostgreSQL database cluster in the specified directory
initdb $PREFIX/var/lib/postgresql

# Start the PostgreSQL server using the created data directory
pg_ctl -D $PREFIX/var/lib/postgresql start

# Create a new PostgreSQL superuser with password prompt
# Replace 'yourUserName' with your desired username
createuser --superuser --pwprompt yourUserName

# Create a new database named 'mydb'
createdb mydb

# Connect to the PostgreSQL database 'mydb' using psql
psql mydb

# After connecting, you'll see the PostgreSQL prompt:
# mydb=#
# This indicates you're connected to the 'mydb' database and ready to execute SQL commands
```

Key Notes:

1. $PREFIX - Termux environment variable pointing to /data/data/com.termux/files/usr
2. Superuser - Has full administrative privileges in PostgreSQL
3. You'll be prompted to enter a password when running createuser --pwprompt
4. PostgreSQL must be running (pg_ctl start) before creating users/databases

#### To stop PostgreSQL when done:

```bash
pg_ctl -D $PREFIX/var/lib/postgresql stop
```
