# SRE Editor Component
The editor component has the following props:

-   toolbarElements
-   iconSize
-   editorContent

The editor will by default take up the entire width of its parent container, this can be changed by setting the width of the “svelte-rich-editor” class globally or by changing the width of its parent.

**toolbarElements**:

Defines what elements are on the editor toolbar.

Options include all the struct apply options found here:

[[SRE Content Structure]]

If toolbarElements is not passed as a prop, will default to all available options.

Should be passed as an array

Ex/

```jsx
let toolbarElements = ["BOLD", "ITALICS", "UNDERLINE", "HEADING-1"];

<Editor toolbarElements={toolbarElements} />
```

**iconSize**:

Sets the size of the toolbar icons. Must be passed as a string. The default size is 16.

**editorContent**:

editorContent sets the content of the editor. By default it is empty, but by passing in an SRE Content Structure data, the editor can be populated.

**Toolbar Component**:

has props:

-   elements
-   iconSize

passed from the Editor component