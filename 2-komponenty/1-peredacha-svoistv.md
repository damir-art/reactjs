# Передача свойств
Передаём свойства в палитру, чтобы управлять цветом. Передаём значения свойств, дочерним элементам. Передача свойств осуществляется от предка к потомку.

    <!-- React-приложение -->
    <script type="text/babel">
        // Компоненты

        // Label
        class Label extends React.Component {
            render () {
                const labelStyle = {
                    color: '#333',
                    fontFamily: 'Segoe UI, Tahoma, Geneva, Verdana, sans-serif',
                    fontWeight: 'bold',
                    textTransform: 'uppercase',
                    fontSize: 22,
                    lineHeight: '22px',
                    textAlign: 'center',
                    marginTop: 14
                }

                return (
                    <div style={labelStyle}>
                        {this.props.color}
                    </div>
                )
            }
        }

        // Square
        class Square extends React.Component {
            render () {
                const squareStyle = {
                    height: 150,
                    backgroundColor: this.props.color
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
                    boxShadow: '3px 3px 5px rgba(33, 33, 33, 0.3)',
                    float: 'left',
                    marginLeft: 20
                }

                return (
                    <div style={cardStyle}>
                        <Square color={this.props.color} />
                        <Label color={this.props.color} />
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
                <Card color='#ff6663' />
                <Card color='#ffa737' />
            </div>,
            document.getElementById('root')
        );
    </script>
