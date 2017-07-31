Version 0.1.6 (30-07-17):
-------------------------------------
```
Added:
	Upsidedown versions of the slope blocks!
	Trading!
		/trade playerID itemID amount
	
Changed:
	Removed texturemaping from .json and put it in code!
	Chunk commands:
		They have been replaced with the following commands
		/chunk claim	- replaced /claimchunk
		/chunk unclaim	- replaced /unclaimchunk
		/chunk delete	- for admins to unclaim chunks to stop someone from griefing
	
Fixed:
	Cheese can now be NPC crafted!
	Butter can now be NPC crafted!
	
NOTICE: 
	This will be the last version compatible with Colony Survival 0.2.7
	We are going to start working on compatible for 0.3.0 for from this point on.
```

Version 0.1.5 (28-07-17):
-------------------------------------
```
Added:
	New Arrow Recipe
		1 - Plank, Feather, Iron Ingot = 12 arrows
	Rotatable clay blocks
		Two Step Stairs
		Four Step Stairs
		Slope Inside Corner
	Can now change between the two cube logs
	Now start with 2 bows and 4 flax seeds
	The ability to claim chunks, 
		However we can not stop other players from placing blocks in those chunks at this time.
		Requires "chunk.claim" permission node, with /claimchunk and /unclaimchunk commands
	Online (/online) command
		Requires "online" permission node

Changed:
	Bow recipe has been changed to requires 2 flax
	Food value of cake was increased from 6 to 15
	Increased Dirt Maxstack from 50 to 100
	All the clay decorative blocks are now smelted instead of NPC crafted
	Butter is now NPC crafted instead of player crafted!

Fixed:
	Mint texture
	Fixed missing milk, butter, cheese icons
```

Version 0.1.4 (24-07-17):
-------------------------------------
```
Added:
	Creative Mode cheat
		Adds 1000 of everything into your stockpile
		How to enable: /creative true
		
Fixed:
	Cherry Sapling Mesh
	Cherry Blossom Mesh
	SlopedCorner Mesh
```

Version 0.1.3 (23-07-17):
-------------------------------------
```
Added:
	Rotatable clay blocks
		Curve
		Horizontal Curve
		Corner Curve
		Slope
		Clope Corner
	Logs (cubes)
		Both horizontal and vertical
Fixed:
	Missing icons & textures for some blocks
```

Version 0.1.2 (22-07-17):
-------------------------------------
```
Added:
	Growable crops (without models right now)
		- Potato
		- Lettuce
		- Carrot
		- Onion
	Salt drop from sand
	Added some decorative clay blocks

Fixed:
	Textures on the furnace, Mint
	Meshes for sugarcane
```

Version 0.1.1 (21-07-17):
-------------------------------------
```
Fixed:
- Repackaged release to fix some issues
```

Version 0.1.0 (21-07-17):
-------------------------------------
```
Added:
- Numerous food items (butter/carrot/cheese/egg/jam/lettuce/milk/onion/potato/salt/sugar/sugarcane)
- A few recipes (baked potato/cake/Jambread/omlette)
- Some misc items (feathers)
- World spawns for sugarcane, berry bushes, vegetable patches which drop sugarcane, berries, and a random assortment of vegetables

Changed:
- Some basegame drops 
	- wheat drops less straw now (10% chance not 33.33%)
	- flax is cheaper to buy (200g = 100 flax is now 20g = 10 flax, ratio the same but less amount)
	- flax is generally less difficult to get (3% chance to drop from breaking grass)
	- leaves now drop our custom feathers
- Food values
	- Wheat is now a weaker foodstuff, pushing you quickly to bread/better breads/ better foods
```
