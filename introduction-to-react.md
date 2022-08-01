<div align="center">
  <h1> Getting Started React</h1>
  <sub>
    <p> August, 2022</p>
  </sub>
</div>


- [Getting Started React](#getting-started-react)
  - [1. What is React?](#1-what-is-react)
  - [2. Why React?](#2-why-react)
  - [3. JSX](#3-jsx)
    - [JSX Element](#jsx-element)
    - [Commenting a JSX element](#commenting-a-jsx-element)
    - [Rendering a JSX Element](#rendering-a-jsx-element)
    - [Style and className in JSX](#style-and-classname-in-jsx)
    - [Injecting data to a JSX Element](#injecting-data-to-a-jsx-element)
      - [Injecting a string to a JSX Element](#injecting-a-string-to-a-jsx-element)
      - [Injecting a number to a JSX Element](#injecting-a-number-to-a-jsx-element)
      - [Injecting an array to a JSX Element](#injecting-an-array-to-a-jsx-element)
      - [Injecting an object to a JSX Element](#injecting-an-object-to-a-jsx-element)
  - [Exercises](#exercises)
    - [Exercises: What is React?](#exercises-what-is-react)
    - [Exercises: Why React?](#exercises-why-react)
    - [Exercises: JSX](#exercises-jsx)
    - [Exercises: JSX Elements](#exercises-jsx-elements)
    - [Exercises: Inline Style](#exercises-inline-style)
    - [Exercises: Internal Styles](#exercises-internal-styles)
    - [Exercise: Inject data to JSX](#exercise-inject-data-to-jsx)

## Getting Started React

This section covers prerequisites to get started with React. You should have a good understanding of the following technologies:

- HTML
- CSS
- JavaScript

If you have the skills mentioned above, you will enjoy doing React. 

### 1. What is React?

React is a JavaScript library for building a reusable user interface(UI). It was initially released on May 29, 2013. The current version is 18.2.0 and somehow it is stable. React was created by Facebook. React makes creating UI components very easy. The official React documentation can be found [here](https://reactjs.org/docs/getting-started.html). When we work with React we do not interact directly with the DOM. React has its own way to handle the DOM(Document Object Model) manipulation. React uses its virtual DOM to make new changes and it updates only the element, that needs changing. Do not directly interact with DOM when you build a React Application and leave the DOM manipulation job for the React virtual DOM. In this learning phase, we will develop 4-5 web applications using React. A web application, or a website, is made of buttons, links, forms with different input fields, header, footer, sections, articles, texts, images, audios, videos and boxes with different shapes. We use react to make a reusable UI components of a website.

To summarize:

- React was released in May 2013
- React was created by Facebook
- React is a JavaScript library for building user interfaces
- React is used to build single page applications - An application which has only one HTML page.
- React allows us to create reusable UI components
- React latest release is 18.2.0
- [React versions](https://reactjs.org/versions/)
- React official documentation can be found [here](https://reactjs.org/docs/getting-started.html)

### 2. Why React?

React is one of the most popular JavaScript libraries. Many developers and companies have been using it for the last couple of years. Its popularity has been growing fast and it has a huge community.

Why we choose to use React ? We use it because of the following reasons:

- fast
- modular
- scalable
- flexible
- big community and popular
- open source
- High job opportunity

### 3. JSX

JSX stands for JavaScript XML. JSX allows us to write HTML elements with JavaScript code. An HTML element has an opening and closing tags, content, and attribute in the opening tag. However, some HTML elements may not have content and a closing tag - they are self closing elements. To create HTML elements in React we do not use the _createElement()_ instead we just use JSX elements. Therefore, JSX makes it easier to write and add HTML elements in React. JSX will be converted to JavaScript on browser using a transpiler - [babel.js](https://babeljs.io/). Babel is a library which transpiles JSX to pure JavaScript and latest JavaScript to older version. See the JSX code below.

```js
// JSX syntax
// we don't need to use quotes with JSX
const jsxElement = <h1>I am a JSX element</h1>
const welcome = <h1>Welcome to React</h1>
const data = <small>Aug 2, 2022</small>
```

The above strange looking code seems like JavaScript, but it is not JavaScript and it seems like HTML but not completely an HTML element. It is a mix of JavaScript and an HTML elements. JSX can allow us to use HTML in JavaScript. The HTML element in the JSX above is _h1_ and _small_.

#### JSX Element

As you have seen in the example above, JSX has a JavaScript and HTML like syntax. JSX element could be a single HTML element or many HTML elements wrapped in a parent HTML element.

This JSX element has only one HTML element which is _h1_.

```js
const jsxElement = <h1>I am a JSX element</h1> // JS with HTML
```

Let's make more JSX elements by declaring a new variable named title and content inside _h2_.

```js
const title = <h2>Getting Started React</h2>
```

Let us add a subtitles and other contents to this JSX element by adding additional HTML elements. Every HTML element should be wrapped by an outer HTML element to create a valid JSX element. The name title variable also should be changed to header because our JSX element is containing almost all of the header of the application.

```js
const header = (
  <header>
    <h1>Welcome to React</h1>
    <h2>Getting Started React</h2>
    <h3>JavaScript Library</h3>
  </header>
)
```

Let us keep adding more elements. Additional HTML elements to display the author name and year.

```js
const header = (
  <header>
    <h1>Welcome to Of React</h1>
    <h2>Getting Started React</h2>
    <h3>JavaScript Library</h3>
    <p>Rajat Gandhi</p>
    <small>Aug 2, 2022</small>
  </header>
)
```

As you can see the _header_ element is a parent element for all the inner HTML elements and JSX must be wrapped by an outer parent element. Without the _header_ HTML element or other parent HTML element the above JSX is invalid.

#### Commenting a JSX element

We comment codes for different reasons and it is also good to know how to comment out JSX elements in React.

```js
{
  /*
 <header>
    <h1>Welcome to React</h1>
    <h2>Getting Started React</h2>
    <h3>JavaScript Library</h3>
    <p>Rajat Gandhi</p>
    <small>Aug 2, 2022</small>
  </header>
*/
}
```

#### Rendering a JSX Element

