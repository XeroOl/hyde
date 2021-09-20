---
layout: doc
title: Actors
section: 2
subsection: 1
incomplete: true
---
TODO move this to the chapter header
In NotITG, there is a concept called an Actor. Everything that can be drawn to the screen is an Actor. This section will discuss how to create Actors using XML syntax.

There are a couple of layers of abstraction to learn here. Let's start with XML.
In XML, a "tag" starts with a `<` symbol and ends with a `>` symbol. After the `<` is the tag's "name" of the tag, and then after that is a list of attributes that describe the tag.

Let's look at a simple example of XML.

```xml
<Layer Type="Quad"/>
<Layer Type="ActorProxy" Name="my_proxy"/>
<Layer Type="ActorProxy" Name="my_proxy2"/>
<Layer File="funny.png"/>
<Layer File="other.xml"/>
```
Each tag here represents one Actor object in the scene.
Notice that they all begin with "Layer". NotITG's XML syntax allows any name in this position, but the convention is to use "Layer" everywhere. This is because the game sorts the actors alphabetically to determine the order they are drawn, and it's easier to reason about the drawing order when the actors all have the same name.

The game draws actors from top to bottom in the file. So, in the example above, the Quad actor would be drawn first, then `my_proxy`, then `my_proxy2`, then `funny.png`, then `other.xml`. It's important to understand that something drawn later is drawn *on top of* something drawn earlier. So, in the example, the quad actor is in the back, and the `other.xml` is in the front.

Let's look at what types of actors there are:

## Quad


```xml
<Layer Type="Quad"/>
```

Here's the most basic actor you can have, a plain Quad with no commands or attributes. Quad stands for quadrilatiral, but it really just means a rectangle. Because nothing's done to it, it's going to be the default size of 1x1. It's not very useful without a name, so let's name it something.

```xml
<Layer Type="Quad" Name="foo"/>
```



[CraftedCart's Excellent Lua API Docs for NotITG](https://craftedcart.gitlab.io/notitg_docs/lua_api/index.html)
TODO
Basic:
Type="Quad"
Type="ActorProxy"
Type="Polygon"
Type="BitMapText"

TODO
File= types:
File="something.png"
File="something.xml"
File="something.avi"
File="something.txt"

TODO
Read more later
Type="Sprite"
Type="ActorFrameTexture"

TODO
The most important one:
Type="ActorFrame"


TODO
Then, the properties you can attach:

Key="value"
Type=
Name=
Var=
 Mirin Template Name= is better if you're using the Mirin Template
Condition=
 not used much
TODO
<>Command=
 types of commands
<>MessageCommand=
 Remember that commands are inside of the <> and the ""

TODO
Misc
FOV=
Frag=
Vert=
<children>



Methods:
TODO create next section for examples
Link to craftedcart

