# Создание простого компонента (функции)

Создаём простые компоненты *(функциональные компоненты)* и связываем их друг с другом. Создадим компонент который свяжется с компонентом `App`.

* В папке `src` создаём папку с именем компонента, например `Car`
* В папке `Car` создаём файл с именем `Car.js`
* В файле `Car.js` размещаем функцию простого компонента
* `Car.js` (простые компоненты) ничего не делают, а только отрисовывают элементы

В итоге, мы создали самый простой компонент:

    import React from 'react';

    function Car() {
        return (
            <h2>This is Car component</h2>
        )
    }

    export default Car;

* В файле `App.js` записываем `import Car from './Car/Car';`
* В файле App.js внутри `return` записываем `<Car />` (можно много раз)

## Сокращенная запись
Сокращенные варианты записи простого компонента-функции, в виде стрелочной функции.

Первый вариант:

    const Car = () => {
        return (
            <h2>This is Car component 2</h2>
        )
    }

Воторой вариант:

    const Car = () => <h2>This is Car component 3</h2>

Третий вариант, со множеством элементов:

    const Car = () => (
        <div>
            <h2>This is Car component 4</h2>
            <p>Description</p>
        </div>
    )

Четвертый вариант, сразу экспорт:

    export default () => (
        <div>
            <h2>This is Car component 5</h2>
            <p>Description</p>
        </div>
    )
