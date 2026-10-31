# Max AI v2 — OpenAI Video Studio
Адаптивный веб-сайт с установкой на iPhone/Android как PWA. Сервер вызывает OpenAI Videos API.
## Возможности
- Sora 2 / Sora 2 Pro, prompt-to-video
- Необязательный референс JPG/PNG/WebP до 20 МБ
- 16:9 / 9:16, 4/8/12 секунд
- Асинхронный статус, просмотр и скачивание MP4
- API-ключ только в серверной переменной `OPENAI_API_KEY`
## Запуск
Требуется Node.js 20+: `npm install`, затем задать `OPENAI_API_KEY` в окружении и `npm start`. Откройте http://localhost:3000.
## Render
1. Загрузите файлы репозитория в GitHub.
2. В Render выберите New → Blueprint и подключите репозиторий с `render.yaml`.
3. Добавьте `OPENAI_API_KEY` в Environment как Secret, запустите Deploy.
## Важно перед публичным запуском
Доступ к моделям и API-биллинг должны быть включены в OpenAI. Подписка ChatGPT не заменяет API-биллинг. Это MVP: задания хранятся на стороне OpenAI, отдельной истории пользователей/аккаунтов нет. Перед публичным использованием добавьте авторизацию, квоты и лимиты на пользователя, постоянную БД, очередь, мониторинг, privacy policy и abuse controls. Сейчас публичный endpoint может расходовать API-баланс владельца. Никогда не коммитьте реальный ключ и не вставляйте его в frontend.
Документация: https://developers.openai.com/api/docs/guides/video-generation
