# 2048 — Play the Classic Number Puzzle Online

**[Play 2048 on 2048 Online](https://2048online.top/)** · [Try 2048 Cupcakes](https://2048online.top/2048-CUPCAKES)

Slide numbered tiles across a 4 × 4 board, combine matching values, and work toward the **2048 tile**. This repository contains the lightweight HTML, CSS, and JavaScript game embedded on the 2048 Online homepage. It is a fork of [Gabriele Cirulli's 2048](https://github.com/gabrielecirulli/2048), not a new original game.

## How to play 2048

1. Start with two randomly placed tiles.
2. Use the **arrow keys** to slide the whole board up, right, down, or left. **WASD**, **HJKL**, and single-finger swipes are also supported by the input code.
3. Two equal tiles merge into one tile with twice the value: **2 + 2 → 4**, **4 + 4 → 8**, and so on. Each tile can merge only once during a move.
4. After a move that changes the board, a new 2 or 4 appears in an empty cell. A keypress that cannot move any tile does not add a tile.
5. Reach 2048 to win, then choose **Keep going** to continue. The game ends when there are no empty cells and no adjacent matching tiles.

Use **New Game**, **Try again**, or the **R** key to restart. Restarting replaces the current board.

## Features in this version

- A single-player 4 × 4 number-merging puzzle with animated tile movement.
- A score that increases by the value of each newly merged tile.
- A local best score and unfinished-game state, stored in the current browser when local storage is available.
- Keyboard controls and touch-swipe input.
- A **Keep going** option after reaching 2048.

There is no account-based cloud save or online leaderboard in this game code. Browser storage is specific to the site, browser, and device; clearing it can remove progress. When persistent storage is unavailable, the code uses an in-memory fallback.

## Practical strategy

Keep your largest tile near a corner and try to maintain an ordered row or column beside it. Leave room for incoming low-value tiles, and look at what a move will do to the entire board rather than only the next merge. These are useful habits, not a guarantee of winning: new tiles are random.

## Frequently asked questions

### Can I keep playing after 2048?
Yes. Choose **Keep going** on the win message to continue merging.

### Does every arrow-key press create a new tile?
No. A new tile appears only after a valid move changes the board.

### Is there an undo button?
No undo control is implemented in this version. Restart begins a new game rather than reversing a move.

### Where should I play?
Use the [2048 game page](https://2048online.top/). The site's internal `/game/2048/` path is the embedded game resource, not the main player-facing page.

## Run locally

This is a static browser game; no application build or backend service is required.

```bash
git clone https://github.com/AshinTop/2048.git
cd 2048
python3 -m http.server 8080
```

Open `http://localhost:8080/`. Keep `index.html`, `js/`, `style/`, and the referenced image assets together when serving the game.

### Source layout

- `index.html`: board markup, score display, and controls.
- `js/game_manager.js`: movement, merging, scoring, win and game-over rules.
- `js/keyboard_input_manager.js`: keyboard and swipe controls.
- `js/local_storage_manager.js`: local best score and saved board.
- `style/`: visual presentation and styles.

## 中文简介

[在线玩经典 2048](https://2048online.top/)：在 4 × 4 棋盘上滑动数字，相同数字相遇合并，目标是得到 2048。可使用方向键、WASD 或触屏滑动；有效移动后才生成新方块。达到目标后可以继续游戏，最高分和未结束棋局在浏览器允许时保存在本机。本版本没有撤销按钮或跨设备云存档。

想换一种视觉风格，可尝试[纸杯蛋糕版 2048](https://2048online.top/2048-CUPCAKES)。

## Project Overview

A small clone of [1024](https://play.google.com/store/apps/details?id=com.veewo.a1024), based on [Saming's 2048](http://saming.fr/p/2048/) (also a clone). 2048 was indirectly inspired by [Threes](https://asherv.com/threes/).

### Upstream contributors

[Anna Harren](https://github.com/iirelu/) and [sigod](https://github.com/sigod) are credited as maintainers in the upstream project documentation.

Other notable contributors:

- [TimPetricola](https://github.com/TimPetricola) added best score storage
- [chrisprice](https://github.com/chrisprice) added custom code for swipe handling on mobile
- [marcingajda](https://github.com/marcingajda) made swipes work on Windows Phone
- [mgarciaisaia](https://github.com/mgarciaisaia) added support for Android 2.3

Many thanks to [rayhaanj](https://github.com/rayhaanj), [Mechazawa](https://github.com/Mechazawa), [grant](https://github.com/grant), [remram44](https://github.com/remram44) and [ghoullier](https://github.com/ghoullier) for the many other good contributions.

## Game Screenshot

<p align="center">
  <img src="https://cloud.githubusercontent.com/assets/1175750/8614312/280e5dc2-26f1-11e5-9f1f-5891c3ca8b26.png" alt="Classic 2048 number tiles on a 4 by 4 puzzle grid"/>
</p>

## Contributing

Changes and improvements are more than welcome! Feel free to fork and open a pull request. Please make your changes in a specific branch and request to pull into `master`! If you can, please make sure the game fully works before sending the PR, as that will help speed up the process.

## License

2048 is licensed under the [MIT license.](./LICENSE.txt)
