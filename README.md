# Documentation
This repository contains the files used to generate the documentation on our homepage. \
Example: https://liquidbounce.net/docs/ScriptAPI/Getting%20Started

## Contributing
We appreciate anyone who is willing to help us expand the documentation. If you want to contribute, please consider the following points:
- All files in this repository are licensed under the [GNU General Public License v3.0 (GPL-3.0)](LICENSE).
- We use [Parsedown](https://github.com/erusev/parsedown) to convert markdown to HTML. Please keep its limitations in mind.
- Using HTML inside markdown files is possible but please try using markdown whenever possible.
- Syntax highlighting is being made possible by [PrismJS](https://prismjs.com/).
- All images must be placed inside the `images` folder. Use `$images$` to reference it.
- Do not use `#` (h1).
- If you add a new page, remember to also add it to [mainfest.json](md/manifest.json).
