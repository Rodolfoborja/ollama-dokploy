# Ollama para Dokploy

Docker Compose para ejecutar [Ollama](https://ollama.ai) en Dokploy.

## Configuración

1. Despliega este repositorio en Dokploy como Docker Compose
2. El servicio estará disponible en el puerto `11434`

## Uso

Una vez desplegado, descarga modelos con:

```bash
docker exec ollama ollama pull llama3
```

O desde la API:

```bash
curl http://tu-servidor:11434/api/pull -d '{"name": "llama3"}'
```

## GPU (opcional)

Si tu servidor tiene GPU NVIDIA, descomenta las líneas de `deploy` en el `docker-compose.yml`.

## Modelos recomendados

- `llama3` - Meta Llama 3 (8B)
- `mistral` - Mistral 7B
- `codellama` - Para código
- `phi3` - Microsoft Phi-3 (ligero)
