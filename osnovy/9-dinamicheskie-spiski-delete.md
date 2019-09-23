# Динамические списки (удаление)
* Создадим кнопку, по которой будем удалять авто из списка

## Car.js
    import React from 'react';

    export default (props) => (
        <div style={{
            display: 'inline-block',
            backgroundColor: '#eee',
            marginBottom: '20px',
            marginRight: '20px',
            padding: '20px',
            paddingTop: '0px'
        }}>
            <h2>Car name: {props.name}</h2>
            <p>Year: <b>{props.year}</b></p>
            <p><input type="text" onChange={props.onChangeName} value={props.name} /></p>
            {/* <button onClick={props.onChangeTitle}>Click</button> */}
            <button onClick={props.onDelete}>Delete</button>
        </div>
    )

## App.js
    import React, {Component} from 'react';
    import './App.css';
    import Car from './Car/Car';

    class App extends Component {
        state = {
            cars: [
                {name: 'Ford', year: 2019},
                {name: 'BMW',  year: 2018},
                {name: 'Audi', year: 2016},
                {name: 'Mazda', year: 2012}
            ],
            pageTitle: 'Заголовок страницы',
            showCars: false
        }

        HandlerTitleChange = (newTitle) => {
            this.setState({
                pageTitle: newTitle
            })
        }

        onChangeName(name, index) {
            // console.log(name, index)
            const car = this.state.cars[index]
            // console.log(car)
            car.name = name
            const cars = [...this.state.cars]
            cars[index] = car
            this.setState({
                // cars: cars
                cars
            })
        }

        HandlerCarsShow = () => {
            this.setState({
                showCars: !this.state.showCars
            })
            console.log(this.state.showCars)
        }

        deleteHandler(index) {
            // console.log(this, index)
            const cars = this.state.cars.concat()
            cars.splice(index, 1)
            this.setState({
                // cars: cars
                cars
            })
        }

        render() {

            const divStyle = {
                textAlign: 'center'
            }

            let cars = null

            if (this.state.showCars) {
                cars = this.state.cars.map((car, index) => {
                    return (
                        <Car
                            key = {index}
                            name = {car.name}
                            year = {car.year}
                            // onChangeTitle = {this.HandlerTitleChange.bind(this, car.name)}
                            // onChangeTitle={() => this.HandlerTitleChange(car.name)}
                            onDelete={this.deleteHandler.bind(this, index)}
                            onChangeName={event => this.onChangeName(event.target.value, index)}
                        />
                    )
                })
            }

            return (
                <div style={divStyle}>
                    <h1>{this.state.pageTitle}</h1>

                    <button 
                        onClick={this.HandlerTitleChange.bind(this, 'Hello')}
                    >Изменяем заголовок</button><br /><br />

                    <button 
                        onClick={this.HandlerCarsShow}
                    >Показать / скрыть авто</button><br /><br />

                    {
                        // this.state.showCars ?
                        //     this.state.cars.map((car, index) => {
                        //         return (
                        //             <Car
                        //                 key = {index}
                        //                 name = {car.name}
                        //                 year = {car.year}
                        //                 // onChangeTitle = {this.HandlerTitleChange.bind(this, car.name)}
                        //                 onChangeTitle={() => this.HandlerTitleChange(car.name)}
                        //             />
                        //         )
                        //     })
                        // : null

                        cars
                    }

                </div>
            );
        }
    }

    export default App;
