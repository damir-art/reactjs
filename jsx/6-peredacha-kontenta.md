# Передача контента
Передача контента между компонентами.

`{props.children}` - здесь хранится то, что передано между тегами `Car`.

## App.js
    class App extends Component {
        render() {
            return (
                <div>
                    <h1>Список автомобилей</h1>
                    <Car name={'Ford'} year={2019}>
                        <p style={{color: 'green'}}>Передача контента</p>
                    </Car>
                    <Car name={'BMW'} year={2018} />
                    <Car name={'Mazda'} year={2015} />
                </div>
            );
        }
    }

## Car.js
Props - параметр функции, если параметр один, то скобки можно убрать.

    export default props => (
        <div>
            <h2>Car name: {props.name}</h2>
            <p>Year: <b>{props.year}</b></p>
            {props.children}
        </div>
    )
