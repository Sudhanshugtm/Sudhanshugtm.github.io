---
title: "Canvas Mode"
date: 2025-09-29
description: "Exploring the idea of canvas mode for AI agents - a designer's perspective on improving the workflow between creativity and AI-assisted development."
---

I've been using AI systems since 2022 when ChatGPT launched professionally. As a UX designer, I still remember the early days when solving design problems with AI meant simple text conversations. Then image features were introduced, allowing us to upload screenshots of our work for AI assistance.

Later, systems like Claude launched the artifacts feature, which visualizes ideas shared in text form. This was a game-changer for designers like me. However, I encountered some limitations with this approach:

- Message limits on Claude would interrupt longer design sessions
- The system was often limited to specific tech setups (mainly React apps)
- The workflow felt constrained compared to traditional design tools

Despite these limitations, I found great value in AI-assisted design work. When Claude's coding agent launched, I made an unexpected transition from UI-focused work to spending most of my time in command line interfaces—something I never imagined as a designer.

This shift coincided with Claude's support for MCPs (Model Context Protocol). The Playwright MCP became particularly valuable for front-end development, allowing me to describe design ideas or specific treatments and watch them come to life through iterative development.

## The Challenge with MCPs

One significant problem I discovered with MCPs is their resource intensity—they quickly consume the context window. This became a major bottleneck in my development workflow. When using the MCP for application development, I would consistently run out of context space, forcing the session to end prematurely.

While AI models have implemented auto-compacting techniques to handle context limits, I've found these solutions inconsistent and unreliable for maintaining productive design conversations.

The Playwright MCP presented another challenge: **lack of control**. When I request specific changes, the tool can call multiple functions simultaneously across its 7-8 available tools. As a designer working on subjective visual problems, this automated approach often felt unpredictable.

> The gap between my design vocabulary and the AI's interpretation creates friction in the creative process.

This communication gap might stem from being a non-English speaker, where my word choices and their contextual meanings may differ from the AI's training data. The result is often misaligned interpretations of design intent.

## The Canvas Mode Concept

This led me to envision a different approach: **Canvas Mode**. The concept is straightforward yet powerful.

Imagine you're developing an application running on localhost. Instead of relying solely on the Playwright MCP for design iteration, your localhost environment could enter a special canvas state.

### How Canvas Mode Works

In this mode, I could:
- **Draw directly on the interface** to highlight specific elements
- **Add contextual notes** for improvements right where they're needed
- **Mark 5-6 elements** for simultaneous feedback
- **Establish clear communication** between designer intent and AI understanding

### Implementation Approaches

I considered several methods for communicating feedback back to the AI agent:

1. **Screenshot-based feedback**: Capture annotated screenshots, though this approach raises concerns about token consumption

2. **File-based communication**: Store feedback in a `feedback.md` or `feedback.json` file within the project directory. This creates a structured communication channel where:
   - All canvas annotations are stored with precise UI context
   - The AI can identify exactly which elements need attention
   - Feedback accumulates over multiple design iterations

This approach enables more **opinionated design work**. Rather than the AI forming its own design opinions through general prompts, it responds to specific, contextual feedback directly tied to UI elements.

## Current Implementation

I've created a prototype using **bookmarklet JavaScript** that transforms any localhost page into an interactive canvas. The system includes:

- **Frontend**: Bookmarklet that overlays annotation tools on any webpage
- **Backend**: Server that receives and stores annotations in JSON format
- **Storage**: Structured feedback files that AI agents can parse and understand

### Technical Limitations

As a designer rather than a developer, I recognize several areas for improvement:

- **Mobile compatibility**: Bookmarklets don't work on mobile browsers, limiting the workflow to desktop environments
- **Cross-platform support**: The current implementation needs broader device and browser support
- **Integration depth**: Better integration with existing development tools could streamline the workflow

## The Bigger Vision

I believe AI agents should offer **canvas mode as a native feature**. This would provide designers with a natural interface for expressing design feedback, bridging the gap between visual thinking and AI collaboration.

### Why This Matters

The current terminal-based approach to AI agents offers significant advantages:
- **System-level access** to files and development tools
- **Greater flexibility** compared to web-based interfaces  
- **More powerful capabilities** through CLI integration

However, this power comes at the cost of accessibility for designers. Canvas mode could **integrate designers into the AI development workflow** without sacrificing the technical capabilities that make CLI agents so effective.

By providing a visual feedback layer on top of the powerful terminal-based system, we can create a workflow that serves both technical and creative needs—making AI-assisted development truly collaborative across disciplines.