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
