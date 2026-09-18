# llm-rover

An LLM-powered agentic AI system that plans and executes real-world movement on a physical robot — not just a chatbot, an agent that reasons about a task and acts on it through hardware.

## Why this project

Most AI/LLM projects stop at software — a chatbot, a RAG pipeline, a summarizer. I wanted to build something where the AI layer actually *does* something in the physical world: takes a natural language instruction, plans a sequence of actions, and controls real hardware to carry it out.

## How it works

- **`esp32-firmware/`** — Code running on the ESP32 microcontroller. Handles low-level motor control and reads the ultrasonic sensor for obstacle detection. Exposes simple commands (move forward, turn, stop) over WiFi.
- **`agent/`** — Runs on my laptop. Takes a natural language instruction (e.g. "check what's near the door"), uses an LLM to break it into a sequence of movement commands, and sends them to the ESP32 over HTTP.
- **`PROGRESS.md`** — Dev log of what I built, what broke, and what I learned along the way.

## Status

🚧 Just getting started — hardware not yet assembled, firmware and agent code in progress. Follow `PROGRESS.md` for updates.

## Tech stack

- ESP32 (Arduino framework)
- Python (agent/LLM layer)
- [LLM provider — fill in once decided]

## License

MIT
