# key и fragment
## key
Вместо `div` можно использовать прямые скобки `[ ]` (массивоподобный синтаксис), но при этом необходимо в дочерние теги вставить атрибут `key` с уникальным значением.

Используем `div`:

    return (
        <div>
            <h3>Ford {2 + 2}</h3>
            <p>Hello World!</p>
        </div>
    )

Используем `[ ]` и `key`:

    return (
        [
            <h3 key='1'>Ford {2 + 2}</h3>,
            <p key='2'>Hello World!</p>
        ]
    )

# fragment
Используем `React.Fragment`:

    return (
        <React.Fragment>
            <h3>Ford {2 + 2}</h3>
            <p>Hello World!</p>
        </React.Fragment>
    )

Код можно сократить:

    return (
        <>
            <h3>Ford {2 + 2}</h3>
            <p>Hello World!</p>
        </>
    )
