---
layout: doc
title: Get
section: 5
subsection: 3
incomplete: true
---
```lua
get(modname)
get(modname, pn)
```
Gets the value most recently written to a mod.

Example:
```lua
for i = 1, 10 do
	ease {i, 1, outExpo, 100 - get('invert'), 'invert'}
end
```
