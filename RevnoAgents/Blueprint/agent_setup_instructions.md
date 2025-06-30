# 🔧 Agent Setup Instructions (No Jargon)

This file is your simple guide to build and test agents using Make.com + Cursor + Rune.

---

## 📂 Folder Setup
Make sure your Obsidian folder looks like this:

/RevnoAgents
├── Blueprint/
│ ├── agent_setup_instructions.md ← this file
│ ├── rune_no_jargon_help_guide.md
│ ├── revno_agent_blueprint.md
│ └── scenario_exports/
└── ai_agents/
    ├── tools/
    └── agent_name.md

yaml
Copy
Edit

---

## 🧪 Quick Agent Test (Today's Plan)

We'll build two quick automations to verify things work:

### 1. **Auto Welcome Email Bot**
- **Trigger**: New contact in GoHighLevel
- **Action**: Send email using OpenAI draft
- **Output**: Adds a note in GHL

### 2. **Pain Point Extractor Bot**
- **Trigger**: URL or company name input
- **Action**: Scrapes page, summarizes key pain point
- **Output**: Adds result to Make datastore or GSheet

---

## ✅ What to Do Next (Use Rune)

1. Ask Rune: "Help me build Auto Welcome Email Bot."
2. Rune gives you exact Make.com steps.
3. Paste the OpenAI prompt into Make where it says "Prompt."
4. Run once with test data and verify email goes out.
5. Save scenario JSON into `/scenario_exports/`.

---

## 🧠 Tips

- Always map values like `firstName` and `email` from Step 1 to Step 3.
- Use **Run Once** mode in Make to test flows.
- If it breaks, ask Rune. Paste error or screenshot.

## 🚀 New Quick-Test Automations

1. **Auto Welcome Email Bot**
   - Watches GHL for new contacts, emails a warm welcome, and logs a note.
   - Blueprint saved in `scenario_exports/auto_welcome_email_bot.make.json`.

2. **Pain Point Extractor Bot**
   - Scrapes a company URL, extracts a 30-word pain point, and drops it into a GSheet.
   - Blueprint saved in `scenario_exports/pain_point_extractor_bot.make.json`.

These are now available as step-by-step build instructions in /scenario_instructions/.

*Run once in Make to test.  If you hit any errors, paste the red error text to Rune for help.* 