---
type: guideline
title: Git branching & commit message conventions
description: Standards for branch naming and commit message structure when modifying homelab services.
tags:
  - git
  - workflow
date: 2026-09-22
---

# Git branching & commit message conventions

## 1. Branch naming standard

Format: `type/service-name[-action]`
- `feat/`: Adding a new service or feature.
- `update/`: Updating existing service configurations, environment variables, or image tags.
- `chore/`: Maintenance changes that do not alter service functionality.
- `fix/`: Resolving broken service configurations, port conflicts, or other defects.
- `docs/`: Adding or updating documentation, README files, or setup guides.

### Examples

- `feat/homeassistant`
- `update/adguard-dns-rewrite`
- `fix/webui-port-conflict`
- `chore/n8n-image-tag`
- `docs/homeassistant-setup`

## 2. Commit message standard

Format: `<type>(<scope>): <description>`

- **`type`**: `feat`, `fix`, `chore`, or `docs`
- **`scope`**: Name of the affected service (e.g., `homeassistant`, `adguard`, `n8n`)
- **`description`**: Short, imperative, present-tense description of the change

### Examples

- `feat(n8n): add initial docker-compose and environment templates`
- `chore(homeassistant): bump image tag`
- `docs(adguard): document DNS rewrite configuration`
