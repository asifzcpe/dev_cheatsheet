# Search as sql 'LIKE' statement into json using underscore.js

```JAVASCRIPT
  function searchLike(keyToFilter, searchableItem){
    return _.filter(results, function(d){ return d[keyToFilter].startsWith(searchableItem); })
  }

  searchLike("name", "ra");
```
## Results:

```JSON
  [{
    "id": "203",
    "name": "rana khan"
  },
  {
    "id": "205",
    "name": "ranbir kapoor"
  }]
```
<p style='color:red'>This is some red text.</p>
