# 🔑 Твой ключ на чердаке (Max версия)

Бот-воронка для игропрактика Наташи Люлькиной.  
Платформа: **Max** (max.ru)

## ⚠️ Важно: настройка под Max API

Max использует **собственный формат API**, не Telegram-совместимый.

### Что нужно узнать в личном кабинете Max:

1. **Базовый URL API** — обычно `https://api.max.ru/bot/v1/`
2. **Формат webhook** — как Max присылает сообщения (JSON структура)
3. **Endpoint отправки** — куда POST'ить сообщения
4. **Как передавать токен** — в заголовке или в теле запроса

### Если формат неизвестен

Бот автоматически логирует все входящие webhook'и в файл `unknown_webhooks.jsonl`.  
Отправь боту сообщение, потом скачай этот файл с сервера — и увидишь реальный формат Max.

## Быстрый старт

### 1. Настрой переменные окружения

Скопируй `.env.example` → `.env` и заполни:
- `MAX_BOT_TOKEN` — из кабинета Max
- `MAX_API_BASE` — URL API (из документации Max)
- `ADMIN_ID` — твой ID в Max

### 2. Залей на Render

Так же, как раньше:
- Build: `pip install -r requirements.txt`
- Start: `python bot.py`
- Environment Variables: скопируй из `.env`

### 3. Webhook в Max

В личном кабинете Max (business.max.ru) укажи webhook URL:  
`https://tvoy-klyuch-bot.onrender.com/webhook`

**Не используй** `api.max.ru/bot.../setWebhook` — в Max webhook настраивается в кабинете, не через API.

### 4. Тест

Напиши боту в Max: **ДОМ**
