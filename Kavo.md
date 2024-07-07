# Kavo UI Library

## Getting Loadstring
```lua
local Library = loadstring(game:HttpGet(""))()
```

# C
```lua
local Window = Library.CreateLib("TITLE", "DarkTheme")
```

```lua
local Tab = Window:NewTab("TabName")
```

```lua
local Section = Tab:NewSection("Section Name")
```

```lua
Section:UpdateSection("Section New Title")
```


```lua
Section:NewLabel("LabelText")
```

```lua
label:UpdateLabel("New Text")
```

```lua
Section:NewButton("ButtonText", "ButtonInfo", function()
    print("Clicked")
end)
```

```lua
button:UpdateButton("New Text")
```

```lua
Section:NewToggle("ToggleText", "ToggleInfo", function(state)
    if state then
        print("Toggle On")
    else
        print("Toggle Off")
    end
end)
```

```lua
getgenv().Toggled = false

local toggle = Section:NewToggle("Toggle", "Info", (state)
    getgenv().Toggled = state
end)

game:GetService("RunService").RenderStepped:Connect(function()
	if getgenv().Toggled then
		toggle:UpdateToggle("Toggle On")
	else
		toggle:UpdateToggle("Toggle Off")
	end
end)
```


