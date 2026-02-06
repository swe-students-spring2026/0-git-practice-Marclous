# Game Mechanic Development

## Engineering Focus: Celeste and TowerFall Physics
**By Maddy Thorson**

### Article link
https://maddythorson.medium.com/celeste-and-towerfall-physics-d24bd2ae0fc5

### The Code Behind the Game Feel
This is one of the most transparent looks at character controller logic ever published by a major indie studio. Thorson shares the actual C# code used to drive the character's movement.

I find this interesting because it solves the "floating point error" problem in a clever way. Instead of relying on standard physics engines (which can feel "floaty"), they use a custom **Integer-based Accumulator system**.


> "We can't move in fractions of pixels... we only move when the rounded remainder is non-zero. For each pixel we check ahead for obstructions, and if the coast is clear we move."

It completely demystifies how to create "tight" controls, showing how functions like `MoveX` and `Squish` manage collision detection pixel-by-pixel rather than relying on a black-box physics engine.

### Comments by Jack Escowitz
I really enjoyed this article because I love hearing about how Object Oriented Programming is applied to games where it is most apt. It is fascinating seeing how all in-game physics relies on two fundamental classes, `Solid`s and `Actor`s; it reminds me of my CS101 final project.

### Small change for updated username
### Small change for updated email
---
*Last updated: 2026*