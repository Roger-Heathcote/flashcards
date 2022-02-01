---
tags: flashcards
---

# Web components

## How do you create and populate a template element in Javascript

```
const template = document.createElement('template')
template.innerHTML = `Hello World`
```

## How is a template node cloned

    template.content.cloneNode(true)

## What class do you extend to create a custom element

    HTMLElement

## Given a template element 'template' - what is the basic syntax for a custom component

```
class MyComponent extends HTMLElement {
  constructor() {
    super()
    this.attachShadow({mode: "open"})
    this.shadowRoot.appendChild(template.content.cloneNode(true))
  }
}
```

`elem.shadowRoot.appendChild(template.content.cloneNode(true))`

## How is the DOM told about web components

    customElements.define('tag-name', componentName)


## How are child elements passed into a custom component and how does the component specify where they go

Anything between the custom element's tags is passed in to the component. The component uses the `<slot>` tag to decide where it goes


## Explain named slots

Children can specify a slot attribute e.g.

    <p slot="heading">Bananas</p>

If the custom element has a slot element by that name it is placed there e.g.

    <h1><slot name="heading></slot></h1>


## How can slotted content be styled

By using the slotted pseudo element e.g.

```
::slotted(span) {
    background: pink;
}
```

## Given a template element 'template' - what is the basic syntax for a custom component

```javascript
class MyComponent extends HTMLElement {
  constructor() {
    super()
    this.attachShadow({mode: "open"})
    this.shadowRoot.appendChild(template.content.cloneNode(true))
  }
}
```

## How do you hide a custom element's contents fron Javascript

Pass { mode: "closed" } to .attachShadow() when creating the shadow root AND use private scope for the variable that references it.

```javascript
class MyElem extends HTMLElemnet{
    #root
    constructor(){
        super()
        #root = this.attachShadow({mode: "closed"})
        #root.innerHTML = "<h1>Contents can't be directly changed from outside now</h1>"
    }
}
```


## What methods can be used for event handler setup and teardown

`connectedCallback()` and `disconnectedCallback()`

## What method is run whenever your component's attributes are changed and what are it's parameters

    attributeChangedCallback(attributeName, previousValue, newValue)

## How can you access a component instance's state or methods

Just grab the node and use dot notation e.g.

```javascript
const elem = document.querySelect("my-element")
console.log(elem.someProperty)
elem.someMethod()
```

## How can you bind attributes to underlying properties / methods

Use getters and setters on the attribute's underlying properties 
In those getters/setters use this.getAttribute and this.setAttribute respectively

## How can you access a custom node's DOM tree

Use normal DOM methods on elem.shadowRoot, if it is open
You can't if it's closed

## How can you detect if a custom element's has gained and/or lost children

Listen for the `'slotchange'` event, either on a particular `<slot>` or as it bubbles up to `.shadowRoot`
