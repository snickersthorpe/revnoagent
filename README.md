# Revno Agent - Lead Warmup System

## Overview
This is a comprehensive lead warmup system designed to automate and personalize lead engagement through intelligent agent communication.

## Directory Structure
```
/revno-agent/
├── templates/
│   ├── lead_welcome.md
│   └── follow_up_day1.md
├── agents/
│   └── lead_warmup_bot.md
├── config/
│   └── persona.json
└── README.md
```

## Components

### Templates (`/templates/`)
Contains message templates used by the agent:
- **lead_welcome.md**: Initial welcome message template
- **follow_up_day1.md**: Day 1 follow-up message template

### Agents (`/agents/`)
Contains agent definitions and workflows:
- **lead_warmup_bot.md**: Main lead warmup agent configuration

### Config (`/config/`)
Contains configuration files:
- **persona.json**: Agent personality and behavioral settings

## Usage

### Setting Up a New Lead
1. Add lead information to the system
2. Agent automatically selects appropriate template
3. Personalized message is generated and sent
4. Follow-up sequence is scheduled

### Customization
- Modify templates in `/templates/` directory
- Adjust agent behavior in `/config/persona.json`
- Update agent workflows in `/agents/` directory

## Features
- ✅ Personalized messaging
- ✅ Automated follow-up sequences
- ✅ Lead engagement tracking
- ✅ Template-based responses
- ✅ Configurable agent personality

## Getting Started
1. Review the agent configuration in `/agents/lead_warmup_bot.md`
2. Customize templates in `/templates/` directory
3. Adjust persona settings in `/config/persona.json`
4. Deploy and monitor lead engagement

---
*Revno Agent System v1.0* 