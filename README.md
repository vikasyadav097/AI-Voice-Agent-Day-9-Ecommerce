# 🎮 Voice Game Master - AI-Powered D&D Adventure

An immersive voice-powered Dungeons & Dragons game featuring real-time AI responses, natural conversation flow, and a stunning cyberpunk UI. Built with LiveKit Agents and Murf.ai's ultra-fast voice synthesis.

![Cyberpunk UI](https://img.shields.io/badge/UI-Cyberpunk-00ffff?style=for-the-badge)
![Voice AI](https://img.shields.io/badge/Voice-AI%20Powered-purple?style=for-the-badge)
![Real-time](https://img.shields.io/badge/Real--time-Interaction-ff00ff?style=for-the-badge)

## ✨ Features

### 🎭 Immersive Gameplay
- **Real-time Voice Interaction** - Natural conversation with AI Game Master
- **Dynamic Storytelling** - Your choices shape the adventure
- **Dice Rolling System** - Automated D20 rolls with modifiers
- **Character Progression** - Track HP, stats, inventory, and quests
- **Epic Narrative** - Cinematic descriptions and dramatic encounters

### 🎨 Cyberpunk UI
- **Dark Theme** with neon cyan/purple accents
- **Animated Background** with glowing orbs and particles
- **Real-time Character Sheet** with live stat updates
- **Audio Visualizer** for agent voice feedback
- **Responsive Design** for all screen sizes

### 🤖 AI-Powered Features
- **Natural Language Processing** - Understands complex player commands
- **Context-Aware Responses** - Remembers game state and history
- **Dynamic Quest System** - Generates and tracks objectives
- **Intelligent Combat** - Tactical encounters with dice mechanics
- **Inventory Management** - Track items and equipment

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ and pnpm
- Python 3.11+
- LiveKit account (free tier available)
- Murf.ai API key

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/GhanshyamJha05/Eighth_task_murf_ai.git
cd Eighth_task_murf_ai/ten-days-of-voice-agents-2025
```

2. **Set up the backend**
```bash
cd backend
python -m venv .venv
.venv\Scripts\activate  # Windows
# or
source .venv/bin/activate  # Mac/Linux

pip install -r requirements.txt
```

3. **Configure environment variables**

Create `backend/.env.local`:
```env
LIVEKIT_URL=wss://your-livekit-url
LIVEKIT_API_KEY=your-api-key
LIVEKIT_API_SECRET=your-api-secret
MURF_API_KEY=your-murf-api-key
OPENAI_API_KEY=your-openai-key
```

Create `frontend/.env.local`:
```env
LIVEKIT_API_KEY=your-api-key
LIVEKIT_API_SECRET=your-api-secret
LIVEKIT_URL=https://your-livekit-url
```

4. **Install frontend dependencies**
```bash
cd ../frontend
pnpm install
```

### Running the Application

**Terminal 1 - LiveKit Server:**
```bash
cd ten-days-of-voice-agents-2025
.\livekit-server.exe --dev
```

**Terminal 2 - Backend Agent:**
```bash
cd backend
.venv\Scripts\activate
python src/agent.py dev
```

**Terminal 3 - Frontend:**
```bash
cd frontend
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## 🎮 How to Play

1. **Start the Adventure** - Click "START CALL" on the welcome screen
2. **Speak Naturally** - Describe what you want to do
3. **Make Choices** - Your decisions affect the story
4. **Roll Dice** - Say "roll for [skill]" to make checks
5. **Track Progress** - Monitor your character sheet on the right

### Example Commands
- "I look around for enemies"
- "I want to sneak past the guards"
- "Roll for perception"
- "Check my inventory"
- "I attack with my sword"
- "I cast fireball"

## 🏗️ Architecture

### Tech Stack
- **Frontend**: Next.js 15, React, TypeScript, Tailwind CSS, Framer Motion
- **Backend**: Python, LiveKit Agents, OpenAI GPT-4
- **Voice**: Murf.ai Falcon (ultra-fast TTS)
- **Real-time**: LiveKit WebRTC

### Project Structure
```
ten-days-of-voice-agents-2025/
├── backend/
│   ├── src/
│   │   ├── agent.py          # Main game logic
│   │   └── murf_tts.py       # Murf.ai integration
│   └── .env.local
├── frontend/
│   ├── components/
│   │   └── app/
│   │       ├── welcome-view.tsx
│   │       ├── session-view.tsx
│   │       └── character-sheet.tsx
│   └── .env.local
├── shared-data/
│   └── game_state.json       # Character & world state
└── livekit-server.exe
```

## 🎨 UI Customization

The cyberpunk theme uses:
- **Primary**: Cyan (#00ffff)
- **Secondary**: Purple (#a855f7)
- **Accent**: Pink (#ec4899)
- **Background**: Black (#000000)

Modify `frontend/styles/globals.css` to customize colors and effects.

## 🔧 Configuration

### Game State
Edit `shared-data/game_state.json` to customize:
- Character stats and inventory
- Starting location
- Active quests
- NPCs and world state

### Agent Behavior
Modify `backend/src/agent.py` to adjust:
- Game Master personality
- Dice rolling mechanics
- Quest generation
- Combat system

## 📝 API Keys Setup

### LiveKit
1. Sign up at [livekit.io](https://livekit.io)
2. Create a project
3. Copy API key and secret

### Murf.ai
1. Sign up at [murf.ai](https://murf.ai)
2. Get API key from dashboard
3. Use Falcon model for fastest response

### OpenAI
1. Get API key from [platform.openai.com](https://platform.openai.com)
2. Use GPT-4 for best results

## 🎯 Features Roadmap

- [ ] Multiplayer support
- [ ] Save/load game states
- [ ] Custom character creation
- [ ] More character classes
- [ ] Expanded quest system
- [ ] Combat animations
- [ ] Sound effects
- [ ] Mobile app

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Built for the [Murf.ai Voice Agents Challenge](https://murf.ai)
- Powered by [LiveKit](https://livekit.io)
- Voice synthesis by [Murf.ai](https://murf.ai)
- AI by [OpenAI](https://openai.com)

## 📧 Contact

**Ghanshyam Jha**
- GitHub: [@GhanshyamJha05](https://github.com/GhanshyamJha05)
- LinkedIn: [Connect with me](https://linkedin.com/in/ghanshyam-jha)

---

⭐ Star this repo if you found it helpful!
