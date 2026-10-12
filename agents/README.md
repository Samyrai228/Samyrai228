# agents/

Рабочая папка фермы AI-ботов.

| Папка | Что внутри |
|---|---|
| `skills/` | Официальные n8n-скиллы от n8n-io (Apache-2.0), под n8n ≥ 2.2. Через `.claude/skills` подхватываются автоматически в каждой сессии Claude Code |
| `workflows/` | JSON workflow для импорта в n8n (`Workflows → Import from File`) |
| `docs/` | План, схема БД, промпты, чек-листы тестов |

MCP: `.mcp.json` в корне подключает **n8n-mcp** без API-ключа. Это справочник
по всем нодам и валидатор JSON. Твой локальный n8n он не видит. Чтобы Claude мог сам
создавать workflow в твоём n8n, добавь в `env` значения `N8N_API_URL` (адрес туннеля)
и `N8N_API_KEY` (n8n → Settings → n8n API). Ключ не коммитить.
