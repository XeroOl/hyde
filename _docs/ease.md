---
layout: doc
title: Ease
section: 1
subsection: 2
---

Another basic way to manipulate mods is the `ease` function.
This function takes a mod, and changes it from its current value to another value over a length of time smoothly.
The user can specify an [ease function](eases) to choose the transition used to change the mod.

For more information about eases please reference [https://easings.net](https://easings.net).

```lua
-- This will change drunk from 0% to 100% with a linear ease
-- The change will start at beat 0 and end 10 beats later
ease {0, 10, linear, 100, 'drunk'}

-- This will change tipsy from 0% to 200% with an outCubic ease
-- The change will start at beat 5 and end 15 beats later
ease {5, 15, outCubic, 200, 'tipsy'}
```

Some ease functions won't end on the target value, and will instead return to the original percent.
These are called "transient" eases.
For example, `pop` is a transient ease. Because of this, in the example code below, `tiny` will temporarily go to `-100`, but then return to `0`.

```lua
-- This will move tiny from 0 down to -100, and then back up to 0.
-- It goes back up to 0 because pop is a "transient" ease
ease {0, 1, pop, -100, 'tiny'}
```

The `ease` function also supports some other [extra parameters](players).

---
## Function Signature

```lua
ease {beat, len, ease_fn, percent, mod}
```

Arguments:

| -------------- | ---------- |
| `beat: number` | The song beat when the mod begins to apply. |
| `len: number` | The amount of beats before the ease is complete. |
| [`ease_fn: function`](eases) | The way to approach the target value. |
| `percent: number` | The target amount to set the mod to. |
| `mod: string` | The mod to apply. |
