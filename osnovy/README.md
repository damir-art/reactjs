# Основы React

## Что такое State
State необходим для того чтобы избежать дублирования, например дублирования карточки товара. **State** - это объект который содержит в себе все данные с которыми мы работаем, например база данных. **State** - это свойство, которое присутсвует в компонентах наследующихся от `Component`.

### Простой метод создания State
**State** - это JavaScrpt-объект, который описывает то состояние в котором сейчас находится данный компонент.<br />
**this** - это текущий компонент.

    class App extends Component {
        state = {
            cars: [
                {name: 'Ford', year: 2019},
                {name: 'BMW',  year: 2018},
                {name: 'Audi', year: 2016}
            ]
        }

        render() {
            const cars = this.state.cars

            return (
                <div>
                    <h1>Список автомобилей</h1>
                    <Car name={cars[0].name} year={cars[0].year} />
                    <Car name={cars[1].name} year={cars[1].year} />
                    <Car name={cars[2].name} year={cars[2].year} />
                </div>
            );
        }
    }

### Добавляем второй State
Добавляем еще один State, отвечающий за заголовок страницы (h1).

    class App extends Component {
        state = {
            cars: [
                {name: 'Ford', year: 2019},
                {name: 'BMW',  year: 2018},
                {name: 'Audi', year: 2016}
            ],
            pageTitle: 'Заголовок страницы (h1)'
        }

        render() {
            const cars = this.state.cars

            return (
                <div>
                    <h1>{this.state.pageTitle}</h1>
                    <Car name={cars[0].name} year={cars[0].year} />
                    <Car name={cars[1].name} year={cars[1].year} />
                    <Car name={cars[2].name} year={cars[2].year} />
                </div>
            );
        }
    }
