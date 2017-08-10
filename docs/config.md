## Configuration

ColonyPlusPlus adds a number of configuration parameters to the game, which control many of the features implemented in the mod.

### Finding the Configuration File

First browse to the gamedata folder, as described in [the installation instructions]({{ site.baseurl }}/installation). In this folder, navigate to `/mods/ColonyPlusPlus/`, and find `config.json` in there. You can edit this with any decent text editor, and even with Notepad. You need to ensure the file parses correctly as a JSON file, so be careful. You can verify the contents of a JSON file using any of a number of tools online.

### Example Configuration File

```json
{
	"motd": {
		"enabled": true,
		"message": "Here is the MotD"
	},
	
	"rotatingmessages": {
		"enabled": true,
		"list": [
			"We hope you're all having fun!",
			"Visit http://colonyplusplus.com for more info on this mod!"
		],
		"color": "yellow",
		"style": "bolditalic",
		"interval": 120,
	},
	
	"jobs": {
		"baseXP": 10,
		"maxLevel": 25,
		"xpMultiplier": 2,
		"efficiencyPerLevel": 0.02
	},
	
	"spawnprotection": {
		"enabled": true,
		"radius": 10
	},
	
	"chunks": {
		"enabled": true,
		"maxclaims": 12,
		"enforce": true
	},

	"debug": {
		"enabled": true
	},

	"trade": {
		"enabled": true
	},

	"chat": {
		"enabled": true,
		"colors": [
			{
				"permissionstring": "admin",
				"color": "lime",
				"style": "normal",
				"prefix": "Admin"
			},
			{
				"permissionstring": "moderator",
				"color": "yellow",
				"style": "normal",
				"prefix": "Mod"
			},
		]
	},
	
	"crops": {
		"growthMultiplier": 1
	},
	
	"colony":{
		"enabled": true,
		"limit": 150
	}
}
```

### Config Sections

<div class="contents">
	<a href="#message-of-the-day">Message of the Day</a>
	<a href="#rotating-messages">Rotating Messages</a>
	<a href="#jobs">Jobs</a>
	<a href="#spawn-protection">Spawn Protection</a>
	<a href="#chunk-protection">Chunk Protection</a>
	<a href="#debug">Debug</a>
	<a href="#trade">Trade</a>
	<a href="#chat">Chat</a>
	<a href="#crops">Crops</a>
	<a href="#colony">Colony</a>
</div>

#### Message of the Day

To set a welcome message that appears to everyone who logs in to the server (or single player). 

```
"motd": {
	"enabled": true,
	"message": "Here is the MotD"
},
```

| Key 		| Type 		| Values 			|
| :---  	| :----		| :----				|
| `enabled`	| boolean	| `true` or `false`	|
| `message` | string	| Any string/text 	|


#### Rotating Messages

If you're running a server, its useful to be able to inform users of certain things at defined time intervals - perhaps the URL of your website, or how to contact admins. Rotating messages allow you to do this.

```
"rotatingmessages": {
	"enabled": true,
	"list": [
		"We hope you're all having fun!",
		"Visit http://colonyplusplus.com for more info on this mod!"
	],
	"color": "yellow",
	"style": "bolditalic",
	"interval": 120,
},
```

