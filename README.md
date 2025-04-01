# Web-texnology

## Base URL
`http://localhost:3000/`

## Authentication
JWT Token в заголовке `Authorization: Bearer <token>`

### Endpoints:

| Метод | Путь | Описание |
|-------|------|----------|
| POST  | `/register` | Регистрация пользователя |
| POST  | `/login`    | Авторизация |
| POST   | `/upload`   | Загрузка видео
| POST  | `/chat`  | Отправить сообщение в чат |
| POST   | `/videos/:id` | Открыть видео |

## Примеры запросов:

**Регистрация:**
```bash
curl -X POST https://api.videostream.example.com/v1/register \
  -H "Content-Type: application/json" \
  -d '{"login":"admin", "password":"admin"}'


---

#### 2. **Project Report** (`/docs/report.md`)

```markdown
# VideoStream Platform: Отчёт о разработке

## 📌 Использованные технологии
- **Frontend**: React 18, HTML, CSS
- **Backend**: Django
- **База данных**: SQLite

## 🚀 Ключевые функции
1. Загрузка/просмотр видео
2. Система чатов
3. JWT-аутентификация

## 🔧 Проблемы и решения

### 1.	Проблемы с CORS (Cross-Origin Resource Sharing): 
**Описание**: При взаимодействии между фронтендом и бэкендом, работающими на разных доменах или портах, могут возникать ошибки CORS. 
**Решение**: Настройка сервера для разрешения запросов с определенных источников с помощью заголовков CORS. 
### 2.	Аутентификация и авторизация: 
**Описание**: Обеспечение безопасной аутентификации пользователей и управление доступом к ресурсам. 
**Решение**: Использование JWT (JSON Web Tokens) для аутентификации и настройка маршрутов с учетом ролей пользователей. 
### 3.	Загрузка и хранение видео: 
**Описание**: Обработка больших файлов видео может быть сложной задачей из-за ограничений на размер файла и времени загрузки. 
**Решение**: Настройка сервера для обработки больших файлов и использование асинхронной загрузки. 
### 4.	Проблемы с производительностью: 
**Описание**: Обработка и потоковая передача видео могут потреблять значительные ресурсы сервера. 
**Решение**: Оптимизация кода и использование кэширования, а также рассмотрение возможности использования CDN для доставки контента.


## Структура проекта 
├── front/
│ ├── public/
│ │ ├── index.html 
│ │ ├── favicon.ico
│ │ ├── logo192.png
│ │ ├── logo512.png
│ │ ├── manifest.json 
│ │ └── robots.txt 
│ ├── src/
│ │ ├── index.js 
│ │ ├── App.js 
│ │ ├── App.css 
│ │ ├── components/
│ │ │ ├── Auth/
│ │ │ │ ├── Login.js
│ │ │ │ ├── Register.js  
│ │ │ ├── ChatMessage.js
│ │ │ ├── VideoList.js
│ │ │ ├── VideoPlayer.js
│ │ │ ├── VideoUpload.js 
│ │ │ └── global.css 
│ ├── 1.png 
│ ├── App.css
│ ├── App.js
│ ├── ChatMessage.css
│ ├── index.js
│ ├── logo.svg
│ ├── VideoList.css
│ ├── VideoPlayer.css
│ ├── VideoUpload.css 
│ └── package.json 
│
├── back/
│ ├── src/
│ │ ├── main.py 
│ │ ├── config/
│ │ │ └── settings.py 
│ │ ├── api/
│ │ │ ├── init.py
│ │ │ ├── auth.py 
│ │ │ ├── videos.py 
│ │ │ └── chat.py 
│ │ ├── models/
│ │ │ ├── user.py 
│ │ │ ├── video.py 
│ │ │ └── message.py 
│ │ ├── services/
│ │ │ ├── auth_service.py 
│ │ │ └── stream_service.py 
│ │ ├── static/ 
│ │ ├── templates/ 
│ │ └── requirements.txt 
│ ├── Dockerfile 
│ ├── .env 
│ └── nginx/
│ └── nginx.conf
│
├── docker-compose.yml
├── README.md
└── docs/
├── API.md 
└── DEPLOYMENT.md 
