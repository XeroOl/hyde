---
layout: doc
title: Ease Tricks
section: 1
subsection: 5
---

There are some ways to get finer control over the available ease functions.

## Flipped Eases

The function `flip` takes in an ease, and produces a flipped version of that ease function.

```lua
--- Use a flipped ease function
ease {0, 1, flip(outExpo), 100, 'invert'}
```

This will instantly jump up to `100` invert, and then follow an `outExpo` curve back down to `0`.

## Ease Parameters

Some eases can accept a number of parameters that affect the shape of the curve. Parameters can be passed in by calling the `.params` field of the ease.

```lua
ease {0, 1, outElasic.params(1, 1), 100, 'invert'}
```

Check the [eases](docs/eases) page to see which eases take in parameters, and how many parameters there are.
