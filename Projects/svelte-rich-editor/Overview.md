# Overview

svelte-rich-editor will allow a dev to implement a rich text editor based on given settings. For example, they can specify they want Bold, italics, headings 1 and 2, and JS embed but no other features and that is all they will get.

The editor will work by saving the contents in a special format indicating what text needs what effects. This format can then be converted into HTML so it can be easily displayed outside the editor.