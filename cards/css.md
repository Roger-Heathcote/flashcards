# CSS

## What CSS property specifies which box model to use

    box-sizing


## What are the two possible values for box-sizing

    content-box and border-box

## What symbol denotes a direct descendant

    >  (greater than)

## What symbol is used to join (AND) selectors

    .  (period)

## What symbol is used to join (OR) selectors

    ,  (comma)

## What is the syntax for attribute selectors

    "[attributeName='attributeValue'] // single quotes optional for single word values"

## What is the order for padding shorthand with 4 values

    NESW, starting at top

## What is the order for padding shorthand with 3 values

    top sides bottom

## What is the syntax for defining and using CSS variables

    --variable-name, var(--variable-name)

## Where should you put CSS vars to be globally available

    :root

## What property is used for 2d graphical manipulations

    transform

## What are the four values of transform

    translate, scale, rotate and skew

## What units do rotate and skew use

    deg, turn, rad and grad

## What are the five possible values for position

    static, relative, absolute, fixed, sticky

## Is a higher z-index closer or further away

    closer

## What property can be used to provide a background that fades between colors

    linear-gradient

## What are the arguments to linear-gradient

    angle in deg, start color, end color

## What symbol denotes a descendant

    ' ' (space) (descendant combinator)

## How do you make an attribute selector case insensivite

    add an i before the closing square bracket

## How do you select elements where a given string appears within an attribute value that is a space separated list

    "~= e.g. [attributeName~=""list of values""]"

## What property gives a shadow effect and what are its basic params

    box-shadow: horizontal offset, vertical offset, (blur, spread,) colour

## What are the four core flexbox properties

    display: flex, justify-content, align-items, flex-direction

## What property controls spacing when flex content is wrapped

    align-content

## What property is used to define how images and videos should adjust to their containers

    object-fit

## What property allows the order of flex items to be overridden

    order

## What property allows the alignment of a flex item to be overridden

    align-self

## How do you select elements where a specified substring appears within an attribute value

    [attributeName*='attributeValue']

## Which two properties are used to select elements based on their position amongst their siblings

    :nth-child and :nth-of-type

## How would you select every 3rd element in a list starting with the second

    :nth-child(3n+2)

## How can you make a flexbox item larger or smaller than it's siblings when there is more space available

    flex-grow: >1
    flex-shrink: >1

## How do you set the default length of a flex-box item along the primary axis

    flex-basis: 10em;

## Explain the difference between `display: none` and `visibility: hidden`

    `visibility: hidden` reserves space in the layout, making it better for some animation effects.

## How do you change which cursor appears over your element

    cursor: pointer;
