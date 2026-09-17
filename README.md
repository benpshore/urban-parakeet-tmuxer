# urban-parakeet-tmuxer
stubbed, tiny utility designed to implement a tmux bootstrap that automatically attaches or recreates a tmux multi window, multi host config with idempotent operation as part of a bootstrap makefile /justfile operation to prepare a dev machine or server for resumable work. 

the tmux session will be optimized for remote access over iOS, both in Shortcuts.app and Termius.app. 

starting point: one window that attaches iff no existing session named “gh” exists otherwise creates gh tmux session. 
```sh
tmux new-session -A -s main -n gh -c "$HOME/code/GitHub"
```

