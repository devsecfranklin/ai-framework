# AI Framework Project

This project is a centralized repository for documentation, scripts, and configuration for various AI frameworks, primarily focused on Google's Gemini (via `gemini-cli`) and Ollama.

## Project Structure

- `google/`: Contains documentation and assets related to Google AI.
  - `slides/`: Presentation files (`.odp`, `.tex`).
  - `README.md`: Quick start for `gemini-cli`.
- `ollama/`: Contains scripts and configuration for Ollama.
  - `build_ollama_jetson.sh`: Script for building Ollama on NVIDIA Jetson.
  - `gpu_selector.sh`: Script for GPU selection.
  - `Modelfile`: Custom model configuration for Ollama.
  - `ollama.service`: Systemd service file for Ollama.
  - `README.md`: Detailed setup and usage guide for Ollama.

## Key Frameworks

### Google Gemini
Usage primarily through `gemini-cli`:
```sh
npx @google/gemini-cli
```

### Ollama
Used for local LLM inference. Supports multimodal input and REST API interactions.

- **Local Endpoint:** `http://localhost:11434`
- **Remote/Network Endpoint:** `http://thelio.lab.bitsmasher.net:11434`

#### Common Commands
- Create a model: `ollama create franklin-test -f Modelfile`
- Show model info: `ollama show --modelfile llama3.2`

## Conventions & Workflows

- Documentation is primarily stored in `README.md` files within subdirectories.
- Shell scripts for hardware-specific setups are kept in the `ollama/` directory.
