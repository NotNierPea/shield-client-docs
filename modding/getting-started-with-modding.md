---
description: Modding Guide.
---

# Getting Started with Modding

## Setting Up Folder For Mods

Create a directory in the Black Ops 4 install `project-bo4/mods`

***

## Creating "metadata.json"

Create a directory with a json file `metadata.json` in it.

For example `project-bo4\mods\demo_mod\metadata.json`.

The format of this json is:

```
{
    "name": "Demo mod",
    "data": [
        {
            "type": "asset type",
            "name": "path in game",
            "path": "path from the mod dir or absolute"
        }
    ]
}
```

More configs are available.
