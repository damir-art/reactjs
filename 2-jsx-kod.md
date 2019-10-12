# JSX-код
## Разница между JSX и JavaScript
Все теги (и одиночные) в JSX должный быть закрыты.

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

Если нужно добавить абзац или какой-нибудь еще какой-нибудь HTML-элемент, то их надо будет обрамить `div` тегом:

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

Внутри React можно использовать как JSX так и JavaScript:

    <script type="text/babel">
        const destination = document.getElementById('root')

        ReactDOM.render(
            <h1>Это React</h1>,
            destination
        );
    </script>

## Разное
* имена тегов нужно записывать с маленькой буквы
* имена компонентов должны начинаться с большой буквы (CamelCase)
* JSX-код может располагаться вне функций `render()` и `return()`
