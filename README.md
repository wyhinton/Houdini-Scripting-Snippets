# Houdini-Scripting-Snippets

### Get the type of a node

```python
node.type() # get the type of a node
```

### Copy node info to clipboard

```python
import subprocess
def copy2clip(txt):
    cmd='echo '+txt.strip()+'|clip'
    return subprocess.check_call(cmd, shell=True)

#copy the node types icon
copy2clip(node.type().icon())

#copy a nodes rgb color
rgbVal = node.color().rgb()
copy2clip(f'{rgbVal[0]}, {rgbVal[1], rgbVal[2]}')
```

### Get the currently active Network Editor

```python
import toolutils
curNetwork = toolutils.networkEditor()
```

Set a custom shape for a node in the OnCreated Script

```python
kwargs["node"].setColor(hou.Color((1, 0.725, 0)))
kwargs["node"].setUserData('nodeshape', 'circle')
```

### All Custom Shapes Options

```python
'rect', 'bone', 'bulge', 'bulge_down', 'burst', 'camera', 'chevron_down', 'chevron_up', 'cigar', 'circle', 'clipped_left', 'clipped_right', 'cloud', 'diamond', 'ensign', 'gurgle', 'light', 'null', 'oval', 'peanut', 'pointy', 'slash', 'squared', 'star', 'tabbed_left', 'tabbed_right', 'tilted', 'trapezoid_down', 'trapezoid_up', 'wave'
```
