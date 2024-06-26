# Помощник GPT в Telegram

## Описание

Помощник GPT для Telegram — это не бот, а интеллектуальный помощник, который реализован на основе технологий OpenAI и Yandex. Это решение предоставляет возможность пользователям взаимодействовать с моделями искусственного интеллекта прямо через свой аккаунт в Telegram, отправляя сообщения в диалоги и получая ответы.

## Особенности
- **Использование AI моделей от OpenAI и Yandex Cloud.**
- **Личная авторизация:** все сообщения отправляются от имени пользователя.
- **Поддержка нескольких диалогов:** управление и сохранение истории переписки с различными собеседниками.
- **Интеграция с Python и Telegram API,** что обеспечивает гибкую настройку и расширение функциональности.
- **Автоматическая отправка сообщений** с формируемыми задержками, что делает общение более естественным.

## Начало работы

### Необходимые условия
Убедитесь, что у вас установлен Python 3.6 или выше, а также следующие библиотеки:
- `pyrogram`
- `tgcrypto`
- `openai`
- `tiktoken`
- `ipywidgets`

### Установка зависимостей
```bash
pip install -U pyrogram tgcrypto openai tiktoken ipywidgets
```

### Требуемые ключи API
- **API ID и API HASH для Telegram:** получить можно [здесь](https://core.telegram.org/api/obtaining_api_id).
- **OAuth Token для Yandex Cloud:** инструкции [здесь](https://yandex.cloud/ru/docs/iam/operations/iam-token/create#api_1).
- **API ключ для OpenAI:** доступен на [платформе OpenAI](https://platform.openai.com/api-keys).

### Конфигурация
В начале скрипта необходимо задать все ключи и токены:
```python
api_id = 'ВАШ_API_ID'
api_hash = 'ВАШ_API_HASH'
OAuthTokenYa = 'ВАШ_YANDEX_OAUTH_TOKEN'
FOLDER_ID = 'ВАШ_YANDEX_FOLDER_ID'
api_key = 'ВАШ_OPENAI_API_KEY'
```

### Запуск
Скрипт предполагает запуск в среде, поддерживающей выполнение IPython-скриптов (например, Jupyter Notebook).

## Использование
Во время первого запуска скрипт запросит выбор активных диалогов в Telegram. После выбора идентификатора диалога, скрипт последовательно выполнит следующие шаги:
1. Загрузит историю сообщений.
2. Отформатирует полученные сообщения для передачи в модель AI.
3. Отправит полученные данные на сервер OpenAI или Yandex для получения ответа.
4. Вернёт и отобразит сгенерированный ответ в формате текста.
