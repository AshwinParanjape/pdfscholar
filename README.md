# pdfscholar
A lightweight crossplatform pdf organization tool

## Minimum feature requirements
* Store PDF files locally, no dependency on hosted servers
* Completely accessible from the browser
 * Save pdf files with a single click from any browser
 * Open organization interface from the browser itself
 * Open pdf within the browser
* Assign tags to pdfs and list with them

## Future features
* Be able to assign multiple tags to each pdf
* Be able to search/list via tags
* Notes for a pdf
* Annotate parts of pdf
* Search text, notes, annotations

## Roadmap - Stage 1 (Node.js server Process)
* Use [electron](http://electron.atom.io/) because it is cross platform and works with native file system
* The background process using [Chokidar](https://github.com/paulmillr/chokidar) monitors `Downloads` folder (configurable) for any new downloaded pdfs
* pdfs are transferred to a `Publications` folder (configurable) where pdfs are saved (the user can delete files in `Downloads`) 
* New pdf download triggers transfer to `Publications` folder and opens a new tab showing the pdf in browser (configurable) 
* The electron app starts a server in background (Stage 2)
* Configurations can only be done through the app, as they can be a security issue if exposed. 

## Roadmap - Stage 2 (Node.js server Process)
* A separate node.js server runs in background serving organization interface and pdfs being served on localhost
* Optionally organization interface and pdfs are available via the electron app directly
* The node.js server can be also used to self-host the service independent of electron app

## Roadmap - Stage 3 (Reader Interface)
* Open pdf using pdf.js
 * [GitHub repo] (https://github.com/mozilla/pdf.js)
 * [api.js] (https://github.com/mozilla/pdf.js/blob/master/src/display/api.js)
 * [Patchy API documentation] (https://mozilla.github.io/pdf.js/api/draft/index.html)
* Add tag to pdf

## Roadmap - Stage 4 (Organization Interface)
* List all pdf files
* List all tags for pdf files
* List all pdfs for a tag (or a combination of tags)

To use
```
npm install
npm start
```

## Links
### Annotation
* https://github.com/instructure/pdf-annotate.js/
* https://www.npmjs.com/package/pdf-annotate
