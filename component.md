# React компонент

Создадим простой компонент на примере карточки товара на странице категорий: Название авто, год выпуска. Структура кода у товаров одинаковая их много, стиль и поведение можно реализовать одним компонентом.

React создаёт функцию, которая возвращает структуру компонента. В теге, атрибут `class` меняем на `className`

Простой React-компонент (обычная функция):

    function Car() {
        return (
            <div className="car">
                <div className="car__name">Ford Focus</div>
                <div className="car__year">2017</div>
            </div>
        )
    }

Внедряем простой React-компонент:

    ReactDOM.render(
        <Car />,
        document.querySelector('#root')
    );
