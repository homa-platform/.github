<p align="center">
  <img src="homa-face.png" alt="Homa" width="160">
</p>

<h1 align="center">Homa</h1>

<p align="center"><b>H</b>ome <b>O</b>rchestration and <b>M</b>onitoring <b>A</b>ssistant</p>

Homa is a self-hosted household assistant. You talk to it by voice through a
small ESP32 board or by text in Telegram, and it keeps the house's calendar,
reminders, messages and documents in order. It runs on hardware you own and
works with any OpenAI-compatible model, local or in the cloud.

The smallest setup is one Go server and a chat model. Everything else (voice
boards, Telegram, calendar, e-mail, web search, document reading, memory) is
optional and switches on with configuration.

## Repositories

| Repository | What it is |
|---|---|
| [homa-agent](https://github.com/homa-platform/homa-agent) | The server: conversations, tools, skills, voice pipeline, Telegram and e-mail channels |
| homa-esp32 | Firmware for the voice boards: wake word, face, follow-up listening, signed updates *(coming)* |
| homa-wakeword | Training the on-device wake-word model *(coming)* |
| docs-mcp | Reading PDFs, scans and photos for the agent *(coming)* |
| homa-adr | Architecture decision records *(coming)* |

## Principles

- **Runs at home.** Speech recognition and speech synthesis can stay on your own
  machines, even when the chat model is in the cloud.
- **Private by default.** Documents with personal data reach a cloud model only
  as copies with placeholders.
- **Simple first.** One endpoint and one model to start; every integration is
  optional.
