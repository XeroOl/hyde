---
layout: doc
title: Set
section: 1
subsection: 1
---

The `set` function is the simplest function that the Mirin Template offers.
It allows the user to set a [mod](mods) to a value at a specific beat in the song.

```lua
-- This sets the speed mod to 1x at beat 0
set {0, 1, 'xmod'}

-- This will set the mod 'drunk' to 100 at beat 10
set {10, 100, 'drunk'}
```

After any mod is set to a value, it will stay at that value until the end of the song, or until another function modifies it.

```lua
-- Set the mod 'drunk' like the previous example
set {10, 100, 'drunk'}

-- Set drunk back to 0 at beat 20
set {20, 0, 'drunk'}
```

The `set` function, like many other Mirin Template functions, allows you to set multiple mods in the same function call.

```lua
-- Set the mods 'drunk' and 'tipsy' to 100 at beat 10
set {10, 100, 'drunk', 100, 'tispy'}
```
The `set` function also supports some other [extra parameters](players), which will be covered later.
---

## Function Signature
```lua
set {beat, percent, mod}
```

| -------------- | ---------- |
| `beat: number` | The song beat when the mod applies. |
| `percent: number` | The target amount to set the mod to. |
| `mod: string` | The mod to apply. |
