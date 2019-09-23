# Работаем со списком
Работаем с тысячами простых компонентов (<Car />) как с одним.

## App.js
Удаляем `const cars = this.state.cars`, удаляем все простые компоненты `<Car />`:

    <Car
        name={cars[0].name}
        year={cars[0].year}
        onChangeTitle={this.HandlerTitleChange.bind(this, cars[0].name)}
    />

Вместо удалённого кода, создаём цикл, который пройдется по State:

    state = {
        cars: [
            {name: 'Ford', year: 2019},
            {name: 'BMW',  year: 2018},
            {name: 'Audi', year: 2016}
        ]
    }

Цикл, вместо множества `<Car />`:

    { this.state.cars.map((car, index) => {
        return (
            <Car
                key = {index}
                name = {car.name}
                year = {car.year}
                // onChangeTitle = {this.HandlerTitleChange.bind(this, car.name)}
                onChangeTitle={() => this.HandlerTitleChange(car.name)}
            />
        )
    }) }

* this.state.cars - массив
* this.state.cars.map() - итерирует каждый элемент массива, возвращает результирующий массив
* this.state.cars.map(function) - функция итератор, обрабатывает каждый элемент массива
* car - каждый из элементов массива
* key - спец атрибут, который должен присутствовать при итерации списков, для оптимизации
* index - используется с key

В отличии от других фреймворков, React использует циклы JavaScript.
