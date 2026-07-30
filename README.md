# RimWorld Mod Template

## Overview

Replace the content of this file with info about your mod!

This template is for both XML and C# mods. Delete whatever you don't need.

Use `LoadFolders` to ensure that your patches and defs only activate if the relevant mods/DLCs are active.

Add more folders under [Mod-Specific](Mod-Specific/) to categorize patches for mods by Author, collection, etc. Examples: "Vanilla Expanded", "Cohesive", "Progression".

I recommend sorting your `LoadFolders`, `LoadAfter`, and `ModDependencies` entries by the same categories above, and then alphabetically, as that's how they'll show up in the folder structure. Just remember that LoadFolders determines the order of operation, so some adjustment may be necessary.


## Basic Templates

Defs:

```xml
<?xml version="1.0" encoding="utf-8"?>
<Defs>
    <ThingDef>
        <defName>Someone.Thing</defName>
        <label>thing name</label>
        <description>A thing.</description>
    </ThingDef>
</Defs>
```

```xml
<?xml version="1.0" encoding="utf-8"?>
<Patches>
    <Operation Class="PatchOperationAdd">
        <xpath>Defs/ThingDefs[defName="foo"]</xpath>
        <bar>foobar</bar>
    </Operation>
</Patches>
```
