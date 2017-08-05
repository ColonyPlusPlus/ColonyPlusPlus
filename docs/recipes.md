## Recipes

ColonyPlusPlus adds a number of [types to the game]({{ site.baseurl }}/types), many of which can be crafted using the recipes below. 


## Contents
<div class="contents">
  {% for craftingtype in site.data.craftingtypes %}
  <a href="#{{craftingtype.title}}">{{craftingtype.title | capitalize}}</a>
  {% endfor %}
</div>

{% for craftingtype in site.data.craftingtypes %}

<h3 id="{{craftingtype.title}}">{{craftingtype.title | capitalize}}</h3>

<table>
  <thead>
    <tr>
      <th>Recipe Result</th>
      <th style="text-align: left">Player Craftable</th>
      <th style="text-align: left">Requirements</th>
      <th style="text-align: left">Results</th>
    </tr>
  </thead>
  <tbody>
  	{% for recipe in site.data.recipes %}

  	{% if recipe.type == craftingtype.type %}
    <tr>
      <td>{{ site.data.typenames[recipe.mainresulttype]}}</td>
      <td style=""><code class="highlighter-rouge">{{recipe.playerCraftable}}</code></td>
      
      <td style="text-align: left">
        {% for req in recipe.requirements %}
        <code class="highlighter-rouge">{{req.type}} x{{req.amount}}</code>
        {% endfor%}
      </td>
      <td style="text-align: left">
        {% for req in recipe.results %}
        <code class="highlighter-rouge">{{req.type}} x{{req.amount}}</code>
        {% endfor%}
      </td>
    </tr>
    {% endif %}
    {% endfor %}
  </tbody>
</table>

{% endfor %}