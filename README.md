# 🌀 A-Maze-ing Viewer

> A beautiful browser-based maze visualizer built for the **42 School `A-Maze-ing`** project.  
> Zero dependencies. Just open the HTML file in your browser.
🌐 [TEST](https://amazing.ahmadkailany.com/)  
---

## ✨ Features

| Feature | Description |
|---|---|
| 📂 **Load Maze** | Paste your maze file output directly — auto-parses grid, entry, exit & path |
| ✦ **Auto-Solve** | BFS shortest path animates your player dot step by step |
| 🎮 **Play Mode** | Navigate yourself with `WASD` or arrow keys |
| ✨ **Generation Replay** | Watch the DFS backtracker carve your maze from darkness |
| ⚠️ **3×3 Checker** | Detects forbidden 3×3 open blocks, highlights them in red on canvas |
| 🎨 **7 Themes** | Cyber, Pac-Man, Minecraft, Mouse & Cheese, Ocean, Dungeon, Retro CRT |
| 🌙 **Dark / Light** | Toggle in the header |

---

## 🗂️ Maze File Format

Your maze file should look like this:

```
BB955515395395395153
AAA953E9687AC3C6BAD2
A86A94569692BC156C3A
...

0,0
18,12
SSSSSSSEESSSwseennn...
```

- **Grid rows** — each character is one cell, hex encoded (`1 char = 4 wall bits`)
- **Blank line** separator
- **Entry** `x,y`
- **Exit** `x,y`
- **Path string** (optional) — `N/S/E/W` directions from your solver

### Wall Bit Encoding

```
bit 0 = North wall
bit 1 = East  wall
bit 2 = South wall
bit 3 = West  wall
```

Example: `0xB` = `1011` → North + East + West walls, South is open.

---

## 🎨 Themes

| Theme | Player | Entry | Exit | Special |
|---|---|---|---|---|
| 🔮 Cyber | Orange dot | Teal S | Red E | Neon glow walls |
| 👾 Pac-Man | Pac-Man mouth | 🟡 | 👻 | Dots in passages |
| ⛏️ Minecraft | 🧑 | 🚪 | 💎 | Pixel dirt blocks + grass |
| 🐭 Mouse & Cheese | 🐭 | 🐭 | 🧀 | Warm wooden style |
| 🌊 Deep Ocean | 🐠 | 🐠 | 🦞 | Bioluminescent path |
| 🔥 Dungeon | ⚔️ | 🗝️ | 🔥 | Lava orange glow |
| 💾 Retro CRT | Green dot | S | E | Scanlines effect |

---

## 🚀 Usage

```bash
# No install needed — just open in browser
open maze-visualizer.html
```

1. Paste your maze file in the left panel
2. Click **▶ Load Maze**
3. Use **Auto-Solve**, **Play Mode**, or **Replay Generation**
4. Switch themes in the bottom-left sidebar

---

## 🏫 About

Built as a debugging & visualization tool for the **42 School `so_long`** common core project.  
The `so_long` project requires building a 2D game with a maze, and this tool helps verify:
- ✅ The maze is solvable (BFS check)
- ✅ No forbidden 3×3 open cell regions exist
- ✅ Entry and exit are correctly placed

---

## 👤 Author

**Ahmad Kailany**  
42 Istanbul — Common Core

🌐 [ahmadkailany.com](https://ahmadkailany.com)  
🐙 [github.com/ahmadkailany](https://github.com/ahmadkailany)

---

<p align="center">Made with ❤️ by <a href="https://ahmadkailany.com">Ahmad Kailany</a></p>
