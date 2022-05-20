```js

import _ from 'lodash'

var users = [
  { firstName: "John", lastName: "Doe", age: 28, gender: "male" },
  { firstName: "Jane", lastName: "Doe", age: 5, gender: "female" },
  { firstName: "Jim", lastName: "Carrey", age: 14, gender: "male" },
  { firstName: "Kate", lastName: "Winslet", age: 40, gender: "female" }
];

var user = _.find(users, { firstName: "John", lastName: "Doe" });
// { firstName: "John", lastName: "Doe", age: 28, gender: "male" }

console.log(user);

var underAgeUser = _.find(users, function (user) {
  return user.age < 18;
});

console.log(underAgeUser);
// { firstName: 'Jane', lastName: 'Doe', age: 5, gender: 'female' } 

```
