# Tmux simple git status

Prints current pane git branch and uncommited changes (if avaialble).

![screenshot](https://i.imgur.com/yLXoTtK.png)

## Installation
### Installation with [Tmux Plugin Manager](https://github.com/tmux-plugins/tpm) (recommended)

Add plugin to the list of TPM plugins in `.tmux.conf`:

    set -g @plugin 'kristijanhusak/tmux-simple-git-status'

Add `#{simple_git_status}` to your `status-left` or `status-right` tmux option:

```
set -g status-left "#{simple_git_status}"
```

Hit `prefix + I` to fetch the plugin and source it.

### Manual Installation

Clone the repo:

    $ git clone https://github.com/kristijanhusak/tmux-simple-git-status ~/clone/path

Add this line to the bottom of `.tmux.conf`:

    run-shell ~/clone/path/simple_git_status.tmux

Add `#{simple_git_status}` to your `status-left` or `status-right` tmux option:

```
set -g status-left "#{simple_git_status}"
```

Reload TMUX environment:

    $ tmux source-file ~/.tmux.conf

