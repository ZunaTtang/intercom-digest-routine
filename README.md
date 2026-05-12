# Intercom Daily Digest Routine

Claude Code Routine for posting a daily Intercom open conversations digest to Slack.

## What it does

Every day at 10:00 KST, this Routine:
1. Fetches all open Intercom conversations
2. Filters out unassigned and bot-only chats
3. Categorizes by priority (🔴 urgent / 🟠 needs action / 🟡 pending / 🟢 monitor)
4. Posts a formatted Block Kit message to Slack

## Stack

- **Runtime**: Claude Code Routines (Anthropic-managed)
- **Trigger**: Daily at 09:00 GMT+9 (10:00 KST — adjust in trigger)
- **Connectors**: Intercom MCP, Slack MCP
- **Model**: Sonnet 4.6

## Files

- The Routine prompt itself lives in the Claude Code Routines UI (not in this repo)
- This repo exists only to satisfy the Routine's required repository binding

## History

Migrated from AWS Lambda + EventBridge to reduce operational overhead and improve security (no root credentials, no manual zip deployment).
