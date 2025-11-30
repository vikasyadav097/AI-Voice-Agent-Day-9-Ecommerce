🛍️ Day 9 — E-commerce Voice Shopping Agent

A fully functional voice-powered online shopping assistant built using LiveKit Agents, Next.js, and Murf TTS, featuring natural voice conversations, real-time cart updates, and a beautiful cyberpunk shopping UI.

🌟 Features
🧠 Voice Shopping Assistant

Natural conversations with your AI shopping buddy (Alex)

Product discovery: Ask anything about items, pricing, or inventory

Smart cart management: Add/remove items using voice commands

Voice checkout: Complete your order simply by talking

🛒 Real-time Shopping Cart

Live syncing between voice agent & UI

File-based persistence (cart.json)

Cyberpunk UI with smooth animations

Add/remove items with instant visual feedback

📦 Order Management

Unique Order ID generated automatically

Order history stored as JSON

Complete order summary with totals

Success animation on checkout

🛠️ Tech Stack
Frontend

Next.js 15

React + TypeScript

Tailwind CSS

Framer Motion

Backend

Python

LiveKit Agents SDK

Voice & AI

Deepgram Speech-to-Text

Google Gemini 2.0 Flash

Murf.ai TTS

Storage

JSON file-based database

📦 Product Catalog
☕ Mugs

Cyberpunk Coffee Mug — ₹899

Hacker's Energy Mug — ₹1299

👕 T-Shirts (S, M, L, XL)

Neural Network Tee — ₹799

AI Developer Tee — ₹699

🧥 Hoodies (M, L, XL)

Cyberpunk Hoodie — ₹1999

Code Warrior Hoodie — ₹2299

🎧 Accessories

Tech Geek Cap — ₹499

Developer Backpack — ₹2499

RGB Gaming Mouse — ₹1499

Mechanical Keyboard — ₹3999

🚀 Quick Start
📌 Prerequisites

Python 3.10+

Node.js 18+

pnpm

LiveKit account (cloud or local)

API Keys: Deepgram, Google AI, Murf

📥 Setup
1️⃣ Clone the repository
git clone https://github.com/vikasyadav097/AI-Voice-Agent-Day-9-Ecommerce 
🖥️ Backend Setup
cd backend
python -m venv .venv


Activate venv:

Windows:

.venv\Scripts\activate


Mac/Linux:

source .venv/bin/activate


Install packages:

pip install -r requirements.txt


Create env file:

cp .env.example .env.local


Add your API keys to .env.local.

🎨 Frontend Setup
cd frontend
pnpm install
cp .env.example .env.local


Add your LiveKit credentials.

🛰️ Start LiveKit Server (root folder)

Windows:

.\livekit-server.exe --dev


Mac/Linux:

./livekit-server --dev

🤖 Start Backend Agent
cd backend
.venv\Scripts\python.exe src/agent.py dev

🌐 Start Frontend
cd frontend
pnpm dev


Open: http://localhost:3001

💬 Voice Commands
🔍 Browsing

“What products do you have?”

“Tell me about the gaming mouse.”

“Show me hoodies.”

“What's the price of the keyboard?”

🛒 Adding Items

“Add the keyboard to my cart.”

“I want a mouse.”

“I’ll take the hoodie in size large.”

🧹 Cart Management

“What’s in my cart?”

“Remove the mouse.”

“Show my cart.”

💳 Checkout

“I’m ready to checkout.”

“Complete my order.”

“Checkout please.”

🎨 UI Features
📚 Product Catalog (Left Panel)

Browse products

Add items with a button

Neon cyberpunk visual effects

🛒 Shopping Cart (Right Panel)

Real-time item updates

Quantity + total price

Trash icon to remove items

✔️ Checkout Animation

Green checkmark

Order summary

Auto-close after 5 seconds

📁 Project Structure
backend/
 ├── src/
 │    ├── agent.py
 │    ├── commerce.py
 │    └── murf_tts.py
 └── .env.local

frontend/
 ├── app/
 │   └── api/
 │       ├── cart/
 │       ├── checkout/
 │       └── products/
 ├── components/app/
 │       ├── product-catalog.tsx
 │       ├── shop-cart.tsx
 │       └── session-view.tsx
 └── .env.local

shared-data/
 ├── catalog.json
 ├── cart.json
 └── orders/

livekit-server.exe

🔧 Configuration
Backend .env.local
LIVEKIT_URL=ws://localhost:7880
LIVEKIT_API_KEY=your_key
LIVEKIT_API_SECRET=your_secret
DEEPGRAM_API_KEY=your_key
GOOGLE_API_KEY=your_key
MURF_API_KEY=your_key

Frontend .env.local
NEXT_PUBLIC_LIVEKIT_URL=ws://localhost:7880
LIVEKIT_API_KEY=your_key
LIVEKIT_API_SECRET=your_secret

🎯 Key Features Implemented

✅ Voice product browsing
✅ Natural language cart control
✅ Real-time cart sync
✅ Persistent cart storage
✅ Order creation
✅ Checkout success screen
✅ Friendly AI personality
✅ Cyberpunk UI
✅ Fully responsive
✅ Error-handled backend

🐛 Troubleshooting
Cart Not Updating

Wait 2 seconds

Check shared-data/cart.json

Ensure frontend running on port 3001

Voice Agent Not Responding

Check backend logs

Verify API keys

Ensure LiveKit server is running

Checkout Issues

Make sure items are in cart

Check shared-data/orders/ exists

Verify file write permissions

📝 License

MIT License — see LICENSE file.


🙏 Acknowledgments

LiveKit for real-time infra

Murf AI for TTS

Google Gemini for intelligence

Deepgram for accurate STT

Built for 10 Days of Voice Agents Challenge — Day 9 🎉

| Day      | Status         |
| -------- | -------------- |
| Day 1    | ✅ Completed    |
| Day 2    | ✅ Completed    |
| Day 3    | ✅ Completed    |
| Day 4    | ✅ Completed    |
| Day 5    | ✅ Completed    |
| Day 6    | ✅ Completed    |
| Day 7    | ✅ Completed    |
| Day 8    | ✅ Completed    |
| Day 9    | ✅ Completed    |
| Day 10   | 🔜 Coming soon |
