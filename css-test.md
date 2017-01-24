# GH Stylesheet Test

Testing GitHub stylesheet (Primercss.io) in Markdown via classes.

## Alerts

Testing use of alerts within markdown doc. Should display a boxed content, like the one found here:

- http://primercss.io/alerts/

Test source:

```html
<div class="flash-messages">
  <div class="flash">
    Flash message goes here.
  </div>
</div>
```
renders to:
---------------
<div class="flash-messages">
  <div class="flash">
    Flash message goes here.
  </div>
</div>
----------------

**TEST FAILED**: Styling didn't work.

The problem is due to GitHub's HTML sanitation. Classes are being stripped from raw divs.

The final HTML output in document preview is:

```html
<div>
  <div>
    Flash message goes here.
  </div>
</div>
```
