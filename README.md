# Tmmux Config
### tmux Terminology

- **Sessions**: The top-most layer in tmux, containing at least one window. Multiple sessions can be open, but only one can be attached at a time.
- **Windows**: Containers for one or more panes, similar to browser tabs. Each session shows its windows at the bottom of the screen, indicating the active window.
- **Panes**: Splits within a window, allowing multiple terminals in a single window. You can create panes by splitting windows horizontally or vertically. Only one pane is active at a time.

## Key Bindings

To execute tmux commands, use the prefix key (`Ctrl+b`) followed by the command key:

| Key | Description |
| --- | ----------- |
| `c` | Create a new window and set it as active |
| `n` | Move to the next window |
| `p` | Move to the previous window |
| `0-9` | Switch to window number |
| `:` | Enter a command (e.g., `swap-window`) |
| `&` | Kill the current window |
| `%` | Split the window vertically |
| `"` | Split the window horizontally |
| Arrow Keys | Switch panes directionally |
| `{`, `}` | Swap panes |
| `q` followed by `1` | Switch to pane 1 |
| `z` | Zoom into the current pane |
| `!` | Convert the current pane into a window |
| `x` | Close the current pane |
| `s` | List sessions |
| `w` | View a preview of windows and attach via `Enter` |
| `d` | Detach from session |

## Commands

### Creating and Managing Sessions

- **Create a New Session**: 
  - Without an active session: `tmux`
  - Naming a new session: `tmux new-session -s webserver`
  - In an active session: `:new`

- **List Sessions**: `tmux ls`

- **Attach to a Session**: `tmux attach -t webserver`

### Closing and Reopening Sessions

- **Detach from a Session**: Press `Ctrl+b` then `d`. This will detach your session but keep it running in the background, allowing you to reattach later.

- **Close a Session**: To close a session, you can detach from it and then close all windows and panes within the session. Alternatively, exit all shells in the session's windows and panes. To kill a session forcefully, use `tmux kill-session -t session-name`.

- **Open an Existing Named Session**: If you have previously created and named a session (and it is still running in the background), you can reattach to it using `tmux attach -t session-name` where `session-name` is the name you assigned to the session.

## Resources

- [Cheat Sheet](http://tmuxcheatsheet.com)

## Vim Tmux Navigator

This configuration allows using `Ctrl` + `h/j/k/l` for navigation between panes, enhancing workflow efficiency.

---

**Note**: Remember to double-check the cheat sheet link for accuracy. tmux
