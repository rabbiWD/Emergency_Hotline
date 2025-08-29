1. What is the difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll?
Ans: The difference between getElementById, getElementsByClassName, and querySelector / querySelectorAll is -> 
# getElementById: Selects a single element by its unique id attribute. It returns the element directly or null if not found. 
# getElementByClassName is all elements that share a specific class name. Returns a live HTMLCollection (an array-like object) containing all elements that match the given class name(s). If no elements with the specified class exist, it returns an empty HTMLCollection.
and,
The main difference is that  #querySelector() returns the first element that matches a specified CSS selector, while #querySelectorAll() returns a static, non-live collection of all elements that match the selector

2. How do you create and insert a new element into the DOM?
Ans: Create and insert a new element into the DOM in two main steps:
* creating the Element: Use document.createElement(tagName) to create a new HTML element node. tagName is a string representing the type of element. Set attributes (like id, class, src, href) using element.setAttribute(attributeName, value).

* Inserting the Element: ParentNode.appendChild(childNode): Appends the childNode as the last child of the parentNode.  Inserts the specified element at a given position relative to the element it's called on

3. What is Event Bubbling and how does it work?
Ans: *Event bubbling is the process where a triggered DOM event moves up the DOM tree, from the target element to its ancestors, allowing parent elements to handle the event.
How it's work->
Event Trigger: A user action, such as a click, occurs on a specific element (the target element) within a nested structure of HTML elements.
Target Phase: The event handler on the target element is executed first.
Bubbling Phase: The event then travels upward through the Document Object Model (DOM) tree.
Ancestor Handlers: As the event moves up to each parent element, any event listeners attached to those ancestors are triggered.
Root Reached: This process continues until the event reaches the root of the DOM (the <html> or window object), at which point it stops, unless explicitly prevented

4. What is Event Delegation in JavaScript? Why is it useful?
Ans: Event delegation in JavaScript is a technique where a single event listener is attached to a parent element to manage events triggered by its child elements, rather than adding separate event listeners to each individual child.
Why it is useful:
# Improved Performance and Reduced Memory Usage:
Instead of creating numerous event listeners for each child element, only one listener is created on the parent.
# Simplified Code and Maintainability:
It centralizes event handling logic in one place, making the code cleaner, more organized, and easier to manage. 
# Handling Dynamically Added Elements:
Event delegation automatically handles events on elements that are added to the DOM after the initial page load. 

5. What is the difference between preventDefault() and stopPropagation() methods?
* Difference between preventDefault() vs stopPropagation() Methods->
# event.preventDefault() Method: 
Prevent the default action of browsers taking on that event.
It is a method present in the Event interface.
This method does not take any parameters
# event.stopPropagation() Method:
Prevent further propagation of current events by parent or child elements.
This method is also present in the Event interface.
This method also does not take any arguments in its definition