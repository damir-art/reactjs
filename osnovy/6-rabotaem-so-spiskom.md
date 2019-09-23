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

    {this.state.cars}

* this.state.cars - массив
* this.state.cars.map() - итерирует каждый элемент массива, возвращает результирующий массив
* this.state.cars.map(function) - функция итератор, обрабатывает каждый элемент массива

В отличии от других фреймворков, React использует циклы JavaScript.
