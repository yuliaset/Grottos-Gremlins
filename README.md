# Grottos-Gremlins

Play Area: 16x16 grid

Obstacles and Entities:

- Walls: Three wall segments, each five cells long, are randomly placed on the board. Placement is carefully validated so that a new wall segment does not touch existing walls (even diagonally).

- Trees: Ten trees are also placed randomly on the grid, serving as obstacles that block movement.

- Enemies: The game uses an “enemy deck” of 40 cards (comprising 8 copies of each of five enemy types: Goblin, Wraith, Troll, Imp, and Serpent). At the start of each level, five enemy cards are drawn and placed on the board. Each enemy type has its own hit point (HP) value and is denoted by a rune (e.g., “G” for Goblin)

Once all enemies have been cleared from a level (or if the enemy deck runs low), the grid and obstacles are reset, and a new set of enemies is drawn from the deck. The game ends if fewer than five enemy cards remain.

Classes:

- Warrior:

Base Damage: 6

Allowed Moves:
A short-range move set (similar to adjacent cell movements) consisting of diagonal moves upward (up-left, up-center, up-right), horizontal moves (left and right), and one downward move. This limited movement pattern makes the Warrior more of a front-line fighter with higher damage output.

- Mage:

Base Damage: 3

Allowed Moves:
Uses the same basic move set as the Warrior—moving diagonally upward, side-to-side, and downwards. The Mage typically relies on ranged or magical attacks (as suggested by the skill) despite having a similar movement limitation as the Warrior.

- Cleric:

Base Damage: 4

Allowed Moves:
Identical to the Warrior and Mage in terms of movement. The Cleric’s focus might be on support or healing (typically found in role-playing games), though in this implementation it functions similarly to a melee fighter with a unique skill name.

- Rogue:

Base Damage: 2

Allowed Moves:
The Rogue moves like a knight in chess, using the classic “L-shape” moves: (2, 1), (1, 2) and their symmetric opposites. This movement pattern allows the Rogue to jump over obstacles and perform “horse moves” both when moving and attacking. The AI logic for Rogues includes specialized pathfinding that leverages these moves.

- Assassin:

Base Damage: 0.5

Allowed Moves:
The Assassin enjoys movement similar to a chess rook—any number of cells vertically or horizontally. The available moves are precomputed by iterating through possible displacements along the x- or y-axis (excluding the zero vector). This grants the Assassin long-range mobility along straight lines, ideal for striking targets from a distance.

- Bomber:

Base Damage: 0.5

Allowed Moves:
The Bomber can move within a confined square region defined as a 4×4 block (from –2 to +1 in both x and y directions, excluding staying in place). This unique move set suggests an area-control style where the Bomber might be used to deliver explosive effects over a clustered area, although in the given code the skill itself is only named and not deeply programmed.

- Paladin:

Base Damage: 0.5

Allowed Moves:
The Paladin combines the long-range diagonal movement of a bishop with the ability to make single-step moves in the cardinal directions (up, down, left, right). Essentially, it moves like a “promoted bishop” in shogi, making it versatile in both long-distance diagonal engagements and short-range tactical repositioning.

- Dragon:

Base Damage: 4

Allowed Moves:
The Dragon is limited to one-cell moves in any of the eight directions (including diagonals). This classic omnidirectional movement reflects the notion of a dragon slowly advancing but possibly with powerful, area-of-effect “breath” attacks (as indicated by its skill).

