# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a **product design prototyping** repository (产品设计稿). It contains ~20 independent sub-projects, each representing a product UI prototype. The core workflow is:

1. Write a **prompt file** (`.md` or `.txt`) describing a product concept, design style, and technical requirements
2. Feed the prompt to an AI to generate a **standalone HTML** prototype
3. The HTML file is the deliverable — a self-contained UI mockup

## Project Structure

Each top-level directory is an independent project. There is no shared code or build system.

| Directory | Description |
|-----------|-------------|
| `ACCRM/` | Enterprise CRM sales management system |
| `AcLauncher/` | Desktop launcher application |
| `AI聊天/` | AI chat application with knowledge base |
| `APP-资产管家/` | Asset management mobile app |
| `AYB/` | Business reporting |
| `AYKK/` | Dental/oral health products |
| `AYKK-MINI/` | Mini-program version of AYKK |
| `baby-product/` | Baby products app |
| `CodeWave/` | Audio/note-to-podcast app (声记) — includes PRD, Pencil `.pen` design file |
| `dear-agent/` | Desktop AI companion app with live2d avatar |
| `IM/` | IM/chat web application |
| `niuyin/` | Various product pages (login, partnership, etc.) |
| `RTC/` | Audio/video calling |
| `商城管理/` | E-commerce mall management |
| `芝士学爆-app/` | Short-video knowledge learning app |

## Common Patterns

- **Prompt files** follow a standard template: `#角色` (role), `#设计风格` (design style), `#技术规格` (technical specs), `#任务` (task)
- **HTML outputs** use Tailwind CSS via CDN (`cdn.tailwindcss.com`), Remix Icons (`remixicon.css`), and open-source placeholder images
- All HTML files are standalone — no bundler, no framework, no npm
- Design style is consistently: elegant minimalism, blue accent, glassmorphism, soft gradients, card-based layouts
- Screen specs: usually 1080p desktop (with browser frame) or 375×812 iOS mobile (with phone frame)

## Development

No build commands needed. To preview any HTML file, open it directly in a browser:

```
start <filename>.html
```

## Creating a New Prototype

1. Create a new directory for the project
2. Write a prompt `.md` file with role, style, specs, and task sections
3. The prompt is then used to generate a `ui.html` (or similarly named) output file
4. `.pen` files (Pencil design tool) can be created alongside HTML for high-fidelity design work
