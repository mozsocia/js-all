Give me vanilla js code for showing image in img tag which is selected in input tag (file type)

Sure, here's a vanilla JavaScript code snippet that will show the selected image in an `img` tag when a user selects an image using an `input` tag with `type="file"`:

HTML:

```html
<input type="file" id="fileInput">
<img id="selectedImage">

```

JavaScript:

```js
const fileInput = document.getElementById('fileInput');
const selectedImage = document.getElementById('selectedImage');

fileInput.addEventListener('change', (event) => {
  const file = event.target.files[0];
  const reader = new FileReader();

  reader.addEventListener('load', (event) => {
    selectedImage.src = event.target.result;
  });

  reader.readAsDataURL(file);
});

```

In this code, we first get a reference to the `input` element with `type="file"` and the `img` element where we want to display the selected image.

Next, we add an event listener to the `input` element for the `'change'` event. This event will be triggered when the user selects a file.

Inside the event listener, we first get a reference to the selected file from the event target's `files` array. We then create a new `FileReader` object and add an event listener to it for the `'load'` event. This event will be triggered when the FileReader has finished reading the file.

Inside the `'load'` event listener, we set the `src` attribute of the `img` element to the `result` property of the FileReader's event target. This property contains the data URL of the selected image, which we can use to display the image in the `img` element.

Finally, we call the `readAsDataURL` method of the FileReader object and pass it the selected file. This will start the process of reading the file and triggering the `'load'` event when it's done.


use jquery

Certainly! Here's the same functionality implemented using jQuery:

HTML:

```html
<input type="file" id="fileInput">
<img id="selectedImage">

```

jQuery:

```js
$(document).ready(function() {
  $('#fileInput').on('change', function(event) {
    const file = event.target.files[0];
    const reader = new FileReader();

    reader.addEventListener('load', function(event) {
      $('#selectedImage').attr('src', event.target.result);
    });

    reader.readAsDataURL(file);
  });
});

```

In this code, we first wait for the document to be ready using the `$(document).ready()` function. Then we attach an event listener to the `input` element with `type="file"` using the `on()` method.

Inside the event listener, we get a reference to the selected file from the event target's `files` array, create a new `FileReader` object, and add an event listener to it for the `'load'` event.

Inside the `'load'` event listener, we use the `attr()` method to set the `src` attribute of the `img` element to the `result` property of the FileReader's event target.

Finally, we call the `readAsDataURL` method of the FileReader object and pass it the selected file. This will start the process of reading the file and triggering the `'load'` event when it's done.
