```js

import _ from 'lodash'


var users = [
  { 'user': 'barney one', 'active': true, id: 1 },
  { 'user': 'aarney two', 'active': true, id: 7 },
  { 'user': 'fred', 'active': false, id: 6 },
  { 'user': 'pebbles', 'active': true, id: 2 },
  { 'user': 'fred 11', 'active': false, id: 4 },
];




_.sortBy(users, item => { return item.id });
/*[
  { user: 'barney one', active: true, id: 1 },
  { user: 'pebbles', active: true, id: 2 },
  { user: 'fred 11', active: false, id: 4 },
  { user: 'fred', active: false, id: 6 },
  { user: 'aarney two', active: true, id: 7 }
]*/
_.sortBy(users, ['id']);
/*[
  { user: 'barney one', active: true, id: 1 },
  { user: 'pebbles', active: true, id: 2 },
  { user: 'fred 11', active: false, id: 4 },
  { user: 'fred', active: false, id: 6 },
  { user: 'aarney two', active: true, id: 7 }
]*/



var object = [
  { 'obj': 'moto', 'price': 10 },
  { 'obj': 'oppo', 'price': 6 },
  { 'obj': 'moto', 'price': 2 },
  { 'obj': 'oppo', 'price': 8 },
  { 'obj': 'moto', 'price': 3 },

];

_.sortBy(object, ['obj']);
/*
[
  { obj: 'moto', price: 10 },
  { obj: 'moto', price: 2 },
  { obj: 'moto', price: 3 },
  { obj: 'oppo', price: 6 },
  { obj: 'oppo', price: 8 }
]*/

_.sortBy(object, ['obj', 'price']);
/*
[
  { obj: 'moto', price: 2 },
  { obj: 'moto', price: 3 },
  { obj: 'moto', price: 10 },
  { obj: 'oppo', price: 6 },
  { obj: 'oppo', price: 8 }
]*/

let gfg = _.orderBy(object, ['obj', 'price'], ['desc', 'desc']);
console.log(gfg);

/*
[
  { obj: 'oppo', price: 8 },
  { obj: 'oppo', price: 6 },
  { obj: 'moto', price: 10 },
  { obj: 'moto', price: 3 },
  { obj: 'moto', price: 2 }
]*/


var users2 = [
  { 'user': 'darney one', 'profile': { 'active': true, id: 1 } },
  { 'user': 'aarney two', 'profile': { 'active': false, id: 5 } },
  { 'user': 'barney three', 'profile': { 'active': true, id: 3 } },

];

_.sortBy(users2, ['profile.id']);
/*
[
  { user: 'darney one', profile: { active: true, id: 1 } },
  { user: 'barney three', profile: { active: true, id: 3 } },
  { user: 'aarney two', profile: { active: false, id: 5 } }
]*/

```
