# Create DockUI
```lua
local DockUI = 
```

<hr>

- Create Window
```lua
local Window = DockUI:UI("Ui Library")
```

| Numbering | Type    | Default      |
|-----------|---------|--------------|
| 1         | name    | "UI Library"  |
| 2         | author  | nil          |

<hr>

- Create Tab
```lua
local tab1 = DockUI:tab("Tab Name", "Icon")
```

| Numbering | Type    | Default       |
|-----------|---------|---------------|
| 1         | name    | "UI Library"   |
| 2         | icon    | "95423264010702"|

<hr>

# Elements

- Create Section
```lua
local Select1 = Tab1:Select("Category", true)
```

| Numbering | Type    | Default       |
|-----------|---------|---------------|
| 1         | name    | "Category"    |
| 2         | Status  | true          |


local Select1 = Tab1:Select('Category', true)
local Select2 = Tab1:Select('Category false', false)
local Select3 = Tab1:Select('Update Toggle', true)

local tabSelect1 = Tab2:Select('Category', true)
local tabSelect2 = Tab2:Select('DropDown', true)


Select1:Button('Button', function()
    print('Click!')
end)

Select1:Toggle('Toggle true', true, function(Value)
    if Value then
        print('true')
        else
        print('false')
    end
end)

Select1:Toggle('Toggle false', false, function(Value)
    if Value then
        print('true')
        else
        print('false')
    end
end)

local Update = Select3:Toggle('Toggle', true, function(Value)
    if Value then
        print('true')
        else
        print('false')
    end
end)

Select3:Button('true', function()
    Update:UpdateToggle('true', true)
end)

Select3:Button('false', function()
    Update:UpdateToggle('true', false)
end)


tabSelect1:Slider('Slider', 0, 120, 1, 30, function(Value)
    game.Workspace.Camera.FieldOfView = Value
end)

tabSelect1:Slider('Slider', 0, 120, 10, 0, function(Value)
    game.Workspace.Camera.FieldOfView = Value
end)
