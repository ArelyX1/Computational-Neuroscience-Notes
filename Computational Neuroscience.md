---
file_name: Computational Neuroscience
date: 2026-11-04
tags:
end_date:
---

``````````````col-md
```dataviewjs
const gifUrl = "https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExdTdnaXk3YXEyd3Bub3o0aGoycXk4NzlrbXNudnMxNWQ0cDR1Mmg4ciZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/fmkYSBlJt3XjNF6p9c/giphy.gif";

const box = document.createElement('div');
const variacion = -200;

// box.style.borderRadius = '20px';
box.style.overflow = 'hidden';
box.style.boxShadow = '0 4px 18px rgba(0,0,0,0.18)';
box.style.background = `url('${gifUrl}') center center no-repeat`;
box.style.backgroundSize = 'cover';

const img = new Image();
img.src = gifUrl;

img.onload = () => {
  box.style.width = img.width+220 + 'px';
  box.style.height = img.height-400 + 'px';
  dv.paragraph(box.outerHTML);
};

// En caso de error cargando el GIF, asigna un tamaño por defecto
img.onerror = () => {
  box.style.width = '200px';
  box.style.height = '200px';
  dv.paragraph(box.outerHTML);
};

```
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
  <img src="Work/Plugins/PNGs/Anexo/pngwing.com(2).png" style="width: 100%; max-width: 310px; transform: scaleX(-1); display: block;">
</div>

`);
```
````````````
`````````````
``````````````

``````col
flexGrow=2;
===
```dataviewjs
dv.paragraph(`![[momone.gif]]`);
```

`````col-md
```dataviewjs
const startDateLuxon = dv.current().date;
const startFormatted = startDateLuxon.toFormat("dd LLLL yyyy");
const endDate = dv.current().end_date;

if (!endDate) {
  dv.paragraph("⚠️ Error: falta definir `end_date` en el frontmatter.");
  throw new Error("end_date no definido");
}

const endDateLuxon = DateTime.fromISO(endDate);
const endFormatted = endDateLuxon.toFormat("dd LLL yyyy");
dv.el("div", `
  <div style="position:relative; display:inline-block;">
    <img src="title(1).png" style="width:320px;">
    <div style="
      position:absolute;
      top:85px;
      left:1px;
      padding:12px 16px;
      border-radius:8px;
      font-size:0.8em;
      font-family:'Segoe UI',sans-serif;
      line-height:1.5;
      box-shadow:0 2px 17px rgba(0,0,0,0.25);
      z-index:10;
      min-width:150px;
      letter-spacing: 0.01em;     
      z-index:2;    
	      --jpop-pink: #FFAFDE;    
	      --jpop-blue: #8DE9FF;    
	      --hacker-green: #69FFA8;
		transform: rotate(-6deg);
    ">
      <div style="font-size:2.05em; 
      font-weight:600; 
      letter-spacing:0.033em; 
      color:var(--jpop-pink); 
      margin-bottom:10px; 
      text-shadow: 0 0 8px #f3c5f5;">
	      Limit time
      </div>     
      <div style="margin-bottom:6px; color:var(--hacker-green); 
	      font-weight:bold; font-size:1em; 
	      text-shadow: 0 0 3px #51e9b7;">      
	      ꜱᴛᴀʀᴛ: <span style="color:var(--jpop-blue); 
	      font-weight:800;">${startFormatted}</span>    
      </div>    
      <div style="margin-bottom:6px; color:var(--jpop-blue); 
	      font-weight:bold;">      
	      🅴🅽🅳: <span style="color:var(--hacker-green); 
	      font-weight:800;">${endFormatted}</span>    
      </div>    
      <div style="font-size:1.4em; 
	      color:#F0FCFF; 
	      letter-spacing:0.3em; 
	      text-shadow: 0 0 7px var(--jpop-pink);">(•̆ꈊ•̆ )(•̆ꈊ•̆ )</div>  
      </div>
    </div>
  </div>
