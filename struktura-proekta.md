# Обзор проекта React.js

На реакт создают SPA, для этого реакт и создан.

## Структура простейшего проекта
    public
        index.html (главная страница)
    src
        index.js  (подключение реакта и код)
        style.css (стили реакта)

## Структура проекта по-умолчанию
    node_modules (ничего там не трогаем, это различные пакеты, отвечающие за функционал нашего проекта/приложения)
    public
        favicon.ico   - фавиконка приложения
        index.html    - шаблон, входная страница приложения (SPA), стили, скрипты, сюда внедряются компоненты
        manifest.json - настройки для мобильных и десктоп приложений
    src (в основном кодим тут)
        index.js         - всё начинается с него
        App.js           - скрипт компонента (не нужен, тестовый)
        serviceWorker.js - сервисы для более эффективной работы приложений
    .gitignore        (заносит в игнор папки и файлы, которые не должны попасть в git)
    package-lock.json (не трогаем, системный файл)
    package.json      (dependencies - зависимости приложения)

## Работаем с проектом по-умолчанию
* Редактируем файл src/App.js (всё работает)
* В файле src/App.js удаляем всё внутри `className="App"`
* В файле src/App.js внутри `className="App"` пишем `<h1>Hello World!</h1>`
* В файле src/App.css всё удаляем
* Удаляем файл src/App.test.js
* Удаляем файл src/logo.svg

--
* В папке src удаляем всё кроме файла index.js
* В папке public удаляем всё кроме файла index.html
* Полностью очищаем файл index.js
* Частично очищаем файл index.html
