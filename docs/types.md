## Types

ColonyPlusPlus adds a number of types to the game. This list may be incomplete, as new blocks are added with almost every release.


### Spawning items

You can spawn items by first enabling cheats using `/cheats on` then using the loot command: `/loot {typeid} {number}` replacing `typeid` with the ID below, and then `number` with the number you wish to add to your inventory.

### Types

| Icon        | Type ID           | Description  |
| ------------- |:-------------:| :-----|{% for type in site.data.types %}
| <img src="https://raw.githubusercontent.com/ColonyPlusPlus/ColonyPlusPlus/master/ColonyPlusPlus/textures/icons/{{type.id}}.png">     | `{{type.id}}` | {{type.description}} |{% endfor %}