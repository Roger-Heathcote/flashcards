---
tags: flashcards
---

# HTML Flashcards

## What should the first line of a HTML5 webpage be


    <!DOCTYPE html>


## How many H1 elements should you have in a page

One per page OR, if you have sections, One per `<section>`

## What element should you use to wrap the primary content of your page

    <main>

## What element can be used to wrap blocks of content which make sense on their own i.e. are self contained

    <article>

## What element can be used for the thematic/semantic grouping of content

    <section>

## What element should be used to wrap blocks of navigation links and what is best practice if there are more than one such block

    <nav>

If there are several nav areas you should add an `aria-label` for each e.g. main, breadcrumbs, footer etc

## What is the syntax for the audio element

```
    <audio controls loop>
        <source src="" type="audio/mpeg">
        <source src="" type="audio/ogg">    
        Fallback text/link
    </audio>
```

## What elements are used to wrap and label visual information

```
    <figure>
    <figcaption>
```

## In a form, what attribute sets the POST URL

`action`  e.g. `<form action="https://example.com">`

## How do you make an input field mandatory

Use the required attribute e.g.

    <input name="name" type="text" required>


## How do you add example text or instructions to an input

Use the placeholder attribute e.g.

    <input name="name" placeholder="Your name...">


## In a select option, what attribute sets the text that is sent, and what attribute sets the default option

`value` and `select` e.g. 

    <option value="pie" selected>A Pie</option>

## How are labels used

The label's `for` attribute specifies the id of the element to label e.g.

```
    <label for="flungePipeQuanity">Number of Flunge Pipes Required:</label>
    <input type="text" id="flungePipeQuantity" name="name">
```

## What elements are used to group and label related fields

```
    <fieldset>
    <legend>

e.g.

    <fieldset>
        <legend>
            These are related fields
        </legend>
        <input name="pies">
        <button type="submit">Go</button>
    </fieldset>
```

## How can you do basic validation in vanilla HTML forms

Use the pattern attribute to specify a regex. Form will not submit unless regex matches.

e.g. `<input name="pies" pattern="0-9+" required>`

Note that required might silently fail if any preceding attributes are bad so put it at the front, just in case.

## How can you trigger different onscreen keyboards (including numeric and none) per input field

The inputmode attribute e.g.

    <input name="pies" pattern="0-9+" inputmode="numeric">

## What is the syntax for setting a viewport and what happens if you omit it

    <meta name="viewport" content="width=device-width, initial-scale=1>

If you do not define a viewport The browser assumes a default viewport width of 980px and will scale your content up or down to fit, either requiring vertical scroll or pinch zoom.
       
## How can you indicate an element should, or should not be, spellchecked

Use the spellcheck attribute.

    <textarea name="x509-public-key" spellcheck="false"></textarea>


## What tag can you use to display raw text, including spacing

`<pre>`