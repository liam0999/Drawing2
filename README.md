# Drawing2
A fixed and cleaner version of a Roblox-GUI wrapper which mimics the Synapse X Drawing library

> [!NOTE]
> This library requires custom functions to work properly. If your executor does not support the following functions, this will not work.
> 
> `crypt.base64.decode`,
> `gethui`,
> `getcustomasset`,
> `isfolder`,
> `makefolder`,
> `readfile`,
> `writefile`,
> `isfile`,
> `delfile`

<details>
<summary>Documentation</summary>

## Drawing.Font.new

### Default Fonts
> - `[0] UI`
> - `[1] System`
> - `[2] Plex`
> - `[3] Monospace`
> - `[4] Pixel`

### Register Fonts

```lua
<Font> Drawing.Font.new(<string> FontName, <string> FontData)
```

> With File
> ```lua
> Drawing.Font.new("FontName", "FontName.ttf")
> ```

> With Base64
> ```lua
> Drawing.Font.new("FontName", "BASE64 ENCODED DATA HERE")
> ```

> With rbxasset
> ```lua
> Drawing.Font.new("FontName", "rbxasset://fonts/families/fontname.json")
> ```

## Drawing.new

### Base Properties
- `<bool>` Visible
- `<void>` Remove
- `<void>` Destroy
- `<Color3>` Color
- `<number>` Transparency
- `<number>` ZIndex

### Line
- `<Vector2>` From
- `<Vector2>` To
- `<number>` Thickness


```lua
local Line = Drawing.new("Line")
Line.Color = Color3.new(1, 1, 1)
Line.From = Vector2.new(0, 0)
Line.To = Vector2.new(100, 100)
Line.Thickness = 1
Line.Transparency = 0.5
Line.ZIndex = 1
Line.Visible = true
```

### Circle
- `<Vector2>` Position
- `<number>` NumSides
- `<number>` Radius
- `<bool>` Filled

```lua
local Circle = Drawing.new("Circle")
Circle.Color = Color3.new(1, 1, 1)
Circle.Position = Vector2.new(100, 100)
Circle.Radius = 50
Circle.NumSides = 10
Circle.Thickness = 1
Circle.Transparency = 0.5
Circle.ZIndex = 1
Circle.Filled = false
Circle.Visible = true
```

### Square
- `<Vector2>` Position
- `<Vector2>` Size
- `<number>` Rounding
- `<bool>` Filled

```lua
local Square = Drawing.new("Square")
Square.Color = Color3.new(1, 1, 1)
Square.Position = Vector2.new(100, 100)
Square.Size = Vector2.new(100, 100)
Square.Transparency = 0.5
Square.ZIndex = 1
Square.Visible = true
```

### Image
- `<Vector2>` Position
- `<Vector2>` Size
- `<number>` Rounding
- `<string>` Data
- `<string>` Uri

```lua
local Image = Drawing.new("Image")
Image.Color = Color3.new(1, 1, 1)
Image.Position = Vector2.new(100, 100)
Image.Size = Vector2.new(100, 100)
Image.Data = readfile("image.png")
Image.Uri = "https://www.example.com/image.png"
Image.Transparency = 0.5
Image.ZIndex = 1
Image.Visible = true
```


### Triangle
- `<Vector2>` PointA
- `<Vector2>` PointB
- `<Vector2>` PointC
- `<number>` Thickness
  
```lua
local Triangle = Drawing.new("Triangle")
Triangle.Color = Color3.new(1, 1, 1)
Traingle.PointA = Vector.new(10, 10)
Triangle.PointB = Vector2.new(15, 10)
Triangle.PointC = Vector2.new(10, 15)
Triangle.Transparency = 0.5
Triangle.ZIndex = 1
Triangle.Visible = true
```

### Quad
- `<Vector2>` PointA
- `<Vector2>` PointB
- `<Vector2>` PointC
- `<number>` Thickness
  
```lua
local Quad = Drawing.new("Quad")
Quad.Color = Color3.new(1, 1, 1)
Quad.PointA = Vector.new(10, 10)
Quad.PointB = Vector2.new(20, 20)
Quad.PointC = Vector2.new(5, 20)
Quad.PointD = Vector2.new(25, 20)
Quad.Transparency = 0.5
Quad.ZIndex = 1
Quad.Visible = true
```

### Text
- `<string>` Text
- `<number>` Size
- `<bool>` Outline
- `<bool>` Center
- `<Color3>` OutlineColor
- `<Font, string, number>` Font
- `<Vector2> <readonly>` TextBounds
  
```lua
local Text = Drawing.new("Text")
Text.Color = Color3.new(1, 1, 1)
Text.Position = Vector2.new(100, 100)
Text.Center = true
Text.Outline = true
Text.Text = "Text Test!"
Text.Font = "Plex"
Text.Font = 2
Text.Size = 13
Text.Transparency = 0.5
Text.ZIndex = 1
Text.Visible = true
```
</details>
