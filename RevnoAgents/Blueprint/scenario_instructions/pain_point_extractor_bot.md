# 🛠️ Pain Point Extractor Bot (Manual Make.com Build Guide)

> **This is a manual Make.com build guide, not an import file.**

---

## 📋 Module Order & Settings

1. **HTTP: Get**
   - **URL:** `{{input.url}}`
   - This step fetches the HTML content of the company page.

2. **OpenAI: Create Completion**
   - **Model:** `gpt-4o`
   - **Connection:** `OpenAI_Conn`
   - **Prompt:**
     ```text
     Summarize this company's biggest pain point in ≤30 words. Return only the pain point.

     HTML:
     {{1.data}}
     ```
   - **Output Variable:** `painPoint`
   - **Map:** HTML from Step 1 into the prompt

3. **Google Sheets: Add Row**
   - **Sheet:** `revno agent data`
   - **Values:** `[{{input.url}}, {{2.painPoint}}]`
   - **Connection:** `GoogleSheets_Conn`

---

## 🔗 Required Connections
- `OpenAI_Conn` (OpenAI)
- `GoogleSheets_Conn` (Google Sheets)

---

## 🧪 Testing Notes
- Use a real company URL as input to test the flow.
- Check that the pain point summary appears in the correct Google Sheet.
- If the row doesn't appear, check your mapping and connection settings.

---

## 📝 What to Map
- The input URL to Step 1 and Step 3.
- The HTML from Step 1 to the OpenAI prompt in Step 2.
- The pain point output from Step 2 to the new row in Step 3.

---

**Tip:** Test with a variety of company URLs to ensure the summaries are accurate and concise. 