| Key 		| Type 		| Values 					|
| :---  	| :----		| :----						|
| `enabled`	| boolean	| `true` or `false`			|
| `list` 	| string[]	| An array of strings/text, one will be displayed per rotation 	|
| `color` 	| string	| [Color]({{ site.baseurl }}/chatconfig#colors) of the text	|
| `style` 	| string	| [Style]({{ site.baseurl }}/chatconfig#styles) of the text	|
| `interval`| integer	| Any number less than 65532, the number of seconds between messages. 	|

#### Jobs

ColonyPlusPlus adds a number of jobs, and also adds an [XP system for NPCs]({{ site.baseurl}}/npcxp).

```json
"jobs": {
	"baseXP": 10,
	"maxLevel": 25,
	"xpMultiplier": 2,
	"efficiencyPerLevel": 0.02
},
```

| Key 		| Type 		| Values 			|
| :---  	| :----		| :----				|
| `basexp`	| integer	| The amount of base XP needed per level	|
| `maxLevel`	| integer	| The maximum level an NPC can go to	|
| `xpMultiplier`	| integer	| The exponent of the increase in XP needed per level	|
| `efficiencyPerLevel`	| decimal	| The percentage efficiency boost per level - 0.02 = 2% per level	|

This example above will allow up to 25 levels with a 2% boost in efficiency per level (resulting in a maximum of 50% efficiency boost). The efficiency boost is essentially a multiplier for crafting/job time. So 50% speed means effectively the speed doubles.

*Example Using the Above Settings*

|	Level	|	XP Needed	|	Efficiency boost	|
| :---		| :----:		| :----:				|
|	1	|	20	|	2%	|
|	2	|	40	|	4%	|
|	3	|	80	|	6%	|
|	4	|	160	|	8%	|
|	5	|	320	|	10%	|
|	6	|	640	|	12%	|
|	7	|	1280	|	14%	|
|	8	|	2560	|	16%	|
|	9	|	5120	|	18%	|
|	10	|	10240	|	20%	|
|	11	|	20480	|	22%	|
|	12	|	40960	|	24%	|
|	13	|	81920	|	26%	|
|	14	|	163840	|	28%	|
|	15	|	327680	|	30%	|
|	16	|	655360	|	32%	|
|	17	|	1310720	|	34%	|
|	18	|	2621440	|	36%	|
|	19	|	5242880	|	38%	|
|	20	|	10485760	|	40%	|
|	21	|	20971520	|	42%	|
|	22	|	41943040	|	44%	|
|	23	|	83886080	|	46%	|
|	24	|	167772160	|	48%	|
|	25	|	335544320	|	50%	|


For further information on how XP level work, please see the [NPC XP system documentation]({{ site.baseurl}}/npcxp).

#### Spawn Protection

```json
"spawnprotection": {
	"enabled": true,
	"radius": 10
},
```

| Key 		| Type 		| Values 			|
| :---  	| :----		| :----				|
| `enabled`	| boolean	| `true` or `false`	|
| `radius` | integer	| The radius of protection around the starting X and Y 	|


#### Chunk Protection

```json
"chunks": {
	"enabled": true,
	"maxclaims": 12,
	"enforce": true
},
```

| Key 		| Type 		| Values 			|
| :---  	| :----		| :----				|
| `enabled`	| boolean	| `true` or `false`	|
| `maxclaims` | integer	| The maximum number of chunks a player can own 	|
| `enforce`	| boolean	| `true` or `false`	|

If chunk protection is enabled ith `enforce` disabled, players will be able to place blocks or break blocks in any chunk they own, or in any unclaimed area. If `enforce` is enabled, players will only be able to build in chunks they have claimed (leaving a permanent record of the chunk ownership). For more information see [chunk protection]({{ site.baseurl}}/chunks).

#### Debug

Enabling debug has no real benefit to most users. The [commands]({{site.baseurl}}/commands#debug) for debug are generally for admins only, who might need an output of things like JSON generated by the mod.

```json
"debug": {
	"enabled": true
},
```

| Key 		| Type 		| Values 			|
| :---  	| :----		| :----				|
| `enabled`	| boolean	| `true` or `false`	|

#### Trade

ColonyPlusPlus allows players to [trade with each other]({{site.baseurl}})/trade, this can be disabled by either removing the permissions strings for the player's usergroup, or by disabled trade entirely on the server.

```json
"trade": {
	"enabled": true
},
```

| Key 		| Type 		| Values 			|
| :---  	| :----		| :----				|
| `enabled`	| boolean	| `true` or `false`	|


#### Chat

Now you can add custom chat colours to any given group, by simply creating an entry in the chat config, then adding that permission to their group. You can easily add a `donator` group by simply giving the `donator` permission to users, then also creating the respective `donator` chat configuration item.

```json
"chat": {
	"enabled": true,
	"colors": [
		{
			"permissionstring": "admin",
			"color": "lime",
			"style": "normal",
			"prefix": "Admin"
		},
		{
			"permissionstring": "moderator",
			"color": "yellow",
			"style": "normal",
			"prefix": "Mod"
		},
	]
},
```

| Key 		| Type 		| Values 			|
| :---  	| :----		| :----				|
| `enabled`	| boolean	| `true` or `false`	|
| `colors`	| array	| An array of settings	|


##### Color Config

| Key 					| Type 		| Values 			|
| :---  				| :----		| :----				|
| `permissionstring`	| string	| The permission string used in your permissionsgroups.json file to denote this group	|
| `color` 	| string	| [Color]({{ site.baseurl }}/chatconfig#colors) of the text	|
| `style` 	| string	| [Style]({{ site.baseurl }}/chatconfig#styles) of the text	|
| `prefix`	| string	| A prefix to add to the user - e.g. `Mod` becomes `[Mod] Tom Kent: some message here` when used in chat	|


#### Crops

```json
"crops": {
	"growthMultiplier": 1
},
```

The growth rate of custom crops added by ColonyPlusPlus can be controlled using these settings, allowing for you to change the rate at which our crops grow.

| Key 		| Type 		| Values 			|
| :---  	| :----		| :----				|
| `growthMultiplier`	| decimal	| The multiplier for the growth rate, 1 = 100% rate	|


#### Colony

You can impose limitations on colony size by enabling these settings.

```json
"colony":{
	"enabled": true,
	"limit": 150
}
```

| Key 		| Type 		| Values 			|
| :---  	| :----		| :----				|
| `enabled`	| boolean	| `true` or `false`	- enable colony settings|
| `limit`	| integer	| The maximum number of colonists a player can have	|
