# Оператор расширения `...`
Используем оператор расширения `...` при передаче свойств, компонентам. Оператор расширения, разворачивает массив на отдельные элементы.

Расмотрим пример на JavaScript без **оператора расширения**:

    const cars = ['Ford', 'BMW', 'Audi']

    function carsName(a, b, c) {
        return a + ' ' + b + ' ' + c
    }

    console.log(carsName(cars[0], cars[1], cars[2]))

Пример на JavaScript с **оператором расширения**:

    const cars = ['Ford2', 'BMW2', 'Audi2']

    function carsName(a, b, c) {
        return a + ' ' + b + ' ' + c
    }

    console.log(carsName(...cars))

## Оператор расширения в React

    class Auto extends React.Component {
        render () {
            return (
                <div>
                    <AutoName {...this.props} />
                    <ul>
                        <li>{this.props.brand}</li>
                        <li>{this.props.model}</li>
                        <li>{this.props.color}</li>
                    </ul>
                    <AutoColor {...this.props} />
                    <hr />
                </div>
            )
        }
    }
