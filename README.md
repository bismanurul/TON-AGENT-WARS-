# ⚡ TON AGENT WARS — Mainnet Edition

> **Hackathon Submission** · TON Ecosystem · User-Facing AI Agents + Agent Infrastructure Tracks · $10,000 Prize Pool

![TON Agent Wars](https://img.shields.io/badge/TON-Mainnet-0088cc?style=for-the-badge&logo=telegram)
![License](https://img.shields.io/badge/License-MIT-ffb300?style=for-the-badge)

TON address claim reward hackaton = UQA82xd8FoBc0aTHfNvm0UZbZfyWPxdX4ibBLd8KmNwaTnRM

## 🎮 Overview

**TON Agent Wars** is a professional browser-based RPG where AI agents battle across the TON blockchain network. Players deploy intelligent agents powered by Claude AI, fight malicious nodes and legendary bosses, and earn real TON rewards on Mainnet.

### Live Demo
🔗 **[Play Now → https://YOUR_USERNAME.github.io/ton-agent-wars](https://YOUR_USERNAME.github.io/ton-agent-wars)**

---

## 🏆 Hackathon Tracks

| Track | Implementation |
|---|---|
| **User-Facing AI Agents** | Claude-powered Battle Agent with real-time Q&A, strategy analysis, and auto-execution |
| **Agent Infrastructure** | TON Connect Mainnet wallet integration, on-chain reward tracking, agent-to-agent combat system |

---

## ✨ Features

### 🤖 AI Battle Agent (Claude Sonnet)
- Real-time combat strategy analysis via Claude API
- **Auto-executes** the optimal move based on battle state (HP%, MP%, enemy type, zone)
- Full **Q&A chat** — ask anything about strategy, TON blockchain, or game mechanics
- Persistent conversation memory across turns
- Typing indicator with live streaming feel

### 🔗 TON Connect — Mainnet
- Full **TON Connect 2.0** protocol integration
- Supports **Tonkeeper**, MyTonWallet, TonHub, and all TON Connect wallets
- Real balance fetched from **TonCenter Mainnet API**
- Live wallet address displayed in banner + game panels
- On-chain reward claim flow (production-ready hook)
- Wallet state persisted across sessions via `restoreConnection()`

### ⚔️ Gameplay
- **3 Agent Classes**: Validator (ATK), Oracle (MP/AoE), Guardian (DEF/reflect)
- **6 Network Zones**: Mainnet → Testnet → DeFi Hub → TON Bridge → Genesis → Hackathon
- **4 Unique Bosses**: The Rug Master, Bridge Daemon, Genesis Virus, Final Judge AI
- Boss intro cinematic with stats overlay
- Critical hits, DEF piercing, status effects (dodge, reflect, stun)
- MP regen, level-up system, XP progression
- Real-time damage floaters and arena flash effects

### 🎨 Professional UI
- Cyberpunk neo-noir design — Orbitron + Rajdhani + JetBrains Mono typestack
- Scanline overlay, animated grid background, vignette
- 3-column responsive layout (Status | Arena | AI Agent)
- Animated sprites with glow effects and floating animations
- Combat log with timestamp, status strip with live buffs/debuffs
- Battle history tracker with TON reward display

---

## 🚀 Quick Start

### Option 1: GitHub Pages (Recommended)
```bash
# 1. Fork this repo
# 2. Go to Settings → Pages → Source: main branch / root
# 3. Update tonconnect-manifest.json with your GitHub Pages URL
# 4. Done! Your game is live at https://USERNAME.github.io/ton-agent-wars
```

### Option 2: Local Development
```bash
git clone https://github.com/YOUR_USERNAME/ton-agent-wars.git
cd ton-agent-wars

# Serve with any static server (manifest must be served over HTTP)
npx serve .
# or
python3 -m http.server 8080
```

Open `http://localhost:8080` in your browser.

---

## ⚙️ Configuration

### 1. TON Connect Manifest
Edit `tonconnect-manifest.json`:
```json
{
  "url": "https://YOUR_USERNAME.github.io/ton-agent-wars",
  "name": "TON Agent Wars",
  "iconUrl": "https://YOUR_USERNAME.github.io/ton-agent-wars/assets/icon.png"
}
```

### 2. Update Manifest URL in `index.html`
Find and replace:
```javascript
// Line ~200 in index.html
const MANIFEST_URL = 'https://YOUR_USERNAME.github.io/ton-agent-wars/tonconnect-manifest.json';
```

### 3. Claude API (Optional — works without key for demo)
The game uses the Anthropic API via the Claude.ai artifact system. For standalone deployment, add your API key:
```javascript
// In the callClaude() function, add header:
'x-api-key': 'YOUR_ANTHROPIC_API_KEY'
```

> ⚠️ **Never expose API keys in frontend code for production.** Use a backend proxy.

---

## 🏗️ Architecture

```
ton-agent-wars/
├── index.html                 # Main game (single-file app)
├── tonconnect-manifest.json   # TON Connect dApp manifest
├── assets/
│   └── icon.png               # App icon (add your own)
├── docs/
│   ├── terms.md               # Terms of use
│   └── privacy.md             # Privacy policy
└── README.md
```

### Tech Stack
| Layer | Technology |
|---|---|
| Frontend | Vanilla HTML/CSS/JS (zero dependencies) |
| AI Agent | Anthropic Claude Sonnet (`claude-sonnet-4-20250514`) |
| Wallet | TON Connect UI v2 (`@tonconnect/ui@latest`) |
| Balance API | TonCenter Mainnet REST API |
| Fonts | Google Fonts (Orbitron, Rajdhani, JetBrains Mono) |

---

## 🔮 Roadmap (Post-Hackathon)

- [ ] Smart contract for on-chain reward distribution
- [ ] Leaderboard stored on TON chain
- [ ] NFT agent skins as SBT (Soulbound Tokens)
- [ ] Multiplayer agent-vs-agent battles
- [ ] Agent coordination via TON smart contracts (Agent Infrastructure)
- [ ] Telegram Mini App integration

---

## 📜 How TON Connect Works

```
User clicks "Connect Wallet"
        ↓
TON Connect UI opens modal
        ↓
User scans QR or selects wallet
        ↓
Wallet approves connection
        ↓
onStatusChange(wallet) fires
        ↓
App receives address + chain info
        ↓
TonCenter API fetches real balance
        ↓
Wallet address displayed in-game
```

---

## 🤝 Contributing

Pull requests welcome! For major changes, open an issue first.

```bash
git checkout -b feature/my-feature
git commit -m 'feat: add my feature'
git push origin feature/my-feature
```

---

## 📄 License

MIT © 2025 — Built for the TON Hackathon

---

## 🙏 Credits

- [TON Connect SDK](https://github.com/ton-connect/sdk) — Wallet integration protocol
- [Anthropic Claude](https://anthropic.com) — AI battle strategy engine
- [TonCenter API](https://toncenter.com) — Mainnet balance queries
- Built with ❤️ for the TON Ecosystem

---

*⚡ TON AGENT WARS — Where AI meets blockchain in battle*
