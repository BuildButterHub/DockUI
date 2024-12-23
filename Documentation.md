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

| Numbering | Type    | Default         |
|-----------|---------|-----------------|
| 1         | name    | "UI Library"    |
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

<hr>

- Create Button

```lua
Select1:Button("Button", function()
    print('Click!')
end)
```

<hr>

- Create Toggle

```lua
Select1:Toggle("Toggle", false, function(Value)
    if Value then
        print('true')
        else
        print('false')
    end
end)
```

- Update toggle
```lua
UpdateToggle('Toggle', true)
```

| Numbering | Type     | Default       |
|-----------|----------|---------------|
| 1         | name     | "Toggle"      |
| 2         | Status   | false         |
| 3         | callback | nil           |

<hr>

- Create Slider
```lua
Select1:Slider("Slider", 0, 120, 1, 0, function(Value)
    game.Workspace.Camera.FieldOfView = Value
end)
```

| Numbering | Type     | Default       |
|-----------|----------|---------------|
| 1         | name     | "Slider"      |
| 2         | min      | 0             |
| 3         | max      | 120           |
| 4         | step     | 1             |
| 5         | default  | 0             |
| 6         | callback | nil           |

<hr>
