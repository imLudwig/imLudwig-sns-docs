# Ludwig Skillz

Das Skript stellt unser Skillsystem dar, um einen Skill abzufragen kann sowohl Clientseitig als auch Serverseitig ein Export angewandt werden.

## Serverseitig:

`return`: Integer 0 - 10

```lua
local skill = "Holzfäller" 
local skillLevel = exports.ludwig_skillz:getSkill(source, "Holzfäller").skillLevel or 0
```

## Clientseitig

`return`: Integer 0 - 10

```lua
local skill = "Holzfäller" 
local skillLevel = exports.ludwig_skillz:getSkill("Holzfäller").skillLevel or 0
```

Es gibt aktuell folgende optionen: 

"Leben", "Ausdauer", "Resistenz", "Genauigkeit", "Farmer", "Holzfäller", "Minenarbeiter","Glück","Jäger","Langfinger",
