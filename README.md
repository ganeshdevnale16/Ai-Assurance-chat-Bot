# AI Assurance Chat Bot – Demo

A dummy government-style portal (**National Roads & Highways Department – Demo**) with a floating virtual assistant, **Sadak Mitra**, built to show clients how AI Assurance limits and corrects a misbehaving chatbot.

> This is a fictional demonstration website by Devnale Globals. It is not affiliated with any government body.

## What it shows

| Guardrail | Bot behaviour |
|-----------|---------------|
| **Off** | The bot replies rudely and gives illegal or unsafe advice (bribery, drink driving, hit-and-run, skipping helmets, etc.). Each reply is tagged “Unmonitored reply”. |
| **On** | Every reply passes an AI Assurance check (tone, legal compliance, safety, policy). Violations are flagged with scores and law references, the original reply is blocked, and a compliant reply is shown instead. |

## Features
- Realistic Indian government portal layout: accessibility bar, A-/A/A+ font sizes, contrast (dark) mode, tricolour strip, notices/tenders tabs, news ticker
- Full **English / हिन्दी** language switch (site and chatbot)
- Floating chat icon → chat window with typing indicator, quick-reply chips, mobile full-screen
- **Demo controls** panel (bottom-left): guardrail switch, live counters (replies checked, violations caught, replies corrected), reset chat

## Demo script
1. Open the chat and ask: *“Can I drive after 2 drinks?”* (guardrail off) → rude, unsafe reply.
2. Expand **AI Assurance demo controls** and switch the guardrail **on**.
3. Ask the same question → watch the check run, the reply get blocked, and the corrected answer appear. Click **See what was blocked**.
4. Switch to **हिन्दी** and repeat.

Topics the bot understands: greeting, driving licence, e-challan, helmet/seat belt, drink driving, speeding, accidents, potholes/complaints, FASTag/toll, vehicle registration, thanks.

## Run locally
It is a single static file. Open `index.html` in a browser, or:
```bash
npx serve .
```

## Deploy
- **GitHub Pages:** Settings → Pages → Deploy from branch → `main` / root.
- **Render:** New → Static Site → publish directory `.` (no build command).

## Next steps
- Replace the scripted replies with a live LLM (e.g. Azure OpenAI) for the “unguarded” bot
- Run the AI Assurance check as a real moderation/compliance model between the LLM and the user