`);
```
`````
``````

```dataviewjs
const { DateTime } = dv.luxon;

// 🎉 GIFs
const nyanCatUrl = "mexinyancat.gif"; // Archivo local o en carpeta .obsidian/snippets
const gifFilled = "https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExbDVsY2J2bzlqYWg3YzI2djRuaG16NzVpa2x3NHJjYnM0NmF5cHRlOCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/URZcG7uLd9h4s/giphy.gif";
const gifEmpty = "https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExOWQ3dnJmdGphcjIzZW9tcnF2ZzR6cGhmbzYyYWpud3lrOTZybmpoYyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/KidI5b7H1WrgnPCIEC/giphy.gif";

// 📅 Fechas desde el Frontmatter
const startDate = dv.current().date;
const endDate = dv.current().end_date;

if (!startDate || !endDate) {
  dv.paragraph("⚠️ Error: falta definir `date` o `end_date` en el frontmatter.");
  throw new Error("Falta start o end date.");
}

// ✅ Convertir fechas
const startDateLuxon = DateTime.fromISO(startDate);
const endDateLuxon = DateTime.fromISO(endDate);
const now = DateTime.now(); // 🎯 Se usa para saber la fecha actual del sistema

// 📈 Cálculos
const totalDuration = endDateLuxon.diff(startDateLuxon, "days").days;
const elapsedDuration = now.diff(startDateLuxon, "days").days;
const clampedElapsed = Math.max(Math.min(elapsedDuration, totalDuration), 0);
const progress = clampedElapsed / totalDuration;
const percent = (progress * 100).toFixed(2);

// 🖼 Barra de progreso visual con GIFs
const bar = `
<div style="display: flex; align-items: center; gap:1em; font-family: 'JetBrains Mono', monospace;">
  <img src="${nyanCatUrl}" 
       style="height:64px; margin-bottom:71px; transform: scaleX(-1); border-radius:12px;">
  <div style="flex:1;">
    <div style="height: 30px; border-radius: 15px; overflow: hidden; position: relative; box-shadow: 0 2px 10px rgba(0,0,0,0.15); background: none;">
      <div style="
        width: 100%;
        height: 100%;
        background: url('${gifEmpty}') repeat-x;
        background-size: cover;
        position: absolute;
        top: 0; left: 0; right: 0; bottom: 0;
        z-index: 1;
        border-radius: 15px;
        opacity: 0.5;">
      </div>
      <div style="
        width: ${percent}%;
        height: 100%;
        background: url('${gifFilled}') repeat-x;
        background-size: 180px 30px;
        position: absolute;
        top: 0; left: 0; bottom: 0;
        z-index: 2;
        border-radius: 15px 0 0 15px;
        transition: width 0.8s cubic-bezier(.6,-0.28,.74,.05);">
      </div>
    </div>
    <div style="font-size:1em; color:#27e0a7; letter-spacing:0.09em; margin-top:4px;">
      ${percent}% <span style="color: #b0c5c4;">COMPLETED (${clampedElapsed} / ${Math.round(totalDuration)} días)</span>
    </div>
  </div>
</div>
`;

dv.paragraph(bar);

