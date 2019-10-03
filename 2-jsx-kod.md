# JSX-код
## Разница между JSX и JavaScript

JSX:

    <script type="text/babel">
        ReactDOM.render(
            <h1>Это React</h1>,
            document.getElementById('root')
        );
    </script>

JavaScript (без `type="text/babel"`):

    <script>
        ReactDOM.render(
            React.createElement(
                'h1',       // название тега
                null,       // дополнительные свойства
                'Это React' // то что внутри тега (текст или другие теги)
            ),
            document.getElementById('root')
        );
    </script>

Если хотим добавить абзац или какой-нибудь еще какой-нибудь HTML-элемент, то их надо будет обрамить `div` тегом:

    <!-- React-приложение -->
    <script type="text/babel">
        ReactDOM.render(
            <div>
                <h1>Это React</h1>
                <p>Добро пожаловать на курс</p>
            </div>,
            document.getElementById('root')
        );
    </script>
