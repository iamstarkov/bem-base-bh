# Base bem lib

Base library of initially required blocks. This lib deliver blocks `meta`, `metalink` and `page` (with elems `head`, `title` and `body`) for "root" tags and blocks `css`, `js`, `image`, `link` for make it easy write usual elements of page.

## Blocks list

* [page](#page) (with elements: [head](#head), [title](#title) and [body](#body))
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


### meta

Tag: `meta`

Usual meta tags.

**Usage:**
```js
{ block: 'meta', attrs: { charset: 'utf-8' }}
```

### metalink

Tag: `link`

Use for favicons and microformates.

**Usage:**
```js
{ block: 'metalink', url: '/favicon.ico', attrs: { rel: 'icon', type: 'image/x-icon' }}
```

### css

Include CSS stylesheet. Prop `url` transforming to `href`.

Tag: `link`

**Usage:**
```js
{ block: 'css', url: 'index.css' }
```

### js

Tag: `script`

Include JS script. Prop `url` transforming to `src`.

**Usage:**
```js
{ block: 'js', url: 'index.js' }
```

### image

Tag: `img`

Usual image. Prop `url` transforming to `src`.

**Usage:**
```js
{ block: 'image', url: 'image.jpg' }
```

### link

Tag: `a`

Usual link (anchor). Prop `url` transforming to `href`.

**Usage:**
```js
{ block: 'link', url: 'https://google.com', content: 'Google' }
```
