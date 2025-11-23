# Day 3 – Health & Wellness Voice Companion

## Primary Goal (Required)

Build a daily health & wellness–oriented voice agent that acts as a supportive, but realistic and grounded companion.

### Core Requirements

1. **Clear, grounded system prompt**
   - Supportive but realistic tone
   - Non-medical, non-diagnostic approach
   - Focus on practical self-care

2. **Conducts short daily check-ins via voice**
   - Ask about mood and energy
   - Inquire about stress or concerns
   - Collect 1-3 daily objectives/intentions
   - Offer simple, realistic advice
   - Close with a brief recap

3. **Persists key data from each check-in in a JSON file**
   - Store in `wellness_log.json`
   - Include: date, time, mood, energy, stress, objectives, notes

4. **Uses past data to inform the next conversation**
   - Reference previous check-ins naturally
   - Show continuity between sessions

## Implementation Status: ✅ COMPLETE

### What Was Built:

#### Backend (`backend/src/agent.py`)
- ✅ Wellness companion with supportive persona
- ✅ 5 function tools for data collection:
  - `set_mood()` - Record current mood
  - `set_energy()` - Record energy level
  - `set_stress()` - Note stress/concerns
  - `add_objective()` - Add daily goals (1-3)
  - `add_note()` - Additional reflections
  - `complete_checkin()` - Save to JSON log
- ✅ JSON persistence in `wellness_log.json`
- ✅ Previous check-in context loading
- ✅ Real-time data publishing to frontend

#### Frontend (`frontend/components/app/wellness-display.tsx`)
- ✅ Visual checklist display (similar to Day 2)
- ✅ Real-time updates as agent collects data
- ✅ Checkmark indicators for completed items
- ✅ Blue wellness theme
- ✅ Compact, non-obtrusive UI
- ✅ Completion status animation

### Data Structure

```json
{
  "check_ins": [
    {
      "date": "2025-11-23",
      "time": "22:00:00",
      "timestamp": "2025-11-23T22:00:00",
      "mood": "good",
      "energy": "high",
      "stress": "work deadline",
      "objectives": ["finish report", "exercise", "relax"],
      "notes": "feeling motivated",
      "summary": "Mood: good, Energy: high, Objectives: 3"
    }
  ]
}
```

### Conversation Flow

1. **Greeting** - Warm welcome with reference to previous session
2. **Mood Assessment** - "How are you feeling today?"
3. **Energy Check** - "What's your energy level like?"
4. **Stress Inquiry** - "Anything stressing you out?"
5. **Daily Objectives** - "What 1-3 things would you like to accomplish?"
6. **Practical Advice** - Small, actionable suggestions
7. **Recap & Confirmation** - Summary of mood, energy, and goals
8. **Data Persistence** - Save to `wellness_log.json`

## Advanced Goals (Optional)

### Advanced Goal 1: MCP Integration for Tasks/Notes
- Connect to MCP servers (Notion, Todoist, Zapier)
- Create tasks/notes in external systems
- Conversational triggers for integrations

### Advanced Goal 2: Weekly Reflection Using JSON History
- Analyze mood trends over time
- Track goal completion rates
- Provide supportive insights

### Advanced Goal 3: Follow-up Reminders via MCP Tools
- Detect time-based activities
- Create reminders via MCP
- Confirmation flow before creating

## Resources

- LiveKit Agents: https://docs.livekit.io/agents/build/tools/
- MCP Documentation: https://modelcontextprotocol.io/docs/getting-started/intro
- Example Code: https://github.com/livekit-examples/python-agents-examples/tree/main/mcp
