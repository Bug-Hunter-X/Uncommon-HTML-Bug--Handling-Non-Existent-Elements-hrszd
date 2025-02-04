# Uncommon HTML Bug: Handling Non-Existent Elements

This repository demonstrates a subtle but important bug in HTML/JavaScript where attempting to manipulate a DOM element that does not exist can lead to unexpected behavior.

The `bug.html` file shows an incorrect approach, while `bugSolution.html` illustrates the correct way to prevent errors when interacting with potentially missing elements.

## The Bug

The common mistake is directly attempting to modify a DOM element's properties (e.g., `innerHTML`) without first checking if it actually exists in the document. If the element isn't found, a JavaScript error will usually occur (depending on the browser). Even worse, no visible change will occur, making it difficult to debug.

## The Solution

The recommended solution is to always check if the element exists using `document.getElementById()` before trying to access or modify its properties.  Handle the case where the element is not found gracefully (e.g., display a message or log an error) to prevent unexpected behavior.