# Стили CSS в React

Стили можно назначать тегам, классам, атрибутам style и т.д

## Назначаем стили тегу

    <style>
        #root {
            background-color: #eee;
            padding: 50px;
        }
        #root > div {
            text-align: center;
        }
        #root div div {
            color: #333;
            font-family: 'Courier New', Courier, monospace;
            background-color: #ffde00;
            display: inline-block;
            padding: 10px;
            margin: 10px;
            font-size: 32px;
        }
    </style>

    <!-- Место куда будет внедрятся наш React-код -->
    <div id="root"></div>
    
    <!-- React-приложение -->
    <script type="text/babel">
        class Vowel extends React.Component {
            render () {
                return (
                    <div>
                        {this.props.children}
                    </div>
                )
            }
        }

        ReactDOM.render(
            <div>
                <Vowel>А</Vowel>
                <Vowel>Е</Vowel>
                <Vowel>Ё</Vowel>
            </div>,
            document.getElementById('root')
        );
    </script>
