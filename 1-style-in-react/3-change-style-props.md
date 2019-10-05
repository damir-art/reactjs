# Изменить стиль свойства
С помощью `props` можно изменять значения свойств стилей, при вызове компонента. Изменим фон компонента при его вызове.

    <!-- React-приложение -->
    <script type="text/babel">
        const letter = {
            textAlign: 'center',
            backgroundColor: '#eee',
            padding: 50
        }

        class Vowel extends React.Component {
            render () {
                const letterItem = {
                    color: '#333',
                    backgroundColor: this.props.bgcolor,
                    fontSize: 36,
                    fontWeight: 'bold'
                    fontFamily: 'Courier New, Courier, monospace',
                    display: 'inline-block',
                    padding: 10,
                    margin: 10,
                }

                return (
                    <div style={letterItem}>
                        {this.props.children}
                    </div>
                )
            }
        }

        ReactDOM.render(
            <div style={letter}>
                <Vowel bgcolor='#58b3ff'>А</Vowel>
                <Vowel bgcolor='#ff605f'>Е</Vowel>
                <Vowel bgcolor='#ffd52e'>Ё</Vowel>
            </div>,
            document.getElementById('root')
        );
    </script>
