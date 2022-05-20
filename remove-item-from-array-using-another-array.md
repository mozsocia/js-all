```js 
let posts = [
  {
    "id": 1,
    "title": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit",
   },
  {
    "id": 2,
    "title": "qui est esse"
  },
  {
    "id": 3,
    "title": "ea molestias quasi exercitationem repellat qui ipsa sit aut"
  }
 ]

let another = [5, 6, 7, 3]


let result = posts.filter(item => !another.includes(item.id))

console.log(result);


/* result 

[
  {
    id: 2,
    title: 'qui est esse'   
  }
]
*/




let balanceCodes = [
  { ID: 1, StringValue: "dummy" },
  { ID: 2, StringValue: "data" }
];
let allCodes = [
  { ID: 1, StringValue: "dummy", Color: "red", Order: "low" },
  { ID: 2, StringValue: "data", Color: "green", Order: "medium" },
  { ID: 3, StringValue: "extra", Color: "black", Order: "low" },
  { ID: 4, StringValue: "options", Color: "grey", Order: "high" }
];

var result = _.differenceBy(allCodes, balanceCodes, 'ID');

console.log(result);
/*
[
  { ID: 3, StringValue: 'extra', Color: 'black', Order: 'low' },       
  { ID: 4, StringValue: 'options', Color: 'grey', Order: 'high' }      
]*/
```
