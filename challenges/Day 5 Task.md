# Day 5 – Simple FAQ SDR + Lead Capture

## Implementation Status: ✅ COMPLETE

### What Was Built:

#### Company: Razorpay
- Indian fintech startup providing payment solutions
- Complete FAQ with 12+ questions
- Product information for 5 main products
- Detailed pricing information
- Target customer segments

#### SDR Agent Features

✅ **Professional SDR Persona**
- Warm, consultative greeting
- Asks about visitor's needs
- Focuses on understanding pain points
- Natural conversation flow

✅ **FAQ-Based Question Answering**
- Searches company FAQ for relevant answers
- Covers products, pricing, features, security
- Handles questions about:
  - What Razorpay does
  - Who it's for
  - Pricing and free tier
  - Integration time
  - Payment methods
  - Security and compliance

✅ **Lead Information Collection**
- Name
- Company
- Email
- Role/Position
- Use case
- Team size
- Timeline (now/soon/later)
- Questions asked during call

✅ **End-of-Call Summary**
- Detects when user is done
- Provides verbal summary
- Saves lead data to JSON file
- Professional closing

#### Technical Implementation

**Backend (`backend/src/sdr_agent.py`)**
- SDRAgent class with three main tools:
  - `search_faq` - Searches FAQ for answers
  - `collect_lead_info` - Stores lead details
  - `end_call_summary` - Ends call and saves data
- Simple keyword-based FAQ search
- JSON-based lead storage
- Murf AI TTS integration (Ryan voice)

**Content (`shared-data/day5_company_faq.json`)**
- Company information
- 5 product descriptions
- Detailed pricing structure
- 12 FAQ entries
- Target customer list
- Key benefits

**Lead Storage (`shared-data/leads.json`)**
- Automatically created when first lead is captured
- Stores all lead information
- Timestamped entries
- Conversation summaries

### How It Works

1. **User connects** → SDR greets warmly
2. **User asks questions** → SDR searches FAQ and answers
3. **SDR collects info** → Naturally asks for lead details
4. **User says "done"** → SDR summarizes and saves lead
5. **Lead stored** → JSON file with all details

### Example Conversation Flow

```
SDR: "Hi! Welcome to Razorpay. I'm here to help you learn about our payment solutions. What brings you here today?"

User: "I'm looking for a payment gateway for my e-commerce store."

SDR: "Great! I'd love to learn more about your store. What's your name?"

User: "I'm Rahul."

SDR: "Nice to meet you, Rahul! And what's your company name?"

User: "It's called ShopEasy."

SDR: "Excellent! Tell me, what kind of products do you sell?"

User: "We sell electronics online. How much does your payment gateway cost?"

SDR: [Uses search_faq tool] "Our pricing is simple - 2% for domestic cards, UPI is free, and 3% for international cards. No setup fees!"

User: "That sounds good. We have a team of 5 people."

SDR: [Uses collect_lead_info] "Got it, team of 5. When are you looking to integrate a payment solution?"

User: "We need it within the next month."

SDR: [Collects timeline] "Perfect! That's all I need to know."

SDR: [Uses end_call_summary] "Thank you, Rahul! I've captured all the details about ShopEasy and your need for payment integration within the next month. Our team will follow up with you shortly!"
```

### Files Created

1. `backend/src/sdr_agent.py` - Main SDR agent
2. `shared-data/day5_company_faq.json` - Company FAQ and info
3. `shared-data/leads.json` - Lead storage (auto-created)

### Running Day 5 Agent

```bash
# Terminal 1 - LiveKit Server
./livekit-server.exe --dev

# Terminal 2 - SDR Agent
cd backend
.venv\Scripts\activate
python src/sdr_agent.py dev

# Terminal 3 - Frontend
cd frontend
npm run dev
```

## Primary Goal: ✅ COMPLETE

All requirements met:
- ✅ SDR persona for Razorpay
- ✅ FAQ-based question answering
- ✅ Lead information collection
- ✅ End-of-call summary
- ✅ JSON storage of leads

## Advanced Goals: Not Implemented

The following advanced goals are optional and not required for Day 5 completion:
- Meeting scheduler
- CRM-style call notes & qualification score
- Persona-aware pitching
- Follow-up email draft
- Return visitor recognition

## Resources Used

- LiveKit Agents SDK
- Murf AI Falcon TTS (Ryan voice)
- Deepgram Nova-3 STT
- Google Gemini 2.5 Flash LLM
- Simple keyword-based FAQ search
