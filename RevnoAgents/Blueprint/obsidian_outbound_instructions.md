# 📤 How to Send a File from Make.com into My Obsidian Vault

This guide shows how to send a Markdown note (like a log or update) from Make.com into your GitHub repo — and have it show up automatically in your Obsidian vault.

---

## 🔧 What You'll Need

- A **Make.com account**
- A **GitHub repo** (yours is: `snickersthorpe/revnoagents`)
- Your **Obsidian vault** already synced with GitHub (yours is)
- A **GitHub token** with access to update your repo (you've already created this)

---

## ✅ Step 1: Open Make.com

1. Go to [https://make.com](https://make.com)
2. Click "Create a new Scenario"

---

## ✅ Step 2: Add a Webhook

This webhook is like a door that waits for data.

1. Search for **Webhooks** → choose **Custom webhook**
2. Click **Add** → name it `obsidian_outbound`
3. Click **Run once**
4. Copy the URL Make gives you (you'll use it in the next step)

---

## ✅ Step 3: Send a Test Message to the Webhook

This helps Make.com understand what kind of data you'll send.

### If using Cursor:
1. Open your terminal in Cursor
2. Paste this command **(change the URL to your webhook)**:

```bash
curl -X POST https://hook.us2.make.com/YOUR_WEBHOOK_URL_HERE \
  -H "Content-Type: application/json" \
  -d '{
    "path": "logs/test_log.md",
    "content": "# ✅ Hello from Make!",
    "commit_msg": "Add test log file"
  }'
``` 