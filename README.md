# Emergency-Hotline-Service
## What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?
## => 
i. getElementById: selector type ID, select the first element with mataching id.
ii. getElementsByClassName: HTML collection and selector type is Class name, selecting all the element with the matching class
iii. querySelector: selector type is CSS selector which select first element that matching with selector 
iv. querySelectorAll: selector type is CSS selector (static nodeList) which select all element that matching with selector

## How do you create and insert a new element into the DOM?
## => 
step1: create new element 
```js 
    const newElement = document.createElement('div') 
```
step2: Add content 
```js
    newElement.textContent = 'Hi there, I am new Element' 
```
step3: Insert into Dom
```js
    const target = document.getElementById('otherElement')
    document.body.insertBefore(newElement, target) 
```
or
```js
    const exampleDiv = document.getElementById('exDiv')
    exampleDiv.appendChild(newElement) 
```

## What is Event Bubbling and how does it work?
## =>
Event Bubbling is like when a pebble is dropped into a pond and the ripples spread out. When a user clicks on something on a webpage, the event starts on the clicked element but then “bubbles up” to its parent elements one by one. For example, if a button inside a box is clicked, the click event happens first on the button, then on the box, and then possibly on the entire page. This is useful because it allows developers to listen for events on a larger container instead of adding a listener to every individual element.

## What is Event Delegation in JavaScript? Why is it useful?
## =>
Event Delegation is this cool trick I use in JavaScript where instead of putting event listeners on every single element, I just slap one listener on their parent. Then, whenever something happens on any of the kids, that one listener catches it and figures out exactly which one caused it.

Why do I like it? Because it saves me from adding and managing a bunch of listeners everywhere. Plus, when new stuff gets added or removed on the page, I don’t have to worry about adding or removing listeners — the one on the parent just takes care of it all automatically.

## What is the difference between preventDefault() and stopPropagation() methods?
## =>
I like to think of preventDefault() as hitting the pause button on what the browser normally does when something happens, like stopping a link from opening right away. On the other hand, stopPropagation() is more like telling the event to keep quiet and not spread out to parent elements. So while preventDefault() handles what the browser does by default, stopPropagation() controls how far the event travels through the page. Both come in handy depending on what needs to be controlled.