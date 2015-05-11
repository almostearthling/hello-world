# Minimap not showing code on some tabs

The minimap does not render code in some of the tabs that were not on foreground on Atom startup.

![Minimap Behaviour](https://raw.githubusercontent.com/almostearthling/hello-world/master/images/bug_minimap.gif)

When the window is resized, or the minimap settings are tinkered with, the minimap shows again. Also, if the code can be scrolled, scrolling it causes the minimap to rendere correctly.

## Repro Steps

1. At startup, click the code tabs
2. Some of them, other than the one that was initially focused, don't show the minimap

**Expected:** Minimap showing correctly
**Actual:** Code not shown, sometimes a small dot is highlighted on the upper right corner of the minimap

## Command History

```
     -0:12.2 editor:detached (atom-text-editor.editor)
     -0:12.2 editor:will-be-removed (atom-text-editor.editor)
     -0:12.2 pane:item-removed (atom-pane.pane.active)
     -0:12.2 editor:detached (atom-text-editor.editor)
     -0:12.2 editor:will-be-removed (atom-text-editor.editor)
     -0:12.2 uri-opened (atom-workspace.workspace.scrollbars-visible-always.theme-flatland-dark.theme-seti-ui)
     -0:09.0 pane-container:active-pane-item-changed (atom-pane-container.panes)
     -0:09.0 pane:active-item-changed (atom-pane.pane.active)
     -0:05.9 pane-container:active-pane-item-changed (atom-pane-container.panes)
     -0:05.9 pane:active-item-changed (atom-pane.pane.active)
     -0:00.0 bug-report:open (ul.list-inline.tab-bar.inset-panel)
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
