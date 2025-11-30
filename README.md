---

# 🛍️ Day 9 — E-commerce Voice Shopping Agent

A fully functional **voice-powered online shopping assistant** built using **LiveKit Agents, Next.js, and Murf TTS**, designed to give users a futuristic, hands-free shopping experience.

---

## 🌟 Key Features

### 🎙️ Voice Shopping Assistant

* **Natural, conversational AI assistant (Alex)** for product exploration
* **Product discovery by voice** — ask about any item
* **Smart cart management** — add/remove items via voice
* **Voice-based checkout** with smooth confirmation flow

### 🛒 Real-time Shopping Cart

* Automatic **live sync** between UI and voice agent
* **File-based persistence** for cart state
* Stylish **cyberpunk UI animations**
* Easy item management with instant feedback

### 📦 Order Management

* Auto-generated **unique order IDs**
* All orders stored safely as JSON
* View complete order breakdown (items + total)
* Clean checkout success animation

---

## 🛠️ Tech Stack

### Frontend

* Next.js 15
* React + TypeScript
* Tailwind CSS
* Framer Motion

### Backend

* Python
* LiveKit Agents SDK

### Voice & AI

* Deepgram STT
* Google Gemini 2.0 Flash
* Murf TTS

### Real-time

* LiveKit WebRTC

### Storage

* JSON file-based data handling

---

## 🛍️ Product Catalog

### ☕ Mugs

* Cyberpunk Coffee Mug — ₹899
* Hacker's Energy Mug — ₹1299

### 👕 T-Shirts (S, M, L, XL)

* Neural Network T-Shirt — ₹799
* AI Developer Tee — ₹699

### 🧥 Hoodies (M, L, XL)

* Cyberpunk Hoodie — ₹1999
* Code Warrior Hoodie — ₹2299

### 🎒 Accessories

* Tech Geek Cap — ₹499
* Developer Backpack — ₹2499
* RGB Gaming Mouse — ₹1499
* Mechanical Keyboard — ₹3999

---

## ⚡ Quick Start Guide

### 🔑 Prerequisites

* Python 3.10+
* Node.js 18+
* pnpm
* LiveKit Cloud account (or local server)
* API keys: Deepgram, Gemini, Murf

---

### 1️⃣ Clone Repository

```bash
git clone https://github.com/vikasyadav097/AI-Voice-Agent-Day-9-Ecommerce 
```

### 2️⃣ Backend Setup

```bash
cd backend
python -m venv .venv
.venv\Scripts\activate      # Windows
source .venv/bin/activate   # Mac/Linux
pip install -r requirements.txt
cp .env.example .env.local
# Add API keys to .env.local
```

### 3️⃣ Frontend Setup

```bash
cd frontend
pnpm install
cp .env.example .env.local
# Add LiveKit credentials
```

### 4️⃣ Start LiveKit Server

```bash
.\livekit-server.exe --dev      # Windows
./livekit-server --dev          # Mac/Linux
```

### 5️⃣ Start Backend Agent

```bash
cd backend
.venv\Scripts\python.exe src/agent.py dev
```

### 6️⃣ Start Frontend

```bash
cd frontend
pnpm dev
```

### 7️⃣ Open Browser

👉 [http://localhost:3001](http://localhost:3001)

---

## 🎤 Supported Voice Commands

### 🔍 Browsing

* “What products do you have?”
* “Show me hoodies”
* “Tell me about the gaming mouse”

### ➕ Add to Cart

* “Add the keyboard to my cart”
* “I want a mouse”
* “Take a hoodie in size large”

### 🗑️ Cart Management

* “What’s in my cart?”
* “Show my cart”
* “Remove the mouse”

### 💳 Checkout

* “Checkout please”
* “Complete my order”

---

## 🎨 UI Highlights

### 📚 Product Catalog (Left Panel)

* View all products with images, prices & features
* Quick “Add to Cart” button
* Smooth hover & click animations

### 🛒 Shopping Cart (Right Panel)

* Real-time updates
* Quantities & totals
* Remove items instantly
* Checkout button with animations

### ✔️ Success Screen

* Smooth checkmark animation
* Order summary popup
* Auto-dismiss after 5 seconds

---

## 📁 Project Structure

```
├── backend/
│   ├── src/
│   │   ├── agent.py
│   │   ├── commerce.py
│   │   └── murf_tts.py
│   └── .env.local
├── frontend/
│   ├── app/
│   ├── components/
│   └── .env.local
├── shared-data/
│   ├── catalog.json
│   ├── cart.json
│   └── orders/
└── livekit-server.exe
```

---

## 🔧 Environment Variables

### Backend `.env.local`

```env
LIVEKIT_URL=ws://localhost:7880
LIVEKIT_API_KEY=your_key
LIVEKIT_API_SECRET=your_secret
DEEPGRAM_API_KEY=your_key
GOOGLE_API_KEY=your_key
MURF_API_KEY=your_key
```

### Frontend `.env.local`

```env
NEXT_PUBLIC_LIVEKIT_URL=ws://localhost:7880
LIVEKIT_API_KEY=your_key
LIVEKIT_API_SECRET=your_secret
```

---

## 🐛 Troubleshooting Guide

### ❌ Cart Not Updating?

* Wait 2 seconds for polling
* Check `shared-data/cart.json`
* Ensure frontend is running on port 3001

### 🎙️ Voice Agent Not Responding?

* Check backend terminal logs
* Verify API keys
* Ensure LiveKit server is active

### 💳 Checkout Issues?

* Ensure cart has at least one item
* Confirm `shared-data/orders/` exists
* Check file permissions

---

## 📝 License

MIT — see `LICENSE` for details.

---


---

## 🎉 Acknowledgements

* LiveKit — real-time infrastructure
* Murf AI — fast & natural TTS
* Google Gemini — intelligent reasoning
* Deepgram — accurate STT

---

## 🚀 Built For

**10 Days of Voice Agents Challenge — Day 9**

---

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

