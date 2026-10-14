# n8n workshop materials (Argos Club UMN, 15 Oct 2026)

Seven beginner flows of increasing difficulty for the Argos Club n8n workshop. Every attendee builds or imports them on the staging n8n instance.

Before the session, everyone must complete [PREWORK.md](PREWORK.md).

## The flows

| # | File | What it does | Mode in the room | Needs |
|---|------|--------------|------------------|-------|
| F1 | `flows/F1-city-weather.json` | Live weather sentence for your city | Built together | Nothing |
| F2 | `flows/F2-earthquake-radar.json` | Top 5 strong earthquakes of the last 24 hours | You build it | Nothing |
| F3 | `flows/F3-phone-buzz.json` | The strongest 3 quakes land on your phone | Guided | Telegram |
| F4 | `flows/F4-morning-briefing.json` | Scheduled briefing: weather plus NASA picture of the day | Import then complete | Telegram |
| F5 | `flows/F5-neighbours-form.json` | A web form that sends messages to your Telegram | Import then modify | Telegram |
| F6 | `flows/F6-ai-news-anchor.json` | Gemini writes a quake bulletin in the language and tone you pick | Import then edit the prompt | Telegram and Gemini |
| F7 | `flows/F7-agent-with-tools.json` | Chat with an AI agent that uses weather, Wikipedia and a calculator | You build it | Gemini |

## How to import a flow

Option A, Import from URL (works only if this repository is public): open a new workflow in n8n, click the three dots menu, choose **Import from URL** and paste the raw link of the file.

Option B, copy and paste: open the file on GitHub, click **Raw**, select everything and copy it. Click on the empty n8n canvas and press Ctrl+V.

After importing:

1. Open each Telegram or Gemini node and choose **your own** credential.
2. Replace `PUT-YOUR-CHAT-ID-HERE` with your Telegram chat ID (F3 and F5 in the Telegram nodes; F4 and F6 in the **My Settings** node).
3. Run the flow with **Execute workflow**.

Credentials are never included in these files. Each attendee creates their own.

## Notes for the instructor

- The staging instance is reachable over NetBird only. Telegram Trigger and any incoming webhook from the Internet will not work. All flows only send messages.
- F4 uses the NASA key `DEMO_KEY` by default. It allows 30 requests per hour per IP, and the room shares one IP. Replace it with a real key in **My Settings** before the session.
- F6 and F7 use the model `models/gemini-3.1-flash-lite`. Check at rehearsal that the key accepts it.
- Each flow has a Notes box with its challenge.

## Closing checklist for attendees

- Delete your Gemini API key in Google AI Studio.
- Revoke or delete your Telegram bot (send `/revoke` or `/deletebot` to @BotFather).
