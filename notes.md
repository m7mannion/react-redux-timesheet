#Workshop Notes

##Setup

[Workshop Site](https://react-training.objectpartners.com/)

* Github `create-react-app`
* Webpack
* hapijs.com
* Facebook.github.io/jest testing framework
    * BDD-style
* Axios/moxios http client for browser and node.js
    * Mocks and stubs
* `yarn` is similar to `npm install` to pull module dependencies
* `yarn start` is like `npm start`
* Key piece is JSX
  * Don't write it where you write specifics, allow babel to transpile from JSX
  * Uppercase vs. lowercase convention. UpperCase = Component, lowercase = HTML tag
  * `htmlFor` instead of `for`
  * `className` instead of `class`
* Replica of the Browser DOM. Efficiently diffs and updates. See link on slide
* React Components are the key structure - independent reusable pieces
* `Functional Component` is just a function
* `Class Component` ES6 class that extends React.Component
* Has state, must implement the `render()` method
* `render()` does not mutate component state. Should return the same result each tim it is invoked and should not read from or write to the DOM
* `contructor()` invoked at object creation. Use state to change aspects
* Component lIfecyle: mounting, updating, unmounting
* props: contains the props that were defined by the caller of the component. `props.children`
* `PropTypes` Validate props being passed to your component. Shows up in the console but not in production mode.
```javascript
import PropTypes from ‘prop-types’;
...
Foo.propTypes: {
  max:        PropTypes.number.isRequired,
  maxVisible: PropTypes.number,
  onChange:   PropTypes.func.isRequired
};
```
* `state` contains data specific to the component that may change over time. Should use setState() to mutate, never done directly
*  `JSX Expression Bindings` - in curly braces
* React16 introduced fragments
* Enzyme for testing

###Dom Query methods
* `find()` - find all nodes that match the selector

###React and Local State
* `state` anything changeable. Used for behavior
* Best practice to use arrow function so you don't have to bind in the constructor.
* Use setState(), don't update directly. See examples

> Good
```javascript
this.setState({
  name: 'Tim'
});
```
> Bad
```javascript
this.state.name = 'Tim';
```

* Asynchronous state updates...see slides 4.8
 

###Routing
* Github react-router
* Community created and controlled. Defacto mechanism
* `BrowserRouter`: uses HTML5 history API
* `Route` - core path routing component
* `path` - pattern used to match this route against url
* `component` The React component to be rendered
* `exact & strict` See slides
* `Redirect` Navigates to a new location. Good for transitioning
* `Switch` Renders the first chile Route/Redirect that matches. Renders only the first one
* `Link` Declarative navigation. Renders an `a` tag. Specialized version `navLink`.
* `Route Props` match, location, history
  * `match`
  * `location` Represents where the app is, was or will be
  * `history`
* 
