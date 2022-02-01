---
tags: flashcards
---

# SASS

## What is the file extension for the more modern sass syntax

scss

## How are variables declared in sass

$variable (dollar sign)

## What is the sass equivalent of an object/dict. How are they defined and how are they read

A map.

They are defined with parentheses e.g.

$myMap = (foo: red; bar: green;);

And they are read with map-get e.g.

background: map-get($myMap, foo);

## What are the disadvantages of using sass's nested selectors

Specificity can get out of hand as it increases with each level of nesting.

It also does not promote code re-use, can violate DRY.

## What are scss modules called. How are they defined and consumed

They are called partials

They are regular scss files who's name starts with the underscore character _.

They are imported with the @use keyword at the top of the file, and accessed via dot notation. The file name becomes the namepace.

## How are sass mixins defined and consumed

Defined with the @mixin then your mixin name, parameters optional e.g.

```sass
@mixin myMixin($optionalVariable: defaultValue){
    width: $optionalVarable;
}
```
    
Consumed with @include. Arguments are optional if parameters have defaults e.g.

```sass
.submitButton{
    @include stdPadding;
}
```

## How do sass conditionals work

@if a comparitor b {} @else {}

## What directive is used to slot rules into a sass mixin

@content e.g
```sass
@mixin sky {
    background: light-blue;
    @content
}
```

## What directive is used to pull one set of sass rules into another

@extend e.g.

```sass=
.sea{ background: navy; }
.gull{ color: white; @extend .sea }

```

## What are the constraints on calculations in sass

They are non-dynamic i.e  they are pre-calculated at build time

You can't mix units

## What is the syntax for looping in scss

@each $key, $val in $myMap e.g.

```sass
@each $key, $val in $myMap {
    .color-for-#{$key} {
        color: $val;
    }
}
```

## What is the syntax for interpolation in sass

Hash then curlies e.g #{$variableName}
