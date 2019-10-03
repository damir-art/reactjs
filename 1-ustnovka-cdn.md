# Установка React через CDN
Подключаем React с помощью CDN, скачать HTML-шаблон можно тут https://reactjs.org/docs/getting-started.html#online-playgrounds, ссылка 'download this HTML file'.

JS-файлы Rect'а подключаемые через CDN, лучше сохранить в виде файлов в корне проекта в папке react-cdn (иначе приложение будет долго откликаться).

Ядро React состоит из двух библиотек: сам react и react-dom (для работы с DOM-элементами). Babel нужен для преобразования JSX-кода в JS-код.

ReactDOM - библиотека отвечающая за то, чтобы внедрить какие-либо данные в HTML-код.

ReactDOM.render(JSX-код, куда_внедрить) - внедряет JSX-код (компоненты) в HTML-код
