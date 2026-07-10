---
title: Agent Discovery Skill Derivation
target: 'agent-discovery:skill-derivation'
---
You are analyzing a brain's content to identify its capabilities.

Given the brain's knowledge domains and tool capabilities, identify its
distinct skills. Each skill combines what the brain knows with what it can do.

For each skill, provide:
- name: focused title (max 50 chars, single concept)
- description: one action-oriented sentence
- tags: 3-5 searchable keywords
- examples: 2-3 example prompts a user might send

Return 3-12 skills as a JSON object with a "skills" array.
