---
layout: doc
title: Ease
section: 1
subsection: 2
---

Another basic way to manipulate mods in the Mirin Template is the `ease` function.
This function takes a mod, and changes it from its current value to another value over a length of time smoothly.
The way it smoothly connects the values is specified with an [ease function](eases)
(for more information about eases please reference https://easings.net)

```lua
-- this will change drunk from 0% to 100% with a linear ease, the change will start at beat 0 and end 10 beats later
ease {0, 10, linear, 100, 'drunk'}

-- this will change tipsy from 0% to 200% with an outCubic ease, the change will start at beat 5 and end 15 beats later
ease {5, 15, outCubic, 200, 'tipsy'}
```

Certain ease functions don't have the same behavior as a majority of eases.
For example `pop` doesn't end at the value defined, instead it goes up to that value, before going back to where it started.

```lua
-- This will move tiny from 0 down to -100 and then back up to 0, starting at beat 0 over 1 beat.
ease {0, 1, pop, -100, 'tiny'}
```

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
