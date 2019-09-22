# Передача параметров
Передаём параметры из одного компонента в другой.

## Car.js
Props - параметр функции, если параметр один, то скобки можно убрать.

    export default props => (
        <div>
            <h2>Car name: {props.name}</h2>
            <p>Year: <b>{props.year}</b></p>
        </div>
    )

## App.js
    class App extends Component {
        render() {
            return (
                <div>
                    <h1>Список автомобилей</h1>
                    <Car name={'Ford'} year={2019} />
                    <Car name={'BMW'} year={2018} />
                    <Car name={'Audi'} year={2016} />
                    <Car name="Mazda" year="2015" />
                </div>
            );
        }
    }

Если передаём обычную строку, то можно убрать фигурные скобки: `<Car name="Ford" year="2019" />`
