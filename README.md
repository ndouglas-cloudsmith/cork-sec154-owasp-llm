# cork-sec154-owasp-llm
This repository exists as a way to share simple copy-and-paste commands for investigating insecure Hugging Face models


## Pulling models from Hugging Face

This pulls the [26B MoE model](https://huggingface.co/unsloth/gemma-4-26B-A4B-it-GGUF) directly from a trusted **Hugging Face** [GGUF](https://huggingface.co/docs/hub/en/gguf) repo:
```
ollama run hf.co/unsloth/gemma-4-26B-A4B-it-GGUF
```

This will automatically select a balanced quantisation (usually ```Q4_K_M```) for you.
