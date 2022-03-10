# esx_components
usefull script to get, set and match components
you can use this for saving attachments in properties, trunks, inventories etc

# Server Exports
## GetComponents
#### Usage: `exports['esx_components']:GetComponents(player, weapon)`
Returns false if the player does not have the weapon

If the player does have the weapon it will return a list of all the attachments the player has for that weapon

Example
```
local components = exports['esx_components']:GetComponents(1, "WEAPON_ASSAULTRIFLE")
```

## SetComponents
#### Usage: `exports['esx_components']:SetComponents(player, weapon, components)`
Returns false if the player does not have the weapon

If the components are added to the weapon it will return true

Example
```
local components = {
  "scope",
  "luxary_finish",
  "grip",
  "suppressor"
}
exports['esx_components']:SetComponents(1, "WEAPON_ASSAULTRIFLE", components)
```

## MatchComponents
#### Usage: `exports['esx_components']:MatchComponents(components1, components2)`
Returns false if the tables do not match

Return true if the tables match

Example
```
local components1 = {
  "scope",
  "luxary_finish",
  "grip"
}

local components2 = {
  "luxary_finish",
  "grip",
  "scope"
}
exports['esx_components']:MatchComponents(components1, components2)
```
