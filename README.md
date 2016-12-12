# github-tests
A repo for testing GitHub functionality and services.

This paragraph has a hard-line break right here:
And this is a newline line.

## Github Flavoured Markdown Cheat Sheet

Writing text without any specific symbol(s) and/or syntax(es) will be wrapped into `<p>`.

How have I done that `inline code highlighting`?

```
Writing text without any specific symbol(s) and/or syntax(es) will be wrapped into `<p>`.

How have I done that `inline code highlighting`?
```
---

# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6

How?

```
# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```
Remember `<h1>` and `<h2>` gets `border-bottom` automatically.

And all the headings are assigned with `unique-id`.

Alternate syntax for `<h1>` and `<h2>`:

```
Heading 1
=========
Heading 2
---------
```
<hr />

> Blockquote ? Yes it is.

How?

```
> Blockquote ? Yes it is.
```
<hr />

~~Strikethrough~~

How?

```
~~Strikethrough~~
```
<hr />

* Hi
* How 
* Are 
* You?

How?

```
* Hi
* How 
* Are 
* You?
or 
* Hi
+ How
- Are
* You?
```

**What about ordered list?**

1. One (Hi)
2. Two (How)
3. Three (Are)
4. Four (You)

How?

```
1. One (Hi)
2. Two (How)
3. Three (Are)
4. Four (You)
```

**Sub lists**

1. Getting started
  + Download
  + Install
2. Make a dummy file

How?

```
1. Getting started
  + Download
  + Install
2. Make a dummy file
```

or

1. Getting started
  1. Download
  2. Install
2. Make a dummy file

```
1. Getting started
  1. Download
  2. Install
2. Make a dummy file
```


**Complex**

1. Level 1
  1. Level 2
    + Level 3
      - Level 4
        * Level 5

How ?

```
1. Level 1
  1. Level 2
    + Level 3
      - Level 4
        * Level 5
```

<hr />

*`em` tag*

How?

```
*`em` tag*  OR
_`em` tag_
```

**`strong` tag**

How?

```
**`strong` tag** OR
__`strong` tag__
```

Noticed? Just written inline-code in `em` and `strong` tag.

If you want to produce __\*__ and **\_** then add `\` before `_` and `*`. So `\*` = \* and `\_` = \_

<hr />

**Image:**

![alt text](http://lorempixel.com/100/100/ "title here")

How?

```
![alt text](http://lorempixel.com/100/100/ "title here")
```

Another way:


`![alt text][id]`  
`[id]: http://lorempixel.com/100/100/ "title here"`  

<hr />

**Link:**

[Github](http://github.com "title here")

How?

```
[Github](http://github.com "title here")
```

Another way:


`[github][id2]`  
`[id2]: http://github.com "title here"`

<hr />

**Automatic Links? (Yeah)**

http://github.com

How? just paste with the full url means with `http://` or `https://`. e.g. `http://github.com`.

<hr />

You can also use HTML tags.

<table>
  <tr>
    <th> Number </th>
    <th> Name </th>
  </tr>
  <tr>
    <td> 1 </td>
    <td> Kaushalya </td>
  </tr>
</table>

Yes, Table with HTML tags.

<hr />

**Code Highlighting**

**HTML**

```html
<body>
  <div class="loader"></div>
  <div class="pause">Click To Pause</div>
</body>
```

<hr />

**SCSS**

```scss

$width: 7em;
$height: 3em;
$c-0: #34495e;
$c-1: lighten(#e74c3c,5%);
$c-2: lighten(#e67e22,5%);
$c-3: lighten(#f1c40f,5%); 

label[for="checkbox"] {
  font-size: 2em;
  position: absolute;
  margin-top: 0.2em;
  text-transform: capitalize;
  color: $c-0;
  transition: all 0.5s ease-in-out;
}

input[type="checkbox"] {
  appearance: none;
  width: $width;
  height: $height;
  background: lighten($c-0,25%);
  border-radius: $width / 2;
  position: relative;
  overflow: hidden;
  outline: none;
  transition: all 0.5s ease-in-out;
  
  &:before {
    width: $width / 2;
    height: $height;
    content: '';
    position: absolute;
    background: linear-gradient( lighten($c-1,17%), lighten($c-2,17%), lighten($c-3,17%) );
    transition: all 0.5s ease-in-out;
  }
  &:checked {
    &:before {
      margin: 0 $width / 2;
    }
  
    background: lighten($c-0,35%);
    opacity: 0;
  
    ~label[for="checkbox"] {
      &:before {
        transition: 0.5s all ease-in-out;
        content: '';
        position: absolute;
        height: 0.5em;
        width: 1em;
        margin: -0.1em -2.0em;
        box-shadow:
          0.3em -0.1em 0 $c-0,
          0.3em -0.2em 0 $c-0,
          0.3em -0.1em 0 $c-0;
        background: transparent;
        transform: rotate(120deg);
      }
    }
  }
}
```

<hr />

**CSS**

```css
@import url(http://fonts.googleapis.com/css?family=Source+Code+Pro);

body {
  background: #eee;
}
.logo {
  -webkit-animation-play-state: running !important;
  animation-play-state: running !important;
  font: bolder 4em 'Source Code Pro', sans-serif;
  letter-spacing: -0.12em;
  color: #ddd;
  animation: shadow 2s linear infinite;
  text-shadow: 1px 1px 3px grey, 2px 2px 4px lightgrey, 3px 3px 5px #aaa, 4px 4px 6px #aaa, 5px 5px 6px #bbb, 6px 6px 7px #ccc, 7px 7px 8px #ddd, 8px 8px 9px #eee;
}
@keyframes shadow {
  to {
    text-shadow: 8px 8px 9px #eee, 7px 7px 8px #ddd, 6px 6px 7px #ccc, 5px 5px 6px #bbb, 4px 4px 6px #aaa, 3px 3px 5px #aaa, 2px 2px 4px lightgrey, 1px 1px 3px grey;
    color: grey;
  }
}

```

**How to highlight code?**

- You can highlight code with **4 spaces** or with **```(language-name(optional))**.

**Highlight without any language syntax**

```
" ```
  <-- code here -->
  ``` "
```
  
  - This will just wrap `code` in `pre` tag.
  - Ignore `"` because It's not showing alone, So I've to use it.

**Highlight with any language syntax**
  
```html
" ```html
  <-- code here -->
  ``` "
```
  
  - I've written `html` because I want to highlight `html code`. 
  - You can use other languages, For example: `scss`, `sass`, `python`, `ruby`, `javascript`, `jade`, `less`, `php` etc.
  - Ignore `"` because It's not showing alone, So I've to use it.

---


Horizontal Line? `<hr />`

---

How?

```
This, 
--- 
or this,
<hr />
```

Break Line? `<br />`

How?

- Either write two space after a sentence or Write next line after hitting `Enter` (Hit `Enter` one time if you're in the next line of the previous line or Hit two times `Enter` if you are on the line in which after you want line break.)

---

**Resources \- [Github Help on GFM] (https://help.github.com/articles/github-flavored-markdown "Help From Github on GFM"), [CSSDeck Docs] (http://cssdeck.com/labs/learning-the-markdown-syntax "Markdown Help")**


**Thanks,**  
<strong> \- By [Kaushalya Mandaliya][link_to_twitter] | http://seebeetee.com </strong>

[link_to_twitter]: https://twitter.com/kmandalwala "Kaushalya on Twitter"
[official_md_docs]: http://daringfireball.net/projects/markdown/ "Markdown Docs"

*Remember: This is <strong>Github Flavoured Markdown,</strong> [Official Markdown Docs][official_md_docs].*
