# Настройка GitHub для аккаунта finetique13

## 1. Создать репозиторий на GitHub

1. Войдите на [github.com](https://github.com) под аккаунтом **finetique13**
2. Нажмите **+** → **New repository**
3. **Repository name:** `trader-diary`
4. **Description:** Дневник трейдера — учёт торговых результатов
5. Выберите **Public**
6. **НЕ** добавляйте README, .gitignore, license — репозиторий уже есть локально
7. Нажмите **Create repository**

## 2. Отправить код

После создания пустого репозитория выполните в терминале:

```bash
cd /Users/vladimirsolin/AI
git push -u origin main
```

## 3. Аутентификация

При запросе учётных данных:
- **Username:** finetique13
- **Password:** используйте **Personal Access Token** (не пароль от аккаунта)

### Создание токена:
1. GitHub → Settings → Developer settings → Personal access tokens
2. **Tokens (classic)** → **Generate new token**
3. Выберите срок действия и права: `repo` (полный доступ к репозиториям)
4. Скопируйте токен и вставьте как пароль при `git push`

## 4. Альтернатива: SSH

Если настроите SSH-ключ:
```bash
git remote set-url origin git@github.com:finetique13/trader-diary.git
git push -u origin main
```

## 5. GitHub Pages (опционально)

Для публикации дневника в интернете:
1. Repo → Settings → Pages
2. Source: **Deploy from a branch**
3. Branch: **main** → папка **/trader-diary** (или root)
4. Save — сайт будет на `https://finetique13.github.io/trader-diary/`
