```js
let batman = () => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      console.log("yes")
      resolve()
    }, 3000);
  });
}


async function b() {
  await batman()

  console.log("ses")
}


b()

```
