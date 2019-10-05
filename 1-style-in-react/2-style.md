# Встроенный стиль style = ' '
При создании компонентов, React рекомендует использовать встроенные стили `style=' '`, а по сути это чистый JavaScript-код.

* Создаём JavaScript объект состоящий из CSS-правила
* Данный объект помещаем в компонент в метод `render()`
* Двойные имена CSS-свойств записываем в `camelCase`
* Имя объекта оборачиваем в фигурные скобки и помещаем в качестве значения атрибута `style={objectName}`

    <!-- React-приложение -->
    <script type="text/babel">
        const letter = {
            textAlign: 'center',
            backgroundColor: '#eee',
            padding: 50
        }

        class Vowel extends React.Component {
            render () {
                const letterItem = {
                    color: '#333',
                    fontFamily: 'Courier New, Courier, monospace',
                    backgroundColor: '#ffde00',
                    display: 'inline-block',
                    padding: 10,
                    margin: 10,
                    fontSize: 32
                }

                return (
                    <div style={letterItem}>
                        {this.props.children}
                    </div>
                )
            }
        }

        ReactDOM.render(
            <div style={letter}>
                <Vowel>А</Vowel>
                <Vowel>Е</Vowel>
                <Vowel>Ё</Vowel>
            </div>,
            document.getElementById('root')
        );
    </script>
