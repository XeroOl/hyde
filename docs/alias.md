---
layout: doc
title: 5.4 - Alias
section: 5
incomplete: true
---
```lua
alias {'oldmodname', 'newmodname'}
```
The `alias` function tells the game to replace all occurances of modstring `oldmodname` with `newmodname`. It affects anywhere that modstrings are used, including `ease`, `set`, `add`, `definemod`, and anywhere else mod names are used. The game will internally use the second provided name.

Arguments:

| -------------- | ---------- |
| `oldmodname: string` | The name of the mod to rename. |
| `newmodname: string` | The new name of the mod. |

Example:
```lua
alias {'confusionzoffset', 'confusionoffset'}
```
