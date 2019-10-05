# Назначаем стиль классу

В JSX, классы тегам назначаются через `className=' '`

    <style>
        .letter {
            text-align: center;
            background-color: #eee;
            padding: 50px;
        }
        .letter__item {
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
                    <div className="letter__item">
                        {this.props.children}
                    </div>
                )
            }
        }

        ReactDOM.render(
            <div className="letter">
                <Vowel>А</Vowel>
                <Vowel>Е</Vowel>
                <Vowel>Ё</Vowel>
            </div>,
            document.getElementById('root')
        );
    </script>
