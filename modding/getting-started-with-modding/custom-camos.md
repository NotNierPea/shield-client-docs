---
description: Custom camos instructions (replacing images, custom config)
---

# Custom Camos

## Tools Required

Download [CamoTools](https://github.com/NotNierPea/shield-client-docs/releases/download/release/CamoTools.zip).

## Replace Camo Images

You can replace camo images in two ways.

### Use the example mod

1. Download the example mod [ImageReplacementDemo](https://github.com/NotNierPea/shield-client-docs/releases/download/release/ImageReplacementDemo.zip).
2. Add it to `project-bo4/mods`.
3. Open the mod folder.
4. Put your custom `.dds` images in the `images` folder.
5. Use the same filename or hash as the camo image you want to replace.

### Use your own mod

1. Open `metadata.json` in your mod folder.
2. Choose one of these methods:
   * Enable `autoloadImages`
   * Add entries to `imageReplacements`

#### Enable `autoloadImages`

```json
{
    "name": "ImageReplacementDemo",
    "enabled": true,
    "autoloadImages": true
}
```

Then put the matching `.dds` files in your mod's `images` folder.

#### Add `imageReplacements` entries

Add an `imageReplacements` array to your `metadata.json`.

Each entry uses one of these keys:

* `asset` for named assets
* `hash` for `unk_0x...` hashes

Use `asset` for dumps named like `i_t8_camo_115_alt_c_<W>x<H>...`.

Use `hash` for dumps named like `unk_0xHEX_<W>x<H>...`.

Put the matching `.dds` files in your mod's `images` folder.

Example entries:

```json
{
    "imageReplacements": [
        { "asset": "i_mtl_wpn_t8_camo_bomber_01_c", "file": "i_mtl_wpn_t8_camo_bomber_01_c.dds" },
        { "asset": "i_mtl_wpn_t8_camo_bomber_02_c", "file": "i_mtl_wpn_t8_camo_bomber_02_c.dds" },
        { "asset": "i_mtl_wpn_t8_camo_bomber_03_c", "file": "i_mtl_wpn_t8_camo_bomber_03_c.dds" },
        { "asset": "img_t8_menu_zm_preview_escape", "file": "img_t8_menu_zm_preview_escape.dds" },
        { "asset": "img_t8_menu_zm_preview_escape_playlist", "file": "img_t8_menu_zm_preview_escape_playlist.dds" },
        { "asset": "img_t8_menu_zm_preview_office_playlist", "file": "img_t8_menu_zm_preview_office_playlist.dds" },
        { "hash": "0x1E396C4DAA5C356A", "file": "unk_0x1E396C4DAA5C356A.dds" },
        { "hash": "0x5D872E3A3D920FBE", "file": "unk_0x5D872E3A3D920FBE.dds" },
        { "hash": "0x5FA4296630868E75", "file": "unk_0x5FA4296630868E75.dds" },
        { "hash": "0x378BEF4DB883D003", "file": "unk_0x378BEF4DB883D003.dds" }
    ]
}
```

Full example:

```json
{
    "name": "ImageReplacementDemo",
    "enabled": true,
    "imageReplacements": [
        { "asset": "i_mtl_wpn_t8_camo_bomber_01_c", "file": "i_mtl_wpn_t8_camo_bomber_01_c.dds" },
        { "hash": "0x1E396C4DAA5C356A", "file": "unk_0x1E396C4DAA5C356A.dds" }
    ]
}
```

## Find the Correct Camo Images

1. Run `dump_ct2d` in the console.
2. Open the camo selection screen in-game.
3. Hover over the camo you want to replace.
4. Find the dumped files in `Call of Duty Black Ops 4\project-bo4\dump\ct2d`.

If the camo does not appear in the dumped folder, it means the game already loaded the camo image, restart the game and try again.

## Edit the Camo Images

1. Copy the dumped camo files into the `dds` folder inside CamoTools.
2. Drag the `dds` folder onto `dds2png.bat`.
3. Edit the generated `.png` files in your image editor.
4. Only edit the largest image.
5. The smaller images are not needed.
6. Move the edited `.png` files into the `pngs` folder in CamoTools.
7. Drag the `pngs` folder onto `camo-build-dds.bat`.
8. Copy the generated `.dds` files into your mod's `images` folder.
9. Restart the game for the camo changes to be applied.
