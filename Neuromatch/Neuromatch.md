---
file_name: Neuromatch
date: 2026-06-26
tags:
  - code
  - dev
  - computational-neuroscience
  - neuromorphic-computing
---
> [!quote] If you accept the expectations of others, especially negative ones, then you never will change the outcome.
> — Michael Jordan
`````````````col
````````````col-md
```dataviewjs
const filePath = "Work/Plugins/Music/Music.md";
const content = await dv.io.load(filePath);
const lines = content.split(/\r?\n/).filter(line => line.trim() !== "");

const rand = lines[Math.floor(Math.random() * lines.length)];

const winner = rand
dv.paragraph(`
<iframe style="border-radius:12px" src="https://open.spotify.com/embed/track/${winner}?utm_source=generator&theme=0" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
`);
```
````````````
````````````col-md
flowGrow=2
===
```dataviewjs
dv.el("div", `

<div style="position: relative; display: inline-block; overflow: hidden; max-width: 100%;">
  <img src="Work/Plugins/PNGs/Anexo/pngwing.com(7).png" style="width: 100%; max-width: 310px; transform: scaleX(-1); display: block;">
</div>

`);
```
````````````
`````````````
___

![[Work/Plugins/GIFs/pp.gif]]
```dataviewjs
dv.paragraph(`<div style="text-align: center; font-size:1em; color:#27e0a7; letter-spacing:0.09em; margin-top:4px;">
      <span style="color: #b0c5c4;">by ArelyXl ദ്ദി ˉ͈̀꒳ˉ͈́ )✧</span>
    </div>`);
```

___
![photo by Lex Melony(https://unsplash.com/@lexmelony?utm_source=templater_proxy&utm_medium=referral) on Unsplash](https://images.unsplash.com/photo-1629970815849-402b18449245?crop=entropy&cs=srgb&fm=jpg&ixid=M3w2NDU1OTF8MHwxfHJhbmRvbXx8fHx8fHx8fDE3ODI1MTYwMTl8&ixlib=rb-4.1.0&q=85)

[[pre-neuromatch]]
[[Model Types]]
[[Model Fitting]]
[[Generalized Linear Models]]