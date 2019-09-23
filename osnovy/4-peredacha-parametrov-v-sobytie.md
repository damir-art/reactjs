# Передача параметров в события
Передаем параметры через события в обработчики событий.<br />
Кликаем по кнопке, передаем текст (параметр) в обработчик, этот текст заменяет текст заголовка.


## Первый способ, передача через bind()

Car.js (обработчик события)

    HandlerTitleChange = (newTitle) => {
        this.setState({
            pageTitle: newTitle
        })
    }

Car.js (компонент)
    
    <button 
        onClick={this.HandlerTitleChange.bind(this, 'Hello')}
    >Изменяем заголовок</button>

    <Car
        name={cars[0].name}
        year={cars[0].year}
        onChangeTitle={this.HandlerTitleChange.bind(this, cars[0].name)}
    />

App.js (простой компонент)

    export default (props) => (
        <div>
            <h2>Car name: {props.name}</h2>
            <p>Year: <b>{props.year}</b></p>
            <button onClick={props.onChangeTitle}>Click</button>
        </div>
    )

## Второй способ, передача через ссылку на функцию
Второй способ, передачи параметра, это передача ссылки на функцию.

Car.js

    <Car
        name={cars[1].name}
        year={cars[1].year}
        onChangeTitle={() => this.HandlerTitleChange(cars[1].name)}
    />
