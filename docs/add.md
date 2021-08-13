---
layout: doc
title: Add
section: 1
subsection: 3
incomplete: true
---

```lua
add {beat, len, ease_fn, relative_percent, mod}
```
The `add` function works like `ease`, except it is relative. The `add` function will add to the old value of the mod instead of overriding the old value of the mod with a new value. So, for example, if a mod is currently at `200`, and an `add` runs with the value of `100`, the result would be `300`.

Arguments:

| -------------- | ---------- |
| `beat: number` | The song beat when the mod begins to apply. |
| `len: number` | The amount of beats before the ease is complete. |
| [`ease_fn: function`](eases) | The way to approach the target value. |
| `percent: number` | The amount to add to the mod. |
| `mod: string` | The mod to apply. |

Example:
```lua
add {1, 2, inExpo, 360, 'rotationz'}
```

`add` can also be [player specific](players).
