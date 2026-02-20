# dotfiles

Personal dotfiles managed by [chezmoi](https://www.chezmoi.io).

## Bootstrap a new machine

```sh
sh -c "$(curl -fsLS get.chezmoi.io)" -- init --apply rajagopal-parthasarathi
```

This installs chezmoi and applies all dotfiles in one step.

## Daily use

| Task | Command |
|------|---------|
| Pull and apply latest changes | `chezmoi update` |
| Edit a dotfile | `chezmoi edit ~/.gitconfig` |
| Preview pending changes | `chezmoi diff` |
| Apply changes | `chezmoi apply` |
| Add a new dotfile | `chezmoi add ~/.zshrc` |

## Files

| Source | Target | Purpose |
|--------|--------|---------|
| `dot_gitconfig` | `~/.gitconfig` | Git identity, SSH commit signing, delta pager |

## Prerequisites

- [delta](https://github.com/dandavison/delta) — git pager used in `.gitconfig`
- SSH key at `~/.ssh/id_hinge.pub` for commit signing
