# HTML Style Guide

_A guide to writing and maintaining good markup._


<!-- MarkdownTOC -->

- [Keep HTML structure as simple as possible.](#keep-html-structure-as-simple-as-possible)
- [Elements should be appropriately nested to maintain a sensible hierarchical document structure.](#elements-should-be-appropriately-nested-to-maintain-a-sensible-hierarchical-document-structure)
- [Stick to proper semantics.](#stick-to-proper-semantics)
- [Use 2 spaces for indentation.](#use-2-spaces-for-indentation)
- [Lowercase all element and attribute names.](#lowercase-all-element-and-attribute-names)
- [For "empty" elements, do not use XHTML-style closing syntax `` — just use ``.](#for-empty-elements-do-not-use-xhtml-style-closing-syntax--—-just-use-)
- [Don't omit closing tags.](#dont-omit-closing-tags)
- [Order of elements in the ``.](#order-of-elements-in-the-)
- [Include styles in the ``](#include-styles-in-the-)
- [Include scripts at the end of the ``](#include-scripts-at-the-end-of-the-)
- [Keep content, presentation, and behavior separate.](#keep-content-presentation-and-behavior-separate)
- [Use ARIA roles and labels when appropriate.](#use-aria-roles-and-labels-when-appropriate)
- [Use HTML5 form control *types* when applicable](#use-html5-form-control-types-when-applicable)

<!-- /MarkdownTOC -->




<a name="keep-html-structure-as-simple-as-possible"></a>
### Keep HTML structure as simple as possible.


<a name="elements-should-be-appropriately-nested-to-maintain-a-sensible-hierarchical-document-structure"></a>
### Elements should be appropriately nested to maintain a sensible hierarchical document structure.


<a name="stick-to-proper-semantics"></a>
### Stick to proper semantics.

* Don't use a `<div>` or `<span>` when a more meaningful element is available.
  * `<ul>` for lists
  * `<a>` for links
  * <input type="button"> or <button> for buttons
  * etc.
* Never add a `<div>` or `<span>` with no attributes.


<a name="use-2-spaces-for-indentation"></a>
### Use 2 spaces for indentation.

Set your editor to use spaces, not tabs.


<a name="lowercase-all-element-and-attribute-names"></a>
### Lowercase all element and attribute names.


<a name="for-empty-elements-do-not-use-xhtml-style-closing-syntax--—-just-use-"></a>
### For "empty" elements, do not use XHTML-style closing syntax `<br />` — just use `<br>`.


<a name="dont-omit-closing-tags"></a>
### Don't omit closing tags.

Although HTML5 allows omitting certain closing tags, like `</p>` and `</li>`, *Don't*.


<a name="order-of-elements-in-the-"></a>
### Order of elements in the `<head>`.

Keep `<head>` section in the following order:

1. `<meta>` elements
2. `<title>` element
3. Style sheets


<a name="include-styles-in-the-"></a>
### Include styles in the `<head>`

They should start loading & rendering as soon as possible.


<a name="include-scripts-at-the-end-of-the-"></a>
### Include scripts at the end of the `<body>`

Scripts should generally be included at the end so they don't block loading of content or styles.


<a name="keep-content-presentation-and-behavior-separate"></a>
### Keep content, presentation, and behavior separate.

* No inline styles.
* No inline JavaScript/event handlers.


<a name="use-aria-roles-and-labels-when-appropriate"></a>
### Use ARIA roles and labels when appropriate.

(Expand on this)


<a name="use-html5-form-control-types-when-applicable"></a>
### Use HTML5 form control *types* when applicable 

E.g., `url`, `email`, etc.

Doing this communicates semantics to user agents and assistive tech. For example, using `type="numeric"` might trigger the appropriate keyboard state on mobile.


