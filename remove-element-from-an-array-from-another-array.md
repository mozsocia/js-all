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
