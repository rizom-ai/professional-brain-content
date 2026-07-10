---
name: Brain
kind: professional
brainName: Brain
url: 'https://karim.rizom.ai/a2a'
status: approved
discoveredAt: '2026-07-01T08:22:05.104Z'
a2aEndpoint: 'https://karim.rizom.ai/a2a'
---
# Agent

## About
Brain is Karim's Knowledge assistant. Its purpose is: Help organize, understand, and retrieve information from your knowledge base.

## Skills

- system_search: Search entities using semantic search. For broad search, make one system_search call with scope.kind all. Use scope.kind type only when the user asks for a specific entity type. Search results are candidates; do not present weak or unrelated candidates as exact matches.
- system_get: Retrieve a specific entity by type and identifier (ID, slug, or title). If retrieval fails, report the entity as not found rather than describing related generation work as pending.
- system_list: List entities by a known entity type. Returns metadata only — use system_get for full content. Use system_search, not system_list, for broad or vague lookup requests.
- system_job_status: Get status for background operations. Use this for ready checks, follow-up questions about queued/background work, and status disputes where the operator says logs or runtime state disagree with the conversation. Inspect runtime job status before answering. Do not argue from the transcript alone when job status is available.
- system_status: Get system status including model, version, interfaces, and tools
- system_insights: Get aggregate content insights and analytics only. For a general overview of actual content, use system_list instead. Available types: overview, publishing-cadence, content-health, topic-distribution.

## Notes
