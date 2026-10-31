## Start with ollama:

```bash
# Install ollama
curl -fsSL https://ollama.com/install.sh | sh
ollama --version
# Get qwen3:14b locally
ollama pull qwen3:14b
# Run the model
ollama run qwen3:14b
# Watch the hardware reponse
watch -n 0.5 nvidia-smi
watch -n 1 sensors
# Check the current running local LLMs
ollama ps
```


