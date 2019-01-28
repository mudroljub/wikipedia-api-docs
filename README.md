# Wikipedia API docs

Important note: all client requests should contain `&origin=*`.

## Examples

Get first 20 search results with info:

```
https://en.wikipedia.org/w/api.php?action=query&list=search&prop=info&inprop=url&utf8=&format=json&origin=*&srlimit=20&srsearch=belgrade
```

Get first 10 search results with info and page URL:

```
https://en.wikipedia.org/w/api.php?action=opensearch&format=json&redirects=return&search=belgrade&origin=*
```

