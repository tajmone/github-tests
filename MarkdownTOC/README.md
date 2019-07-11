# MarkdownTOC Tests

    MarkdownTOC v3.0.4

Testing configurations of Sublime Text [MarkdownTOC] package for edge cases on GitHub previews.


-----

**Table of Contents**

<!-- MarkdownTOC autolink="true" bracket="round" autoanchor="false" lowercase="only_ascii" uri_encoding="true" levels="1,2,3" -->

- [GitHub Configuration](#github-configuration)
- [Issues With Inline Code in Headings](#issues-with-inline-code-in-headings)

<!-- /MarkdownTOC -->

-----


# GitHub Configuration

These are the guidelines for setting up MarkdownTOC for GitHub previews:

- https://github.com/naokazuterada/MarkdownTOC#github-configuration

```json
{
  "defaults": {
    "autolink": true,
    "bracket": "round",
    "lowercase": "only_ascii"
  }
}
```

# Issues With Inline Code in Headings

Problem experienced with MarkdownTOC v3.0.4.
See [Issue #139] on MarkdownTOC repository for full details:

> The generated TOC doesn't cope well with special characters in the heading (backticks in this case, for inline code in headings).

Here I've created some test documents to try different settings combinations:


|    file    | autolink | bracket | autoanchor |  lowercase   | uri_encoding |  result |
|------------|----------|---------|------------|--------------|--------------|---------|
| [TEST1.md] | `true`   | `round` | `false`    | `only_ascii` | `true`       | *fails* |
| [TEST2.md] | `true`   | `round` | `false`    | `only_ascii` | `false`      | *fails* |

The problem is that MarkdownTOC is not handling properly the `%` in the heading: 

|    file    |        expected       |        generated         |
|------------|-----------------------|--------------------------|
| [TEST1.md] | `#the-code-directive` | `#the-%25code-directive` |
| [TEST2.md] | `#the-code-directive` | `#the-%code-directive`   |


[TEST1.md]: ./TEST1.md "View document"
[TEST2.md]: ./TEST2.md "View document"

<!-----------------------------------------------------------------------------
                               REFERENCE LINKS                                
------------------------------------------------------------------------------>

[MarkdownTOC]: https://github.com/naokazuterada/MarkdownTOC "Visit MarkdownTOC repository on GitHub"

[Issue #139]: https://github.com/naokazuterada/MarkdownTOC/issues/139

<!-- EOF -->