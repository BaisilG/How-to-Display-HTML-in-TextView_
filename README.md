# How-to-Display-HTML-in-TextView_

You need to use Html.fromHtml() to use HTML in your XML Strings. Simply referencing a String with HTML in your layout XML will not work.

This is what you should do:

if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.N) {
    textView.setText(Html.fromHtml("<h2>Title</h2><br><p>Description here</p>", Html.FROM_HTML_MODE_COMPACT));
} else { 
    textView.setText(Html.fromHtml("<h2>Title</h2><br><p>Description here</p>"));
}
