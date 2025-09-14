# 🎭 Meme Forge

Welcome to Meme Forge, a dynamic web application where you can create, share, and vote on the best memes. This project features a unique, custom-built authentication system and leverages Supabase for its backend data storage, offering a seamless and real-time user experience.

## ✨ Features

- **Meme Creation**: Generate memes using popular templates like "Drake," "Distracted Boyfriend," and "Doge."
- **Custom Authentication**: Secure sign-up and sign-in functionality built from scratch, independent of Supabase Auth.
- **Meme-based Password Recovery**: A unique password reset mechanism that requires users to remember a "meme password" for added security.
- **Real-time Feed**: A live leaderboard of the top-voted memes, updated in real-time using Supabase Channels.
- **Voting System**: Upvote your favorite memes to help them climb the leaderboard.
- **User-Managed Content**: Users can delete their own published memes.
- **Theming**: Switch between a sleek light mode and a cool dark mode, with your preference saved locally.
- **Responsive Design**: A modern, clean, and responsive UI that looks great on any device.

## 🛠️ Tech Stack

- **Frontend**: Vanilla JavaScript, HTML5, CSS3 (single-page application)
- **Backend**: [Supabase](https://supabase.io/) (PostgreSQL Database, Storage, and Real-time Subscriptions)
- **Authentication**: Custom JavaScript solution using `crypto.subtle` for password hashing (SHA-256) and `localStorage` for session management.

## 🚀 Getting Started

### Prerequisites

- A modern web browser.
- A Supabase account and project.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Aral-167/meme-battle.git
    cd meme-battle
    ```

2.  **Set up Supabase:**
    - Create a new project on [Supabase](https://supabase.io/).
    - In your Supabase project, go to the **SQL Editor**.
    - You will need to run several SQL commands to set up the necessary tables (`users`, `profiles`, `memes`, `likes`), views (`meme_leaderboard`), and RPC functions (`set_meme_secret`, `verify_meme_secret`, `delete_user_meme`). These scripts were generated during our development conversation.
    - Ensure Row Level Security (RLS) is enabled on your tables and the correct policies are in place.

3.  **Configure Supabase Credentials:**
    - Open the `index.html` file.
    - Find the following lines and replace the placeholder values with your Supabase project's URL and Anon Key:
      ```javascript
      const SUPABASE_URL = 'https://ycmozdaoyqarwwpxudxa.supabase.co';
      const SUPABASE_ANON_KEY = '...'; // Your Supabase Anon Key
      ```

4.  **Run the application:**
    - Simply open the `index.html` file in your web browser. Using a live server extension in your code editor is recommended for a better development experience.

## Usage

1.  **Sign Up**: Create a new account with your email and password.
2.  **Set Meme Password**: After signing up, you'll be prompted to create a "meme password" for account recovery.
3.  **Sign In**: Log in with your credentials and verify your meme password.
4.  **Create Memes**: Use the editor to select a template, add text, and publish your creation.
5.  **Vote**: Browse the real-time feed and upvote your favorite memes.
6.  **Toggle Theme**: Use the 🌙/☀️ icon in the toolbar to switch between dark and light mode.

---

This README provides a comprehensive overview of the Meme Forge application, its features, and the steps required to get it up and running.
