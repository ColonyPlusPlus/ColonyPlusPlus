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

Trade commands can be used to swap items with other players, at least until trading is added to the base game. If you want a list of type ID's, you can find them [here]({{ site.baseurl }}/types).

### Sending items to players

To send an item to a player, use the command `/trade give {playername} {type} {amount}`.

### Trading with other players

You can trade with other palyers (trading some of your items for theirs) using the following command:

`/trade send {playername} {myitemid} {myitemamount} {theiritemid} {theiritemamount}`

### Accepting and rejecting trade requests

You can accept or decline a trade request by using `/trade accept` or `/trade reject`. You can only have 1 open trade request at a time.



## Chunk Commands

### Claiming a chunk

You can claim the current chunk you are in (which will notify players who enter your chunk that it belongs to you) using the `/claimchunk` command. This requires the `chunk.claim` permission node.

This only works on the chunk you are currently stood in.

### Unclaiming a chunk

You can unclaim the current chunk you are in (which will stop notifying players who enter your chunk that it belongs to you) using the `/unclaimchunk` command. This requires the `chunk.claim` permission node.

This only works on the chunk you are currently stood in.


