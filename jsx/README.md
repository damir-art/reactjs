# Основы JSX

JSX - специальный синтаксис языка React.

## index.js
    ReactDOM.render(
        <App />,
        document.getElementById('root')
    );

`<App />` - это компонент (функция), вместо него можно написать любой HTML-код (он должен быть обрамлен одним тегом):

    ReactDOM.render(
        <div>
            <h1>Заголовок</h1>
            <p>Абзац</p>
        </div>,
        document.getElementById('root')
    );
    
## App.js

Код написанный на JSX:

    function App() {
        return (
            <div></div>
        );
    }

Такой же код, но без JSX:

    function App() {
        return React.createElement(
            'div', // тег
            null   // оциии тега
        )
    }
