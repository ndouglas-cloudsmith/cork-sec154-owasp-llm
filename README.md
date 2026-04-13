# Cork|Sec-154: OWASP LLM Security
This repository exists as a way to share simple copy-and-paste commands for investigating insecure Hugging Face models


## Pulling models from Hugging Face

This pulls the [26B MoE model](https://huggingface.co/unsloth/gemma-4-26B-A4B-it-GGUF) directly from a trusted **Hugging Face** [GGUF](https://huggingface.co/docs/hub/en/gguf) repo:
```
ollama run hf.co/unsloth/gemma-4-e4b-it-GGUF
```

This will automatically select a balanced quantisation (usually ```Q4_K_M```) for you.
<br/><br/>

The easiest way to pulls these models is via [Ollama registry](https://ollama.com/library/gemma4:e2b) directly.
```
ollama run gemma4:e2b
```

However, there's a whole community of forked models from security-focused authors such as [bartowski](https://huggingface.co/bartowski):
```
ollama pull hf.co/bartowski/Qwen2.5.1-Coder-7B-Instruct-GGUF:Q4_K_M
ollama run hf.co/bartowski/Qwen2.5.1-Coder-7B-Instruct-GGUF:Q4_K_M
```

You can of course cleanup the download model at any time:
```
ollama rm hf.co/bartowski/Qwen2.5.1-Coder-7B-Instruct-GGUF:Q4_K_M
```
