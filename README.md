# Lua Color Converter

Convert HEX or RGB values into decimal rgb color values, compatible with Corona and Defold format, (numbers from 0 to 1).

### How To Install:

1. Put **lua-color-converter.lua** into your project directory

2. Load it in your scripts when neccesary:

```lua
local color = require("lua-color-converter")
```

3. Use it to convert from hex:

```lua
color.hex("ff00ff") -- 0.5, 0, 0.5

-- You can include "#" in your string if needed

color.hex("#ff00ff") -- 0.5, 0, 0.5
```

.. and to convert from regular byte rgb:

```lua
-- r,g,b
color.rgb(255, 0, 255) -- 0.5, 0, 0.5
```

You can use one more argument to set alpha channel:

```lua
color.hex("ff00ff", 0.5) --alpha set to 50%
color.rgb(255, 0, 255, 75) --alpha set to 75%
```

### Examples:

```lua
local myText = display.newText( "example from Corona Docs", 0, 0, native.systemFontBold, 12 )
myText:setFillColor( color.hex("#ff10ae") )
```

```lua
go.set("#label", "color", vmath.vector4(color.rgb(255, 16, 174, 1))
```
