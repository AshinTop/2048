# 2048

Made just for fun. [Play it here!](https://2048online.top/)

## 2048 Overview

2048 is a single-player puzzle game where players combine tiles with the same number to gradually achieve higher numbers, with the goal of reaching 2048. The gameplay is simple but challenging, requiring players to think about how to merge tiles efficiently while managing limited space to avoid a game over.

In this project, we will implement a web-based version of the 2048 game, allowing players to play through their browsers using keyboard controls.

### Features

1. **Game Board**: The game board is a 4x4 grid, where each position can hold a number (2, 4, 8, 16, 32, etc.).
2. **Tile Merging Rule**: Players slide tiles in four directions (up, down, left, right) to combine tiles with the same number. The merged tile's value will be doubled.
3. **New Tile Generation**: After each move, a new tile (either 2 or 4) will randomly appear in an empty space.
4. **Game Over**: The game ends when no valid moves are left. Players must avoid filling the board and having no tiles left to combine.
5. **Score**: Every time tiles are merged, the player earns points equal to the value of the newly formed tile.

### Game Rules

1. **Starting State**: The game starts with two tiles placed randomly on the board, each with a value of either 2 or 4.
2. **Controls**: Players control the tiles using the arrow keys (up, down, left, right).
3. **Merging Rule**:

- Tiles with the same number can only merge once.
- The merged tile will have a value equal to the sum of the two merged tiles.

4. **Tile Generation**: After each move, a new tile (2 or 4) will randomly appear in an empty space.
5. **Game Over**: The game ends when there are no valid moves left on the board.

## Project Overview

A small clone of [1024](https://play.google.com/store/apps/details?id=com.veewo.a1024), based on [Saming's 2048](http://saming.fr/p/2048/) (also a clone). 2048 was indirectly inspired by [Threes](https://asherv.com/threes/).

### Contributions

[Anna Harren](https://github.com/iirelu/) and [sigod](https://github.com/sigod) are maintainers for this repository.

Other notable contributors:

- [TimPetricola](https://github.com/TimPetricola) added best score storage
- [chrisprice](https://github.com/chrisprice) added custom code for swipe handling on mobile
- [marcingajda](https://github.com/marcingajda) made swipes work on Windows Phone
- [mgarciaisaia](https://github.com/mgarciaisaia) added support for Android 2.3

Many thanks to [rayhaanj](https://github.com/rayhaanj), [Mechazawa](https://github.com/Mechazawa), [grant](https://github.com/grant), [remram44](https://github.com/remram44) and [ghoullier](https://github.com/ghoullier) for the many other good contributions.

## Game Screenshot

<p align="center">
  <img src="https://cloud.githubusercontent.com/assets/1175750/8614312/280e5dc2-26f1-11e5-9f1f-5891c3ca8b26.png" alt="Screenshot"/>
</p>

## Contributing

Changes and improvements are more than welcome! Feel free to fork and open a pull request. Please make your changes in a specific branch and request to pull into `master`! If you can, please make sure the game fully works before sending the PR, as that will help speed up the process.

## License

2048 is licensed under the [MIT license.](./LICENSE.txt)
