gnome-terminal-new-tab-in-existing-window
=========================================

Anything else to explain besides the name?

```bash
gnome-terminal-new-tab-in-existing-window [any additional options here]
```

This flimsy wrapper behaves like `gnome-terminal --tab ...`, but opens a new tab in the
existing window if possible. Options are passed on directly to `gnome-terminal`.

In fact, it only sets two environment variables, `GNOME_TERMINAL_SERVICE` and
`GNOME_TERMINAL_SCREEN`.

## Dependencies

* `busctl`
  * Get current bus name and screen ID of `gnome-terminal`
* `xdotool`
  * Activate the existing window after a new tab opened
