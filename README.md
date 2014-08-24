# Base bem lib

Base library of initially required blocks. This lib deliver blocks `meta`, `metalink` and `page` (with elems `head`, `title` and `body`) for "root" tags and blocks `css`, `js`, `image`, `link` for make it easy write usual elements of page.

## Blocks list

* [page](#page) (with elements: [head](#head), [title](title) and [body](#body))
* [meta](#meta) 
* [metalink](#metalink)
* [css](#css)
* [js](#js)
* [image](#image)
* [link](#link)

## Shortcut attributes

Shortcut attributes is attributes which is not required to be written into block's `attrs` object.

### page

Tag: `html`
Shortcut attributes: `class`
Properties: `doctype` (default: `<!DOCTYPE html>`)

**Usage:**
```js
{
    block: 'page',
    // doctype: 'non html5 doctype'
    content: [
        {
            elem: 'head',
            content: [
                { elem: 'title', content: 'Page title'}
            ]
        },
        {
            elem: 'body',
            content: []
        }
    ]
}
```

#### head

Tag: `head`

**Usage:**
```js
{
    elem: 'head',
    content: [/*…*/]
}
```

#### title

Tag: `title`

**Usage:**
```js
{ elem: 'title', content: 'Page title'},
```

#### body

Tag: `body`
Shortcut attributes: `class`

**Usage:**
```js
{
    elem: 'body',
    content: [/*…*/]
}
```
