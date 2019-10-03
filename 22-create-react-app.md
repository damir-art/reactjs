# create-react-app
https://create-react-app.dev/<br />
https://github.com/facebook/create-react-app

**create-react-app** позволяет работать со множестовм файлов и страниц, имеет автообновление и babel не нужно подключать. Всё это работает намного быстрее чем через CDN.

Автоматизирует работу с React, в отличии от HTML-шаблона быстро работает, автоматом компилирует JSX в JS и обновляет страницу браузера. Позволяет созавать приложения основываясь на React, не настраивая вообще ничего.

## Установка create-react-app
Создём локальную среду разработки для React. Сконфигурируем все инструменты для разработки:
* Устанавливаем node.js (проверяем версию node.js и версию npm)
* Устанавливаем глобально утилиту Create React APP `npm install -g create-react-app`

## Создание проекта
* Переходим в терминале в папку где хотите расположить проект.
* Вводим `create-react-app react-theory` (создаём проект с именем 'react-theory').
* Папка 'react-theory' создастся автоматически, долго будет грузиться и создаваться (скачивание и установка необходимых пакетов, списков зависимостей и т.д.).
* Переходим в папку `cd react-theory`
* Набираем `npm run start` (или `npm start`)
* В браузере откроется страница http://localhost:3000/ с приветствием от React
* Ctrl + C (остановить проект)

**ВНИМАНИЕ** чтобы работать с проектом, в терминале `react-app` должен быть всегда запущен.
Иногда нужно принудительно обновлять страницу браузера, чтобы увидеть изменения.

При установке проектов, их *можно* создавать и запускать через `yarn` (технологию фейсбук), для этого её нужно установить `npm install -g yarn`.


## Команды проекта
    npm start     # старт проекта, сервера зразработки
    npm run build # собирает проект для продакшена (хостинга)
    npm test      # запускает скрипт для теста проекта
    npm run eject # Removes this tool and copies build dependencies, configuration files and scripts into the app directory. If you do this, you can’t go back!
    
    cd react-theory # переходим в папку проекта
    npm start       # стартуем проект