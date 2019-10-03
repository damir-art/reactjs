# React компонент

Создадим простой компонент  - карточка товара на странице категорий, который будет содержать: название авто, год выпуска. Структура кода у товаров одинаковая их много, стиль и поведение можно реализовать одним компонентом. ReactDOM.render() - внедрение компонента в HTML.

Создаём функцию, которая возвращает структуру компонента. В теге, атрибут `class` меняем на `className`.

    <script type="text/babel">
        // Простой React-компонент (обычная функция):
        function Car() {
            return (
                <div className="car">
                    <div className="car__name">Ford Focus</div>
                    <div className="car__year">2017</div>
                </div>
            )
        }

        // Внедряем простой React-компонент:
        ReactDOM.render(
            <Car />,
            document.querySelector('#root')
        );
    </script>

## Добавляем свойства (props)

    <script type="text/babel">
        function Car(props) {
            return (
                <div className="car">
                    <h3 className="car__name">{props.name}</h3>
                    <p className="car__year">Year: <strong>{props.year}</strong></p>
                </div>
            )
        }

        ReactDOM.render(
            <Car name="Ford Focus" year="2015" />,
            document.querySelector('#root')
        );
    </script>

## Добавляем много товаров
В метод .render() можно занести лишь один элемент, чтобы добавить несколько, их нужно обернуть в один элемент:

    <script type="text/babel">
        function Car(props) {
            return (
                <div className="car">
                    <h3 className="car__name">{props.name}</h3>
                    <p className="car__year">Year: <strong>{props.year}</strong></p>
                </div>
            )
        }

        const App = (
            <div>
                <Car name="Ford Focus" year="2015" />
                <Car name="Ford Mondeo" year="2016" />
                <Car name="Opel Astra" year="2017" />
                <Car name="Mazda 3" year="2017" />
            </div>
        )

        ReactDOM.render(
            App,
            document.querySelector('#root')
        );
    </script>
