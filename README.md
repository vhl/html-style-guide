# HTML Style Guide

_A guide to writing and maintaining good markup._


<!-- MarkdownTOC -->

- [Keep HTML structure as simple as possible.](#keep-html-structure-as-simple-as-possible)
- [Elements should be appropriately nested to maintain a sensible hierarchical document structure.](#elements-should-be-appropriately-nested-to-maintain-a-sensible-hierarchical-document-structure)
- [Stick to proper semantics.](#stick-to-proper-semantics)
- [Use 2 spaces for indentation.](#use-2-spaces-for-indentation)
- [Lowercase all element and attribute names.](#lowercase-all-element-and-attribute-names)
- [Use a slash in self closing tags.](#use-a-slash-in-self-closing-tags)
- [Don't omit closing tags.](#dont-omit-closing-tags)
- [Order of elements in the ``.](#order-of-elements-in-the-)
- [Include styles in the ``](#include-styles-in-the-)
- [Include scripts at the end of the ``](#include-scripts-at-the-end-of-the-)
- [Keep content, presentation, and behavior separate.](#keep-content-presentation-and-behavior-separate)
- [Use ARIA roles and labels when appropriate.](#use-aria-roles-and-labels-when-appropriate)
- [Use HTML5 form control *types* when applicable](#use-html5-form-control-types-when-applicable)
- [Links, Buttons, & Anchors](#links-buttons-anchors)

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


<a name="use-a-slash-in-self-closing-tags"></a>
### Use a slash in self-closing tags.

For "empty" elements, do use XHTML-style closing syntax `<br />` — just use `<br>`.


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

<a name="links-buttons-anchors"></a>
### Links, Buttons & Anchors
#### Links
```
<a href="www.google.com">Search Google</a>
```

Use this style of anchor tag to create links to other pages.

If using a link anchor tag as a placeholder (`<a href="#">Not a real link</a>`), then be sure to add `ev.preventDefault()` to your JS click event heandler. Alternatively, use `href="#0"` to prevent the default link action. `#0` works because ids cannot start with a number. Otherwise, the page will jump to the top every time a user clicks your placeholder.

Note: This is *NOT* the same thing as `<link rel="">`.

#### Buttons
```
<button type="submit">Text</button>
<button type="button">Text</button>

<input type="submit">Text</input>
<input type="button>Text</input>
```

A `button` is by default a *submit* button, and will trigger the action of a form if it's inside one. Add `type="button"` to make it a non-submit button.

The advantage of `<button>` is that you can put other elements inside it, whereas you can only use plain text labels for `<input>`-style buttons.

#### Anchors
```
<a name="#some-text">Text</a>
```

Anchors are great for jumping to information farther down a page. 

#### Buttons vs.Links vs. Anchors
##### The semantic question of link vs button:
 * A button invokes an action: Save, Cancel, Exterminate.
  * Activated with the `Space` or `Enter` key. Screen reader users may assume this is a form submission and be slightly more trepidacious about activating it than a link.
  * Identified in screen readers as a button, and included in the list of form controls.
 * A link takes you somewhere (navigates).
  * Activated with the `Enter` key.
  * Identified in screen readers as a link, and included in the list of page links.

##### Considerations when choosing an element:
 * If you style a link to look like a button, a keyboard user will not know to use the `Enter` key to click on it.
 * `<input>` elements belong inside a `<form>`.

##### There _are_ ambiguous cases:
* One common pattern is to present the primary action as a button and the secondary action as a link (e.g., Save button and Cancel link). 
* If the button/link is meant to reveal hidden information, such as an info modal, use `<a href="#0">Show Me Stuff!</a>`.

As with everything, it's not simply a matter of style -- the semantics are important, and have real consequences for keyboard and screen reader users.

##### Further reading:
- [The Difference Between Anchors, Inputs, and Buttons](https://davidwalsh.name/html5-buttons)
- [When to Use the Button Element](https://css-tricks.com/use-button-element/)
