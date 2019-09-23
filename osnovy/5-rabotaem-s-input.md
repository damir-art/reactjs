# Работаем с input
Пишем в input текст, данный текст заменяет текст заголовка.

App.js

    // Обработчик
    HandlerTitleChangeInput = (event) => {
        console.log('input', event.target.value)
        this.setState({
            pageTitle: event.target.value
        })
    }
    
    // Заголовок
    <h1>{this.state.pageTitle}</h1>

    // Событие
    <input onChange={this.HandlerTitleChangeInput} type="text" />
