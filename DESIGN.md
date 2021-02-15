# Ironrift
A sci-fi first/third-person battlefield-style shooter.  

## Premise
_Ironrift_ is to be set in a galaxy governed by an advanced predominant race of being (name TBD). The governing species is known for subtle oppressive rule and corruption. Most other races residing in the galaxy are very much against the current governance. Many systems have joined an alliance in rebellion towards the galactic government.  

With advanced technology at everyone's disposal, combat is executed using autonomous constructs utilizing advanced AI. The player takes the roll of a commanding artificial consciousness that is sent on various missions and commands various battles. Consciousness' are placed in units temporarily until a new one is needed. For the purposes of the MVP, the player will only be partaking in standard large-scale battles with a singular opposing force.

Gameplay is very similar to Star Wars: Battlefront I/II (Classic), with ideally much more realism and freedom.

## Features and Goals
### MMVP (Mostly Minimum Viable Product)
- Simple menu to start a match
- Selection of at least 1 map
- Map loading/decoration population
- Map-based physics (use map mesh as surface)
- Basic player controls
- At least 1 spawn point for each team
- Unit (including player) spawning
- Respawning
- At least 1 weapon that fires (obviously)
- Necessary controls
- Health
- Unit model (different color for each side?)
- Simple sounds
- Simple win objective (destroy all enemies)
- Functional on 3 major operating systems

### Ideal Objectives
- More than 1 unit type
- ^ Multiple weapons?
- Separate unit models for each side
- Selection of 2 or more maps/planets
- Multiple spawn points
- Radar
- Swap with existing unit on respawn
- Pre-battle planning (unit groups, locations)
- Bases (capturable/destroyable)
- A few more objectives (capture, hunt, etc)
- Basic vehicle(s)

### Future Ideas
- Choose a place to battle on a given planet
- Dynamically loaded maps (load any part of planet)
- "Open world"esque
- Location-dependent features (e.g. sensor array -> radar)
- Lead other units
- Customizable units (visual only?)
- Story mode
- Weather and time of day
- Multiplayer

## Structure
_Ironrift_ is built using [Rust](https://www.rust-lang.org/) and the [Bevy game engine](https://github.com/bevyengine/bevy/).  

_"Why Rust?"_ - Mostly because it has been recommended to me numerous times and I'd like to avoid C-langs. On top of that, safety makes my life easier in the long run. I also might want to package the game closed-source, which means a compiled language is a must.  

_"Why Bevy?"_ - While it may be relatively young, it is growing quickly, has a strong community, is simple, and cross-platform. Also, I wasn't a huge fan of Amethyst.  

### Future in Mind
_Ironrift_ must be developed with future possibilities in mind. Keeping hard-coding to a minimum allows features to be added easier later.  

### Modular
Every piece of _Ironrift_ must be designed in a "plug-n-play" manner to keep maintenance headache to a minimum. Being able to swap out modules is also useful for updating/upgrading behaviors and logic.  

### Abstraction
The visuals and logic should be as independent as possible. In an ideal world a headless version of the game can run on a server. Keeping the two separate makes debugging each part simpler.  

### Aspect-Oriented
Rust and Bevy by nature encourage aspect-oriented design which is very useful for applications managing a lot of objects. In the case of large-scale battles handling NPC logic in an aspect-oriented manner can be much simpler in implementation and be more efficient. Many parts of _Ironrift_ will still be object-oriented, however.  
