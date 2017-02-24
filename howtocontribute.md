[Title]: Contributing

## How to contribute
Contributions to this site can be submitted to its [GitHub repository](https://github.com/blay09/BlaysModsDocs). Pages are built using the Markdown format.

## Guidelines
* Ore-dictionary item images should be kept to a minimum (e.g. only be used in recipes or when necessary to convey information).
* Item links should only be used where it would make sense for the user to read more. For example, there's probably no need to link minecraft:dirt.

## Markdown Extensions

### Page Attributes
At the top of each page you can define a title and logo. We abuse Markdown references for this.
It does not like spaces at the moment, but you can use underscores. They will be replaced by spaces when the site is displayed.
```
[Title]: My_Cool_Page
[Icon]: excompressum:chicken_stick
```
See the Item Images section for the Icon attribute.

### Item Links
You can link items without providing their actual URL. To do that, simply use an inline link and instead of an URL, provide an item identifier.

Example Source:
```
[This is a link!](excompressum:iron_mesh)
```

Preview:

[This is a link!](excompressum:iron_mesh)

### Item Images
Embedding item images works the same as linking, but with inline images instead. You can also specify metadata by putting it at the end of the identifier, separated by a colon (e.g. excompressum:compressed_block:2).
Unlike normal inline images, they will always be treated as a link as well. They will also be given a tooltip on hover.

Example Source:
```
![Iron Mesh](excompressum:iron_mesh)
```

Preview:

![Iron Mesh](excompressum:iron_mesh)

### Crafting Recipes
To display a crafting recipe, an inline image can be used with the custom crafting:// protocol.

The image title (what's normally within the square brackets) becomes the result of the crafting operation.
For crafting operations that result in more than one item, you can put the amount in front of the result (e.g. 8*excompressum:uncompressed_coal).

Following the crafting:// prefix in the Image URL (round brackets) comes the crafting matrix from left-to-right, top-to-bottom.
Empty slots in the grid should be 'null'.

Example Source:
```
![excompressum:iron_mesh](crafting://minecraft:iron_bars,minecraft:iron_bars,null,minecraft:iron_bars,minecraft:iron_bars,null,null,null,null)
```

Preview:
![excompressum:iron_mesh](crafting://minecraft:iron_bars,minecraft:iron_bars,null,minecraft:iron_bars,minecraft:iron_bars,null,null,null,null)

### Image Maps

For interfaces, it can be useful to add tooltips to define the different areas in a GUI screen. For this, you can use the imagemap:// protocol.

Example Source:
```
![excompressum/images/auto_hammer_gui.png](imagemap://Input Slot=16,70,32,32;Upgrade Slots=16,124,80,32;Output Slots=114,16,176,140;Energy=302,14,36,143;Player Inventory=16,168,320,148)
```

Preview:
![excompressum/images/auto_hammer_gui.png](imagemap://Input Slot=16,70,32,32;Upgrade Slots=16,124,80,32;Output Slots=114,16,176,140;Energy=302,14,36,143;Player Inventory=16,168,320,148)