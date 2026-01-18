### Install Nodejs on Termux

#### Basic System Updates

```bash
apt update && apt upgrade
pkg update && pkg upgrade
```

#### Storage Permission

```bash
termux-setup-storage
```

#### Install Node.js

```bash
pkg install nodejs
```

#### Install npm packages globally

```bash
npm install -g http-server mongodb mongosh nodemon
```
