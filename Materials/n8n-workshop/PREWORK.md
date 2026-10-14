# Pre-work: do this before the workshop

It takes about 15 minutes. You need a phone with Telegram and a laptop connected to NetBird.

## 1. Connect to the staging n8n

1. Make sure NetBird is connected on your laptop.
2. Open https://lxc-staging-n8n-idn-umn.TheIOFoundation.net
3. Log in with the account you were given. If you have no account yet, tell the instructor.

## 2. Create your Telegram bot (needed from flow F3)

1. Install Telegram on your phone.
2. Open a chat with **@BotFather** (the account with the blue tick).
3. Send `/newbot`. Give it a name and a username that ends in `bot`.
4. BotFather replies with a **token**. Copy it. Treat it like a password and never share it or paste it in a chat.
5. Open your new bot from the link BotFather gives you and press **Start**. A bot cannot message you until you do this.
6. Send any message to **@get_id_bot**. It replies with your **chat ID** (a number). Write it down.

## 3. Create your Telegram credential in n8n

1. In n8n open **Credentials** and choose **Create credential**.
2. Pick **Telegram API**.
3. Paste your token and save. n8n tests it for you.

## 4. Get a free Gemini API key (needed from flow F6)

1. Go to https://aistudio.google.com and sign in with your @Community account.
2. Click **Get API key** and then **Create API key**.
3. Copy the key. Treat it like a password.
4. In n8n create a **Google Gemini(PaLM) API** credential and paste the key. Save.

If AI Studio refuses your account, tell the instructor before the workshop.

## 5. Get your own NASA API key (needed for flow F4)

1. Go to https://api.nasa.gov and fill in the Generate API Key form (first name, last name and email).
2. The key appears on the page straight away. NASA also emails it to you.
3. Keep it. In flow F4 you paste it in the **My Settings** node, in the field `nasaKey`, instead of `DEMO_KEY`.

Do not use `DEMO_KEY` in the room: the whole class shares one limit and it runs out fast.

## After the workshop

- Delete your Gemini API key in AI Studio.
- Send `/revoke` to @BotFather to invalidate your bot token (or `/deletebot` to delete the bot).
