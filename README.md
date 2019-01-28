# Wikipedia API docs

See also: [official documentation](https://www.mediawiki.org/wiki/API:Main_page)

## Usage

All client requests should contain `&origin=*`.

## Examples

Get first 20 search results with info and page title:

```
https://en.wikipedia.org/w/api.php?action=query&list=search&prop=info&inprop=url&utf8=&format=json&origin=*&srlimit=20&srsearch=belgrade
```

Get first 10 search results with info, page URL and thumbnail image:

```
https://en.wikipedia.org/w/api.php?format=json&origin=*&action=query&generator=search&gsrlimit=10&prop=pageimages|extracts&exintro&explaintext&exlimit=max&gsrsearch=belgrade
```

ALTERNATIVE:

Get 10 search results with info and page URL:

```
https://en.wikipedia.org/w/api.php?action=opensearch&format=json&redirects=return&search=belgrade&origin=*
```

