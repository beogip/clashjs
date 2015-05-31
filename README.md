# Unnamed js AI game.

This is an experimente. The idea is to create a battle game, where the participants code their AI, and then we make them fight!

The repo doesn't contain any code yet, just work-in-progress specs.

# The Game. Spec.

## Introduction.
Games and coding are fun! I want to make a game where we can confront AI vs AI.

The game is simple: we will put all the players in a battle arena, and then make them fight to death. We will put a coin in the arena, and the players should try to collect it. The last player alive, or the first to collect a certain number of coins, wins!

### Game characteristics.
* Every player will have a position and direction on the grid. A player can not go over the grid limits, and can only face north, west, south or east.
* The game will be turn based. Every turn we will excecute the AI of every player passing as arguments:
	* The current position and direction of the player.
	* The position of all other players (but not the direction).
	* The position of the coins.
	* A environment configuration option with:
		* Grid size.
		* Number of coins to collect to win.
* Every turn a player must execute some of the following actions:
	* Move one step in its current directino.
	* Turn into any of the four directions.
	* Shot.
* A player can shot to try to destroy another player. The shots have the following characteristics:
	* All the shots are executed before the movements in every turn.
	* A shot have a range of 3 squares.
	* After a shot, a player will be paralized for the following 3 turns.
* A player can collect a coin in the moment it steps over it. A new coin may appear in any moment of the game.


## Constraints.
* Be safe. A player code should not be able to modify anything other than itself.
* Be resilient as possible. If a Player crashes or stop responding, the show must go on.