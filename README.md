 Swappable is a jQuery plugin enables a group of DOM elements to be swappable. Click on and drag an element to a new spot within the list; drag element and drop one will swap and the other items will not affected. By default, swappable items share sortable properties.

DETAILS

Similar to "Sortable", but only two elements of the selected group are affected: dragged and dropped which are swapped. All other elements stay at their current positions. This plugin is built based on existing "Sortable" jQuery plugin and inherits all sortable options except "cursorAt" and "items" ones (explained below)

Depends:

    jquery.ui.core.js
    jquery.ui.mouse.js
    jquery.ui.widget.js
    jquery.ui.sortable.js

To add the feature to a group of elements:
Minimal configuration:
<pre>
$("#swappable").swappable({
   items: '.itemClass',
   cursorAt: {top:-10}
});
</pre>

Option's specific:

    Always set option "cursorAt: {top: -nn} " as a negative Integer.

    Always set option "items" with items' class name, not element or filter.

Example:
<pre>
&lt;ul id="foo"&gt;
   &ltli class="bar"&gt;&lt;li&gt;
   &ltli class="bar"&gt;&lt;li&gt;
   &ltli class="bar"&gt;&lt;li&gt;
&lt/ul&gt;

$("#foo").swappable({
   items:'.bar', // Mandatory option, class only.
   cursorAt: {top:-20}, // MUST be set to negative. Default doesn't work!
});
</pre>

Add this statement (optional) to disable unwilling text selection
$("#swappable").disableSelection();