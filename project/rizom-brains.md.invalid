---
title: Rizom Brains
slug: rizom-brains
status: published
publishedAt: '2024-12-19T12:00:00.000Z'
description: >-
  A plugin-based knowledge management system that turns markdown into an
  intelligent, AI-powered digital brain.
year: 2024
technologies:
  - TypeScript
  - Bun
  - SQLite
  - Preact
  - Tailwind CSS
  - Anthropic Claude
url: 'https://github.com/rizom-ai/brains'
---
## Context

The modern knowledge worker faces an overwhelming amount of information spread across countless tools and platforms. Notes in one app, bookmarks in another, conversations scattered across messaging platforms. Traditional knowledge management tools often create more friction than they solve, requiring manual organization and offering little intelligence about the connections between ideas.

The goal was to build a system that could serve as a true digital brain - one that not only stores information but actively helps surface relevant knowledge, generate insights, and present ideas in various formats for different audiences.

## Problem

Existing solutions fell short in several key areas:

**Fragmentation**: Knowledge scattered across multiple tools with no unified way to access or query it. Each tool had its own mental model and organization system.

**Manual overhead**: Users spent more time organizing and tagging content than actually using it. The maintenance burden often led to abandoned systems.

**Lack of intelligence**: Most tools were glorified file systems. They couldn't understand the content, find connections, or help generate new insights from existing knowledge.

**Presentation gap**: Raw notes rarely translate well to shareable formats. Creating blog posts, presentations, or portfolios from knowledge bases required significant manual effort.

## Solution

Rizom Brains takes a fundamentally different approach by treating the brain as a composable system of plugins, each handling a specific concern:

**Plugin Architecture**: A shell application provides core services (entity management, AI integration, job queues) while plugins extend functionality. This allows users to customize their brain for their specific needs - writers might focus on blog and essay plugins, while developers might prioritize link capture and code documentation.

**Markdown as Truth**: All content lives in plain markdown files with YAML frontmatter. This ensures portability, version control compatibility, and the ability to edit content with any tool. The database serves only as an index, never as the source of truth.

**AI-Native Design**: Every plugin can leverage AI capabilities through a unified interface. The summary plugin maintains running conversation digests. The topics plugin extracts themes across content. The blog plugin can generate draft posts from prompts that reference existing knowledge.

**Multi-Interface Access**: The same brain can be accessed through CLI for power users, Matrix for conversational interaction, MCP for IDE integration, or a static website for public sharing. Each interface exposes appropriate tools based on user permissions.

**Automatic Site Generation**: The site-builder plugin transforms brain content into a themed static website. Entity types like posts, decks, and projects get automatic routing, templates, and navigation. Changes sync to production via CDN.

## Outcome

Rizom Brains successfully demonstrates that knowledge management can be both powerful and pleasant to use. Key achievements:

**Reduced friction**: The directory-sync plugin means users can simply save markdown files and have them automatically processed, indexed, and made available across all interfaces.

**Intelligent connections**: Topics extraction and entity linking surface relationships that would otherwise require manual tagging. The embedding service enables semantic search across all content.

**Multiple output formats**: A single piece of knowledge can appear as a note, become part of a blog post, or be presented as slides - all while maintaining the source content as the single source of truth.

**Proven in production**: The system powers the yeehaa.io website, handling blog posts, presentations, topic exploration, and portfolio projects through a unified architecture.

The plugin architecture has proven flexible enough to add new capabilities (like this portfolio plugin) without modifying the core system, validating the architectural approach.
