HT1

Author: Mironov Alexander

Game Overview:
HT1 is an obstacle-runner, where player needs
to run to the finish while avoiding traps and obstacles.
Player can enter a new map via reaching portal on the
other side of the current map.

Controls:
Movement - WASD
Jumping - Spacebar
You can freely move camera around your character

Feature set:

Third-person view
Ability to run in each direction and look around
Ability to jump and have limited control midair

Obstacles include barricades, spike traps, moving
spike traps, pitfalls, moving platforms, rotating pushing
traps, mazes

Player can pickup bonuses to help pass the level:
Ghost bonus - turns player invincible for 5 seconds
and let's him walk through walls
Time slow bonus - slows time for 1,25 seconds, excluding
player himself. Time slow strength is 0,25.

Level Generation:

I use a set of sublevels, created by hand. 
The game has 3 maps, first is easy, second is medium
and third is hard difficulty. Each map has it's own set of sub-levels,
that I randomise when player loads and fill the map with them.
Therefore player will encounter easy set of levels, then medium 
and last level will include the most complex maps. 
Randomized generation can create unique and challenging experience
for players.


Bonuses:
All bonuses are rotating actors, that destroy themselves
on contact with player. Once touched they activate events inside player's
blueprint, that corresponds to the bonus effect.
Bonuses originate from blueprint - BP_BonusSpawner.
It has a 25% chance to spawn a random bonus in the beginning
of the play.

Moving obstacles:
BP_DeathWall - a giant red wall, that starts moving when
player begins the level, it kills him on contact.

BP_MovablePlatform - an actor that goes back and forth between
it's origin and designated vector. Player can ride it.

BP_MovingSpike - an actor, consists of cube and a spike, contact
with spike kills player. The actor will move back and forth a few units
in the direction, that it is facing.

BP_Rotator - an actor which just rotates around itself,
can push player into undesirable position.

BP_RotatingPlatform - an actor which just rotates around itself.
Serves as a platform for the player and other obstacles, will rotate them too.
Has a boolean value which enables rotation and can be controlled via
collision box.


