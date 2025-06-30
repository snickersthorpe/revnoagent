# 🛠️ Auto Welcome Email Bot (Manual Make.com Build Guide)

> **This is a manual Make.com build guide, not an import file.**

---

## 📋 Module Order & Settings

1. **GoHighLevel: Watch Contacts**
   - **Trigger:** `contact.created`
   - **Connection:** `GHL_Conn`

2. **OpenAI: Create Completion**
   - **Model:** `gpt-4o`
   - **Connection:** `OpenAI_Conn`
   - **Prompt:**
     ```text
     Write a friendly 100-word welcome email to {{1.firstName}} from Revno.
     Tone: helpful, warm, one emoji max.
     Mention we'll be in touch soon.
     ```
   - **Output Variable:** `emailBody`
   - **Map:** `firstName` from Step 1 into the prompt

3. **GoHighLevel: Send Email**
   - **To:** `{{1.email}}`
   - **Subject:** `Welcome to Revno!`
   - **Body:** `{{2.emailBody}}`
   - **Connection:** `GHL_Conn`

4. **GoHighLevel: Create Note**
   - **Contact ID:** `{{1.id}}`
   - **Content:** `Sent welcome email`
   - **Connection:** `GHL_Conn`

---

## 🔗 Required Connections
- `GHL_Conn` (GoHighLevel)
- `OpenAI_Conn` (OpenAI)

---

## 🧪 Testing Notes
- Use a test contact in GoHighLevel to trigger the scenario.
- Check that the email is sent and a note is added to the contact.
- If the email or note doesn't appear, check your mapping and connection settings.

---

## 📝 What to Map
- `firstName`, `email`, and `id` from Step 1 to later steps.
- The OpenAI prompt should use the mapped `firstName`.
- The email body from Step 2 is used in Step 3.

---

**Tip:** Always test with real or sample data and check the GoHighLevel contact record for both the email and the note. 