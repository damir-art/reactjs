# Изменяем имя заголовка страницы
По событию, изменяем имя заголовка страницы, которое хранится в **State**.

Чтобы изменить State (состояние), нужно использовать метод у `Component`, который нам доступен благодаря наследованию. Данный метод называется `setState()`.

    class App extends Component {
        state = {
            cars: [
                {name: 'Ford', year: 2019},
                {name: 'BMW',  year: 2018},
                {name: 'Audi', year: 2016}
            ],
            pageTitle: 'Заголовок страницы'
        }

        HandlerTitleChange = () => {
            const oldPageTitle = this.state.pageTitle
            const newPageTitle = oldPageTitle + '. Изменён!'

            this.setState({
                pageTitle: newPageTitle
            })
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
