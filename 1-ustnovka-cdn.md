# Установка React через CDN
Самый простой способ начать работу с React, это подключить все необходимые файлы через CDN. Для этого можно скачать HTML-файл с официального сайта: https://reactjs.org/docs/getting-started.html#online-playgrounds, где кликаем по ссылке **download this HTML file**.

Либо можно воспользоваться моей версией HTML-файла:

    <!DOCTYPE html>
    <html>
    <head>
        <meta charset="UTF-8" />
        <title>React</title>
        <!-- React - Основная библиотека React -->
        <script src="https://unpkg.com/react@16/umd/react.development.js"></script>
        <!-- React-DOM - компонент React для работы с DOM -->
        <script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
        <!-- Babel - библиотека Babel для преобразования JSX-кода в JavaScript-код -->
        <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
    </head>
    <body>

        <!-- Место куда будет внедрятся наш React-код -->
        <div id="root"></div>

        <!-- React-приложение -->
        <script type="text/babel">
            ReactDOM.render(
                <h1>Это React</h1>,
                document.getElementById('root')
            );
        </script>

    </body>
    </html>

Подключаемые через CDN файлы React и Babel, лучше сохранить на диске в отдельной папке например `reactCDN`, в корне вашего проекта, чтобы ваше приложение быстрее откликалось.

Ядро React состоит из двух библиотек: сам react и react-dom (для работы с DOM-элементами). Babel нужен для преобразования JSX-кода в JS-код.

ReactDOM - библиотека отвечающая за то, чтобы внедрить какие-либо данные в HTML-код.

ReactDOM.render(JSX-код, куда_внедрить) - внедряет JSX-код (компоненты) в HTML-код
