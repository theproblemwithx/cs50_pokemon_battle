# CS50 Final Project
## Author: Carlos Faustino Mar Díaz

### Title: Pokemon Battle Simulator

#### Motivation

At first I wanted to create a web player trying to emulate Spotify, but quickly realized that while interesting and challenging, that might take more time than the one I had left in the year. Besides, I am planning on completing CS50 Web after this, so that project seemed more appropriate for that course. I decided to move on and complete a project in C, since it would involve less of a learning curve and it could provide greater reinforcement on all the topics covered during the first five weeks of CS50x.

I am also enrolled in a BS of Computer Science in Mexico, and our first programming class involved programming with C. While that class has already finished, I decided to dedicate the rest of the time in the year to reviewing C and reading a C book (C Programming - A Modern Approach). This is the project that I originally wanted to create for that class, but did not have the time to tackle it. Instead I ended up creating a simpler Pokemon trivia game.

#### Project Description
This project attempts to recreate the battle structure of the original Pokemon GameBoy games. These were developed by GameFreak and Nintendo and released in the 1990s. The GameBoy games were originally written in a mixture of C and Assembly language, according to sources found online.

The second source of inspiration was the Nintendo 64 game titled "Pokemon Stadium". In this game, players were given the option to do "Instant Battles" where a pre-defined set of 12 Pokemon were presented, and the player could choose 3 for a battle against another player or the CPU. These Pokemon would all be the same level with pre-defined moves.
![Pokemon Stadium Batle Example](https://gandoriongames.com/cdn/shop/products/Pokemon_Stadium_Nintendo_64_-_Gandorion_Games_d36a2cff-917b-4a29-a289-bb43d5573ab4-409443.jpg?v=1705420352)

#### Key Challenges
The two main challenges for this project were how to store Pokemon and their related moves, and how the main battle logic would work.

For storage, I decided to create two structs, one for Pokemon and one for their respective moves. The current limitation is that these have to me manually populated. A better program would be one that could read from a text file, randomly select Pokemon, and populate the structs with that information.

The Pokemon struct contains the name, type, level, hp, Moves struct and an array of weaknesses. These are accessed during battle to give options to the user and move the game forward.

The Moves struct contains the attacks that each Pokemon has, the power, type, and accuracy. This last item is not used in the current code, but could be adapted to add interactivity.

Once these were set, the challenge was how to start the battle and access each Pokemon's moves. I created functions for most of the logic, but left most of the battle logic in main since I thought it would make the general flow clearer, and since this is were most of the game happens.

#### How to Use
The general structure of the game is straigthforward. After compiling and running the program, the user is greeted and asked for their name. They are given a list of 6 Pokemon from which they can choose only one. The opponent and their Pokemon are chosen at random, and this information is presented to the user.

The user gets 4 options, as per the original GameBoy game:
* FIGHT
* PKMN
* ITEM
* RUN
![Pokemon fight example](https://cdn.theouterhaven.net/wp-content/uploads/2016/02/N3DS_PokemonYellow_02.jpg)

Due to time constraints, only the FIGHT option works for now. The other 3 options print a message to the user and return to the selection menu, until the user chooses to fight.

#### CS Concepts
This project showcases the basic ideas presented in an introduction to CS course with C, including:
* Variables
* Pointers
* Functions
* Libraries
* Conditionals
* Structs
* Arrays
* Abstraction
* Input Validation
* Flow Control

#### To Do (Nice to have) / Improvements
The following items are nice things for the project to have that I originally thought of implementing, but I am leaving them for another time since the year is coming to an end and I need to submit the final project.

* Displaying "It's not very effective!" when the attack's type is weak against the opponent
* 12 Pokemon as per the original N64 Pokemon Stadium
* Implement the 3 Pokemon battle, and ability to change Pokemon
* Options for using Items (Potion, Heal)
* Expand attack side-effects (Poisoned, Burned, Sleep, etc.) and modify HP accordingly
* Attack can miss based on accuracy from the Moves struct


