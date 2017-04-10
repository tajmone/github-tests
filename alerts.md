## GitHub Alerts in Raw HTML

This is an alert in Raw-HTML:

``` html
<div class="flash-messages">
<div class="flash ">
TEXT
</div>
</div>
```

... previewed as:

<div class="flash-messages">
<div class="flash ">
TEXT
</div>
</div>

FAILED! It looks like Primer-CSS's alerts can't be used directly in markdown via Raw-HTML and classes.

## GitHub Alerts in Raw HTML - Take 2

Now I'll test using a wrapper.

This is an alert in Raw-HTML:

``` html
<div class="container">
<div class="markdown-body">
<div class="flash-messages">
<div class="flash ">
TEXT
</div>
</div>
</div>
</div>
```

... previewed as:

<div class="container">
<div class="markdown-body">
<div class="flash-messages">
<div class="flash ">
TEXT
</div>
</div>
</div>
</div>

FAILED AGAIN! It looks like Primer-CSS's alerts aren't accessible from markdown previews.
