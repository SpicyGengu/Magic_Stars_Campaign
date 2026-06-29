#Writers_Notes 
# Ship Stats
### Figure
- **Size:** How many squares the ship occupies.
- **AC:** Ships armor class. Used for calculating hits.
- **HP:** Ships maximum hit-points.
### Movement
- **Top Speed:** The speed at witch the ship can sail under perfect conditions (per round).
- **Steering (turns per round):** The amount of turns the sip is allowed to make per round.
### Range
- **Close Range:** The range at witch the cannons cannot miss. A d20 is still rolled in case of a critical failure or critical success, resulting in a 0.5x or 2x damage modifier respectively.
- **Medium Range:** The range at witch the shooting works much like a ranged attack.
- **Long Range:** Long range works like medium range but with disadvantage.
### Fire-power
Fire-power refers to the type of artillery the ship has.
### Ammo
The type of ammo a ship carries can vary from ship to ship.
# Initiative
The initiative is calculated by a perception contest between the two people who most likely spotted the other ship first.
# Roles
When the initiative is calculated, the players have to divide into one of 3 roles: [[Naval Combat#Pilot|Pilot]], [[Naval Combat#Cannoneers|Cannoneers]] or [[Naval Combat#Deck Runners|Deck Runners]].
## Pilot
Optimally there is only one pilot at any time. This is because the pilot has full control over the ships movement. Having two or more pilots will disadvantage the ships steering in the case of disagreement. 
### Pilot Actions
- **Steer**; Depending on the ships stats, the pilot can use the ships turns to turn the sips trajectory. The ship can only go straight unless turned. The ship can move forward in 8 directions on the board. Turning the ship only moves it one tile to the left or right.
- **Pivot**; Pivoting is a technique where the anchor is thrown overboard while the ship is still in motion. The ship moves up to it's size and it is allowed to use 4 turns while choosing direction. This Locks the ships movement to a radius of it's size. Un-anchoring requires 3 rounds to be spent by the [[Naval Combat#Deck Runners|Deck Runners]] retrieving the anchor. This number can vary depending on weather the [[Naval Combat#Cannoneers|Cannoneers]] also decide to help. Preforming this maneuver requires an intelligence check from the pilot, resulting in ship damage if failed.
- **Attach**; When the vessel is next to another vessel or land, the pilot can use a free action to connect to the object. This requires the [[Naval Combat#Cannoneers|Cannoneers]] and the [[Naval Combat#Deck Runners|Deck Runners]] to roll a dexterity check. If successful the two objects now share a speed, determined by the average with account to size. 
## Cannoneers
- **Fire!!!**; Firing the cannon requires the round to be spent solely on that. The cannons can only fire in a straight line. That means they can only hit where they point. This action can only be taken if the cannons are loaded.
- **Load**; Loading the cannons requires the round to be spent. While loading the cannons the Cannoneers also need to decide on the type of ammo to load.
- **Switch Post**; A cannoneer can only focus on one post at a time. Running over to the other side of the ship for example, requires the cannoneer to spend their turn on that.
## Deck Runners
- **Hoist/Unfurl The Sails**; This action changes the speed at witch the ship sails. More specifically the $S_\%$ variable can be changed.
- **Repair**; The deck runner has to make a crafting check in order to repair the ship. Usually this gives the ship 1d8 of heals with it being double for critical success and negative for critical failure.
- **Load**; Deck Runners, exactly like [[Naval Combat#Cannoneers|Cannoneers]], can load cannons. Loading the cannons requires the round to be spent. While loading the cannons the deck runners also need to decide on the type of ammo to load.
# Ship Speed Calculation
The way a ship moves in on a certain turn is in no way linear. The specific amount of tiles a ship moves forward in a direction is decided by the following equation:  
$$
Speed = \frac{T_s \cdot S_\% \cdot (5 - dp)}{5}
$$

| Variable |    Definition     | Domain  |
| :------: | :---------------: | :-----: |
|  $T_s$   |     Top Speed     | \[1, 5] |
|  $S_\%$  | Sails Percentile  | \[0, 1] |
|   $dp$   | Direction Penalty | \[0, 4] |
___The equation is rounded up to the nearest integer with a 0.5 being converted to 1.___
## Calculation Visualization
![[naval_visualize.jpeg]]

| Speed | Ts = 5 | Ts = 3 | Ts = 2 |
| :---: | :----: | :----: | :----: |
|   N   |   5    |   3    |   2    |
|  NE   |   4    |   2    |   1    |
|  NW   |   4    |   2    |   1    |
|   E   |   3    |   2    |   1    |
|   W   |   3    |   2    |   1    |
|  SE   |   2    |   1    |   1    |
|  SW   |   1    |   1    |   1    |
|   S   |   1    |   1    |   0    |
