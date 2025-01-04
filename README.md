# Uncommon HTML Bug: innerHTML Overwriting Event Handlers

This repository demonstrates an uncommon bug related to the use of `innerHTML` in HTML.  When using `innerHTML` to modify HTML content that contains inline event handlers, subsequent modifications can overwrite existing handlers. This can lead to unexpected behavior and is not always easy to detect.

The `bug.html` file shows the problematic code. The `bugSolution.html` file offers a solution that leverages event delegation or avoids `innerHTML` to prevent such issues.

## Bug Description
The code adds HTML elements using `innerHTML`.  The first `innerHTML` assignment adds a paragraph with an inline onclick event handler. However, the second `innerHTML` assignment overwrites the previous content and the event handler is lost.

## Solution
The solution avoids direct manipulation of `innerHTML`.  Instead, it uses `createElement` to create elements. This method prevents the unintended overwriting of elements and maintains the functionality of all inline event handlers.