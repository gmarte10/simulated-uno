# simulated-uno

This is a project from my Intro to Software Engineering class.
Simulated Uno is a simplified version of the uno game. It creates and runs a game based on
values given by the user.

## Installation

Download and extract the project from github

## Usage

Use intellij to open the Uno folder. Go to the RunOneGame class to run a single game.
Input the values you want to create the game.

Values to create the game:
countPlayers — number of players

countInitialCardsPerPlayer — number of cards initially dealt to each player

countDigitCardsPerColor — number of normal cards for each digit and color. 
For example, 2 means 2 Red “0” cards, 2 Yellow “0” cards, 2 Blue "0" cards, 2 Green "0" cards, etc.

countSpecialCardsPerColor — number of special cards of each kind for each color. 
For example, 1 means 1 Red Skip card, 1 Yellow Skip card, ..., 1 Red Reverse card, 1 Yellow Reverse card, etc.
May be 0. There are is only Skip, Reverse and Draw 2.

countWildCards — number of total wild cards. May be 0.

Instructions of how the game is played:
* This is a simplified version of uno

Cards:
The deck contains “normal cards” and “wild cards”.
Each normal card has a color (red, yellow, green, or blue), and it has either a digit (“0” to “9”) or a special instruction on its face.
There are the following kinds of special cards:
* “Skip”: The next player is skipped, and the player after the skipped player takes the next turn.
* “Reverse”: The order of play around the circle is reversed. If it was previously clockwise, it now becomes counter-clockwise, and vice versa.
* “Draw Two”: The next player must draw two cards, and then their turn is over, and play continues with the player after them.
  They do not get an opportunity to play a card that turn.
A wild card has no color, but the player declares a wild card’s “effective” color when the card is played.

Playable Cards:
A playable card is a card that can be discarded onto the top of the discard pile.
A normal card is playable if it matches either the color or the face of the top card on the discard pile. 
For example, a Red 7 can be played on top of a Red 3, or a Red Skip, or a Blue 7; but it cannot be played on top of a Blue 3.
A wild card is always playable.
If the top card on the discard pile is a wild card, it is treated as the color declared by the player who played it.

Taking Turns:
When it is a player’s turn, if the player has any playable cards in their hand, they must play one of them, and then their turn ends. 
If the player does not have any playable cards, they must draw one card from the draw pile; 
if they draw a playable card, they must immediately play it, and then their turn ends. Otherwise they add the drawn card to their hand, and their turn ends.

Running Out of Draw Cards:
If the draw pile becomes empty, it is refreshed from the discard pile. The top card of the discard pile is retained;
the new discard pile consists of only that card. The other cards in the discard pile are shuffled and placed face-down, and they become the new draw pile.

