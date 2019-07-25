[![Build Status](https://travis-ci.org/agirorn/metalsmith-title.svg?branch=master)](https://travis-ci.org/agirorn/metalsmith-title)

# @agirorn/metalsmith-title

> This is a clone of the original [metalsmith-title](https://www.npmjs.com/package/metalsmith-title)

  A Metalsmith plugin that automatically add page title from first heading in
  processed file

  This clone of metalsmith-title adds an option to remove title after detecting
  it and setting it as metadata. Useful when you want to use markdown documents
  verbatim, but have special treatments for titles in your templates, such as
  putting them inside of <header> tags.

## Installation

**Using [npm](https://docs.npmjs.com/cli/install.html)**

```shell
  npm install @agirorn/metalsmith-title
```

**Using [yarn](https://yarnpkg.com)**

```shell
  yarn add @agirorn/metalsmith-title
```


## Usage

  Extract the first tile from all (HTML and Markdown) files.

```js
  const title = require('metalsmith-title');
  metalsmith.use(title());
```

  Use the `title` in
  a [metalsmith-layouts](https://www.npmjs.com/package/metalsmith-layouts)

```handlebars
	<title>{{ title }}</title>
```

  The `title` can be removed from the file after extraction.

```js
  const title = require('metalsmith-title');
  metalsmith.use(title({ remove: true }));
```

## CLI Usage

  Install via npm and then add the `metalsmith-title` key to your
  `metalsmith.json`

```json
  {
    "plugins": {
      "metalsmith-title": true
    }
  }
```

## License

  MIT
