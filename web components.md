---
tags: flashcards
---

# Web components

## How do you create and populate a template element in Javascript

```javascript=
const template = document.createElement('template')
template.innerHTML = `Hello World`
```


## How is a template node cloned

template.content.cloneNode(true)


## Given a template element 'template' - whaty is the basic syntax for a custom component

```javascript=
class MyComponent extends HTMLElement {
  constructor() {
    super()
    this.attachShadow({mode: "open"})
    this.shadowRoot.appendChild(template.content.cloneNode(true))
  }
}
```


## How are custom components bound into the DOM

customElements.define('tag-name', componentName


## How are child elements passed into a custom component and how does the component specify where it goes

Anything between the custom element's tags is passed in to the component. The component uses the <slot> tag to decide where it goes


## Explain named slots

Children can specify a slot attribute e.g.

<p slot="heading">Bananas</p>

If the custom element has a slot element bythat name it is placed there e.g.

<h1><slot name="heading></slot></h1>


## How can slotted content be styled

By using the slotted pseudo element e.g.

```css=
::slotted(span) {
    background: pink;
}
```

## How do you choose if custom element content is addressable by DOM queries once mounted

The mode property of the first argument to .attachShadow() is either "open" or "closed" e.g.

```javascript=
this.attachShadow({mode: "closed"})
```

## What methods can be used for event handler setup and teardown

connectedCallback and disconnectedCallback

## What method is run whenever your component's attributes are changed and what are it's parameters

attributeChangedCallback(attributeName, previousValue, newValue)

