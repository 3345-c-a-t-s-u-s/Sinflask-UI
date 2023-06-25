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

# Test Code
```lua
local SinFlask = loadstring(game:HttpGet(('https://raw.githubusercontent.com/3345-c-a-t-s-u-s/Sinflask-UI/main/source')))()
local Value = 1
local Window = SinFlask:NewWindow("Sinflask - Test",Enum.KeyCode.X,Value)
local Tab1 = Window:NewTab("Tab1")
local Tab2 = Window:NewTab("Tab2")

Tab1:NewButton("Button",function()
	print('Click Button')
end)

Tab1:NewLabel("Label")

Tab1:WarningLabel("Warning Label")

Tab1:NewToggle("Toggle",false,function(Boolen)
	print('Toggle Is: '..tostring(Boolen))
end)

Tab1:NewSlider("Slider",1,150,1,function(number)
	print(number)
end)

Tab1:NewDropdown("Dropdown",{"1","2","3"},function(chose)
	print(chose)
end)

Tab2:WarningLabel("Tab 2 - None")
```
