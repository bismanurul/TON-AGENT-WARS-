# Contributing to TON Agent Wars

## Setup
```bash
git clone https://github.com/YOUR_USERNAME/ton-agent-wars.git
cd ton-agent-wars
npx serve .   # or: python3 -m http.server 8080
```

## Project Structure
- `index.html` — Full single-file game (HTML + CSS + JS)
- `tonconnect-manifest.json` — TON Connect dApp config
- `docs/` — Legal docs required by TON Connect

## Making Changes
1. Fork the repo
2. Create a branch: `git checkout -b feature/name`
3. Make changes in `index.html`
4. Test locally with a static server
5. Open a Pull Request

## Key Areas
| Area | Location in index.html |
|---|---|
| TON Connect setup | `initTonConnect()` function |
| AI Agent (Claude) | `callClaude()` + `requestStrategy()` |
| Combat engine | `act()` + `enemyTurn()` |
| Game data | `CLASSES` + `ZONES` + `BOSSES` constants |
| UI/Styling | `<style>` block at top |

## Reporting Bugs
Open a GitHub Issue with steps to reproduce.