```

```````col
``````col-md
```dataviewjs
let root = dv.current().file.folder;
const rootLen = root.length + (root ? 1 : 0);
if (root === "") root = "/";

// Encontrar solo subcarpetas directas
const folders = app.vault.getAllLoadedFiles()
  .filter(f => f.children)
  .map(f => f.path)
  .filter(path =>
    path.startsWith(root + (root ? "/" : "")) &&
    path !== root &&
    path.slice(rootLen).indexOf("/") === -1
  )
  .map(path => {
    const parts = path.split("/");
    return {
      folderName: parts.at(-1)
    };
  }).filter(item => item.name !== "Anexo")
  .sort((a, b) => a.folderName.localeCompare(b.folderName));

// Generar HTML terminal-style
let html = `
<div style="
  box-shadow: 0 0 16px #39ff1488, 0 2px 12px #0f0;
  color: #87ff73; 
  font-family: 'JetBrains Mono', 'IBM Plex Mono', 'Fira Mono', 'Courier New', monospace;
  max-width: 480px;
  margin: 16px 0;
  padding: 0.6em 0 0.6em 0;
  ">
  <div style="
    border-bottom: 2px solid #39ff14; 
    letter-spacing: 0.04em;
    font-size: 1rem; 
    padding: 0.5em 1.1em; 
    background: #060;">
    ╔═══════════════ SYSTEM MODULE SCAN ═══════════════╗<br>
    ║  Root: <span style='color:#39ff14;font-weight:bold'>${root}</span>
    <span style='float:right;'>${(new Date()).toLocaleString()}</span>║<br>
    ╚══════════════════════════════════════════════════╝
  </div>
  <div>
    <ul style="margin:0.8em 0 0 0; padding: 0 1.5em;">
      ${
        folders.length
          ? folders.map((f, i) => 
            `<li style="
              list-style:none;
              margin-bottom: .15em;
              padding: .15em .5em;
              border-left: 2px solid #39ff14;
              background: linear-gradient(90deg, #181 50%, transparent 100%);
              color: #b5ffb0;
              font-size: 1.02em;
              transition: background 0.2s, color 0.2s;
              cursor:pointer;
            " 
            onmouseover="this.style.background='#22ff9b22';this.style.color='#fff';"
            onmouseout="this.style.background='linear-gradient(90deg, #181 50%, transparent 100%)';this.style.color='#b5ffb0';"
            >[${String(i + 1).padStart(2, '0')}] ${f.folderName}</li>`
          ).join('\n')
          : `<li style="color:#ff8484">[ERROR 404: NOT FOUND]</li>`
      }
    </ul>
  </div>
</div>
`;

// Render HTML
dv.paragraph(html);
```
``````
``````col-md
```dataviewjs
const gifUrl = "https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExcnM5MTI2Y2Jrd3A3d2YyOHo5aG5tdm83cXo3amsyeWZseWZ1MnMxciZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/a2l0ZKRaaBsaJaSUu6/giphy.gif";

const box = document.createElement('div');
const variacion = -160;

// box.style.borderRadius = '20px';
box.style.overflow = 'hidden';
box.style.boxShadow = '0 4px 18px rgba(0,0,0,0.18)';
box.style.background = `url('${gifUrl}') center center no-repeat`;
box.style.backgroundSize = 'cover';

const img = new Image();
img.src = gifUrl;

img.onload = () => {
  box.style.width = img.width+variacion + 'px';
  box.style.height = img.height+variacion + 'px';
  dv.paragraph(box.outerHTML);
};

// En caso de error cargando el GIF, asigna un tamaño por defecto
img.onerror = () => {
  box.style.width = '200px';
  box.style.height = '200px';
  dv.paragraph(box.outerHTML);
};


```
``````
```````


![[Work/Plugins/GIFs/pp.gif]]

```dataviewjs
dv.paragraph(`<div style="text-align: center; font-size:1em; color:#27e0a7; letter-spacing:0.09em; margin-top:4px;">
      <span style="color: #b0c5c4;">by ArelyXl ദ്ദി ˉ͈̀꒳ˉ͈́ )✧</span>
    </div>`);
```


`[MOD-01]` [[Computational Neuroscience|Computational Neuroscience.md]]
`[MOD-02]` [[Work/Neuroscience-Computing-Notes/LICENSE|LICENSE]]
`[MOD-03]` [[Neuromatch|Neuromatch]]
`[MOD-04]` [[Work/Computational Neuroscience Notes/Phychophysics|Phychophysics.md]]
`[MOD-05]` [[Work/Neuroscience-Computing-Notes/PythonNotes/PythonNotes|PythonNotes]]
`[MOD-06]` [[README|README.md]]


