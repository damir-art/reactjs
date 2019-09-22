# Передача параметров
Передаём параметры из одного компонента в другой.

    class App extends Component {
        render() {
            return (
                <div>
                    <h1>Список автомобилей</h1>
                    <Car name={'Ford'} year={2019} />
                    <Car name={'BMW'} year={2018} />
                </div>
            );
        }
    }

Если передаём обычную строку, то можно убрать фигурные скобки: `<Car name="Ford" year="2019" />`
