### Reactjs On Termux

First, ensure your Termux is updated:

```bash
pkg update && pkg upgrade
```

#### Step 1: Install Required Packages

```bash
# Install Node.js and npm
pkg install nodejs -y

# Install Git (optional but recommended)
pkg install git -y

# Install text editor (choose one)
pkg install vim   # or nano, micro, etc.
```

#### Step 2: Verify Installation

```bash
node --version
npm --version
```

#### Step 3: Create React App

##### Option A: Using Create React App (Recommended for beginners)

```bash
# Install create-react-app globally
npm install -g create-react-app

# Create a new React app
npx create-react-app my-app

# Navigate to your app directory
cd my-app

# Start the development server
npm start
```

##### Option B: Using Vite (Faster, Modern)

```bash
# Create a new Vite React app
npm create vite@latest my-vite-app -- --template react

# Navigate to your app
cd my-vite-app

# Install dependencies
npm install

# Start development server
npm run dev
```

#### Step 4: Access Your React App

After running npm start or npm run dev, you'll see:

Local access: Open browser on your Android device and go to http://localhost:3000 (for Create React App) or http://localhost:5173 (for Vite)