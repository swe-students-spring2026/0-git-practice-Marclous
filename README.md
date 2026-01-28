# 🛠️ Game Mechanic Development

## Engineering Focus: [Celeste and TowerFall Physics](https://maddythorson.medium.com/celeste-and-towerfall-physics-d24bd2ae0fc5)
**By Maddy Thorson**

### The Code Behind the Game Feel
This is one of the most transparent looks at character controller logic ever published by a major indie studio. Thorson shares the actual C# code used to drive the character's movement.

I find this interesting because it solves the "floating point error" problem in a clever way. Instead of relying on standard physics engines (which can feel "floaty"), they use a custom **Integer-based Accumulator system**.


> "We can't move in fractions of pixels... we only move when the rounded remainder is non-zero. For each pixel we check ahead for obstructions, and if the coast is clear we move."

It completely demystifies how to create "tight" controls, showing how functions like `MoveX` and `Squish` manage collision detection pixel-by-pixel rather than relying on a black-box physics engine.

---
*Last updated: 2026*