# Wikipedia API docs

For advanced use see [Official Mediawiki API documentation](https://www.mediawiki.org/wiki/API:Main_page)

## Usage

All client requests should contain `&origin=*`.

## Examples

GET first 20 search results (`srlimit`) with page title and info (`prop=info`):

```
https://en.wikipedia.org/w/api.php?action=query&list=search&prop=info&inprop=url&utf8=&format=json&origin=*&srlimit=20&srsearch=belgrade
```

GET first 10 search results (`gsrlimit`) with page title, info and thumbnail image (`prop=extracts|pageimages`):

```
https://en.wikipedia.org/w/api.php?action=query&generator=search&gsrlimit=10&prop=pageimages|extracts&exintro&explaintext&format=json&origin=*&gsrsearch=belgrade
```

Alternative way: GET 10 search results with info and page URL:

```
https://en.wikipedia.org/w/api.php?action=opensearch&format=json&redirects=return&search=belgrade&origin=*
```

