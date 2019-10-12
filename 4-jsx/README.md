# JSX
## Как работает JSX
JSX &ndash; синтаксический сахар. Babel превращает JSX-код в JavaScript.

## JSX Syle
    class Car extends React.Component {
        render () {
            const carStyle = {
                color: '#333',
                fontFamily: 'Courier New, Courier, monospace',
                display: 'inline-block',
                margin: 10,
                fontSize: 32,
                lineHeight: '32px'
            }

            return (
                <div style={carStyle}>
                    <h3>Ford</h3>
                </div>
            )
        }
    }

## JSX vs JavaScript

JSX:

    return (
        <div style={carStyle}>
            <h3>Ford</h3>
        </div>
    )

JavaScript:

    return React.createElement (
        'div',
        {style: carStyle},
        React.createElement (
            'h3',
            null,
            'Ford'
        )
    )
