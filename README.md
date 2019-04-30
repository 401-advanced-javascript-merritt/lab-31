# lab-31

## Code Sandbox Links:
Completed part 1:
[Part 1](https://codesandbox.io/s/91vj7oopr)

Completed part 2:
[Part 2](https://codesandbox.io/s/6wnnp2rxrk)


## Modules:
### Part 1:

#### Components:

 * app.js:
   * render a div that shows the initial state of the 'someStuff' props, passed through by redux.
   * mapStateToProps(state):
     * set the state of the store to someStuff.
   * mapDispatchToProps(dispatch, getState):
     * map the `handlechange` function to this.props

#### Redux files: 

* actions.js:
  * pass along the 'CHANGE' action and the payload to the reducer when the 'changer()' function is called.

* reducers.js:
  * set the initial state to be `{foo: 'bar'}`
  * listen for the 'CHANGE' action, then log the payload and return a random number as `{foo: random}`

### Part 2:

#### Components:

* app.js: 
  * render a div that renders the props app.name passed through from the store by redux.
  * div onClick run changeMyName()
  * changeMyName():
    * run the handlechange function passed through by props with a random word from the set of [foo, bar, baz]
  * mapStateToProps(state):
    * set the props.app to be the same as the store state.app.
  * mapDispatchToProps(dispatch, getState):
    * set the handleChange function to call the nameChanger action.

* numbers.js:
  * render a div that displays the state of numbers passed through by props.
  * on div click handleReset passed through by props.
  * mapStateToProps(state):
    * set this.props.numbers to be state.numbers.
  * mapDispatchToProps(dispatch, getState):
    * map handleReset to the resetNumbers action from numbers-actions.js

#### Redux Files:

* app-actions.js:
  * pass the 'CHANGE' action and payload to the reducers.

* app-reducer.js:
  * Set the initial state to be `{name: 'John}`
  * listen for the 'CHANGE' action, then set name to the payload or a random number and return that value.

* numbers-action.js:
  * pass the 'RESET' action and payload along to the reducers.

* numbers-reducer.js:
  * set the initial state to be `{numbers: 10}`
  * listen for the 'RESET' action then set and return `{numbers: initial state of numbers}`
  * listen for the 'CHANGE' action then set the number to a random value then return that value.

* index.js: declare an object with the reducers then export those.

## UML:

Credit to Billy and Greg for help with these.

![part1](https://i.imgur.com/naB1Wsy.jpg)

![part2](https://i.imgur.com/JTy6Rwl.jpg)
