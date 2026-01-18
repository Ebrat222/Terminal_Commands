### Install SQLite In Termux

```bash
# Update Termux packages
pkg update && pkg upgrade

# Install SQLite database system
pkg install sqlite

# Request storage permissions for Termux
termux-setup-storage

# Launch SQLite (opens in-memory temporary database)
sqlite3

# Alternative: Create/open a persistent database file
# sqlite3 mydatabase.db
```

Notes:

1· First 3 lines set up SQLite in Termux
2· sqlite3 alone creates temporary database
3· Commented line shows how to create persistent file