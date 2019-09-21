# inline стили в JSX

inline стили внутри React-компонента.

## App.js

    import React, {Component} from 'react';
    import './App.css';

    class App extends Component {
        render() {
            const divStyle = {
                textAlign: 'center'
            }

            return (
                <div style={divStyle}>
                    <h1 style={{color: 'green', textDecoration: 'underline'}}>Hello World!</h1>
                </div>
            );
        }
    }

    export default App;
