# Передача параметров в события
Передаем параметры через события в обработчики событий.

Car.js (компонент)

    <Car
        name={cars[0].name}
        year={cars[0].year}
        onChangeTitle={this.HandlerTitleChange}
    />

App.js (простой компонент)

    export default (props) => (
        <div>
            <h2>Car name: {props.name}</h2>
            <p>Year: <b>{props.year}</b></p>
            <button onClick={props.onChangeTitle}>Click</button>
        </div>
    )
