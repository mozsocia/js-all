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


var underAgeUser = _.find(users, function (user) {
  return user.age < 18;
});


// { firstName: 'Jane', lastName: 'Doe', age: 5, gender: 'female' } 


var posts = [
  { id: "1abc", title: "First blog post", content: "..." },
  { id: "2abc", title: "Second blog post", content: "..." },
  // more blog posts
  { id: "34abc", title: "The blog post we want", content: "..." }
  // even more blog posts
];

posts = _.keyBy(posts, "id");
/*{
  '1abc': { id: '1abc', title: 'First blog post', content: '...' },    
  '2abc': { id: '2abc', title: 'Second blog post', content: '...' },   
  '34abc': { id: '34abc', title: 'The blog post we want', content: '...' }
}*/


var data = [{
  "name": "jim",
  "type": "admin",
  "age": "22"
}, {
  "name": "Sam",
  "type": "user",
  "age": "33"
}, {
  "name": "eddie",
  "type": "user",
  "age": "77"
}];

console.log(_.groupBy(data, 'type'));

/*
{
  admin: [ { name: 'jim', type: 'admin', age: '22' } ],
  user: [
    { name: 'Sam', type: 'user', age: '33' },
    { name: 'eddie', type: 'user', age: '77' }
  ]
}
*/


```
