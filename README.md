# HTML Style Guide

_A guide to writing and maintaining good markup._

Probably, as [@davexunit](https://github.com/davexunit) says, we should stop writing all this by hand and make it programmatic. 


<!-- MarkdownTOC -->

- [Keep HTML structure as simple as possible.](#keep-html-structure-as-simple-as-possible)
- [Structure markup to create meaningful hierarchical relationships.](#structure-markup-to-create-meaningful-hierarchical-relationships)
- [Stick to proper semantics.](#stick-to-proper-semantics)
- [Use 2 spaces for indentation.](#use-2-spaces-for-indentation)
- [Lowercase all element and attribute names.](#lowercase-all-element-and-attribute-names)
- [For "empty" elements, do not use XHTML-style closing syntax `` — just use ``.](#for-empty-elements-do-not-use-xhtml-style-closing-syntax--—-just-use-)
- [Don't omit closing tags.](#dont-omit-closing-tags)
- [Order of elements in the HEAD.](#order-of-elements-in-the-head)
- [Give your document a useful title.](#give-your-document-a-useful-title)
- [Include all stylesheet links in the HEAD.](#include-all-stylesheet-links-in-the-head)
- [Include scripts at the end of the BODY.](#include-scripts-at-the-end-of-the-body)
- [Keep content, presentation, and behavior separate.](#keep-content-presentation-and-behavior-separate)
- [Use ARIA roles and labels when appropriate.](#use-aria-roles-and-labels-when-appropriate)
- [Use HTML5 input types when applicable](#use-html5-input-types-when-applicable)

<!-- /MarkdownTOC -->




<a name="keep-html-structure-as-simple-as-possible"></a>
### Keep HTML structure as simple as possible.


<a name="structure-markup-to-create-meaningful-hierarchical-relationships"></a>
### Structure markup to create meaningful hierarchical relationships.

Ideally, if you view your document with all styles turned off, a page should resemble a sensible outline. Among other things, this is a foundation for good accessibility.


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

Although HTML5 allows omitting certain closing tags, like `</p>` and `</li>`, *DON'T*. It just makes your markup harder to comprehend.


<a name="order-of-elements-in-the-head"></a>
### Order of elements in the HEAD.

Keep `<head>` section in the following order:

1. `<meta>` elements
2. `<title>` element
3. Style sheet `<link>`s


<a name="give-your-document-a-useful-title"></a>
### Give your document a useful title.

<a name="include-all-stylesheet-links-in-the-head"></a>
### Include all stylesheet links in the HEAD.

They should start loading & rendering as soon as possible.


<a name="include-scripts-at-the-end-of-the-body"></a>
### Include scripts at the end of the BODY.

Scripts should generally be included at the end so they don't block loading of content or styles.


<a name="keep-content-presentation-and-behavior-separate"></a>
### Keep content, presentation, and behavior separate.

* No inline styles.
* No inline JavaScript or event handlers.


<a name="use-aria-roles-and-labels-when-appropriate"></a>
### Use ARIA roles and labels when appropriate.

If you must use a non-semantic element, add an [ARIA](http://www.w3.org/TR/wai-aria/ "Accessible Rich Internet Applications") role to give hints to user agents/assistive technology. [Link to ARIA Roles]

```html
  For an element that has click behavior attached, but isn't a sensible
  clickable element (not that you're EVER going to do this): 

  Bad: no semantics
  <span class="buttony">
    Grok
  </span>
  
  Good: Semantics via ARIA role
  <span class="buttony" role="button">
    Grok
  </span>

  Better: Use the right element in the first place
  <button class="buttony">
    Grok
  </button>
```


<a name="use-html5-input-types-when-applicable"></a>
### Use HTML5 input types when applicable 

E.g., `url`, `email`, etc.

[Full list of HTML5 input types](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#attr-type)

Doing this communicates semantics to user agents and assistive tech. For example, using `type="numeric"` might trigger the appropriate keyboard state on mobile.


