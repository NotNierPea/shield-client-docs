---
description: Scripts GSC/CSC Guide.
---

# Scripts

### Scripts

It is possible to load script file with the support of GSIC file, a custom format from the T8-Compiler to replace script functions from the game.

To inject a script, 2 ways are possible, to replace an already existing one or to inject a new one. To tell the game when an injected script should be loaded, a hook script config is available. When a hook script is loaded, the injected script will be loaded.

The hooks of a script are defined with the `"hooks": [ "hook.gsc" ]` config. For example the script demo.gsc loaded when the script zm\_common/load.gsc is loaded.

```
{
    "name": "Demo mod",
    "data": [
        {
            "type": "scriptparsetree",
            "name": "scripts/shield/demo.gsc",
            "path": "compiled.gsic",
            "hooks": [
                "scripts/zm_common/load.gsc"
            ]
        }
    ]
}
```

***

## Compiler to use

For client gsc/csc detours: [https://github.com/ate47/t7-compiler-custom](https://github.com/ate47/t7-compiler-custom)

or you can use acts cod tools: [https://github.com/ate47/atian-cod-tools](https://github.com/ate47/atian-cod-tools) (does not support detours!)
