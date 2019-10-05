# Свойства (props)
Компонент это аналог функции, давайте сделаем так чтобы компонент (как функция) начал принимать аргументы. И в этом нам помогут свойства (props).

    <!-- React-приложение -->
    <script type="text/babel">
        class Countries extends React.Component {
            render () {
                // Свойство компонента, принимает параметры
                return <li>{this.props.country}</li>
            }
        }

        ReactDOM.render(
            // Вызываем компонент с аргументами, передаем параметры (значения свойств) в компонент
            <ul>
                <Countries country='Англия' />
                <Countries country='США' />
                <Countries country='Россия' />
                <Countries country='Германия' />
                <Countries country='Китай' />
            </ul>,
            document.getElementById('root')
        );
    </script>

* `{ }` - в JSX внутри фигурных скобок, можно использовать JavaScript (внутри `ReactDOM.render()`)
* `this.props` - получаем доступ к свойству текущего компонента
* `this.props.capital` - свойство компонента, принимает параметры
* `country='Англия'` - атрибут HTML-подобного элемента (свойство, значение)

Свойств может быть сколько угодно.

## this.props.children - дочерние элементы компонентов
    render () {
        // Свойство компонента, принимает параметры
        return <li>{this.props.country}: {this.props.capital}, {this.props.children}</li>
    }
