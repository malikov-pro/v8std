# Стандарты разработки 1С

https://v8std.ru

## Локальный MCP

```bash
docker compose -f docker-compose/docker-compose.yml up -d v8std-mcp
```

MCP-сервер будет доступен на `http://127.0.0.1:8765/mcp`. Если образа
`malikovpro/v8std-mcp` нет локально, он будет собран из репозитория.

Запуск без клонирования репозитория:

```bash
docker run -d --name v8std-mcp -p 127.0.0.1:8765:8765 malikovpro/v8std-mcp:latest
```

```bash
codex mcp add v8std-local --url http://127.0.0.1:8765/mcp
```
