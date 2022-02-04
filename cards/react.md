---
tags: flashcards
---

# React

## What is the basic syntax for a functional component

    export default function ComponentName(props){
        return <p>Content</p>
    }

## How do you inject components into the DOM

    import ReactDOM from 'react-dom'
    ReactDOM.render(component, DOMNode)

## What is the basic syntax for a class component

    import React from 'react'
    class MyComponent extends React.Component {
        constructor(props) {
            super(props)
        },
        render () {
            return <h1>Content</h1>
        }
    }

## What is the basic syntax for a functional component

    export default function ComponentName(props){
        return <p>Content</p>
    }

## What is the syntax for a React functional component without JSX

    import React from 'react'
    function MyElement(){
        return React.createElement(elementName, props, children)
    }

## In a class component when can you omit the constructor

1. If you don't need to initialize state
2. You don't need to bind event handlers to methods

## How do you use local state in a class component

1. Define `this.state = {someVar: 0}` in the constructor
2. Read state from `this.state.someVar`
3. Always update state with setState in a function e.g.

    this.setState((st8)=>{someVar: st8.someVar+1})

## How can you get a reference to a node/element declared within a functional component's render method.

1. Import { useRef } from 'react'
2. const myRef = useRef(null)
3. Set the attribute `ref` on the element you want to that name e.g. <p ref={myRef}>Foo<p>
4. myRef.current is null until the component is mounted, then it is a ref to the DOM node in question

## How can you monitor and respond to changes in DOM nodes/elements

Use the useEffect and useRef hooks together e.g.
    
useEffect(changeHandlerFunction, [myRef.current?.offsetHeight]


