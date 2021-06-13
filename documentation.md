---
layout: page
title: Documentation
children: doc
---
[Getting Started](getting-started)
<br>
Here is a reference for *most* of the available features in the Mirin Template.
<div style="display:flex">
<div style="flex:50%" markdown="1">
* [setdefault](docs/setdefault)
* [set](docs/set)
* [ease](docs/ease)
* [add](docs/ease#add)
* [func](docs/func)
* [function eases](docs/func#func_for_function_eases)
* [extra players](docs/players)
* [flip](docs/flip)
* [poptions](docs/func#poptions)
</div>
<div style="flex:50%" markdown="1">
* [definemod](docs/definemod)
* [aux](docs/doc-aux)
* [node](docs/aux#node)
* [reset](docs/reset)
* [alias](docs/alias)
* [get](docs/get)
* [list of mods](docs/mods)
* [list of ease functions](docs/eases)
</div>
</div>

Misc / todo:
* [aft](docs/aft)
* [actors](docs/actors)
* [Index](docs/globals) - in progress
* mode='end'
* shaders

Bonus:
* [Learn Lua](https://www.lua.org/manual/5.1/)
* [Gradients](docs/gradients)
* [Splines](docs/splines)

Example code:
```lua
-- turn on invert
ease {0, 1, outExpo, 100, 'invert'}
-- turn off invert
ease {7, 1, outExpo, 0, 'invert'}
```


Documentation by XeroOl, Chegg, Kirby5464
