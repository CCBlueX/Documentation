# Documentation
This repository contains the files used to generate the documentation on our homepage. \
Example: https://liquidbounce.net/docs/script-api/getting-started

## Contributing
Fixes and new pages are welcome, just open a pull request.
- All files in this repository are licensed under the [GNU General Public License v3.0 (GPL-3.0)](LICENSE).
- Pages are GitHub Flavored Markdown, rendered on the website. HTML, YouTube iframes and `video` tags work too, but please prefer Markdown.
- Name the language of code blocks for syntax highlighting. Blocks marked `mermaid` are drawn as diagrams.
- All images must be placed inside the `images` folder. Use `/images` to reference it.
- Do not use `#` (h1).
- If you add a new page, remember to also add it to [manifest.json](md/manifest.json). Its URL uses the section and page names from there, lowercased and hyphenated, not the file name. For example, `"Anti-Cheat Test Server": "servers/test-server.md"` in the `Servers` section has the URL `/docs/servers/anti-cheat-test-server`.
- If you move or rename a page, add its old URL path to `$redirects` in the manifest, mapped to the new one, so existing links keep working. For example, `"tutorials/fixing-fps": "troubleshooting/fixing-fps"` redirects `/docs/tutorials/fixing-fps`.
