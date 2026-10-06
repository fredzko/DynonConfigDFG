# Introduction
The .dfg config file can be loaded into a Dynon Skyview Display Device to modify how the screen renders different airspaces on the map. The options include border colors, line widths and dashes/ticks on the borders, fill colors and label colors.

# dfg file format
The entire *.dfg file is contained inside the curly braces of `map_bling={}`  
Each item is formatted as follows:  
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
