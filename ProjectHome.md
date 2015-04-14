# W3C DOM Ranges for IE #

**IERange is a feature-complete implementation of W3C [DOM Ranges](http://www.w3.org/TR/DOM-Level-2-Traversal-Range/ranges.html) for Internet Explorer, allowing users to write one cross-browser version of their range manipulation code.**

Internet Explorer 6–8 supports text ranges and document editing, but it does not support one of the more useful features when it comes to DOM manipulation, [DOM Ranges](http://www.w3.org/TR/DOM-Level-2-Traversal-Range/ranges.html). Internet Explorer has a native implementation of its own ["Text Ranges"](http://msdn.microsoft.com/en-us/library/ms535872.aspx), which operate solely on text content and is not compatible with the W3C version. Additionally, IE supports a `document.selection` object which is not compatible with other browsers' implementations. IERange emulates W3C ranges on top of the browser's native implementation.

## Test ##

You can try out IERange in the [sandbox](http://ierange.googlecode.com/svn/trunk/sandbox.html).

## Implementation Support ##

**Ranges:**
  * `document.createRange()`
  * `startContainer`, `startOffset`, `endContainer`, `endOffset`, `commonAncestorContainer`, `collapsed`
  * `setStart()`, `setEnd()`, `setStartBefore()`, `setStartAfter()`, `setEndBefore()`, `setEndAfter()`, `selectNode()`, `selectNodeContents()`, `collapse()`
  * `insertNode()`, `surroundContents()`
  * `extractContents()`, `cloneContents()`, `deleteContents()`
  * `compareBoundaryPoints()`, `cloneRange()`, `createContextualFragment()`, `toString()`

**Selection:**
  * Range support (Webkit-style)
  * `window.getSelection()`
  * `addRange()`, `removeAllRanges()`, `getRangeAt()`, `toString()`

**Not yet implemented:**
  * DOM Exception throwing
  * `detach()`
  * Live range support (Mozilla-style), `removeRange()`