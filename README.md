# convert-markdown-to-pdf

[![node version](https://img.shields.io/node/v/convert-markdown-to-pdf.svg)](https://www.npmjs.com/package/convert-markdown-to-pdf)
[![npm version](https://badge.fury.io/js/convert-markdown-to-pdf.svg)](https://badge.fury.io/js/convert-markdown-to-pdf)
[![downloads count](https://img.shields.io/npm/dt/convert-markdown-to-pdf.svg)](https://www.npmjs.com/package/convert-markdown-to-pdf)

:hammer: Convert Markdown file to PDF.

> Give a ⭐️ if this project helped you!

## Features

* :white_check_mark: Build PDF file form Markdown file
* :white_check_mark: Generate a PDF file in the same directory as the Markdown file
* :white_check_mark: Use one of the built-in themes
* :white_check_mark: Support custom path to a theme file
* :white_check_mark: Support set output directory and output file name

## Usage

```js
const { buildPDF } = require('convert-markdown-to-pdf');
buildPDF({
  source: '/tmp/source.md',
  target: '/tmp/document.pdf'
});
```

## CLI

### Installation

```bash
npm install -g convert-markdown-to-pdf
```

### :arrow_right: Use case: Regular usage

```bash
convert-markdown-to-pdf /tmp/source.md
```

### :arrow_right: Use case: Display list of built-in themes

```bash
convert-markdown-to-pdf -l
```

### :arrow_right: Use case: Change theme (built-in)

```bash
convert-markdown-to-pdf /tmp/source.md -t clean
convert-markdown-to-pdf /tmp/source.md -t dark
convert-markdown-to-pdf /tmp/source.md -t default
convert-markdown-to-pdf /tmp/source.md -t nord
convert-markdown-to-pdf /tmp/source.md -t orange
```

### :arrow_right: Use case: Custom theme

```bash
convert-markdown-to-pdf /tmp/source.md -p ~/custom-theme.css
convert-markdown-to-pdf /tmp/source.md --theme-path ~/custom-theme.css
```

### :arrow_right: Use case: Set directory for output file

```bash
convert-markdown-to-pdf /tmp/source.md -d my-files/
convert-markdown-to-pdf /tmp/source.md --directory my-files/
```

### :arrow_right: Use case: Set name of output file

```bash
convert-markdown-to-pdf /tmp/source.md -f agreement.pdf
convert-markdown-to-pdf /tmp/source.md --filename agreement.pdf
```

### :arrow_right: Use case: Display the date of generation in the output file

During the conversion, the following phrase will be replaced with date & time.
For example:

```md
Generated on: $$SIGNATURE$$
```

It will be replaced with:

```md
Generated on: 2023-09-08 23:16:35
```

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />
Feel free to check [issues page](/issues/).

## Versioning

```bash
npm run lint
npm run test
npm run coverage
npm run clear
# npm version major / minor / patch
npm publish
git push --tags
```

## License

[The MIT License](http://piecioshka.mit-license.org) @ 2018-2024
