# Передача свойств в React

Передача свойств от предка к потомкам. В React, передача свойств происходит от родителя к дочернему элементу и далее. Сразу от предка к потомку минуя промежуточные компоненты передать не получится, нужно пройти всю цепочку. Свойство можно передать только от предка к потомку, но не наоборот.

this.props.property<br />
props - объект в котором хранятся все свойства компонента.

* отправляем несколько свойств от компонента к компоненту
* используем оператор расширения

До использования оператора расширения:

    <script type="text/babel">
        class AutoColor extends React.Component {
            render () {
                return (
                    <b>{this.props.color}</b>
                )
            }
        }

        class AutoName extends React.Component {
            render () {
                return (
                    <h3>{this.props.brand} {this.props.model}</h3>
                )
            }
        }

        class Auto extends React.Component {
            render () {
                return (
                    <div>
                        <AutoName brand={this.props.brand} model={this.props.model} />
                        <ul>
                            <li>{this.props.brand}</li>
                            <li>{this.props.model}</li>
                            <li>{this.props.color}</li>
                        </ul>
                        <AutoColor color={this.props.color} />
                        <hr />
                    </div>
                )
            }
        }

        ReactDOM.render(
            <div>
                <Auto brand='Chevrolet' model='Aveo' color='Белый' />
                <Auto brand='BMW' model='3' color='Изумрудный' />
                <Auto brand='Ford' model='Mustang' color='Красный' />
            </div>,
            document.getElementById('root')
        )
    </script>
