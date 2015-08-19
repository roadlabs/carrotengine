# Getting Started #

carrotEngine.js is the engine for the game. it receives data from the game files, and then loads up the appropriate text / images / music for the scene.

# Javascript Objects and Their Properties #
Game - this an object to let the engine know which directory to load the game data from, and also has some properties for counters and timers
  * **directory** - string - defines which directory carrotEngine should load the game from. this will allow you to have multiple games available that are all run by the same engine. so if your game is in a subdirectory called my\_new\_game, you would have this.directory set to **this.directory = "my\_new\_game";**
  * **show\_debug** - Boolean - when this is set to 1, the debug container will be displayed
  * **timer** - integer - can be used by a game needing a global timer
  * **counter** - integer - can be used by a game needed a global counter

Player - this object is used for the character controlled by the player
  * **player\_name** - string - the name of the player character. gets set either by the game data, or by user input in **displayNameEntryScreen()**
  * **hitpoints, strength, intelligence, charisma** - integer - these can be used in **game.js** for doing calculations about the character
  * **experience** - integer - total amount of experience points. this can be used in **game.js** to increase the player's level
  * **level** - integer - current player level. this can be updated when conditions are met based on experience points
  * **lives** - integer - the number of chances the player has before the game is over

Character - this object is a generic object for non player characters in the game
  * **hitpoints, strength, intelligence, charisma** - integer - these can be used in **game.js** for doing calculations about the character
  * **x\_position** - integer - the horizontal position of the character image relative to the viewport
  * **y\_position** - integer - the vertical position of the character image relative to the viewport
  * **interested, amused, happy, sad, angry, confused, tired** - string - these can be set to different images that get displayed when a character is feeling a certain way
  * **attack\_1, attack\_2, attack\_3, attack\_4** - string - these can be set to different images that get displayed when the enemy does an attack
  * **damage\_1, damage\_2, damage\_3, damage\_4** - integer - these can be set to remove a certain number of hitpoints from the Player.
