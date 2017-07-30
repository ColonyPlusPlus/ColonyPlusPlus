## Types

ColonyPlusPlus adds a number of types to the game. This list may be incomplete, as new blocks are added with almost every release.

| Icon        | Type ID           | Description  |
| ------------- |:-------------:| :-----|{% for type in site.data.types %}
| <img src="https://raw.githubusercontent.com/ColonyPlusPlus/ColonyPlusPlus/master/ColonyPlusPlus/textures/icons/{{type.id}}.png">     | `{{type.id}}` | {{type.description}} |{% endfor %}