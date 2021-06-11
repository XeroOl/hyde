---
layout: page
title: Documentation
children: doc
---

[Index](docs/globals) - in progress
<br>
Choosing a template
<br>
[Getting Started](getting-started)
<br>
<div style="display:flex">
<div style="flex:50%" markdown="1">
* [How to set up the template](getting-started)
* [setdefault](docs/setdefault)
* [set](docs/set)
* [ease](docs/ease)
* [add](docs/ease#add)
* [actors](docs/actors)
* [definemod](docs/definemod)
* [reset](docs/reset)
* [aux](docs/doc-aux)
* [node](docs/aux#node)
* [alias](docs/alias)
</div>
<div style="flex:50%" markdown="1">
* [extra players](docs/players)
* [flip](docs/flip)
* [get](docs/get)
* [func](docs/func)
* [function eases](docs/func#func_for_function_eases)
* [poptions](docs/func#poptions)
* [list of mods](docs/mods)
* [list of ease functions](docs/eases)
</div>
</div>
* for loop
* mode='end'
* shaders
* [aft](docs/aft)
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
