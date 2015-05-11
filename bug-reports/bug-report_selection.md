# Selecting a line from the gutter causes the view to scroll

When a line is selected from the gutter near enough to the end of the view, the view unwantedly scrolls up some lines.

![Gutter line selection and scroll](https://raw.githubusercontent.com/almostearthling/hello-world/master/images/bug_lineselect.gif)

This also happens when the line is selected in the upper part of the view, when the user selects either the first or the second visible line. This behaviour can lead to multiline selection in some cases and when the user modifies the text in a destructive way (e.g. deletion or replacement) it can lead to errors.

## Repro Steps

1. Open a file that does not fit in the view
2. Select the first or last fully visible line by clicking on the line number

**Expected:** The line is selected and the view does not scroll
**Actual:** The view scrolls up or down respectively when selecting the last line or the first line

## Command History

```
     -0:21.0 editor:detached (atom-text-editor.editor)
     -0:21.0 editor:will-be-removed (atom-text-editor.editor)
     -0:06.5 cursor:moved (atom-text-editor.editor.is-focused)
     -0:06.5 selection:changed (atom-text-editor.editor.is-focused)
     -0:05.8 cursor:moved (atom-text-editor.editor.is-focused)
     -0:05.8 selection:changed (atom-text-editor.editor.is-focused)
     -0:05.1 cursor:moved (atom-text-editor.editor.is-focused)
     -0:05.1 selection:changed (atom-text-editor.editor.is-focused)
     -0:04.5 cursor:moved (atom-text-editor.editor.is-focused)
     -0:04.5 selection:changed (atom-text-editor.editor.is-focused)
     -0:00.0 bug-report:open (atom-text-editor.editor.is-focused)
```

## Versions

* **Atom:**       0.198.0
* **Atom-Shell:** 0.22.3
* **OS:**         linux 3.13.0-52-generic
* **Misc**
    * apm  0.166.0
    * npm  2.5.1
    * node 0.10.35
    * python 2.7.6
    * git 1.9.1

---

<small>This report was created in and posted from the Atom editor using the package `bug-report` v0.7.0.</small>
