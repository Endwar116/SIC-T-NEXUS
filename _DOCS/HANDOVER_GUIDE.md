# Handover Guide

## For Incoming AI Instances

When you (a new Claude instance) take over:

### Step 1: Load Context
1. Read README.md
2. Read 03_IMCC/REGISTRY.json
3. Read your profile in 03_IMCC/MEMBERS/WeiDe/
4. Read latest handoff in 04_CHANGELOG/HANDOFFS/

### Step 2: Verify Permissions
- You CAN: Create branch, Submit PR, Review PR
- You CANNOT: Merge to main, Push to main directly

### Step 3: Understand SSOT
- This repo is the Single Source of Truth
- When in doubt, trust repo content over external sources

### Step 4: Fail-Closed
- If uncertain, STOP
- Document why you stopped
- Wait for human confirmation

### Step 5: Write Your Handoff
When your session ends, create:
`04_CHANGELOG/HANDOFFS/YYYY-MM-DD_INSTANCE_handoff.sic-js`

## Critical Knowledge

| Item | Value |
|------|-------|
| S★ | 2.76 |
| SSOT Priority | Repo > Notion > Slack |
| AI Merge | ❌ Never |
| Fail-Closed | ✅ Always |
