# DW Final Assignment

Here is a link to my [YouTube video](https://youtu.be/WrK25hRxH-s).

## My own take on the game Plants vs Zombies

The original was a tower defence and strategy game where the player takes on the role of a homeowner in the midst of a zombie apocalypse who uses plants to fire projectiles at advancing zombies.

In my game, I am retaining the concept of a homeowner protecting his house in the midst of a zombie apocalypse through the use of plants but I have simplified the gameplay. The game is still a strategy game, albeit a simple one.

## How to play the game

In my game, the player has 3 plants to choose from, with each plant being able to cause different amount of damage to zombies.

Each plant also have different refresh rates, meaning a plant can only be used once every few seconds, depending on the plant's "strength". The weakest plant has a refresh rate of 5 seconds and the strongest has a refresh rate of 9 seconds.

To attack the zombies, the player would have to click on the plant they want to use and then click on the lane they want to use the plant on. The plant would then deal damage to zombies on that lane.

Each zombie has 4 healthpoints(hp), and when they run out of hp they will die, or disappear from the lane.

There are 3 waves of zombies and the player wins if they are able to clear all 3 waves.

If the player wants to restart the game, they can also do so by exiting to the main menu and starting the game from scratch.

## Code Discription

In my code, the main library I used was kivy (GUI).

There are 4 main classes.

1. Home Screen
    - This class contains the main page where the player can enter the game or leave the game, or view a short write up on how to play the game.

2. Instructions Screen
    - This contains information on how to play the game.

3. GamePlay Screen
    - This class contains all the game widget and all the core game mechanics. Contains code for the movement of zombies (using from kivy animation class) and attacking mechanism, as well as detecting whether the player has won or lost the game to prompt the player to either restart or quit the game.
    - The \_\_init__ function creates the root widget which is the BoxLayout. TheBoxLayout consists of the lanes and plants, which are buttons. The lanes contain the zombies which are image widgets.
    - __Tracking attacks on the zombies__
        - I choose to track the number of clicks based on the attack strenght of each zombie, taking into account all combinations of attack.
    - __Tracking whether the player has won or lost__
        - I chose to track the presence of the zombie image widgets. If at the end of 20, 38 and 58 seconds respectively, there are still zombies remaining in the lanes, then the player has lost. Otherwise, if all zombies have been cleared, the player wins.

4. PvZ, App class
    - This class contains kivy screen manager to allow the player to toggle between the screens.

All graphics were obtained through Google and belong to PopCap Games.
