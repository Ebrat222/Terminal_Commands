#### If You Got Error ? Use This :

```bash
# Update packages
pkg update && pkg upgrade

# Install PostgreSQL
pkg install postgresql

# Initialize database cluster
initdb -D $PREFIX/var/lib/postgresql

# Start PostgreSQL server
pg_ctl -D $PREFIX/var/lib/postgresql start

# Create a database (optional)
createdb testdb

# Access PostgreSQL
psql testdb
```

#### Common Issues & Solutions

1. Port already in use:

```bash
# Change port in postgresql.conf
echo "port = 5433" >> $PREFIX/var/lib/postgresql/postgresql.conf
```

2. Permission issues:

```bash
chmod 700 $PREFIX/var/lib/postgresql
```
3. Start/Stop Commands:

```bash
# Start PostgreSQL
pg_ctl -D $PREFIX/var/lib/postgresql start

# Stop PostgreSQL
pg_ctl -D $PREFIX/var/lib/postgresql stop

# Check status
pg_ctl -D $PREFIX/var/lib/postgresql status

# Restart PostgreSQL
pg_ctl -D $PREFIX/var/lib/postgresql restart
```
