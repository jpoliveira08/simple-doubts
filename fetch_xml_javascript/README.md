## How to fetch XML with Fetch API Javascript

```
async function getXMLfromURL(url) {
    try {
        const response = await fetch(url);
        const content = await response.text();
        const data = await parser.parseStringPromise(content);

        return data;
    } catch (error) {
        console.log(error)
    }
}
```js