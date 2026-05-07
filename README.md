# 🤖 Queen Alina MD 2.0

> **Advanced WhatsApp Multi-Device Bot** built with Node.js and Baileys library.

![Queen Alina MD](https://i.imgur.com/queen-alina-banner.png)

## ✨ Features

### 🎯 Core Features
- ✅ **QR Code Login** - Easy authentication via WhatsApp Web
- ✅ **Auto Reconnect** - Automatic reconnection on disconnect
- ✅ **Clean Architecture** - Well-organized folder structure
- ✅ **JSON/MongoDB** - Flexible database options

### 📥 Download Menu
- YouTube Video/Audio Downloader
- TikTok Video Downloader (No Watermark)
- Facebook Video Downloader

### 👥 Group Menu
- Welcome & Goodbye Messages
- Anti-Link Protection
- Admin Commands (Kick, Promote, Demote)
- Group Settings Management

### 🎮 Fun Menu
- Random Jokes
- Random Facts

### 🤖 AI Menu
- ChatGPT Integration
- AI Image Generation

### 🛠️ Tools Menu
- Sticker Maker (Image/Video to Sticker)
- Text to Sticker
- Translator

### 👑 Owner Menu
- Broadcast Messages
- Block/Unblock Users
- Eval Command (Execute JS)
- Bot Statistics

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ installed
- Git installed
- WhatsApp account

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/queen-alina-md-2.0.git
cd queen-alina-md-2.0
```

2. **Install dependencies**
```bash
npm install
```

3. **Configure environment variables**
```bash
cp .env.example .env
# Edit .env with your settings
```

4. **Start the bot**
```bash
npm start
```

5. **Scan QR Code**
- Open WhatsApp on your phone
- Go to Settings > Linked Devices
- Scan the QR code shown in terminal

## 📁 Project Structure

```
queen-alina-md-2.0/
├── 📄 index.js              # Main entry point
├── 📄 config.js             # Bot configuration
├── 📄 package.json          # Dependencies
├── 📁 src/
│   ├── 📁 commands/         # Command modules
│   │   ├── 📁 download/     # Download commands
│   │   ├── 📁 group/        # Group management
│   │   ├── 📁 fun/          # Fun commands
│   │   ├── 📁 ai/           # AI features
│   │   ├── 📁 tools/        # Utility tools
│   │   └── 📁 owner/        # Owner commands
│   ├── 📁 events/           # Event handlers
│   ├── 📁 database/         # Database handlers
│   ├── 📁 utils/            # Utilities
│   │   ├── logger.js        # Logging system
│   │   ├── helper.js        # Helper functions
│   │   ├── commandHandler.js # Command processor
│   │   └── eventHandler.js  # Event processor
│   └── 📁 lib/              # Libraries
│       └── buttons.js       # Button templates
├── 📁 logs/                 # Log files
└── 📁 tmp/                  # Temporary files
```

## ⚙️ Configuration

Edit `.env` file:

```env
# Bot Configuration
BOT_NAME=Queen Alina MD 2.0
PREFIX=.
OWNER_NUMBER=1234567890
OWNER_NAME=Your Name

# Session
SESSION_NAME=queen-alina-session

# Database (Optional)
MONGODB_URI=mongodb+srv://user:pass@cluster.mongodb.net/db

# OpenAI (Optional)
OPENAI_API_KEY=sk-your-key

# Features
AUTO_READ_STATUS=false
AUTO_TYPING=true
ANTI_CALL=true
WELCOME_MESSAGE=true
GOODBYE_MESSAGE=true
ANTI_LINK=true
```

## 🌐 Deployment

### Deploy on Railway

1. Fork this repository
2. Create new project on [Railway](https://railway.app)
3. Connect your GitHub repository
4. Add environment variables in Railway dashboard
5. Deploy!

### Deploy on Render

1. Fork this repository
2. Create new Web Service on [Render](https://render.com)
3. Connect your repository
4. Set build command: `npm install`
5. Set start command: `npm start`
6. Add environment variables
7. Deploy!

### Deploy on VPS (Ubuntu)

```bash
# Update system
sudo apt update && sudo apt upgrade -y

# Install Node.js 18+
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs

# Install dependencies
sudo apt install -y git ffmpeg

# Clone repository
git clone https://github.com/yourusername/queen-alina-md-2.0.git
cd queen-alina-md-2.0

# Install packages
npm install

# Setup PM2 for process management
sudo npm install -g pm2

# Configure environment
cp .env.example .env
nano .env

# Start with PM2
pm2 start index.js --name queen-alina
pm2 save
pm2 startup
```

## 📱 Commands

### Basic Commands
| Command | Description |
|---------|-------------|
| `.menu` | Show main menu |
| `.ping` | Check bot speed |
| `.alive` | Check bot status |
| `.owner` | Show owner info |

### Download Commands
| Command | Description |
|---------|-------------|
| `.yt <url>` | Download YouTube video |
| `.yta <url>` | Download YouTube audio |
| `.tiktok <url>` | Download TikTok video |
| `.fb <url>` | Download Facebook video |

### Group Commands
| Command | Description |
|---------|-------------|
| `.welcome on/off` | Toggle welcome messages |
| `.goodbye on/off` | Toggle goodbye messages |
| `.antilink on/off` | Toggle anti-link |
| `.kick @user` | Remove user |
| `.promote @user` | Promote to admin |
| `.demote @user` | Demote to member |

### AI Commands
| Command | Description |
|---------|-------------|
| `.ai <text>` | Chat with AI |
| `.img <text>` | Generate AI image |

### Tools Commands
| Command | Description |
|---------|-------------|
| `.sticker` | Create sticker from media |
| `.textsticker <text>` | Create text sticker |
| `.translate <lang> <text>` | Translate text |

### Owner Commands
| Command | Description |
|---------|-------------|
| `.broadcast <text>` | Message all chats |
| `.block @user` | Block user |
| `.unblock @user` | Unblock user |
| `.eval <code>` | Execute JavaScript |

## 🔧 Troubleshooting

### Common Issues

**1. QR Code not showing**
```bash
# Make sure you have qrcode-terminal installed
npm install qrcode-terminal
```

**2. FFmpeg not found**
```bash
# Ubuntu/Debian
sudo apt install ffmpeg

# macOS
brew install ffmpeg

# Windows
# Download from https://ffmpeg.org/download.html
```

**3. MongoDB connection failed**
- Check your MongoDB URI
- Ensure IP whitelist includes your server
- Use JSON database as fallback (leave MONGODB_URI empty)

**4. Session expired**
```bash
# Delete session folder and rescan QR
rm -rf queen-alina-session/
npm start
```

## 📜 License

This project is licensed under the MIT License.

## 🙏 Credits

- [Baileys](https://github.com/WhiskeySockets/Baileys) - WhatsApp Web API
- [OpenAI](https://openai.com) - AI Integration
- [Node.js](https://nodejs.org) - Runtime

## 📞 Support

- **Owner:** [Contact on WhatsApp](https://wa.me/1234567890)
- **Issues:** [GitHub Issues](https://github.com/yourusername/queen-alina-md-2.0/issues)

---

<p align="center">
  <b>Queen Alina MD 2.0</b><br>
  Made with ❤️ by Queen Alina Team
</p>
