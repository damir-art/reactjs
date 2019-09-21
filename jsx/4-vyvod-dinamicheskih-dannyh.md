# Вывод динамических данных

Пишем на JavaScript внутри JSX. Для этого используют фигурные скобки.

    export default () => (
        <div>
            <h2>This is Car component</h2>
            <p>5 + 7</p>
            <p>{5 + 7}</p>
            <p><b>Random:</b> {Math.random()}</p>
            <p>Random <em>(round 1000)</em>: {Math.round(Math.random() * 1000)}</p>
        </div>
    )
    
Внутри фигурных скобок, нельзя использовать сложные конструкции, например определение класса.
