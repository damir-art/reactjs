# Стилизация React
Изучаем стилизацию React компонентов (CSS)

* inline стили
* подключение CSS
* динамические классы
* radium
* CSS модули
* препроцессоры (sass/scss)

# inline стили
* style = {JavaScript-объект}
* style = {{color: 'red'}}
* style = {{width: 400}} если указать просто число, то React посчитает их за пиксели

Пример:

    <div style={{
        display: 'inline-block',
        backgroundColor: '#eee',
        marginBottom: '20px',
        marginRight: '20px',
        padding: '20px',
        paddingTop: '0px',
        boxShadow: '4px 4px 8px 0 rgba(0, 0, 0, 0.2)',
        borderRadius: 5
    }}>
