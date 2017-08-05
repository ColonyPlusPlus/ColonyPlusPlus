## Types

ColonyPlusPlus adds a number of types to the game. This list may be incomplete, as new blocks are added with almost every release.


### Spawning items

You can spawn items by first enabling cheats using `/cheats on` then using the loot command: `/loot {typeid} {number}` replacing `typeid` with the ID below, and then `number` with the number you wish to add to your inventory.

### Types

<table>
  <thead>
    <tr>
      <th>Icon</th>
      <th style="text-align: center">Type ID</th>
      <th style="text-align: left">Name</th>
      <th style="text-align: left">Description</th>
    </tr>
  </thead>
  <tbody>
  	{% for type in site.data.types %}

  	{% if type.newtype == true and type.isbaseblock == true %}
    <tr>
      <td><img src="https://raw.githubusercontent.com/ColonyPlusPlus/ColonyPlusPlus/master/ColonyPlusPlus/textures/icons/{{type.icon}}"></td>
      <td style="text-align: center"><code class="highlighter-rouge">{{type.name}}</code></td>
      {% assign name = type.name %}
      
      <td style="text-align: left">{{name}}{{site.data.typenames[name]}}</td>
      <td style="text-align: left">{{site.data.typeuses[name]}}</td>
    </tr>
    {% endif %}
    {% endfor %}
  </tbody>
</table>
