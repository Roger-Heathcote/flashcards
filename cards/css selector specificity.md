---
tags: flashcards
---

# CSS Selector specificity flashcards

## Which is more specific "div span" or "div"

div span

## Which is more specific "div span ul " or ".mylist"

.mylist

## Which wins, ".main.part h1" or "#thing"

#thing

## What is the 3 digit selectivity notation for "#main li"

101

## What is the 3 digit selectivity notation for "li [type='mango']"

011

## What is a hack to increase the specificity of a class selector

include it twice e.g. .main.main

## What is a hack to decrease the selectivity of an id

Reference it using attribute syntax e.g. [id="wevs"]

## How can a class or Id be used without adding specificity to the selctor, and what hack does this obsolete

The :where pseudoclass has zero specificity e.g h1:where(.title) = 001

Obsoletes the double :not e.g. div:not(:not(#someId))

## What is the 3 digit selectivity notation for "div::after"

002

## Which is more selective "div:empty" or ".empty"

div:empty

## What is the 3 digit notation for the following: "a:not(.rinky, .dinky, #doo)"

101

## Rank the selector types from least to most specific

1. :where
2. elements & pseudoelements
3. attributes, classes & pseudoclasses(except :not :is & where)
4. ids