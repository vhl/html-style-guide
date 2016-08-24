# HTML Style Guide

_A guide to writing and maintaining good markup._


<!-- MarkdownTOC -->

- [Keep HTML structure as simple as possible.](#keep-html-structure-as-simple-as-possible)
- [Elements should be appropriately nested to maintain a sensible hierarchical document structure.](#elements-should-be-appropriately-nested-to-maintain-a-sensible-hierarchical-document-structure)
- [Stick to proper semantics.](#stick-to-proper-semantics)
- [Use 2 spaces for indentation.](#use-2-spaces-for-indentation)
- [Lowercase all element and attribute names.](#lowercase-all-element-and-attribute-names)
- [Use ID attributes sparingly.](#use-id-attributes-sparingly)
- [Don't omit closing tags.](#dont-omit-closing-tags)
- [Order of elements in the HEAD.](#order-of-elements-in-the-head)
- [Include styles in the HEAD](#include-styles-in-the-head)
- [Include scripts at the end of the BODY](#include-scripts-at-the-end-of-the-body)
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


<a name="use-id-attributes-sparingly"></a>
### Use ID attributes sparingly.

* NEVER use IDs as CSS selectors; it makes style overrides unnecessarily difficult.
* Don't use IDs for JavaScript hooks: use a "js-" prefixed classname instead.
* Don't use IDs for automated testing hooks: use a "test-" prefixed classname instead.
* DO use IDs to make associations between elements for accessibility purposes:
  * `<label for="ac-address-field">Address</label> <input type="text" id="ac-address-field">`
  * `<span id="ac-name-label">Name</span> <div class="some-widget" aria-labelledby="ac-name-label"></div>`
* Use the "ac-" prefix convention for accessibility-related IDs.


<a name="dont-omit-closing-tags"></a>
### Don't omit closing tags.

Although HTML5 allows omitting certain closing tags, like `</p>` and `</li>`, *Don't*.


<a name="order-of-elements-in-the-head"></a>
### Order of elements in the HEAD.

Keep `<head>` section in the following order:

1. `<meta>` elements
2. `<title>` element
3. Style sheets


<a name="include-styles-in-the-head"></a>
### Include styles in the HEAD

They should start loading & rendering as soon as possible.


<a name="include-scripts-at-the-end-of-the-body"></a>
### Include scripts at the end of the BODY

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


