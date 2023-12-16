# GasPlusDocumentation

# What is GAS Plus (Gameplay Ability System Plus)
GAS Plus is an extension of the popular Gameplay Ability System created by Epic Games.
It was developed with the intention to make professional Multiplayer experiences available even to smalller/newer developers.
While it primarily aims at creating competitive multiplayer games such as FPS games (e.g. Counter Strike, Call of Duty), MOBA games (e.g. League of Legends, Dota 2) or RPGs (Dark Souls, The Witcher, Genshin Impact),
it can be used in any type of game, as well as singleplayer games.

# Features
 - Character Death and Respawn
 - Projectiles with lag compensation
 - Stun, Root, Slow, etc... functionality
 - Network predicted Movement speed changes (Sprint, Walk, etc...)
 - Gamemplay UI and working Scoreboard (Kills, Deaths, etc...)
 - Input Bindings for Gameplay Abilities
 - Ability Queue for Gameplay Abilities
 - Options Menu (Resolution, Quality, etc...)
 - Fully Blueprint compatible

# How to setup



# Spawning Projectiles
GasPlus makes using projectiles easy. Simply create a child of the class GASPProjectile and spawn it within a Gameplay Ability using the SpawnProjectile node.
For projectile class you now select the projectile you created. When the Gameplay Ability executes the SpawnProjectile node, the projectile will be spawned for all players.

Class: The class of the projectile to spawn. Must be a child of the class GASPProjectile that comes with the plugin.

SpawnMethod: Choose how you want to spawn the projectile. There are 2 options you can choose:
  1. FixedStartingLocationRotation
The projectile will always be spawned using the input variables StartingLocation and StartingRotation.
  2. UseCameraForwardVector
The projectile will be spawned at the location of the socket StartingSocketName traveling in the direction of the camera. This is mainly useful for shooter type games, where your projectiles typically shoot out forward from your camera.
If no socket name is specified, it will default to the spawning characters location. Use IgnoreCameraVectorPitch if you want the projectile to ignore the cameras "up and down" angle.

ActivateAbilityTagOnImpact: Tags to 

ProjectileData: 

Debug: Display debug if set to true.

