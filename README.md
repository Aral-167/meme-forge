# 🎭 Meme Forge (Meme Battle)

A unique social meme creation platform with innovative **meme-based authentication**. Create, share, and vote on memes while experiencing a completely new take on user security.

## ✨ What Makes This Special

Instead of boring passwords, users authenticate using **custom memes**! After signing up with email/password, users create a personalized "meme password" using one of our templates with their own text. Every login requires recreating this exact meme - making it both secure and fun!

## 🚀 Key Features

- **🔐 Meme-Based Authentication**: Revolutionary security using personalized memes
- **🎨 Interactive Meme Creator**: Drag-and-drop text positioning on popular templates
- **❤️ Social Voting**: Like and rank community memes in real-time
- **🏆 Live Leaderboard**: See top-performing memes instantly
- **🌙 Dark/Light Theme**: Toggle between beautiful themes
- **📱 Responsive Design**: Works perfectly on mobile and desktop
- **⚡ Real-time Updates**: Instant feed updates using Supabase real-time
- **🔄 Meme Password Recovery**: Reset your account using your meme password

## 🛠️ Technology Stack

- **Frontend**: Vanilla HTML5, CSS3, Modern JavaScript (ES6+)
- **Backend**: [Supabase](https://supabase.com) (PostgreSQL, Real-time, Storage)
- **Graphics**: Canvas API for meme rendering
- **Templates**: Custom positioned meme templates (Drake, Distracted Boyfriend, Doge)

## 🏃‍♂️ Quick Start

### Prerequisites
- Modern web browser with JavaScript enabled
- Internet connection for Supabase backend

### Running Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/Aral-167/meme-battle.git
   cd meme-battle
   ```

2. **Serve the files**
   You can use any local web server. Here are a few options:
   
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx serve .
   
   # Using PHP
   php -S localhost:8000
   ```

3. **Open in browser**
   Navigate to `http://localhost:8000`

### Deployment

This is a static web application that can be deployed to any hosting platform:
- GitHub Pages
- Netlify
- Vercel
- Firebase Hosting
- Any web server

Simply upload all files to your hosting provider.

## 🎮 How to Use

### First Time Setup
1. **Sign Up**: Enter email and password
2. **Create Meme Password**: Choose a template and add your secret text combination
3. **Start Creating**: You're now ready to make memes!

### Daily Use
1. **Sign In**: Enter your email/password
2. **Verify Meme**: Recreate your exact meme password to access the app
3. **Create & Share**: Make memes and see them appear in the community feed
4. **Vote**: Like your favorite memes to boost them up the leaderboard

### Meme Creation Tips
- Choose from 3 popular templates: Drake Pointing, Distracted Boyfriend, or Doge
- Drag text around the canvas to position it perfectly (when unlocked)
- Use the preview to see how your meme looks before publishing
- Keep text short and punchy for maximum impact

## 🏗️ Project Structure

```
meme-battle/
├── index.html          # Main application (single-page app)
├── templates/           # Meme template images
│   ├── drake.jpg
│   ├── distracted.jpg
│   └── doge.jpg
└── README.md           # You are here!
```

## 🔧 Configuration

The app connects to a Supabase backend. The configuration is embedded in `index.html`:

```javascript
const SUPABASE_URL = 'https://ycmozdaoyqarwwpxudxa.supabase.co';
const SUPABASE_ANON_KEY = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...';
```

## 🎯 Database Schema

The app uses these main Supabase tables:
- `users` - User accounts with hashed passwords
- `profiles` - User profiles with meme password hashes
- `memes` - Published memes with metadata
- `likes` - User likes/votes on memes
- `meme_leaderboard` - View for leaderboard rankings

## 🤝 Contributing

### Adding New Meme Templates

1. Add your image to the `templates/` folder
2. Update the `templates` object in `index.html`:
   ```javascript
   const templates = {
     drake: 'templates/drake.jpg',
     distracted: 'templates/distracted.jpg',
     doge: 'templates/doge.jpg',
     yourtemplate: 'templates/yourtemplate.jpg'  // Add this
   };
   ```
3. Add layout configuration in `templateLayouts`
4. Update all select elements with your new option

### Development Guidelines

- Keep the single-file approach for simplicity
- Use modern JavaScript features (ES6+)
- Follow the existing CSS custom properties pattern
- Test both light and dark themes
- Ensure mobile responsiveness

## 🔒 Security Notes

- Passwords are hashed using SHA-256 with salt
- Meme passwords are stored as hashes in the database
- Session tokens are used for authentication state
- All user content goes through Supabase security rules

## 🐛 Known Issues

- Template positioning is currently locked (set `LOCK_TEMPLATE_SLOTS = false` to enable dragging)
- Password reset requires the exact meme password recreation

## 🎨 Customization

### Themes
Modify the CSS custom properties in the `:root` and `[data-theme="dark"]` sections to customize colors.

### Templates
Add new templates by following the contributing guide above.

### Features
The app is designed to be easily extensible - most features are contained in logical JavaScript sections.

## 📱 Browser Support

- Modern Chrome, Firefox, Safari, Edge
- Mobile browsers (iOS Safari, Chrome Mobile)
- Requires JavaScript and Canvas API support

## 🌟 Credits

Built with creativity and passion for making authentication fun! Uses the amazing Supabase platform for backend services.

---

**Ready to forge some memes?** [Try it live](#) or clone and run locally!

*Made with ❤️ and a sense of humor*
