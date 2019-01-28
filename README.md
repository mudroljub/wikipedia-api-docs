# Wikipedia API docs

Wikipedia API examples. For advanced use see [Official Mediawiki API documentation](https://www.mediawiki.org/wiki/API:Main_page)

Important: All client requests should contain `&origin=*`. 

## Search articles

GET first 10 search results with page title, extract and thumbnail image (`prop=extracts|pageimages`). Article extract is HTML by default:

```
https://en.wikipedia.org/w/api.php?action=query&generator=search&gsrsearch=belgrade&exintro=&prop=extracts|pageimages&format=json&origin=*
```

GET first 20 search results (`srlimit`) with page title and info (`prop=info`):

```
https://en.wikipedia.org/w/api.php?action=query&list=search&prop=info&inprop=url&utf8=&format=json&origin=*&srlimit=20&srsearch=belgrade
```

GET first 20 search results (`gsrlimit`) with page title, extract and thumbnail image (`prop=extracts|pageimages`). Article extract is set to plain text (`explaintext`):

```
https://en.wikipedia.org/w/api.php?action=query&generator=search&gsrlimit=20&prop=pageimages|extracts&exintro&explaintext&exlimit=max&format=json&origin=*&gsrsearch=belgrade
```

GET 10 search results with info and page URL:

```
https://en.wikipedia.org/w/api.php?action=opensearch&format=json&redirects=return&search=belgrade&origin=*
```

## Get an article

GET full Wikipedia article for the requested title (`titles=belgrade`), with images and URL (`inprop=url`). Also, follows redirection (`redirects`) if necessary:

```
https://en.wikipedia.org/w/api.php?action=query&titles=belgrade&prop=extracts|pageimages|info&pithumbsize=400&inprop=url&redirects=&format=json
```
