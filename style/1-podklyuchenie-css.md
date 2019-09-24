# Подключение CSS
Пишем CSS в отдельных CSS-файлах.
* React автоматически поддерживает автопрефикс

Структура компонента Car:

    Car
        Car.js
        Car.css

Код Car.css:

    .Car {
        display: 'inline-block',
        background-color: '#eee',
        margin-bottom: '20px',
        margin-right: '20px',
        padding: '20px',
        padding-top: '0px',
        box-shadow: '4px 4px 8px 0 rgba(0, 0, 0, 0.2)',
        border-radius: '5px'
    }

Код в Car.js:

    import './Car.css'
    
    <div className="Car">
        ...
    </div>
