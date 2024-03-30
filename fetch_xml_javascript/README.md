## How to fetch XML with Fetch API Javascript

```
const parser = new DOMParser();

async function getXMLfromURL(url) {
    try {
        let sniffDocsFile = await fetch(sniffDocsPath);
        let sniffDocsFileContent = await sniffDocsFile.text();
        let sniffDocsFileParsed = parser.parseFromString(sniffDocsFileContent, 'text/xml');

        return sniffDocsFileParsed;
    } catch (error) {
        console.log(error)
    }
}

let data = getXMLfromURL('alou');
// Now we can work with the XML like a we do with HTML with Javascript
let title = sniffDocsFileParsed.querySelector('documentation').getAttribute('title'),
```