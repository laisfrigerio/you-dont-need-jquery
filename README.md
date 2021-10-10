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
5. [Get attribute](#5-get-attribute)
6. [Set attribute](#6-set-attribute)
7. [Get data attribute](#7-get-data-attribute)
8. [Set data attribute](#8-set-data-attribute)
9. [Get Text](#9-get-text)
10. [Get HTML](#10-get-html)
11. [Insert HTML string](#11-insert-html-string)
12. [Insert text string](#12-insert-text-string)
13. [Show element](#13-show-element)
14. [Hide element](#14-hide-element)
15. [Show element with transition](#15-show-element-with-transition)
16. [Hide element with transition](#16-hide-element-with-transition)
17. [Loop through Array](#loop-through-array)
18. [Loop through Object](#loop-through-object)
19. [Add Event Listener](#add-event-listener)
20. [Ajax request](#ajax-request)

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

### 5. Get attribute

Get atrribute value from an element:

```js
  // jQuery
  element.attr('href');

  // ES6
  element.getAttribute('href');
```

### 6. Set attribute

Set value into an attribute from an element:

```js
  // jQuery
  element.attr('href', 'https://www.google.com');

  // ES6
  element.setAttribute('href', 'https://www.google.com');
```

### 7. Get data attribute

Get data atrribute value from an element:

```js
  // jQuery
  element.data('id');

  // ES6
  element.getAttribute('data-id');
```

### 8. Set data attribute

Set value into data attribute from an element:

```js
  // jQuery
  element.data('id');

  // ES6
  element.setAttribute('data-id', 1);
  element.dataset.id = 1;
```

### 9. Get Text

Getting text from an element:

```js
  // jQuery
  element.text();

  // ES6
  element.textContent;
```

### 10. Get HTML

Getting HTML from an element:

```js
  // jQuery
  element.html();

  // ES6
  element.innerHTML;
```

### 11. Insert HTML string

Adding HTML into an element:

```js
  // jQuery
  element.html('<a href="https://www.gogle.com">Google</a>');

  // ES6
  element.innerHTML = '<a href="https://www.gogle.com">Google</a>';
```

### 12. Insert text string

Adding text into an element:

```js
  // jQuery
  element.text('Your text here');

  // ES6
  element.innerText = 'Your text here';
```

### 13. Show element

```js
  // jQuery
  element.show();

  // ES6
  element.style.display = 'block';
```

### 14. Hide element

```js
  // jQuery
  element.hide();

  // ES6
  element.style.display = 'none';
```

### 15. Show element with transition

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

### 16. Hide element with transition

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

### Loop through Array

### Loop through Object

### Add Event Listener

### Ajax request

## :woman: Author

| [<img src="https://avatars.githubusercontent.com/u/20709086?v=4" width="100px;" alt="Lais Frigério"/><br /><sub><b>@laisfrigerio</b></sub>](https://github.com/laisfrigerio)<br /> |
| :---: |

## 📄 License

This project is licensed under the MIT License - see the LICENSE.md file for details