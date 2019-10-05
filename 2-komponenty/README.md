# Компоненты в React
* Обычно разработчика React просят реализовать какой-нибудь пользовательский интерфейс.
* Создаём карточку цветовой палитры.
* Пишем код, при котором, один компонент вызывает другой компонент.

Прежде чем создать пользовательский интерфейс нужно:
* Определить основные визуальные элементы.
* Выяснить какие компоненты нужно будет создавать.

Правила создания компонента:
* Не каждый визуальный элемент должен быть компонентом.
* Компонент (как и функция) должен делать только что-то одно.

## Создаём пользовательский интерфейс
Карточка цветовой палитры состоит из трех компонентов (class): **Card** *(обертка)*, **Square** *(квадрат цвет)*, **Label** *(цвет текстом)*.

    <!-- React-приложение -->
    <script type="text/babel">
        // Компоненты

        // Label
        class Label extends React.Component {
            render () {
                const labelStyle = {
                    fontFamily: 'Segoe UI, Tahoma, Geneva, Verdana, sans-serif',
                    // fontWeight: 'bold',
                    textTransform: 'uppercase',
                    fontSize: 24,
                    lineHeight: '24px',
                    textAlign: 'center',
                    marginTop: 13
                }

                return (
                    <div style={labelStyle}>
                        #ff6663
                    </div>
                )
            }
        }

        // Square
        class Square extends React.Component {
            render () {
                const squareStyle = {
                    height: 150,
                    backgroundColor: '#ff6663'
                }

                return (
                    <div style={squareStyle}></div>
                )
            }
        }

        // Card
        class Card extends React.Component {
            render () {
                const cardStyle = {
                    width: 150,
                    height: 200,
                    backgroundColor: '#f6f6f6',
                    boxShadow: '3px 3px 5px rgba(33, 33, 33, 0.3)'
                }

                return (
                    <div style={cardStyle}>
                        <Square />
                        <Label />
                    </div>
                )
            }
        }

        // ReactDOM.render
        const cards = {
            backgroundColor: '#eee',
            padding: 50
        }

        ReactDOM.render(
            <div style={cards}>
                <Card />
            </div>,
            document.getElementById('root')
        );
    </script>
