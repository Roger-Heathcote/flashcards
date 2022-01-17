---
tags: flashcards
---

# Media Queries

## What is the syntax for a media query that applies to all media types

```css
@media (feature: value){
    rule: {}
}
```

## What is the syntax for a media query that applies only to screens

```css
@media screen {
    rule: {}
}
```

## How could you remove all `<aside>` elements from the flow for print media less than 18 inches wide

```css
@media print and (min-width: 18in){
    aside { display:none }
}
```

## How could you write a media query for screen which is either portrait or has a width of less than 500px, without repeating any clauses.

Write a nested query...

```css=
@media screen {
    @media (orientation: portrait), (max-width: 500px)
}
```

## How can you conditionally import stylesheets based on media queries

Use @import and put the media query at the end e.g.

```css
@import "somesheet.css" print and (min-width: 8in);
```

## What "media feature" allows us to target horizonal or vertical viewports differently and what settings can it have

orientation, and landscape / portrait 

## For media features that support scalar values how can you do comparisons with them

The `min-` and `max-` prefixes

## What javascript browser function can run and listen for media queries

matchMedia

## How can matchMedia be used to check if a given media query returns true or false

matchMedia("media query string").matches


## How can matchMedia be used to act on mediaQuery changes

matchMedia("media query string").addEventListener('change', handlerFunction)

function handlerFunction(event) {
    console.log(event.handler.matches)
}

## With the media feature `width` does the value include the width of the scrollbar

Yes


