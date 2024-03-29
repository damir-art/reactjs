# Условные операторы в React
По нажаьтию по кнопке, скрываем/показываем список автомобилей.<br />
Изучаем работу с условиями в React.
Внутри JSX можно использовать только тернарный оператор.<br />
Выводим элементы по условию.<br />
Если значение `showCars:` равно `false`, то список машин не выводить.<br />
Есть два способа показывать/скрывать список авто.

## App.js
Функция обработчик события

    HandlerCarsShow = () => {
        this.setState({
            showCars: !this.state.showCars
        })
        console.log(this.state.showCars)
    }
    
Кнопка вызова события:

    <button onClick={this.HandlerCarsShow}>Показать/скрыть авто</button>

### Первый способ
Показать список авто с условием, тернарный оператор:

    {
        this.state.showCars ?
            this.state.cars.map((car, index) => {
                return (
                    <Car
                        key = {index}
                        name = {car.name}
                        year = {car.year}
                        // onChangeTitle = {this.HandlerTitleChange.bind(this, car.name)}
                        onChangeTitle={() => this.HandlerTitleChange(car.name)}
                    />
                )
            })
        : null
    }

### Второй способ
* Создаем переменную и условие if внутри `render()` над `return()`
* В `return()` вместо тернарного оператора засовываем `cars`

Показать список авто с условием, if:

    let cars = null

    if (this.state.showCars) {
        cars = this.state.cars.map((car, index) => {
            return (
                <Car
                    key = {index}
                    name = {car.name}
                    year = {car.year}
                    // onChangeTitle = {this.HandlerTitleChange.bind(this, car.name)}
                    onChangeTitle={() => this.HandlerTitleChange(car.name)}
                />
            )
        })
    }
    
    return (
        ...
        { cars }
        ...
    )

Фигурные скобки внутри React, указывают на то, что мы пишем на JavaScript.
Обычные скобки внутри React, после return указывают на то, что мы пишем на JSX.
