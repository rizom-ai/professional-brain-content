---
name: Brain
kind: professional
brainName: Brain
url: 'https://karim.rizom.ai/a2a'
status: approved
discoveredAt: '2026-05-18T09:07:29.770Z'
---
# Agent

## About
Brain is Karim's Knowledge assistant. Its purpose is: Help organize, understand, and retrieve information from your knowledge base.

## Skills

- directory-sync_status: Get sync and git repository status — last sync time, watching state, pending git changes. Use this for status questions, not for actually syncing or backing up.
- system_search: Search entities using semantic search. Optionally filter by entity type.
- system_get: Retrieve a specific entity by type and identifier (ID, slug, or title).
- system_list: List entities by type. Returns metadata only — use system_get for full content.
- system_check-job-status: Check the status of background operations
- system_get-conversation: Get conversation details
- system_list-conversations: List conversations, optionally filtered by search query
- system_get-messages: Get messages from a specific conversation
- system_status: Get system status including model, version, interfaces, and tools
- system_insights: Get aggregate content insights and analytics only. For a general overview of actual content, use system_list instead. Available types: overview, publishing-cadence, content-health, topic-distribution.

## Notes
