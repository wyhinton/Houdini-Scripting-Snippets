# Houdini-Scripting-Snippets

### Get the type of a node

```python
node.type() # get the type of a node
```

### Copy node icon to clipboard (windows)

```python
import subprocess
def copy2clip(txt):
    cmd='echo '+txt.strip()+'|clip'
    return subprocess.check_call(cmd, shell=True)

copy2clip(node.type().icon())
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
