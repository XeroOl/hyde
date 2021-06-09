---
layout: default
title: Home
---
# Mirin Template
[NotITG](https://notitg.heysora.net) is a fork of OpenITG that is designed for creating and playing mod files.

[The Mirin Template](https://www.github.com/XeroOl/notitg-mirin) provides tools to allow mod file creators to implement their ideas.

Join the [NotITG Discord](https://uksrt.heysora.net/discord) to learn more about NotITG.

The Mirin Template is designed to make easing as simple as possible, while remaining incredibly powerful.


## Documentation:
[Index](docs/index) - in progress
<br>
Choosing a template
<br>
[Getting Started](Getting Started)
<br>
<div style="display:flex">
<div style="flex:50%" markdown="1">
* [How to set up the template](Getting Started)
* [setdefault](docs/setdefault)
* [set](docs/set)
* [ease](docs/ease)
* [add](docs/ease#add)
* for loop
* [actors](docs/actors)
* [definemod](docs/definemod)
* [reset](docs/reset)
* [aux](docs/doc-aux)
* [node](docs/aux#node)
* [alias](docs/alias)
</div>
<div style="flex:50%" markdown="1">
* [extra players](docs/players)
* mode='end'
* [flip](docs/flip)
* [get](docs/get)
* [func](docs/func)
* [function eases](docs/func#func_for_function_eases)
* [poptions](docs/func#poptions)
* [aft](docs/aft)
* shaders
* [list of mods](docs/mods)
* [list of ease functions](docs/eases)
</div>
</div>
Bonus:
* [learn Lua](https://www.lua.org/manual/5.1/)
* [gradients](docs/gradients)
* [splines](docs/splines)

Example code:
```lua
-- turn on invert
ease {0, 1, outExpo, 100, 'invert'}
-- turn off invert
ease {7, 1, outExpo, 0, 'invert'}
```


Documentation by XeroOl, Chegg, Kirby5464