```bash
# generar la secret
openssl rand -hex 32

# desplegar la infraestructura
podman kube play --replace infra/play.yaml

podman logs -f open-webui-open-webui

podman kube down infra/play.yaml
```

## environment variables

```bash
# Para modelos LLM (SDK OpenAI / LiteLLM)
OPENAI_BASE_URL=https://ai.hpc.cedia.edu.ec/v1
OPENAI_API_KEY=sk-123fake
OPENAI_MODEL=cedia-qwen-large-thinking

# Para servicios de RAG, Embeddings, Indexación y Rerank (/rag, /index, /search)
CEDIA_ADVANCED_API_KEY=123fake
CEDIA_RAG_COLLECTION=chbueno_collection_espol
```