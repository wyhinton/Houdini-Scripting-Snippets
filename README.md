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
