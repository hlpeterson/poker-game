# Texas Hold 'Em Application
As someone who enjoys strategic gaming, I figured that trying my hand at building a Java application through the likes of a poker game would be a good way to integrate my interest in programming with my enjoyment of strategy games. This project uses foundational Java principles in order to design an interactive GUI within which a user can play Texas Hold 'Em against a "robot" (i.e. a random number generator) opponent. 
## Overview 
### Classes 
This project uses a "Player" class, which is used to represent both of the players and includes all functionality for tracking each player's cards and money remaining, and a "Robot" class, which is a child class of the "Player" class and is used to provide functionality that only applies to the robot (i.e. the automated decision-making process)
### Hand-Ranking System 
This project uses several functions in order to evaluate which hand wins in a given scenario. First, a series of functions are called sequentially upon the conclusion of the final round of betting, with the hand that would produce the highest value being called first (i.e. "checkRoyalFlush) and the hand that would produce the smallest value being attempted last (i.e "evaluateHighCard). If any of the functions producing a hand size greater than high card evaluate with a value, that value will appear on the screen along with the name of the player who possessed the winning hand/whether or not the players tied; otherwise, evaluateHighCard will run automatically and produce an output regarding the winner of the round. The functions "evaluate" and "evaluatePairs" are used to evaluate for non-pair and paired hands, respectively; however, hand comparisons for Royal Flushes and Straight Flushes are done independently of these functions due to the unique nature of evaluating these hands in particular. 
### GUI
This project implements a JFrame in order to host the window in which the game is displayed. In order to simulate the interactiveness of the game, the project uses buttons to enable the user to make decisions as well as an input label in order to enable the user to type in their desired bet/raise sizes. In terms of the game state, the GUI includes labels for the user's chip count, the robot's chip count, and the overall pot size; additionally, images of each of the cards are displayed using a two-dimensional array which corresponds to the cards that the code generates for each round of the game.
### Tracking the Gamestate
This project uses a series of variables to track common game state requirements such as whether or not either of the players has bet or checked, whether or not a player has folded, and the number of chips a player has to remain; then, these values are evaluated through a series of if-statements and functions that run after each betting round to ensure that the rules of the game are being followed and that the GUI is an accurate representation of the game state at all times. A while loop is implemented to allow for hands to be played until one of the two players runs out of money; then, the user will be provided with the option to play again should they so choose. Each of the 52 cards is stored in a two-dimensional array which is accessed prior to the beginning of each hand by a random number generator in order to determine the cards of the user, the A.I. player, and the five community cards. Once each value has been assigned to a card for a particular hand, its value is altered so that it may not be re-assigned to another card during the same round; upon conclusion of the round, each of the cards is restored to their original values in order to prepare for the upcoming round.
## Future Improvements 
### Machine Learning Model for A.I. Opponent
At the moment, my next goal with this project will be to better simulate a CPU player by tracking the action habits of the user and adjusting the behavior of the A.I. player throughout the course of the game.
## Acknowledgements 
# All images were found and used freely via Pixabay. Card fronts: https://pixabay.com/vectors/card-deck-deck-cards-playing-cards-161536/. Card back: https://pixabay.com/photos/playing-card-back-pattern-568200/
