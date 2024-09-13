Date: 2024-07-30
Hub: [[linux]]
Tags: #book
URL/Title: Learning Modern Linux

Three main components:
- Sessions: Logical unit which is basically a working environment dedicated to a task or a divider like session for work and session for personal use
- Windows: Same as a tab in a browser, optional a lot of people simply use one window per session
- Panes: A single instance of a shell running, and can be split vertically or horizontally like a window in vscode or in neovim
Tmux refernce commands:
```
Table 3-4. tmux reference
Target Task Command
Session Create new :new -s NAME
Session Rename trigger + $
Session List all trigger + s
Session Close trigger
Window Create new trigger + c
Window Rename trigger + ,
Window Switch to trigger + 1 … 9
Window List all trigger + w
Window Close trigger + &
Pane Split horizontal trigger + "
Pane Split vertical trigger + %
Pane Toggle trigger + z
Pane Close trigger + x
```

