# Sinflask-UI
Sinflask UI - UI for Script Roblox

## How to Use?

## Creating a Window
```lua
-- Url - https://raw.githubusercontent.com/3345-c-a-t-s-u-s/Sinflask-UI/main/source
local SinFlask = loadstring(game:HttpGet(('https://raw.githubusercontent.com/3345-c-a-t-s-u-s/Sinflask-UI/main/source')))()

local Window = SinFlask:NewWindow(<string>,<Enum.KeyCode>,<number>)

--[[
	<string> = Title
	<Enum.KeyCode> = Toggle Key
	<number> = horizontal or vertical {
		horizontal number = 2
		vertical number = 1
	}
]]


```

## Creating a Tab
```lua
local Tab = Window:NewTab(<string>)
--[[
	<string> = Title
]]
```

## Creating a Button
```lua
local Button = Tab:NewButton(<string>,<function callback>)

Button:SetLabel(<string>)
	
Button:ChangeCallback(<function callback>)
--[[
	<string> = Title
	<function callback> = callback
]]
```

## Creating a Label
```lua

Tab:NewLabel(<string>)

-----------

local Label = Tab:NewLabel(<string>)
Label:SetLabel(<string>)
--[[
	<string> = Title
]]
```

## Creating a Warning Label
```lua

Tab:WarningLabel(<string>)

-----------

local WarningLabel = Tab:WarningLabel(<string>)
WarningLabel:SetLabel(<string>)
--[[
	<string> = Title
]]
```

## Creating a Toggle
```lua
local Toggle = Tab:NewToggle(<string>,<boolen>,<function callback>)
	
----------
	
Toggle:SetLabel(<string>)	
Toggle:Set(<boolen>)
--[[
	<string> = Title
	
	<boolen> = Default value
	
	<function callback> = callback
]]
```

## Creating a Slider
```lua
local Slider = Tab:NewSlider(Title,Min,Max,Increment,Callack)
	
-------------------
	
Slider:Set(<number>)
	
Slider:SetLabel(<string>)
	
--[[
	<string> = Title
	
	<number> = set value to number

]]

```

## Creating a Dropdown
```lua
	local Dropdown = Tab:NewDropdown(Label,List,callback)
	---------
	Dropdown:Change(newList)
	Dropdown:Refresh()
```
