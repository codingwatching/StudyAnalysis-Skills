<div align="center">

# 📚 Knowledge Absorber

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python: 3.8+](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Version: 4.1.0](https://img.shields.io/badge/Version-4.1.0-green.svg)](CHANGELOG.md)

**Universal AI Skill Module | Compatible with Trae, Claude, Gemini, VS Code Copilot, etc.**

[🇺🇸 English](README_EN.md) | [🇨🇳 简体中文](README.md)

---

**Knowledge Absorber** is an independent "External Brain" module. It empowers AI agents with the ability to deeply read long documents, analyze complex content, and generate structured "Knowledge Crystals" (Markdown + HTML).

</div>

---

## 🚀 What's New

> **v4.1.0 Latest Update**

- **🎓 Mentor Mode**: Brand new interactive learning experience
  - **Intelligent Dialogue Assistant**: Click the "Open Mentor Mode" button in the generated HTML page to chat with an AI mentor in real-time
  - **Context-Aware**: The mentor fully understands the current knowledge card content and can answer questions and deepen understanding specifically
  - **Local Relay Service**: Start the local relay service via `python scripts/mentor_relay.py` (default port 8760)
  - **Multi-Model Support**: Compatible with OpenAI, Claude, Gemini, and any OpenAI-compatible API
  - **Sidebar Design**: Elegant sidebar interface that doesn't obstruct the main content, can be opened and closed at any time
  - **Conversation History**: Maintains complete conversation context, supports continuous in-depth questioning

- **💡 Deep Linking Analysis**: Added multi-source input conflict comparison feature, automatically compares conflicts from multiple sources, strengthening AI's fact-checking capabilities

> **v4.0.0 Previous Updates**

- **⚡ High-Speed Concurrent Engine**: Introduced `ThreadPoolExecutor` and `threading.Lock` for simultaneous scraping of multiple links/files, improving processing efficiency by 300%+.
- **🎨 Visual Progress System**: Integrated `Rich` library for high-contrast color tracking, providing a clear task board and real-time progress feedback in the terminal.
- **⚓ Truth Anchoring Protocol**: Added `【💡 Deep Linking】` analysis to automatically identify factual conflicts or complementarities across multiple sources.
- **🔍 Deep Protocol Alignment**: Mandatory integration of the "Seven Holographic Lenses" protocol, ensuring outputs include "Mind Maps" and "Pitfall Guides".
- **🛡️ Enhanced Robustness**: Optimized SSL verification for offline testing and added auto-fix for character encoding issues (Mojibake) on major platforms.
- **⚛️ Deep Fission Module**: Added atomic-level contradiction analysis and version archeology module to reveal counter-intuitive conclusions (Style: `.fission-section`).
- **🔍 Strict Search Filter**: Upgraded HTML interaction; search box now **strictly hides** non-matching content blocks instead of just highlighting, providing a focused reading experience.
- **🛡️ Mermaid Safety Protocol**: Built-in syntax auto-correction mechanism that forcibly escapes special characters to prevent diagram rendering crashes.

---

## 📂 Portability Guide

This module is designed for **"Folder-Level Plug & Play"**.
AI assistants typically scan specific configuration folders in the project root. To let other AIs (like Claude or Gemini) recognize this skill, you simply need to **rename the parent directory**.

### 📂 Directory Structure Adaptation

Assuming your `skills` folder is located at the project root:

1.  **For Trae** (Default):
    ```text
    Project_Root/
    └── .trae/              <-- Keep original name
        └── skills/
            └── knowledge-absorber/
    ```

2.  **For Claude Projects**:
    *   Rename `.trae` to `.claude`.
    ```text
    Project_Root/
    └── .claude/            <-- Rename to .claude
        └── skills/
            └── knowledge-absorber/
    ```

3.  **For Gemini Advanced / AI Studio**:
    *   Rename `.trae` to `.gemini`.
    ```text
    Project_Root/
    └── .gemini/            <-- Rename to .gemini
        └── skills/
            └── knowledge-absorber/
    ```

4.  **For VS Code (Copilot/Cline)**:
    *   Rename `.trae` to `.vscode`.
    ```text
    Project_Root/
    └── .vscode/            <-- Rename to .vscode
        └── skills/
            └── knowledge-absorber/
    ```

> **💡 Core Principle**: AI agents usually have permission to read hidden folders (starting with `.`). As long as the path is correct and you explicitly instruct the AI to "use this skill", it will work.

---

## 🛠️ Installation & Usage

### Step 1: Environment Preparation
Ensure Python 3.8+ is installed on your machine.
Run the following command in the `knowledge-absorber` directory:
```bash
pip install -r requirements.txt
```

### Step 2: When to Activate
Do not use this skill for simple Google searches. Summon it for **"High Cognitive Load"** scenarios:

1.  **Heavy Lifting**: When facing hundreds of pages of PDFs, technical framework docs (e.g., BMad, React Source), or ancient texts.
2.  **Knowledge Crystals Needed**: When you need more than a simple summary—you need a beautifully formatted, archivable HTML card.
3.  **Cross-Source Analysis**: When you need to scrape and compare multiple links (e.g., Zhihu + Blog + Official Docs) for deep Truth Anchoring.

### Step 3: Workflow
You don't need to manually run complex command-line instructions. Just use **Natural Language** in the chat, and the AI will proxy the execution:

*   **User Instruction Examples**:
    > "Help me deeply analyze this link: `https://docs.bmad-method.org/`"
    > "Read `manual.pdf` and apply the [Mechanistic Lens] to generate knowledge cards."

*   **AI Execution Logic**:
    1.  **Ingestion**: Automatically calls `scripts/content_ingester.py` to scrape and clean content concurrently.
    2.  **Lens Analysis**: Applies deep reasoning based on protocols defined in `SKILL.md` (e.g., Mechanistic Lens, Evolution Lens).
    3.  **Delivery**: Automatically generates `.md` (Deep Notes) and `.html` (Visual Cards).

---

## 📦 Outputs

This skill automatically generates files in two formats (located in the `data/` directory):

1.  **Markdown Deep Notes (`.md`)**:
    *   Includes metadata, concept icebreaking, deep deconstruction, mind maps, and pitfall guides.
    *   Supports "Mixed Script Protocol" (Traditional/Simplified) or "Tech Stack Templates".
2.  **HTML Visual Cards (`.html`)**:
    *   Beautiful formatting, perfect for sharing or archiving in a knowledge base.
    *   Supports Dark/Light mode adaptation, with perfected code highlighting and Mermaid diagram display.

---

## 🎓 Mentor Mode Explained

### What is Mentor Mode?

Mentor Mode is Knowledge Absorber's interactive learning feature that allows you to chat with an AI mentor in real-time while browsing generated knowledge cards, deepening understanding and answering questions.

### Core Features

1. **📚 Context-Aware**
   - The mentor fully understands all content in the current knowledge card
   - Can provide in-depth explanations for specific sections and concepts
   - Automatically correlates related knowledge points

2. **💬 Intelligent Dialogue**
   - Supports continuous multi-turn conversations
   - Maintains complete conversation history
   - Allows follow-up questions, deep dives, and examples

3. **🎨 Elegant Interface**
   - Sidebar design that doesn't obstruct the main content
   - Supports dark/light themes
   - Responsive layout, adapts to various screen sizes

4. **🔌 Flexible Configuration**
   - Supports any OpenAI-compatible API
   - Configurable model, temperature, max tokens, and other parameters
   - Runs locally, data security guaranteed

### Usage Steps

#### 1. Start the Relay Service

Run in the `knowledge-absorber` directory:

```bash
python scripts/mentor_relay.py
```

You will see:
```
Mentor relay listening on http://127.0.0.1:8760
```

> 💡 **Tip**: The relay service is a local relay server used to pass messages between the browser and AI models. It does not store your conversation content.

#### 2. Open the Knowledge Card

Open the generated `knowledge_card.interactive.html` file in your browser.

#### 3. Configure AI Connection

Click the "Open Mentor Mode" button in the upper right corner of the page, then in the sidebar:

1. Select API type (OpenAI / Claude / Gemini / Custom)
2. Enter API Key
3. Select model (e.g., gpt-4, claude-3-5-sonnet, etc.)
4. Click "Test Connection" to confirm the configuration is correct

#### 4. Start Chatting

After successful configuration, you can ask questions in the input box! For example:

- "Please explain the core mechanism section in detail"
- "What's the difference between this concept and XXX?"
- "Can you give a practical application example?"
- "I encountered XXX problem in practice, what should I do?"

### Typical Use Cases

1. **Deepen Understanding**
   - Don't quite understand a concept, ask the mentor to explain in simpler terms
   - Need more examples to deepen impression

2. **Extended Learning**
   - Ask about related knowledge points
   - Understand deeper principles

3. **Practical Guidance**
   - Ask how to apply in actual projects
   - Seek advice on specific problems encountered

4. **Comparative Analysis**
   - Compare pros and cons of different technical solutions
   - Understand historical evolution and future trends

### Configuration Instructions

#### Supported API Types

- **OpenAI**: GPT-4, GPT-3.5, etc.
- **Claude**: Claude 3.5 Sonnet, Claude 3 Opus, etc.
- **Gemini**: Gemini Pro, Gemini Ultra, etc.
- **Custom**: Any service compatible with OpenAI API format

#### Advanced Configuration

In the sidebar's "Advanced Settings", you can adjust:

- **Temperature**: Controls creativity of responses (0-2, default 0.7)
- **Max Tokens**: Maximum length of single response (default 2000)
- **System Prompt**: Customize the mentor's role and style

### Important Notes

1. **Relay Service Must Be Running**
   - If the relay service is not started, Mentor Mode will not work
   - Ensure port 8760 is not occupied

2. **API Key Security**
   - API Key is only stored in browser local storage (localStorage)
   - Not uploaded to any server
   - Recommend using API Keys with quota limits

3. **Network Connection**
   - Need to be able to access the corresponding AI service API
   - If using domestic networks, may need to configure a proxy

4. **Reading Mode Only**
   - If just reading knowledge cards, no need to start relay service
   - Search, theme switching, and other features do not depend on relay

### Troubleshooting

**Issue: Clicking "Open Mentor Mode" has no response**
- Check if relay service is running
- Check browser console for error messages

**Issue: Test connection failed**
- Check if API Key is correct
- Check if network connection is normal
- Check if API endpoint URL is correct

**Issue: Dialogue response is very slow**
- May be high model load, wait a moment
- Can try switching to other models
- Check network latency

---

## 🤖 Skill Protocol

The core logic is defined in the `SKILL.md` file.
If you want to modify the AI's way of thinking (e.g., changing the depth of analysis or output style), please edit `SKILL.md` directly.

---

> **Maintainer**: Little Code Sauce
> **Version**: v4.1.0 (Mentor Mode Edition)
