[Merge lines and sum counters](http://stackoverflow.com/questions/16350948/combine-results-of-column-one-then-sum-column-2-to-list-total-for-each-entry-in/16351003#16351003)

```
awk '{a[$1]+=$2}END{for(name in a)print name " " a[name]}'
```
