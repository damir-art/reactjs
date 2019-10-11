# Оператор расширения `...`
Используем оператор расширения `...` при передаче свойств, компонентам.

Расмотрим пример на JavaScript без **оператора расширения**:

    const cars = ['Ford', 'BMW', 'Audi']

    function carsName(a, b, c) {
        return a + ' ' + b + ' ' + c
    }

    console.log(carsName(cars[0], cars[1], cars[2]))

Пример на JavaScript с **оператором расширения**:

    const cars = ['Ford2', 'BMW2', 'Audi2']

    function carsName(a, b, c) {
        return a + ' ' + b + ' ' + c
    }

    console.log(carsName(...cars))
