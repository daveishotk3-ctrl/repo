# Chat

A live chat app with group chats, private chats (password-protected), and real-time messaging powered by Firebase.

## Features

- **Group Chats** - Public chats visible to all users
- **Private Chats** - Password-protected chats that stay hidden until unlocked
- **User Names** - Permanent user identity
- **Nicknames** - Optional display names
- **Live Messaging** - Real-time message sync across all users
- **Message History** - All messages persist with timestamps

## Local Development

1. Clone the repo:
```bash
git clone https://github.com/daveishotk3-ctrl/repo.git
cd repo
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file:
```bash
cp .env.example .env
```

4. Get your Firebase credentials:
   - Go to [firebase.google.com](https://firebase.google.com)
   - Create a new project
   - Create a Realtime Database (start in test mode)
   - Get your Web API credentials from Project Settings
   - Add them to your `.env` file

5. Run the server:
```bash
npm start
```

6. Open [http://localhost:3000](http://localhost:3000)

## Deploy to Railway

1. Push your code to GitHub (already done)

2. Go to [railway.app](https://railway.app) and sign up

3. Create a new project → Deploy from GitHub

4. Select your `daveishotk3-ctrl/repo` repository

5. In the Railway dashboard, add environment variables:
   - `FIREBASE_API_KEY` - Your Firebase API key
   - `FIREBASE_PROJECT_ID` - Your Firebase project ID
   - `FIREBASE_DATABASE_URL` - Your Firebase database URL (https://your-project.firebaseio.com)

6. Railway will automatically detect `package.json` and deploy!

Your app will be live at a URL like `https://your-project.up.railway.app`

## Usage

1. Set your name in Settings (permanent, cannot be changed)
2. Optionally set a nickname (can be changed anytime)
3. Create a new chat or join an existing one
4. Share chat links with friends
5. Messages sync in real-time!

## Notes

- All messages are stored in Firebase and persist forever
- Private chats are hidden from the list until the correct password is entered
- Each chat can have its own password
- No user authentication needed - just set a name!
