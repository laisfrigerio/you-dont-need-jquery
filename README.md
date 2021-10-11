# 🚫 You don't need Jquery

Replace jQuery methods with Vanilla Javascript

<p align="center">
  <a><img src="./images/cover-image-you-dont-need-jquery.png" alt="Capa do repositório escrito: You don't need jQuery" title="Capa do repositório escrito: You don't need jQuery"></a>
</p>

## 📝 Table of Content

1. [Select something](#1-select-something)
2. [Select something within a parent](#2-select-something-within-a-parent)
3. [Add class](#3-add-class)
4. [Remove class](#4-remove-class)
5. [Toggle class](#5-toggle-class)
6. [Get attribute](#6-get-attribute)
7. [Set attribute](#7-set-attribute)
8. [Get data attribute](#8-get-data-attribute)
9. [Set data attribute](#9-set-data-attribute)
10. [Get Text](#10-get-text)
11. [Get HTML](#11-get-html)
12. [Insert HTML string](#12-insert-html-string)
13. [Insert text string](#13-insert-text-string)
14. [Show element](#14-show-element)
15. [Hide element](#15-hide-element)
16. [Show element with transition](#16-show-element-with-transition)
17. [Hide element with transition](#17-hide-element-with-transition)
18. [Loop through Array](#18-loop-through-array)
19. [Loop through Object](#19-loop-through-object)
20. [Add Event Listener](#20-add-event-listener)
21. [Ajax request](#21-ajax-request)

## How to replace jQuery with Vanilla Javascript

### 1. Select something

Selecting element by class name. You can also use to select by tag or identifier:

```js
  // jQuery
  $('.class-name');

  // ES6
  document.querySelector('.class-name'); // single
  document.querySelectorAll('.class-name'); // multiple
```

### 2. Select something within a parent

This example is similar to the one above: with an additional selection throught a parent element:

```js
  // jQuery
  parent.find('.class-name');

  // ES6
  parent.querySelector('.class-name'); // single
  parent.querySelectorAll('.class-name'); // multiple
```

### 3. Add class

Adding a class into an element:

```js
  // jQuery
  element.addClass('.class-name');

  // ES6
  element.classList.add('.class-name');
```

### 4. Remove class

Removing a class from an element:

```js
  // jQuery
  element.removeClass('.class-name');

  // ES6
  element.classList.remove('.class-name');
```

### 5. Toggle class

```js
  // jQuery
  element.toggleClass('.class-name');

  // ES6
  element.classList.toggle('.class-name');
```

### 6. Get attribute

Get atrribute value from an element:

```js
  // jQuery
  element.attr('href');

  // ES6
  element.getAttribute('href');
```

### 7. Set attribute

Set value into an attribute from an element:

```js
  // jQuery
  element.attr('href', 'https://www.google.com');

  // ES6
  element.setAttribute('href', 'https://www.google.com');
```

### 8. Get data attribute

Get data atrribute value from an element:

```js
  // jQuery
  element.data('id');

  // ES6
  element.getAttribute('data-id');
```

### 9. Set data attribute

Set value into data attribute from an element:

```js
  // jQuery
  element.data('id');

  // ES6
  element.setAttribute('data-id', 1);
  element.dataset.id = 1;
```

### 10. Get Text

Getting text from an element:

```js
  // jQuery
  element.text();

  // ES6
  element.textContent;
```

### 11. Get HTML

Getting HTML from an element:

```js
  // jQuery
  element.html();

  // ES6
  element.innerHTML;
```

### 12. Insert HTML string

Adding HTML into an element:

```js
  // jQuery
  element.html('<a href="https://www.gogle.com">Google</a>');

  // ES6
  element.innerHTML = '<a href="https://www.gogle.com">Google</a>';
```

### 13. Insert text string

Adding text into an element:

```js
  // jQuery
  element.text('Your text here');

  // ES6
  element.innerText = 'Your text here';
```

### 14. Show element

```js
  // jQuery
  element.show();

  // ES6
  element.style.display = 'block';
```

### 15. Hide element

```js
  // jQuery
  element.hide();

  // ES6
  element.style.display = 'none';
```

### 16. Show element with transition

```js
  // jQuery
  element.fadeIn();

  // ES6
  function fadeIn (element) {
    element.classList.add('show');
    element.classList.remove('hide');
  }
```

Using vanilla javascript, require extra css:

```css
  .show {
    transition: opacity 400ms;
  }
  .hide {
    opacity: 0;
  }
```

### 17. Hide element with transition

```js
  // jQuery
  element.fadeOut();

  // ES6
  function fadeOut (element) {
    element.classList.add('hide');
    element.classList.remove('show');
  }
```

Using vanilla javascript, require extra css:

```css
  .show {
    opacity: 1;
  }
  .hide {
    opacity: 0;
    transition: opacity 400ms;
  }
```

### 18. Loop through Array

```js
  // jQuery
  array.each((item), function {
    // ...
  });

  // ES6
  array.forEach((item) => {
    // ...
  });
```

### 19. Loop through Object

```js
  // jQuery
  object.each((key, value), function {
    // ...
  });

  // ES6
  for (const key in object) {
    console.log(key, object[key]);
  }

  // or
  for (const [key, value] of Object.entries(object)) {
    console.log(key, value);
  }
```

### 20. Add Event Listener

```js
  // jQuery
  element.on( 'click', function(event) {
    // ...
  });

  // ES6
  element.addEventListener('click', (event) => {
    // ...
  });
```

### 21. Ajax request

```js
  // jQuery
  $.ajax({
    url: 'https://example.com',
    method: 'post',
    dataType: 'json',
    contentType: 'application/json',
    data: JSON.stringify(data),
    success: function(response){
      // ...
    },
    error: function(error){
      // ...
    }
  });

  // ES6
  fetch( 'https://example.com', {
    method: 'post',
    headers: {
      'Accept': 'application/json',
      'Content-Type': 'application/json'
    },
    body: JSON.stringify(data)
  })
  .then(response => {
    // ...
  })
  .catch(error => {
    // ...
  });
```

## How to Contribute

Please, read [CONTRIBUTION.md](https://github.com/laisfrigerio/you-dont-need-jquery/blob/main/CONTRIBUTION.md) file

## 👩 Author

| [<img src="https://avatars.githubusercontent.com/u/20709086?v=4" width="100px;" alt="Lais Frigério"/><br /><sub><b>@laisfrigerio</b></sub>](https://github.com/laisfrigerio)<br /> |
| :---: |

## 📄 License

This project is licensed under the MIT License - see the LICENSE.md file for details