---
status: draft
title: >-
  Your Clawdbot (Moltbot) AI Assistant Has Shell Access and One Prompt Injection
  Away from Disaster
url: 'https://snyk.io/articles/clawdbot-ai-assistant/'
description: >-
  An in-depth security analysis of Clawdbot (now Moltbot), an open-source AI
  assistant with autonomous capabilities, examining critical vulnerabilities
  including prompt injection, supply chain risks, and network exposure.
keywords:
  - AI security
  - prompt injection
  - agentic AI
  - Clawdbot
  - supply chain attacks
domain: snyk.io
capturedAt: '2026-02-01T07:38:01.214Z'
source:
  ref: 'matrix:!4wXe7ZxNeJ_k5RApmnAtQpEPmX4Br8ZCy1wB8MOR-MU'
  label: test-rover-local
---
This article provides a comprehensive security analysis of Clawdbot, an open-source AI assistant created by Peter Steinberger that has gained significant adoption among developers. Unlike traditional chatbots, Clawdbot operates as a functional agent with access to shell commands, email, calendars, messaging platforms, and file systems. The article examines five major security concerns: prompt injection attacks that exploit untrusted data sources like emails to manipulate the agent into performing unauthorized actions; supply chain vulnerabilities through the SKILLS ecosystem and community-contributed dependencies; privacy risks from LLM providers' data handling practices; network security issues with publicly exposed gateway components; and AI model layer considerations. While acknowledging Clawdbot's commendable security-by-default measures and transparent documentation, the article emphasizes that securing agentic AI requires new approaches beyond traditional application security, including continuous red teaming, AI Bill of Materials scanning, runtime protection controls, and MCP server security scanning.
