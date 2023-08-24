# duckduckgo-search

Search for words, documents, images, videos, news, maps and text translation using the DuckDuckGo.com search engine. Ported https://github.com/deedy5/duckduckgo_search/ to JS using ChatGPT

Please note that this module cannot be used in a browser because of duckduckgo CORS policy.

## Installation

You can install the `duckduckgo-search` module using npm:

```bash
npm install --save duckduckgo-search
```

## Usage

1. Import the module in your JavaScript file:

```javascript
const duckduckgoSearch = require("duckduckgo-search");
```

2. Perform an image search using the `images` function:

```javascript
(async () => {
  for await (const result of duckDuckGoSearch.images("example keywords")) {
    console.log(result);
  }
})();
```

3. Perform a text search using the `textApi` function:

```javascript
(async () => {
  for await (const result of duckDuckGoSearch.text("example keywords")) {
    console.log(result);
  }
})();
```

Replace `"example keywords"` with the actual keywords you want to search for.

Please note that the `duckduckgo-search` module returns results asynchronously using ES6 async iterators, which is why we are using the `for await...of` loop to iterate over the results.

## Example

Here's a complete example of how you might use the `duckduckgo-search` module in your project:

```javascript
const duckduckgoSearch = require("duckduckgo-search");

(async () => {
  // Image search
  console.log("Image search results:");
  for await (const result of duckDuckGoSearch.images("beautiful landscapes")) {
    console.log(result);
  }

  // Text search
  console.log("Text search results:");
  for await (const result of duckDuckGoSearch.text("web development tips")) {
    console.log(result);
  }
})();
```

## Support

For any issues, questions, or feedback, please create an issue on the [GitHub repository](https://github.com/luukschipperheyn/duckduckgo-search) for this project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
