# Analytical queries

Allows for complex queries.

Order of items in tuple are `[subject, predicate, object]`

Those are the required entries, but you can also specify a source (defaults to the current furee db) and options:

`["source", "subject", "predicate", "object", "options"]`

## Aggregate queries

Allow mathematical functions to be performed on query data.

```
{
  "select": "(sum ?favNums)",
  "where": [
    ["?person", "person/favNums", "?favNums"]
    ]
}
```

## Across Blocks

This is where we can use our `source` parameter to specify a specific block to query information from.

`fdb` is the default source
`fdb3` would specify block 3 of the fluree db

## Wikidata

Wikidata is a large, open dataset maintained by the Wikimedia Project.

Analytical queries can access "wikidata".

This is accomplished by citing `$wd` in your source field in the where tuple.

Look at Wikidata's resources to determine how to use more extensively.

This looks really cool, and I can't figure out a way to levarage it in an app!
