# Document Object Model (DOM) tree

The DOM tree (Document Object Model tree) is a hierarchical representation of the HTML (or XML) structure of a web page, where each HTML element is represented as a node in the tree. The DOM tree is created by the browser when it parses the HTML code of a web page and generates a structured representation of the document.

The DOM tree has a root node, which represents the entire document, and several child nodes, which represent the different elements of the document. Each node can have zero or more child nodes, which represent the nested elements inside the parent element. The DOM tree is a tree-like structure because each element can have only one parent, but can have multiple child nodes.

The DOM tree is important because it provides a way for JavaScript to interact with the HTML elements on a web page. JavaScript can access and modify the properties and attributes of the elements in the DOM tree, and can add or remove elements from the tree dynamically. This enables web developers to create dynamic and interactive web pages that respond to user actions and events.

## What Is the DOM Tree?

The document object is the base of all of the DOM’s nodes. The nodes are arranged as a tree, with nodes nested under other nodes. Below, is an example of the DOM representation of a simple web page:

```
<!DOCTYPE html>
<html>
    <head>
        <title>Example Page</title>
    </head>
    <body>
        <div id="first-div" class="content-div">
            <p>Example page content.</p>
            <ul>
                <li><span class="numeral-name" style="color: green;">First</span> item</li>
                <li><span class="numeral-name" style="color: red;">Second</span> item</li>
            </ul>
        </div>
        <div id="second-div" class="content-div">
            <p><a href="#">Lorem ipsum</a> dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Tortor condimentum lacinia quis vel eros donec. Purus ut faucibus pulvinar elementum integer enim neque volutpat ac. Netus et malesuada fames ac turpis egestas sed tempus. Nulla posuere sollicitudin aliquam ultrices sagittis orci a scelerisque. Et netus et malesuada fames ac turpis egestas sed. Purus ut faucibus pulvinar elementum integer enim neque. <em>Amet consectetur adipiscing elit ut aliquam.</em></p>
        </div>
    </body>
</html>

```

In the example above, elements nest under other elements. The two div elements are nested under the body element. Text nodes are nested under the p and li elements, and the style attribute is considered a node under the p element, as well.

Plotting the nesting structure out, the DOM resembles the following tree:

```
body
 \_ div
 |   \_ p
 |      \_ [text]
 |      |
 |      \_ [attribute]
 \_ div
     \_ ul
         \_ li
         |   \_ [text]
         |
         \_ li
             \_ [text]
```

<img src="https://www.linode.com/docs/guides/traversing-the-dom/dom-tree-example_huc1be129ee162561ad91a8ea0061e877c_45624_1388x0_resize_q71_bgfafafc_catmullrom_3.jpg"/>

Knowing the arrangement of the DOM tree and its leaves, helps you understand how to access specific nodes when working with JavaScript. This is especially true when you are working with more complicated web pages. The Navigating the DOM Tree section of this guide includes a more in-depth discussion on moving around the nodes of the DOM tree.

The diagram below provides a visualization of the DOM tree for this guide’s example web page. You can also view the example-page.html file in the Before You Begin section of this guide.

## How to Access Elements via Object Methods

1. **'getElementById()'**: This method retrieves the HTML element with a specific ID attribute.

Example :

```
const element = document.getElementById('myElement');
```

2. **'getElementsByClassName()'**: This method retrieves all the HTML elements with a specific class name.

Example :

```
const elements = document.getElementsByClassName('myClass');
```

3. **'getElementsByTagName()'**: This method retrieves all the HTML elements with a specific tag name.

Example :

```
const elements = document.getElementsByTagName('p');
```

4. **'querySelector()'**:  This method retrieves the first HTML element that matches a specified CSS selector.

Example

```
const element = document.querySelector('.myClass');
```

5. **'querySelectorAll()'**: This method retrieves all the HTML elements that match a specified CSS selector.

Example

```
    const elements = document.querySelectorAll('p.myClass');
```

"# DOM_tree" 
