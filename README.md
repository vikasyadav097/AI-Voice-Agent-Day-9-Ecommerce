# 💼 Day 5: AI SDR Agent with Lead Capture

A voice-powered Sales Development Representative (SDR) built with LiveKit Agents and Murf AI TTS that answers company questions and captures lead information naturally during conversations.

## 🎯 Features

### SDR Capabilities
- **Company FAQ** - Answers questions about Razorpay products, pricing, and services
- **Natural Lead Capture** - Collects prospect information during conversation without feeling like an interrogation
- **Professional Call Summary** - Provides closing remarks and saves lead data automatically
- **Smart Question Tracking** - Records all questions asked during the call

### Lead Information Collected
- Name
- Company
- Email
- Role/Position
- Use Case
- Team Size
- Timeline (now/soon/later)
- Questions Asked
- Conversation Summary

### Voice Integration
- **Murf AI Falcon TTS** - High-quality, natural-sounding voice (Ryan voice with Conversational style)
- **Deepgram STT** - Fast and accurate speech recognition
- **Google Gemini 2.5 Flash** - Intelligent conversation handling with function calling

## 🚀 Quick Start

### Prerequisites
- Python 3.11+
- Node.js 18+
- Murf AI API Key
- Deepgram API Key
- Google Gemini API Key
- LiveKit Server

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/GhanshyamJha05/fifth_day_Murf_api.git
cd fifth_day_Murf_api/ten-days-of-voice-agents-2025
```

2. **Setup Backend**
```bash
cd backend
python -m venv .venv
.venv\Scripts\activate  # Windows
# or
source .venv/bin/activate  # Mac/Linux

pip install -r requirements.txt  # or use uv
```

3. **Configure Backend Environment**
Create `backend/.env.local`:
```env
LIVEKIT_URL=ws://localhost:7880
LIVEKIT_API_KEY=devkey
LIVEKIT_API_SECRET=secret
DEEPGRAM_API_KEY=your_deepgram_key
GOOGLE_API_KEY=your_gemini_key
MURF_API_KEY=your_murf_key
```

4. **Setup Frontend**
```bash
cd ../frontend
npm install
```

5. **Configure Frontend Environment**
Create `frontend/.env.local`:
```env
LIVEKIT_URL=ws://localhost:7880
LIVEKIT_API_KEY=devkey
LIVEKIT_API_SECRET=secret
NEXT_PUBLIC_LIVEKIT_URL=ws://localhost:7880
```

### Running the Application

1. **Start LiveKit Server** (Terminal 1)
```bash
cd ten-days-of-voice-agents-2025
./livekit-server.exe --dev  # Windows
# or
./livekit-server --dev  # Mac/Linux
```

2. **Start SDR Agent** (Terminal 2)
```bash
cd backend
.venv\Scripts\activate  # Windows
python src/agent.py dev
```

3. **Start Frontend** (Terminal 3)
```bash
cd frontend
npm run dev
```

4. **Open Browser**
Navigate to `http://localhost:3000`

## 💬 Example Conversation

```
SDR: "Hi! Welcome to Razorpay. What brings you here today?"

You: "I'm looking for a payment solution for my online store"

SDR: "That's great! What's your name?"

You: "I'm John from TechStore"

SDR: "Nice to meet you, John! What kind of products does TechStore sell?"

You: "We sell electronics. How much does your payment gateway cost?"

SDR: "Our pricing is simple - 2% for domestic cards, UPI is free, and there are no setup fees!"

You: "That sounds good. I'm ready to move forward"

SDR: "Thank you so much for your time, John! I've captured all the details about TechStore..."
```

## 📁 Project Structure

```
.
├── backend/
│   ├── src/
│   │   ├── agent.py          # Main SDR agent with lead capture
│   │   └── murf_tts.py       # Murf AI TTS integration
│   ├── .env.local            # Backend environment variables
│   └── pyproject.toml        # Python dependencies
├── frontend/
│   ├── app/                  # Next.js app directory
│   ├── components/           # React components
│   ├── .env.local           # Frontend environment variables
│   └── package.json         # Node dependencies
├── shared-data/
│   ├── day5_company_faq.json # Razorpay FAQ and company info
│   └── leads.json            # Captured leads (auto-created)
├── challenges/
│   └── Day 5 Task.md         # Day 5 challenge documentation
└── livekit-server.exe        # LiveKit server binary
```

## 🔧 Customization

### Change Company Information

Edit `shared-data/day5_company_faq.json` to customize:
- Company name and description
- Products and services
- Pricing information
- FAQ questions and answers

### Modify Voice Settings

In `backend/src/agent.py`, update the TTS configuration:
```python
tts=murf_tts.TTS(
    voice="en-US-ryan",  # Change voice
    style="Conversational",  # Change style
    tokenizer=tokenize.basic.SentenceTokenizer(
        min_sentence_len=5,  # Adjust for faster/slower responses
    ),
)
```

### Adjust Lead Fields

Modify the `lead_data` dictionary in `agent.py` to capture different information.

## 📊 Viewing Captured Leads

Leads are automatically saved to `shared-data/leads.json` after each call. Each lead includes:
- Timestamp
- All collected information
- Questions asked during the call
- Conversation summary

## 🛠️ Tech Stack

- **Backend**: Python 3.11, LiveKit Agents SDK
- **Frontend**: Next.js 15, React, TypeScript
- **Voice**: Murf AI Falcon TTS, Deepgram STT
- **LLM**: Google Gemini 2.5 Flash
- **Real-time**: LiveKit WebRTC

## 📝 API Keys Required

1. **Murf AI** - Get from [murf.ai](https://murf.ai)
2. **Deepgram** - Get from [deepgram.com](https://deepgram.com)
3. **Google Gemini** - Get from [ai.google.dev](https://ai.google.dev)

## 🎓 Learning Resources

- [LiveKit Agents Documentation](https://docs.livekit.io/agents/)
- [Murf AI API Docs](https://murf.ai/api-docs)
- [Deepgram API Docs](https://developers.deepgram.com/)
- [Google Gemini API Docs](https://ai.google.dev/docs)

## 🤝 Contributing

This is a challenge project, but feel free to fork and customize for your own use cases!

## 📄 License

MIT License - See LICENSE file for details

## 🙏 Acknowledgments

Built as part of the Murf AI Voice Agent Challenge - Day 5
- Challenge by Murf AI
- LiveKit for the amazing agents framework
- Razorpay for the example company data

---

**Made with ❤️ by Ghanshyam Jha**
