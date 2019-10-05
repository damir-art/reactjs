# Дочерние элементы компонентов
`this.props.children` &ndash; дочерние элементы компонентов.

* Создадим компонент тега кнопки `<button>`, дочерним элементом компонента сделаем текст кнопки.
* Имена компонентов и свойств можно использовать как имена тегов и атрибутов HTML.

Код скрипта:

    <!-- Место куда будет внедрятся наш React-код -->
    <div id="root"></div>
    
    <!-- React-приложение -->
    <script type="text/babel">
        class Button extends React.Component {
            render () {
                return <button type={this.props.type}>{this.props.children}</button>
            }
        }

        ReactDOM.render(
            <Button type='submit'>Отправить</Button>,
            document.getElementById('root')
        );
    </script>
