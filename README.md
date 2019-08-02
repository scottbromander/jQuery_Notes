# JavaScript Review

JavaScript is a loosely typed, interpreted run-time language.

First of two JS review lectures. Covers

- primitives
- data types
- variables
- expressions and operators
- NaN, null, undefined values
- conditional statements and comparison operators
- loops
- functions

## Jargon
      . - dot
      () - parenthesis, parens
      [] - brackets, square brackets, square braces
      {} - braces, curlies, curly braces, curly brackets
      < - less than, bird, angle brackets
      > - greater than, gator, angle brackets
      / - slash, whack, forward slash
      \ - back slash
      ! - not, bang
      # - pound, hash, number
      * - star, splat
      || - or, pipes
      $ - dollar sign, bling, cash
      NaN - not a number, bread

## Some data types

Data type | Example
--- | ---
Number | `18`
String | `'taco'` and `'18'`

Additional resources: [data types](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Data_structures)

## Variables

`let x = 1`

- `let` is a **keyword** that tells the computer we are defining a variable

- `x` is the **name** of the variable

- `=` is the **assignment operator**

- `1` is the **value** of the variable

### Naming your variables

- Use camel-case
- Start with a letter
- Use a noun (unless you're naming a function)
- Be descriptive

`let firstName = 'Chris';`

`let numberOfPets = 2;`

## Expressions and operators

"An expression is any valid set of literals, variables, operators, and expressions that evaluates to a single value." [[source](http://lib.ru/JAVA/javascr/expr.html)]

```JavaScript
let x = 3; // expression

x = x + 1; // expression

x += 1; // expression using shorthand compound assignment operator

x++; // increments by 1
```

### String Considerations

- `+` will convert a number to a string and concatenate them
 - `'1' + 2 = '12'`
- all other operators will convert a string into a number, if possible
 - `'10' - 5 = 5`
 - `'36' / 6 = 6`
 - `'ten' * 3 = NaN`

## NaN, null, undefined values

**NaN** stands for Not a Number. Value is not a legal number.

**null** represents an empty value.

**undefined** indicates a variable has not been assigned a value.

**not defined** indicates a variable was referenced but it doesn't exist in the correct scope.

## Conditional statements and comparison operators

```JavaScript
if (/*expression is truthy*/) {
  // perform some logic
} else {
  // perform some other logic
}
```

### Comparison Operators

Operator | Description | Example | Returns
--- | --- | --- | ---
`==` | equal to | `8 == 8` | true
`==` | equal to | `'8' == 8` | true
`===` | equal to and type | `8 === 8` | true
`===` | equal value and type | `'8' === 8` | false
`!=` | not equal to | `8 != 8` | false
`!==` | not equal value or type | `'8' !== 8` | true
`>` | greater than | `8 > 8` | false
`<` | less than | `8 < 8` | false
`>=` | greater than | `8 >= 8` | true
`<=` | less than | `8 <= 8` | true

## Loops

Allows us to perform some logic repeatedly until some ending condition is reached. There are various types of loops and in the beginning it seems they all do the same thing. How do you pick which one to use?

### while loops

While loops are typically run until some logical condition is met.

```JavaScript
while (/* expression is truthy */) {
  // perform some logic
}
```

### for loops

For-loops are commonly used to run a set number of times (as opposed to being based on logic like a while loop.) Therefore they are very often used iterate over a collection like an array. They then perform some logic on every item within that collection.

```JavaScript
for (let i = 0; i < 3; i++) {
  // perform some logic
  // the variable i can be used inside this block. It will be a Number
}
```

`let i = 0` acts to *initialize* any variables before the loop is run.

`i < 3` is a *condition* that must be true for the logic in the loop to be performed.

`i++` is the *final expression* evaluated at the end of the current loop iteration.

The use of `i` is very common across languages. It can be thought to represent `incrementor`, `iterator`, or `index`

```JavaScript
const hats = ['stocking cap', 'baseball cap', 'fedora', 'top hat'];
for (let i = 0; i < hats.length; i++) {
  // perform some logic
  // access each element in our hats array using the variable i to stand in for the index number
  console.log( hats[i] );
}
```

## Functions

Functions are blocks of logic we want to be able to run repeatedly, whenever we want. Functions give us the ability to reuse code. Each function should contain all of the logic it needs to do its work. This is called `encapsulation`

Functions often take input, do something with that input, and give us back a result.

```JavaScript
// function declaration
function doubleIt(x) {
  return x * 2;
}

// function expression
let doubleIt = function(x) {
  return x * 2;
}
```

- Each function does the same thing, BUT *function declarations* can appear anywhere in a file, while *function expressions* must be defined before they are used.
- `x` is an **argument**. Arguments allow us to pass data/values to our functions.
- **Arguments** are also called **parameters**
- The value of the function expression is an *anonymous function*: a function that has no name.
- `return` is a keyword that is used to exit a function with a given value.

**Additional resources:** [function expression vs. declaration](https://javascriptweblog.wordpress.com/2010/07/06/function-declarations-vs-function-expressions/)


## JavaScript Built-In Functions, Strings and Arrays

JavaScript comes with a host of useful functions. We explore a few here,
but there are more at [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects).

**Methods** are **functions** that are attached to a specific **object**. **Methods** are more commonly written as _function expressions_. When writing a **function** in the global scope it is more common to use a _function declaration_.

### Built-In Functions

* [Number()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)
* [parseFloat()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/parseFloat)
* [parseInt()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/parseInt)
* [String()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)

### Object Methods

* .toString()

## String Methods

* [.charAt()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/charAt)
* [.length](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/length)
* [.substring()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/substr)

[W3Schools String Methods](https://www.w3schools.com/js/js_string_methods.asp)

### Array Methods

* [.push()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/push?v=control)
* [.pop()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/pop?v=control)
* [.shift()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/shift?v=control)
* [.unshift()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/unshift?v=control)

[W3Schools Array Methods](https://www.w3schools.com/js/js_array_methods.asp)

![array methods](../images/array_methods.png)

### Also...

Convert String to an Array

```JavaScript
let str = "a, b, c, d, e";
let theArray = str.split(",");
```

# JavaScript Object Review

## Object Review

Objects are a data type that allows us to store multiple pieces of information together inside a single variable.

Each piece of data inside an object is called a **property**. Also sometimes called a **key**. Each **property** has a value. The value can be any legal JavaScript data type including Numbers, Strings, Arrays, other objects, or even Functions.


## Object Literals

A quick way to create an object is with an assignment expression with an **Object Literal**. This code creates a single Object variable.

```JavaScript
const topHat = {
    type: 'Top',
    color: 'Black',
    size: 14
};

const baseballHat = {
    type: 'Baseball Cap',
    color: 'Red and White',
    size: 12
}
```

This can be very handy and is used frequently in JavaScript.

Starting with an array of penguins, can you create a function that takes in an array of penguins, and returns only the cute penguins less than a certain size?

```JavaScript
let penguins = [
  {
    name: 'Emperor',
    colors: ['Black', 'White', 'Yellow'],
    size: 1.0,
    isCute: true
  },
  {
    name: 'Little',
    colors: ['Slate-blue', 'White'],
    size: 0.5,
    isCute: true
  },
  {
    name: 'Rockhopper',
    colors: ['Black', 'White', 'Yellow'],
    size: 0.75,
    isCute: true
  },
  {
    name: 'African',
    colors: ['Black', 'White'],
    size: 0.5,
    isCute: true
  },
  {
    name: 'Gentoo',
    colors: ['Black', 'White'],
    size: 0.5,
    isCute: true
  },
  {
    name: 'Sea Gull',
    colors: ['Gray'],
    size: 0.25,
    isCute: false
  },
  {
    name: 'Chinstrap',
    colors: ['Black', 'White'],
    size: 0.25,
    isCute: true
  },
  {
    name: 'Macaroni',
    colors: ['Black', 'White', 'Yellow'],
    size: 0.5,
    isCute: true
  },
];

function checkPenguins(allPenguins, maxHeight) {
  let cutePenguins = [];
  for (let i = 0; i < allPenguins.length; i++) {
    if (!allPenguins[i].isCute && allPenguins[i].size < maxHeight) {
      cutePenguins.push(allPenguins[i].name);
    }
  }
  return cutePenguins;
}

console.log(checkPenguins(penguins, 0.9));
```

## Object Constructors

The downside of object literals is that if we need a lot of different kinds of `hat` or `penguin` objects, we don't want to copy and paste this code over and over again.

Constructor functions are special functions that are used to create objects. We give it some info about the object we want and it `returns` to us an object we can use.

```JavaScript
function Hat(type, color, size) {
    this.type = type;
    this.color = color;
    this.size = size;
}

// Object instances of a Hat
const averageTopHat = new Hat('Top', 'Black', 14);
const funnyHat = new Hat('Beanie', 'Multicolored', 10);
const largeTopHat = new Hat('Top', 'Purple', 24);
```

Using a constructor saves a bunch of time and typing. It also means if you want to change how hats are created, you only need to change the code in the Constructor function.

The `new` keyword is used to denote we want a new object of the given type.

Constructor function names are Capitalized. This is how we know they are a Constructor function instead of a normal function.

# HTML Review

[Code similar to lecture](https://github.com/PrimeAcademy/lecture-html-css-intro/)
[Live hosted code](https://primeacademy.github.io/lecture-html-css-intro/)

Lecture Objectives:

- understand HTML's place in web development
- understand static page limitations
- examples of: containers, lists, tables, forms, links, images
- understand concept of box model
- understand core CSS selectors
- resources


## Overview

Browsers only understand HTML and CSS as a way to render (draw) things on the page. Web development requires at least some knowledge of HTML. Even fancy things like React JSX all boil down to HTML and CSS in the end.

Static HTML pages do not change. Having a site with static pages ("static content") is difficult to maintain and has a lot of repeated code. However, it's a good place to start in learning HTML and CSS.


## Where to Start

Layout your content in big boxes prior to digging into specific components.

```
+===================+
|      Header       |
+===================+
|       Nav         |
+-------------------+
| Content | Content |
+-------------------+
|      Content      |
+-------------------+
|      Footer       |
+-------------------+
```

## HTML Elements

An **element** includes the open **tag**, closing **tag** and everything in between:

> `<span>Hello World</span>`

Some elements are **self-closing** and only need an opening tag with a slash just before the closing angular bracket:

> `<img src="path/to/image.png" />`

> `<input type="text" />`

A **tag** is the open or closing of an **element**:

> `<span>`

They are sometimes used interchangeably but technically have slightly different meanings.

## Nesting

Elements can be nested inside one another. Not all combinations are valid, even through you will not see any errors given. The browser will always try to render whatever you throw at it.

```HTML
<div>
	<h1>Heading!</h1>
	<p>This is <span>valid</span></p>
</div>

<table>
	<div>
		<p>This is not valid at all.</p>
	</div>
</table>

```

Some elements must be used together and are therefore more complicated to use. Tables, lists, drop down menus are some examples.

## Attributes

Some elements allow optional additional parameters called **attributes** which help specify more about this particular element. Attributes include a specific keyword, an equal sign, and a value in double quotes.

### Examples

> `<script src="/scripts/index.js" type="javascript">`

> `<img src="http://images.google.com/superfunimage.jpg" />`

> `<div id="container">`

> `<p class="drop-cap orange">`

## Container Elements

Elements used to contain other elements. Some have an implied meaning or usage, but all of them act like `div`s in terms of layout and style.

- div
- header
- sidebar
- main
- footer
- section

## Lists

```HTML
<ul>
	<li>First item</li>
	<li>Second item</li>
	<li>Third item</li>
	<li>
		<ol>
			<li>Bullet one</li>
			<li>Bullet two</li>
			<li><a href="http://www.google.com">Link to Google</a></li>
		</ol>
	</li>
</ul>
```

## Images

```HTML
<img src="path/to/image.png" />

<div style="background-image: url(path/to/image.png) top left no-repeat">
```

## Links

Things you can click on to go to another URL or HTML document.

> `<a href="path/to/page.html">Click Me</a>`

Don't do this. Buttons and links are different!

> `<button><a href="">Click Me</a></button>`

## Tables

```HTML
<table>
	<thead>
		<tr>
			<th></th>
			<th></th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td></td>
			<td></td>
		</tr>
	</tbody>
</table>
```

## Forms & Inputs

The form element has some built in functionality. Namely, you can hit enter to submit. It reloads your page, though, so avoid it until we learn how to prevent the default behaviour. 

```HTML
<form>
	<input type="text placeholder="name" />
	<input type="submit" />
</form>
```

Inputs can be used outside of forms -- there are many types that help users know what to do!
- [Form Input Types](https://www.w3schools.com/tags/att_input_type.asp)


## Page Layout vs Visual Styling

HTML and CSS will either affect the **layout** of the page (how things are arranged on the page) or they will affect **styling** of elements (how things look).

### In-Line Elements

```HTML
<span>This will not</span>
<span>break the line.</span>
<button>Click Here</button>
<input type="text" />
```

### Block Level Elements

```HTML
<h2>Breaking Element</h2>
<p>Paragraph 1</p>
<p>Paragraph 2</p>
<ol>
	<li>Read</li>
	<li>Write</li>
	<li>Speak</li>
	<li>Teach</li>
</ol>
<ul>
	<li>Charlie</li>
	<li>Thor</li>
</ul>
<div>
	...
</div>
```

---

## Common Element Selectors

See the [Full Reference at w3schools](https://www.w3schools.com/cssref/css_selectors.asp)

Selector | Example | Description
--- | --- | ---
element | div | Selects all elements with that tag
[.class](https://www.w3schools.com/cssref/sel_class.asp) | .intro | Selects all elements with class="intro"
[#id](https://www.w3schools.com/cssref/sel_id.asp) | #firstName | Selects the element with id="firstName"
 [*](https://www.w3schools.com/cssref/sel_all.asp) | * | Selects all elements
[element](https://www.w3schools.com/cssref/sel_element.asp) | p | Selects all <p> elements
[element within another element](https://www.w3schools.com/cssref/sel_element_element.asp) | div p | Selects all <p> elements inside <div> elements
| [multiple elements](https://www.w3schools.com/cssref/sel_element_comma.asp) | h1, h2, h3 | select all these elements

---

## Box Model

If you inspect an element with your browser, you can see a representation of the box model. Everything rendered on the page is a box. These boxes have properties and this is called **The Box Model**.

The parts of the box model are:

- `Content` - The content of the box, where text and images appear.
- `Padding` - Clears an area around the content but inside the element's box. The padding is transparent. Gives us space **inside** the box.
- `Border` - A border that goes around the padding and content
- `Margin` - Clears an area outside the box and border. The margin is transparent. Margin gives us space **between** elements.

---

## CSS properties to know!

- margin
- padding
- border
- height
- width
- display (block, inline, flex, grid, none)
- background-color

## The most common CSS question: HOW DO I CENTER?

Many options to center things. Thats part of the problem. This decision tree is very helpful:

- [Centering In CSS](https://css-tricks.com/centering-css-complete-guide/)


---

## Additional Resources

### HTML

- [HTML5 Elements](https://www.w3schools.com/html/html5_semantic_elements.asp)
- [HTML Tables](https://www.w3schools.com/tags/tag_thead.asp)
- [Form Input Types](https://www.w3schools.com/tags/att_input_type.asp)

### CSS

- [Web Colors](https://en.wikipedia.org/wiki/Web_colors)
- [CSS Selector Reference](https://www.w3schools.com/cssref/css_selectors.asp)
- [Advanced Layout: CSS Grid](https://www.w3schools.com/css/css_grid.asp)
- [Advanced Layout: CSS Flexbox](https://www.w3schools.com/css/css3_flexbox.asp)
- [Centering In CSS](https://css-tricks.com/centering-css-complete-guide/)
- [Normalizing CSS](https://necolas.github.io/normalize.css/)

# jQuery Intro

## Topics

* What is jQuery?
* Getting jQuery
* The Document Object Model (DOM)
* Event-Driven Programming
* Resources

## What is jQuery?

* a software library used to traverse and manipulate the DOM, handle events,
create animations, and make asynchronous requests to a server
* is a layer on top of vanilla JavaScript

## Getting jQuery

You can include jQuery in your projects in two ways:

**Method 1:** Download the minified file from http://jquery.com/download/. Then, source that file into your HTML file.

```HTML
<script src="jquery-3.1.1.min.js"></script>
```

OR

**Method 2:** Include a content delivery network (CDN) source in your HTML file.

```HTML
<script src="https://code.jquery.com/jquery-3.1.1.min.js"></script>
```

**REMEMBER:** Source the jQuery library into your `index.html` file _before_ your JavaScript file.

## The Document Object Model (DOM)

* cross-platform and language-independent convention for representing and interacting with objects in HTML documents
* organized in a tree structure

![](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/DOM-model.svg/220px-DOM-model.svg.png)

## Event-Driven Programming

To create dynamic web pages, we need JavaScript code that is not completely sequential. We need to react to events.

Our code can run at three events:

1. When the page loads the script.
2. When the browser loads the DOM.
3. When other events occur. (Covered in later lecture.)

```JS
$(document).ready(onReady);

function onReady() {
  // Event 2
  // code here runs after DOM is loaded
});

// Event 1
// code here runs when the script (file) is loaded
// non-DOM code can safely go here
```

## Resources

* [jQuery official website](http://jquery.com/)
* [jQuery documentation](http://api.jquery.com/)

# jQuery Selectors, DOM Manipulation and Events

[Code from Lecture](https://github.com/PrimeAcademy/hadar-jquery-intro)

Once the DOM is loaded, we can select elements with the `$()` syntax. When we do this, we get a jQuery object.

To _manipulate_ the DOM, we must first select an element.

## Selectors

* select by ID - `$('#some-id')`
* select by class - `$('.some-class')`
* select descendants - `$('ul li')`
* select multiple elements - `$('.mic, .check')`
* find elements within a selection - `$('#solid').find('.rock')`

**Selectors** return an **Object** that has properties and functions we can call.

## DOM Traversal

Once we select an element, we can navigate to other elements in the DOM tree.

* navigate to parent element - `$('.some-child').parent()`
* get the first-level children of an element - `$('ul').children()`

## DOM Manipulation

Once we select an element, we can change how that element appears on the DOM.

* change an elements text color - `$('#once-blue').css('color', 'blue')`

## Manipulating Classes

Allows us to easily change which pre-defined CSS classes are applied to any element. We can further react to events by applying CSS rules which have visual changes, even animations associated with them.

```JavaScript
addClass('className');    // adds a CSS class by name
removeClass('className'); // removes CSS class by name
toggleClass('className'); // adds if it isn't on the element, removes if it is

// CSS file
 .className {
  color: blue;
}

```

## Getters and Setters

Some manipulation methods that allow us to **set** (i.e. change or update) properties for jQuery objects, can also be used to **get** the current properties of that object.

```JavaScript
$('#an-element').text('Hello World!'); // sets the text in the element to Hello World!

$('#an-element').text(); // returns the value "Hello World!"

$('#an-input').val(); // returns the value of the input field

$('#an-input').val(''); // clears input text
```

## Handling Click Events

- Events are registered to listeners on DOM ready
  - We can only register events to elements that are on the DOM at this time
  - What about buttons that are created on the fly? Can we still add listeners to them?
  - Adding descendant selectors - `$('#section').on('click', '.dynamicallyCreatedButton', function(){});`
- Callback functions contain logic that occurs when event actually triggered

### $(this)

- How we know what was clicked to trigger the event
- Represents the **target** of the **event** (e.g. *click*)

## Appending/Removing from DOM

- `.append()`
- `.remove()`
- `.empty()`


## References

* [jQuery Selector Documentation](http://api.jquery.com/category/selectors/)
* [jQuery Manipulation Documentation](http://api.jquery.com/category/manipulation/)
