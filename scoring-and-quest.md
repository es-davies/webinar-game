## INSTRUCTIONS

Extend the existing game with scoring, quests, fair tile distribution,
and an endless expanding grid.

Do NOT change the hex grid geometry, tile design, or theme.

## TILE DISTRIBUTION:
- Tiles should feel random but evenly distributed — never purely Math.random()
- Use a "bag shuffle" system: fill a bag with a fixed set of tiles
  (e.g. 8 of each type), shuffle the bag, then deal from it one at a time
- When the bag is empty, refill and reshuffle automatically
- This guarantees the player sees all tile types roughly equally

## SCORING:
- Each placed tile scores 10 points base
- Bonus: +15 pts per adjacent hex that contains a matching tile type
- For adjacency use the correct flat-top hex neighbor offsets:
    Even columns: (+1,0),(-1,0),(0,-1),(0,+1),(+1,-1),(-1,-1)
    Odd columns:  (+1,0),(-1,0),(0,-1),(0,+1),(+1,+1),(-1,+1)
- Animate the score counting up when points are earned

## QUEST SYSTEM:
- Add a "CURRENT QUESTS" section in the sidebar showing 3 active quests
- Quest types:
    "Big [Tile 1]" — place N connected Tile 1s (target: 7)
    "Big [Tile 4]" — place N Tile 4s in a line (target: 8)
    "Big [Tile 3]" — place N Tile 3s grouped together (target: 8)
- Each quest card shows: name, progress (e.g. "2 / 8"),
  a progress bar, and reward (e.g. "+5 Tiles, +180 Pts")
- On quest completion: place a 🚩 flag on the grid at that location,
  flash the quest card gold, add bonus points, replace with a new quest

## CONTROLS:
- Undo button reverses the last tile placement (also undoes bag state and frontier)
