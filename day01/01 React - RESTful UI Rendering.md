React: RESTful UI Rendering
===========================

Pete Hunt
@floydophone
[Facebook Github](http://facebook.github.ui/react)

User by Facebook for all their project moving forward.

## Evolution of Distributed Systems

### Message Passing.
 - Problem with message passing is too low level. Difficult to model the state. Almost like assembler for dist system. 
 - e.g.: CORBA, RMI, SOAP, DCOM, etc
 - Multi step multi directional distributed system is slow and unpredictible.

### REST

## Evolution of UI Developmnent
### MVC
 - Similar to dist system in term of some data model can have dependency with multiple model.
 - System based on observation are unpredictible.
 - Multistep, multidirectional callbacks is slow and unreliable - similar to dist object problem.

## React
 - No DOM manipulation.
 - We tell react what to render, not how to render.
 - Cacheable - shouldComponentUpdate options.
 - Renderable component (see TodoList from the code)

### Implementation
(see image)

 - Browser can be swapped with SVG, Canvas, etc.
 - React is RESTful
 - Web components are not RESTful

## QA
 - React has built in support for canvas and SVG.
 - React handles the DOM manipulation for you. Doesn't handle DOM manipulation by other library.
 - The next frontier for web development: flexbox is ok. autolayout on ios?
 - web component is not restful. DOM is stateful. Web component is building more functionality into stateful DOM.
 - Immutable JS in react.
