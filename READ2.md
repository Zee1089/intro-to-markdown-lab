![coding](https://media.istockphoto.com/id/1413837275/photo/abstract-it-design-background-with-a-tilted-triangular-grid-surface-and-python-computer.jpg?s=612x612&w=is&k=20&c=xT84Ak6PPi6BtI5bSZNf-JwHnbpjlmw7T6L8xqgWuZQ=)

# Introduction to the DOM

The **Document Object Model** (DOM), is the data representation of the objects that comprise the structure and content of a document on the web. This guide will introduce the DOM, look at how the DOM represents an [HTML](https://developer.mozilla.org/en-US/docs/Glossary/HTML) document in memory and how to use APIs to create web content and applications. 

## 1. What is the DOM?

The DOM is a programming interface for web documents, it represents the documents as nodes and objects. As an object-oriented representation of the web page, it can be modified with a scripting language such as JavaScript. *For Example*, the DOM specifies the `querySelectorAll` method code snipet must return a list of all p element 

```javascript
const paragraphs = document.querySelectorAll("p");
// paragraphs[0] is the first <p> element
// paragraphs[1] is the second <p> element, etc.
alert(paragraphs[0].nodeName);
``` 

## 2. DOM and JavaScript    

The previous short example, like nearly all examples, is JavaScript. That is to say, it is *written* in JavaScript, but *uses* the DOM to access the document and its element. 



## 3. Fundamental data types

There are a number of different data types being passed around the API that you should be aware of. 

> Note: The majority of code using DOM revolves around manipulating HTML docs, so it's common to refer to the nodes in the DOM as __elements__, anlthough strictly speaking not every node is an element. 

The following table briefly describes these data types. 

| Data type (interface) | Description |
| ------ | ----------- |
| <u>Document | The *ownerDocument* property of an element returns the document to which it belongs, this object is the root document itself.  
| <u>Node | Every object within a doc is a node of some kind. Can be en element node, but also a text node, or attribute node. 
| <u>NodeList | A nodeList is an array of elements. Items in a nodeList are accessed by index in either of two ways: <ul><li> list.item(1)</li><li>list[1]
| <u>Attr | Attributes are notes just like element, though you may rarely use them as such
________


## Interface and objects

When you get a reference to a table object as in the followinf example you routinely use all three of these interfaces interchangeably on the object, perhaps without knowing it. 

```javascript 
JS

const table = document.getElementById("table");
const tableAttrs = table.attributes; // Node/Element interface
for (let i = 0; i < tableAttrs.length; i++) {
  // HTMLTableElement interface: border attribute
  if (tableAttrs[i].nodeName.toLowerCase() === "border") {
    table.border = "1";
  }
}
// HTMLTableElement interface: summary attribute
table.summary = "note: increased border";
```

### Core interface in the DOM

The following is a brief list of common APIs in web and XML page scripting using the DOM:

* [document.querySelector()](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
* [document.querySelectorAll()](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
* [document.createElement()](https://developer.mozilla.org/en-US/docs/Web/API/Document/createElement)
* [Element.innerHTML](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML)

and many more!


Everything is taken from the 
[MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Functions) website! take a look for more info.








![codingPic](./codingPic.jpg)
