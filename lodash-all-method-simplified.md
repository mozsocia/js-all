```js
import _ from 'lodash'


_.chunk(['a', 'b', 'c', 'd'], 2)
// [ [ 'a', 'b' ], [ 'c', 'd' ] ]


_.compact([0, 1, false, 2, '', 3]);
// => [1, 2, 3]


_.drop([11, 21, 31, 34], 2);
// => [ 31, 34 ]


_.dropRight([11, 21, 31, 34], 2);
// => [ 11, 21 ]


```


### _.dropWile kaj kore false ar upor, jekhane false value pabe tar ager sob value fele dibe

```js
var users = [
  { 'user': 'barney one', 'active': true },
  { 'user': 'barney two', 'active': true },
  { 'user': 'barney three', 'active': true },
  { 'user': 'fred', 'active': false },
  { 'user': 'pebbles', 'active': true },
  { 'user': 'fred 11', 'active': false },
  { 'user': 'pebbles 33', 'active': true },

];

const result = _.dropWhile(users, item => { return item.active; });
/*
[
  { user: 'fred', active: false },
  { user: 'pebbles', active: true },
  { user: 'fred 11', active: false },
  { user: 'pebbles 33', active: true }
]
*/
```
