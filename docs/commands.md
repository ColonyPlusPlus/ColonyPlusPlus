# Commands

ColonyPlusPlus adds a number of commands to the game to add additional functionality.

## Contents
- [General Commands](#general-commands)
- [Trade Commands](#trade-commands)
- [Chunk Commands](#chunk-commands)


## General Commands

### Player List

To get the player list you can use the `/online` command. This will print the list of currently online players in your chat window.

This requires the `online` permissions node.

## Trade Commands

### Sending items to players

To send an item to a player, use the command `/trade give {playername} {type} {amount}`.

### Sending Trades

To send a player a trade, use the command `/trade give {playername} {offertype} {offeramount} {requesttype} {requestamount}`

#### Spaces in names

If the player you're sending to has a space in their name, add quotes around it like this: `"Player Name"`

## Chunk Commands

### Claiming a chunk

You can claim the current chunk you are in (which will notify players who enter your chunk that it belongs to you) using the `/claimchunk` command. This requires the `chunk.claim` permission node.

This only works on the chunk you are currently stood in.

### Unclaiming a chunk

You can unclaim the current chunk you are in (which will stop notifying players who enter your chunk that it belongs to you) using the `/unclaimchunk` command. This requires the `chunk.claim` permission node.

This only works on the chunk you are currently stood in.


