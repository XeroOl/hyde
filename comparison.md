---
layout: hidden
title: Choosing a Template
---
## Mod Beginners
When you're starting out with modding, it's important to use a template. Templates allow you to easily apply mods to the players, and schedule different things to happen at different times throughout the song. Any template will have the basic features you need to get started. I recommend choosing a template quickly to get started modding faster, instead of procrastinating by comparing templates forever. Just choose anything, and get started!

However, if you're still interested in vague comparison that doesn't go into details, I'll put it this way:

The mirin template is high level compared to exschwasion template. I don't mean high-level as in more complex, or better than exsch. I'm talking in terms of abstraction. With the exschwasion template, you'll learn to become familiar with things like activation rates, apply modifiers, and the behavior of clearall. You'll be able to read the template code to figure out how the code you write gets transformed into the mods that are actually applied to the game. You'll be working with code closer to the interface that notitg provides to apply mods. However, in the mirin template, there's a non-trivial layer of abstraction on top of notitg's interface. On one hand, this makes it easier to express complex concepts using the mirin template without worrying about lower level concepts like sustain times and activation rates and mod strings. However, on the other hand, because it introduces a layer of abstraction, it's not as easy to get a strong mental model of what's actually going on in the template. Also, the creator of the mirin template (me) has learned enough computer science to be dangerous, and the source code of the mirin template is definitely pretty dangerous. If you were to edit the mirin template, there are a bunch of concepts that you won't have learned just by using the mirin template, and it's relatively opaque. Meanwhile, the exsch template and others are usually much more straightforward in implementation, which makes it easy to learn more. Although, when you're using the mirin template, I don't recommend actually looking at the source. It's much easier to ignore, because it's in a whole separate folder, instead of being in the template with a whole don't touch this kiddo block, which makes it be really confusing.

## Migrating from other Templates
The main difference between the excsh and mirin template is the way that eases work. In the exsch template, eases are kind of like level 2 of modding, where level 1 is mod strings. But in the mirin template, eases are level 1. Eases are simpler to comprehend in mirin because it requires way fewer arguments. You only need to provide the end percent, and the start percent is inferred. That's because the mirin template will remember what value you've eased to last, and then start the next ease from the right percent automatically. Basically, the main point is that I've made eases as simple as possible, so that you can use only eases instead of mixing modstrings and eases. Firstly, this makes it simpler to use the template. You'll never be like "I kind of want this to be eased, but I'm too lazy to do it" ever again. Secondly, because it's using eases everywhere, there's a bunch of stuff that becomes possible that wouldn't be possible in the exsch template. Basically, poptions/nodes/overlapping eases/the reset function/get/default values/etc. is built off of the idea that eases are the core building block used to describe how mods change over time.

As a computer science person, I've put a lot of thought into every decision I've made in the mirin template. If something is done weirdly, you can probably ask me why it's done that way, and I'd give you like a 10 hour rant about comparing and contrasting multiple different options, and the pros and cons, and why I decided to make whatever decision I made.

I tried to prioritize ease of use over writing simple code, which is why stuff like Name= and `node` has a complicated implementation but simple usage.
The exschwasion template takes the other approach, where sustain times are implemented simply, but kind of painful to use in practice.

however, it's really clear to understand how the exsch code works. In the mirin template, the abstractions mean that you can't actually use lower level things very easily.

so you can't manually touch activation rates, raw modstrings, and sustain times. Another thing to mention, completely off topic from the other stuff, is performance.

The mirin template isn't the *best* at performance, but I've spent a lot of effort keeping the big O low. This means that you can insert hundreds of thousands of eases with relatively little issue. Other templates are sometimes bad at handling this sort of thing. GAT2 iirc had to split its tables up because of how bad the performance is when you have a bunch of eases. The mirin template shouldn't run into issues like this.

