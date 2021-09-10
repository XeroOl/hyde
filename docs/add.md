---
layout: doc
title: Add
section: 1
subsection: 3
---

The `add` function works like `ease`, except it is relative. The `add` function will add to the old value of the mod instead of overriding the old value of the mod with a new value.

So, for example, if a mod is currently at `200`, and an `add` runs with the value of `100`, the result would be `300`.


Here's an example that uses `add` with `rotationz`.
```lua
-- Adds 360 to rotationz.
add {1, 2, inExpo, 360, 'rotationz'}
-- Instead of staying at 360, add 360 again to get 720.
add {4, 2, inExpo, 360, 'rotationz'}
```
The `add` function also supports some other [extra parameters](players).
## Function Signature
```lua
add {beat, len, ease_fn, relative_percent, mod}
```
Arguments:

| -------------- | ---------- |
| `beat: number` | The song beat when the mod begins to apply. |
| `len: number` | The amount of beats before the ease is complete. |
| [`ease_fn: function`](eases) | The way to approach the target value. |
| `percent: number` | The amount to add to the mod. |
| `mod: string` | The mod to apply. |
