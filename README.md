# Introduction
The .dfg config file can be loaded into a Dynon Skyview Display Device to modify how the screen renders different airspaces on the map. The options include border colors, line widths and dashes/ticks on the borders, fill colors and label colors.

# dfg file format
The entire *.dfg file is contained inside the curly braces of  
```
map_bling={
}
```
Each consecutive airspace or other item is formatted as follows:  
```
airspace_ctr={
		color0=0012B3FF
		color1=E8370050
		color2=E83700FF
		color3=FFFFFFFF
		width0=1
		width1=4
		width2=6
		cycle=0
		fraction=0
		outline=0
		style=MAP_BLING_DRAW_STYLE_FILLED
		}
```
## Colors
Colors are formatted as hex RGB color with alpha channel in RRGGBBAA (red, green, blue, alpha) format, where AA=00 equals fully transparent and AA=FF fully opaque.  
## Styles
### MAP_BLING_DRAW_STYLE_SOLID
### MAP_BLING_DRAW_STYLE_SOLID_TICKS
### MAP_BLING_DRAW_STYLE_SOLID_UNCLIPPED_TICKS
### MAP_BLING_DRAW_STYLE_SOLID_FADE
is an airspace such as class C in the european style maps that features a solid contour and a faded (partially tranparent) inner border.  
`color0` is the solid border color  
`color1` is the faded inner border color (often alpha = 0x50)  
`width0` is the solid border width (that uses color0)  
`width1` is the faded border width (that uses color1)  
### MAP_BLING_DRAW_STYLE_FILLED
is a filled airspace, such as a CTR and RMZ in the european style maps.
`color0` is the border color  
`color1` is the fill color (often alpha = 0x80)  
`color2` is the text color, in which altitude constraints are shown  
`width0` is the border width  
### MAP_BLING_DRAW_STYLE_FRAG_SHADER
