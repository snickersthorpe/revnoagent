# Lead Warmup Bot

## Agent Overview
This agent is designed to warm up leads through personalized communication and follow-up sequences.

## Capabilities
- Send personalized welcome messages
- Schedule follow-up communications
- Track lead engagement
- Generate custom responses based on lead data

## Workflow
1. **Lead Intake**: Receive new lead information
2. **Welcome Message**: Send personalized welcome using templates
3. **Follow-up Sequence**: Schedule and send follow-up messages
4. **Engagement Tracking**: Monitor lead responses and engagement
5. **Handoff**: Transfer qualified leads to sales team

## Configuration
- Uses templates from `/templates/` directory
- Follows persona defined in `/config/persona.json`
- Integrates with CRM systems

## Response Templates
- Welcome: `lead_welcome.md`
- Day 1 Follow-up: `follow_up_day1.md`
- Custom responses based on lead behavior

---
*Agent ID: lead_warmup_bot* 