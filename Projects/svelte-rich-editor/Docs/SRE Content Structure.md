# SRE Content Structure
The content structure is a JSON structure where the editor data is saved. This structure can be easily converted into HTML and back.

The structure can be easily converted to/from HTML (at least for formatting options) by simply wrapping a tag around the given text (<strong>Bold text</strong>).

**Basic Example**:

_Text:_

> This is **BOLD**, and this is _italicized_.

_Structure:_

```json
{
	"content": [
		{
			"text": "This is "
		},
		{
			"text": "BOLD",
			"apply": ["BOLD"]
		},
		{
			"text": ", and this is "
		},
		{
			"text": "italicized.",
			"apply": ["ITALICS"]
		}
	]
}
```

**NOTE:** _This structure was inspired by quilljs Delta structure_

**Apply Options**:

-   BOLD
-   ITALIC
-   UNDERLINE
-   STRIKE
-   HEADING (1-4)
-   EMBED_LINK
-   ALIGN_(LEFT/CENTER/RIGHT)
-   EMBED_JS

**Embed Structure:**

If applying something like EMBED_LINK, the actual link must also be included.

EMBED_JS will place the “embed” value in the src of a script tag.

```json
{
	"text": "This is a link to my portfolio",
	"apply": ["EMBED_LINK"],
	"embed": "<https://josephtalon.ca>"
},
{
	"text": "This will show as a title/header above the JS embed",
	"apply": ["EMBED_JS"],
	"embed": "<https://gist.github.com/jostal/1d66e660d53a3c060f4fd5038ff22497.js>"
}
```

**NOTE:** EMBED_JS is intended for items like GitHub Gists, not actual logic running scripts