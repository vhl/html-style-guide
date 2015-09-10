# HTML Style Guide

## Guidelines

* Keep HTML structure as simple as possible.
* Use 2 spaces for indentation.
* Lowercase all elements and attributes.
* For "empty" elements, do not use XHTML closing syntax `<br />` — just use `<br>`.
* Although HTML5 allows omitting certain closing tags, like `</p>` and `</li>`, *Don't*.
* Keep `<head>` section in the following order:
  1. `<meta>` elements
  2. `<title>` element
  3. Style sheets
* Stick to proper semantics:
  * Don't use a `<div>` or `<span>` when a more meaningful element is available.
  * That said, it's an application, and there's not much call for `<article>`, `<blockquote>`, or `<>`.
* Avoid unnecessary nesting:
  * Don't add additional `<div>` wrappers just for the sake of adding a class. If you already have a `<ul>` or <`p`>, and the class  doesn't require a specific element, put the class on the `<ul`> or <`p`>.
* Scripts should generally be included at the end so they don't block loading of content or styles.
* Separation of concerns:
  * No inline styles.
  * No inline JavaScript/event handlers.
* Use ARIA roles and labels when appropriate:
  * (expand)
* Use HTML5 form control *types* when applicable (`url`, `email`…):
  * Triggers the appropriate keyboard on mobile 


