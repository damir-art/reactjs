# Добавляем событие
https://ru.reactjs.org/docs/handling-events.html<br />
https://ru.reactjs.org/docs/events.html

* Создадим кнопку, при клике на которой, будет изменяться текст заголовка.
* Имена событий записываются в camel case.
* Обработчики событий (функции) создаём в начале компонента, метод render() обычно располагают в самом конце компонента.
* В именах обработчиков событий обычно используют слово `handler`.

Обработчики событий, обычно записывают как стрелочные функции. Обработчики событий это методы компонента (`this`).

    class App extends Component {
        state = {
            cars: [
                {name: 'Ford', year: 2019},
                {name: 'BMW',  year: 2018},
                {name: 'Audi', year: 2016}
            ],
            pageTitle: 'Заголовок страницы (h1)'
        }

        HandlerTitleChange = () => {
            console.log('HandlerTitleChange')
        }

        render() {
            const divStyle = {
                textAlign: 'center'
            }

            const cars = this.state.cars

            return (
                <div style={divStyle}>
                    <h1>{this.state.pageTitle}</h1>

                    <button onClick={this.HandlerTitleChange}>Изменяем заголовок</button>

                    <Car name={cars[0].name} year={cars[0].year} />
                    <Car name={cars[1].name} year={cars[1].year} />
                    <Car name={cars[2].name} year={cars[2].year} />
                </div>
            );
        }
    }
