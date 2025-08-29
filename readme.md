** Answer the following questions: **
1.What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?
2.How do you create and insert a new element into the DOM?
3.What is Event Bubbling and how does it work?
4.What is Event Delegation in JavaScript? Why is it useful?
5.What is the difference between preventDefault() and stopPropagation() methods?

** ANSWERS: **

Question-1: What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?
ANSWER-1:

document.getElementById("idName"):

1.Finds only ONE element with the exact id.
2.Since IDs must be unique, you will always get just one element or null if not found.
3.Fastest and simplest if you know the element’s id.

document.getElementsByClassName("className"):

1.Finds all elements with the given class.
2.Returns something like a live list not an array, but looks similar.
3.You usually it through loop if there are multiple elements.

document.querySelector("cssSelector"):

1.Finds the first element that matches a CSS selector.
2.Very powerful. You can use #id, .class, div > p etc.
3.When you want one element with flexible selection then it's Great.

document.querySelectorAll("cssSelector"):

1.Finds all elements that match the CSS selector.
2.Returns a static list doesn’t auto update like getElementsByClassName.
3.When you want to grab multiple elements with CSS selector then it flexibility.


Question-2: How do you create and insert a new element into the DOM?
ANSWER-2:

Create the element: First you use document.createElement("tagName").
Example: Create a <p> or <div>.

Add content or attributes: Second you can put text inside or add classes, IDs etc.

Insert it into the page: Third you choose where it should go and attach it using methods like:

1.appendChild() // adds at the end.

2.prepend() // adds at the start.

3.insertBefore() // puts it before another element come.


Question-3: What is Event Bubbling and how does it work?
ANSWER-3:

Event bubbling: Event bubbling is a way web browsers handle events (like clicks) in the Document Object Model (DOM).

When an event happens on an element, it does not just stop there. It "bubbles up" meaning it starts at the target element and then moves up through its parent elements one by one.


Question-4: What is Event Delegation in JavaScript? Why is it useful?
ANSWER-4:

Event Delegation in JavaScript:
Event delegation is a technique in JavaScript where you attach a single event listener to a parent element, instead of adding listeners to each individual child element.
Example:
When an event happens on a child, it bubbles up to the parent and the parent handles it.

Why it useful:

1.Better performance:
Instead of adding lots of event listeners to many child elements, you add just one to the parent. It need less memory and faster performance.

2.Handle new elements automatically:
If you add new child elements later, you don’t need to add new listeners. The parent still handles their events.

3.Cleaner code:
Fewer lines, easier to manage and debug.


Question-5: What is the difference between preventDefault() and stopPropagation() methods?
ANSWER-5:

Both methods are used in event handling in JavaScript. But they do different things. Here describe 2 methodes:

1.preventDefault():
What is do:
Stops the browser’s default behavior for an event.

When it use:
You want to stop something the browser would normally do like submitting a form, following a link, scrolling etc.

2.stopPropagation():

What it do:
Stops the event from bubbling up to parent elements.

When it use:
You want the event to stay only on the target element and not trigger any event listeners on its parents.