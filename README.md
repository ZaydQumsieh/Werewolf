# Werewolf

A webserver to host Werewolf (also known as Mafia). Allows dead players to spectate using masterview.html, which can be projected onto a TV screen as well. A description of how this game works is at https://en.wikipedia.org/wiki/Mafia_(party_game). The server uses python websockets at port "wsport" (the exact value of which should be specified in a json file) in order to communicate with the website.

# Classes Supported

Innocent: Does nothing in any given round

Werewolf: Can kill one person per round

Seer: Can see one person's role per round

Doctor: Can prevent one person from dying per round

Monkey: Can copy one person's role

# How to Run

To run it, all you need is to run __src/WebsocketServer.py__ and host the contents __src/__ on a webserver. You must also provide a json file that specifies the configuration of the server. People join via __create.html__, where they are given parameters that they can use to create a game. Once the game is created, they are then given a link which others can use to join the game. A spectator can open up __masterview.html__ (or optionally it can be projected onto a TV is the game is being played locally) which provides a neat overview of the current status of the game and its players.
