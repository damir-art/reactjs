# Динамические классы
Динамически управляем CSS-классами в элементах React.

* Если что-либо вводим в input, то у него появляется border
* Если input, пустой то border красный
* Если символов в input больше 5, то border становится 6 px

В Car.js возврат сделаем как тело функции.<br />
После чего мы можем добавить код до слова `return()`<br />
Создаём массив.

## Car.js

    import React from 'react'
    import './Car.css'

    export default (props) => {
        const inputCssClass = ['Car__input']

        if (props.name !== '') {
            inputCssClass.push('Car__input--green')
        } else {
            inputCssClass.push('Car__input--red')
        }

        if (props.name.length > 5) {
            inputCssClass.push('Car__input--bold')
        }

        return (
            <div className="Car">
                <h2>Car name: {props.name}</h2>
                <p>Year: <b>{props.year}</b></p>
                <p>
                    <input
                        type="text"
                        onChange={props.onChangeName}
                        value={props.name}
                        className = {inputCssClass.join(' ')}
                    /></p>
                {/* <button onClick={props.onChangeTitle}>Click</button> */}
                <button onClick={props.onDelete}>Delete</button>
            </div>
        )
    }

## Car.css

    .Car {
        display: inline-block;
        background-color: #eee;
        margin-bottom: 20px;
        margin-right: 20px;
        padding: 20px;
        padding-top: 0;
        box-shadow: 4px 4px 8px 0 rgba(0, 0, 0, 0.2);
        border-radius: 5px;
    }

    .Car__input {
        border: 3px solid gray;
    }
    .Car__input:active, .Car__input:focus {
        outline: none;
    }
    .Car__input--green {
        border: 3px solid green;
    }
    .Car__input--red {
        border: 3px solid red;
    }
    .Car__input--bold {
        border: 6px solid green;
        font-weight: bold;
    }
