---
tags: flashcards
---

# CSS Grid Flashcards

## What are the three basic properties used to define a grid

- display: grid
- grid-template: rows / columns
- grid-gap

## What properties dictate which grid cells an item occupies

- grid-column-start
- grid-column-end
- grid-column
- grid-row-start
- grid-row-end
- grid-row
- grid-area

## How can we specify the last horizontal or vertical line in a grid

-1

## How can you specify a range of cells by width (number of columns) starting at a certain line

- grid-column-start: start-line
- grid-column-end: span #cols

or

- grid-column: start-line / span #cols

## How can you specify a range of cells by width (number of columns) ending at a certain line

- grid-column-start: span #cols
- grid-column-end: end-line

or

- grid-column: span #cols / end-line

## How can you specify a 2D grid range on one line and what order are the parameters

grid-area: row-start, col-start, row-end, col-end

## What properties control the space between grid items

- column-gap
- row-gap
- gap

## How can you bump an item to the front of a grid

order: -1

## How can you avoid repetetive declarations when defining a grid

grid-template-columns: repeat(repetitions, value)
