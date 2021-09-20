---
layout: doc
title: More Parameters
section: 1
subsection: 4
---

## `plr=`
`set`, `ease`, `add`, and `acc` all can take in an optional parameters called `plr`, which chooses the target players.
It can be passed in by adding `plr=` inside of the curly braces.

```lua
-- ease only player 1 to 100% invert
ease {0, 1, outExpo, 100, 'invert', plr = 1}
```

Without a `plr`, the ease will affect both players 1 and 2.

`plr` can also be set outside of the curly braces to affect more than one call.
```lua
-- Run a batch of eases using plr as a global, and reset plr when done.
plr = 1

-- The plr affect every call until it is set back to nil
ease {1, 2, outExpo, 100, 'reverse0'}
ease {2, 2, outExpo, 100, 'reverse1'}
ease {3, 2, outExpo, 100, 'reverse2'}
ease {4, 2, outExpo, 100, 'reverse3'}

-- Remember to clear the plr to stop it from affecting further calls
plr = nil
```

Multiple players can be specified by passing in a table to `plr` using curly braces. This is especially useful when using 3+ players.

```lua
-- use a table plr to specify multiple players at once
ease {10, 2, outExpo, 100, 'drunk', plr = {1, 3, 5}}
```

## `time=true`

`set`, `ease`, `add`, `acc`, and `func` can all take in an optional paramerer called `time`, which switches the function to "time based" mode, so the time will be interpreted in seconds instead of beats.

```lua
-- normal call, happens at BEAT 128
set {128, 50, 'flip'}

-- time=true call, happens at SECOND 128
set {128, 50, 'flip', time = true}
```

# Extra Players

### How to enable extra players
Although the game only goes up to 2 players, NotITG internally has 8 players. By default, these players are hidden, and in a special sleeping mode. To turn them on, run the `SetAwake` method, and pass in `true`. They can be disabled again with `SetAwake(false)`.

Example:
```lua
-- awaken P3
P3:SetAwake(true)
-- show P3
P3:hidden(0)
```

## How to set up extra player proxies
The provided default code in `lua/mods.xml` will set up every proxy in the `PP` table to proxy the players. To set up extra player proxies, just add more `PP` layers.
TODO add more info about player proxies.

