📘 MASTER PROMPT — JINROU GAME SYSTEM (FOR CODEX)
🔧 System Context

You are building a full-stack game system.

Before writing any gameplay code:

Check if a project exists
If not, create a new project
Assume Codex is available in the Home Dictionary
Structure code modularly (backend + real-time + UI-ready)
🎮 Game Overview

Create a Jinrou-Game (social deduction) inspired by Among Us, with:

Roles
Day/Night cycles
Chat-based interaction (Discord-like)
AI + Human modes
Real-time decision system
👥 Roles
🟢 Allies (80%)
Normal Person (50%)
No abilities
Can vote
Can be protected
Telepathy (20%)
Can scan players for signals:
Role (high corruption risk)
Alignment
Action trace
Threat level
Vote intent
Consistency
Kill intent (10% accuracy)
Life status (100% accuracy)
1 scan per night
Results may be corrupted
Final weekend → ALWAYS corrupted (except life status)
Knight (10%)
Protect 1 player per Fortnight
Can kill 1 player per 2 weekends
Protector
Protects players (standard protection system)
🔴 Enemies (20%)
Wolf (5%)
Kill:
1 per night
2 on weekends
Cannot vote
Can appear to vote (fake voting system)
Betrayer (15%)
Kill:
0.5 per night
1 on weekends
Cannot vote (but can fake vote)
Can corrupt Telepathy results
🧠 Core Mechanics
🌗 Day / Night System
Night Types
Normal Night
Weekend (every 7th day)
Fortnight (every 14th day)
Day Types
Normal Day → discussion
Extra Long Day → weekend
Vote Day → fortnight
🔄 Auto Progression

Phases:

Protect
Telepathy
Kill
Done → resolve → Day
💬 Chat System (Discord-Like)
Channels
#general
Day only
All players
#vote
Vote phase only
Everyone can “vote”
Only valid votes count
#killed
Read-only
Shows results
Private Channels (Night)
Allies → #allies-private
Killers → #killers
Kill vote → #kill-vote (bot-controlled)
🔌 Night Behavior
Normal players:
Disconnected
See 404 screen + timer
🗳️ Voting System
Dual Layer
Real Votes
Only valid roles count
Fake Votes
Everyone appears to vote
Output Example
Player1 voted for Player3
🔮 Telepathy System
Scan Types
Role
Alignment
Action
Threat
Vote prediction
Consistency
Connection
Kill intent (10%)
Life status (100%)
Corruption Rules
Betrayer can corrupt
Final Weekend:
ALL scans corrupted
Except life status
Output Style

Use varied text:

“is”
“appears to be”
“likely”
glitched text occasionally
🎡 Wheel of Fate

Each player:

Can roll once (optional)
Outcomes
Change role
Self death
Private role reveal
Kill another player
Lucky protection (new)
Lucky Protection
~5% chance to survive any kill
Applies after protection
Hidden from players
🔪 Kill System

Order:

Protection
Lucky protection
Kill
🧠 AI System

Each bot has:

Personality traits:
aggression
confidence
deception
logic
social
noise
loyalty
AI Capabilities
Vote based on beliefs
React to chat
Fake vote if needed
Interpret Telepathy (not blindly trust)
Possibly lie
🎭 Text Style System

Bots use:

Casual text
Hesitation
Confidence
Glitch text
🏁 Win Conditions
Crew wins → all Wolves eliminated
Wolves win → equal or outnumber others
Betrayer wins with Wolves
🌐 Multiplayer System
Modes
Human Mode
Real chat
Custom + preset messages
Join via:
{Domain}/pin/{Code}
AI Mode
Preset messages only
Fully simulated
🧱 Technical Requirements
Use modular architecture
Real-time system (WebSocket or equivalent)
Role-based permission system
Event-driven game loop
Server-authoritative logic
⚠️ Constraints
No UI leaks of hidden mechanics
No direct truth exposure
Maintain uncertainty
Balance randomness vs skill
🚀 Output Requirement

Generate:

Backend architecture
Game loop system
Role system
Chat system
AI system
API endpoints
Data models
END PROMPT
