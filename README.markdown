<h3>Description</h3>
This plugin will let you bind a custom (special) event to your document, namely 'textselect'.

What this does is triggering an event when text is selected in the document, and returning the selected text plus the nearest element containing all the text. What this means is that if a text selection spans over several elements, e.g. &lt;strong>, &lt;strike> etc, it'll select the parent, as that DOM element is containing all the text that has been selected.

Please note, as of now, it doesn't support multi text selections in Webkit/Firefox.

<h3>Usage</h3>
	$(document).bind('textselect', function (evt, string, element) {
		if (string != "") alert('Selected text (' + element.tagName + '): ' + string);
	});
