# Create an AI Chatbot for Any WordPress Site (RAG) - Lesson 08

## Files Included

| File | Description |
|------|-------------|
| `Flow-1-Update-Vector-Database.json` | n8n workflow to fetch WordPress posts and store in vector database |
| `Flow-2-HRC-ChatBot.json` | n8n workflow for chatbot webhook responses |
| `chat-widget.html` | Code for the Chat widget on Wordpress site

---

## WordPress Setup

### Step 1: Install Plugin

1. Login to WordPress Admin Panel
2. Go to **Plugins → Add New**
3. Search for **"WPCode Lite"** by **WPCode**
4. Install and Activate

### Step 2: Add Chat Widget Code

1. Go to **Code Snippets → + Add Snippet**
2. Select **"Add Your Custom Code (New Snippet)"**
3. Choose **HTML Snippet**
4. Set location to **Site Wide Footer**
5. Paste the code from `chat-widget.html`
6. Activate the snippet

### Step 3: Update Your Webhook URL

In the code, `chat-widget.html` find this line:

```javascript
webhookUrl: 'https://your-n8n-webhook-url/webhook/0476ea4a-06f5-40c5-452fc-c4876a8541cd/chat',
```

Replace it with **your actual n8n webhook URL of the Flow-2-ChatBot.json Workflow**.

You can also customize the text and branding in the code.

---

## How to Import n8n Workflows

1. Open n8n
2. Click **"..."** menu → **"Import from File"**
3. Select the JSON file
4. Update credentials (WordPress, Vector DB, AI provider)
5. Activate the workflow

### Import Order:

1. First: `Flow-1-Update-Vector-Database.json` — run this once to index your posts
2. Then: `Flow-2-ChatBot.json` — this handles chat responses

---

## Need Help?

📞 Book a 1-on-1: https://cal.com/muhamadshamsi

✉️ contact@muhamadshamsi.com

🌐 https://muhamadshamsi.com
