# 🚀 GGUF AI HUB

A lightweight, single-file HTML tool to **search, filter, and download GGUF AI models** directly from [Hugging Face](https://huggingface.co) — no backend, no installation, just open and go.

---

## ✨ Features

- 🔍 **Smart Search** — Search multiple model keywords at once (comma-separated), e.g. `gemma, qwen, llama`
- ⚡ **Enter Key Support** — Press `Enter` to search instantly without clicking the button
- 🎯 **File Size Filter** — Filter results by:
  - 🔵 **Lightweight** — Small quantizations (Q2, Q3, or models ≤ 5B)
  - 🟢 **Recommended** — Mid-size models (Q4–Q5, 5B–20B range)
  - 🔴 **Heavy** — Large quantizations (Q6, Q8, or models > 20B)
- 🏷️ **Capability Tags** — Automatically detects model capabilities:
  - `code` — Code generation models
  - `chat` — Instruction / chat-tuned models
  - `reason` — Math / reasoning models
  - `light` — Tiny models (1B–3B)
- 📊 **Progress Bar** — Live progress indicator while fetching model details
- 💻 **System Spec Detection** — Displays GPU (via WebGL), VRAM, physical RAM, DDR generation, and CPU threads
- 🖥️ **Run Commands** — Each `.gguf` file shows ready-to-use run commands for:
  - `llama.cpp`
  - `ollama`
- 🌙 **Dark Mode UI** — Fully dark-themed interface, easy on the eyes

---

## 📸 Preview

> Open `model_downloader.html` in any modern browser — no server needed.

---

## 🚀 Usage

1. **Download** or clone this repository
2. **Open** `model_downloader.html` in your browser (Chrome recommended)
3. **Type** a model name in the search box (e.g. `llama`, `gemma`, `qwen`)
4. Press **Enter** or click **Search**
5. Use the **filter dropdown** to narrow down results by size category
6. **Click** any `.gguf` file link to download directly from Hugging Face

---

## 📂 File Structure

```
AI_model_Search/
└── model_downloader.html   # The entire app in one file
```

No dependencies. No build step. No server required.

---

## ⚙️ How It Works

1. Queries the [Hugging Face Model API](https://huggingface.co/api/models) with your search keyword(s)
2. For each result, fetches the model's file list and filters for `.gguf` files
3. Classifies each file as **Lightweight / Recommended / Heavy** based on quantization type and model size
4. Renders download links with copy-paste run commands for local inference tools

---

## 🧠 Model Classification Logic

| Class | Color | Criteria |
|-------|-------|----------|
| Lightweight | 🔵 Blue | Q2, Q3 quantization **or** model ≤ 5GB |
| Recommended | 🟢 Green | Q4/Q5 range, model 5GB–20GB |
| Heavy | 🔴 Red | Q6, Q8 quantization **or** model > 20GB |

---

## 🛠️ Technologies

- **Vanilla HTML + CSS + JavaScript** — zero frameworks
- **Hugging Face API** — live model data
- **WebGL** — GPU detection via `WEBGL_debug_renderer_info`

---

## 📋 Requirements

- A modern web browser (Chrome, Edge, Firefox)
- Internet connection (for Hugging Face API calls)

---

## 📄 License

MIT — free to use, modify, and share.
