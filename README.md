# My Website — личный сайт-визитка Дениса Грибана

[![English](https://img.shields.io/badge/🌐_Language-English-blue?style=for-the-badge)](README.en.md)

![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-web%20framework-000000?logo=flask&logoColor=white)
![Gunicorn](https://img.shields.io/badge/Gunicorn-WSGI-499848?logo=gunicorn&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-Canvas-F7DF1E?logo=javascript&logoColor=black)

## О проекте

Мой личный сайт-визитка на **Flask**.

![Главная страница](img/home.png)

## Возможности

- **Интерактивный фон на Canvas.** Сетка из точек, соединённых линиями с ближайшими соседями: точки плавно дрейфуют, а линии подсвечиваются вокруг курсора. Анимация работает на JavaScript (Canvas 2D API) и библиотеке GSAP (TweenMax) и подстраивается под размер окна.
- **Ссылки на профили** в виде SVG-иконок с всплывающими подсказками: GitHub, Discord, Steam, почта, Telegram и MAX.
- **Навигация:** HOME, BLOG, WORK и CV.
- **Тёмная тема** оформлена на чистом CSS: flexbox-раскладка, круглый аватар, полупрозрачная фиксированная шапка.

## Используемые технологии

| Технология | Для чего используется |
| ---------- | --------------------- |
| [Python 3](https://www.python.org/) и [Flask](https://flask.palletsprojects.com/) | Серверная часть: маршрутизация и отдача страниц |
| [Jinja2](https://jinja.palletsprojects.com/) | Шаблоны (`render_template`, `url_for`), входит в состав Flask |
| [Gunicorn](https://gunicorn.org/) | WSGI-сервер для запуска в продакшене |
| HTML5, CSS3 | Разметка и оформление: flexbox, подсказки без JavaScript |
| JavaScript (Canvas 2D API) | Анимация фона |
| Inline SVG | Иконки соцсетей |

## Структура репозитория

```
My-Website/
├── app.py                # Flask-приложение и маршруты
├── requirements.txt      # зависимости: flask, gunicorn
├── templates/
│   └── index.html        # главная страница
└── static/
    ├── style.css         # стили
    ├── background.js     # анимация фона на Canvas
    └── img/
        └── main-avatar.jpg
```

## Установка и запуск

1. Установите [Python 3](https://www.python.org/downloads/).
2. Клонируйте репозиторий, создайте виртуальное окружение и установите зависимости:

   ```bash
   git clone https://github.com/DenkiGO/My-Website.git
   cd My-Website
   python -m venv venv
   source venv/bin/activate        # Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. Запустите сервер разработки и откройте <http://127.0.0.1:5000>:

   ```bash
   python app.py
   ```

Для продакшена используйте Gunicorn:

```bash
gunicorn app:app
```