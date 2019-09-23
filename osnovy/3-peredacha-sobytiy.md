# Передача событий
Передача событий от простого компонента к компоненту. В простом компоненте задаем имя события самостоятельно.

Простой функциональный компонент:

    export default (props) => (
        <div>
            <h2>Car name: {props.name}</h2>
            <p>Year: <b>{props.year}</b></p>
            <button onClick={props.onChangeTitle}>Click</button>
        </div>
    )

Обычный компонент, созданный на основе `Component`:

    <Car
        name={cars[0].name}
        year={cars[0].year}
        onChangeTitle={this.HandlerTitleChange}
    />
