# Minecraft Modpack Template

## Modpack Configuration

### Modpack

See [modpack.json](./modpack.json) for an example of what a filled in modpack.json file should look like.

```json5
{
  "name": "<modpack_name>", // The name of your modpack.
  "version": "<modpack_version>", // The version of your modpack, like 0.1.0 or 1.0.0.
  "author": "<author>", // Examples: Jaron Zijlstra, Jaron Zijlsta <info@jaronline.dev>.
  "modloaders": [{
    "name": "<modloader_name>", // Options: forge, fabric, neoforge.
    "version": "<modloader_version>"
  }],
  "minecraft": {
    "version": "<minecraft_version>"
  },
  // Optional configuration for uploading.
  "curseforge": {
    "projectID": "<curseforge_project_id>" // Put your CurseForge project id here.
  }
}
```

### Mods

Mods are nessecary to send with the modpack json, these json files contain the information about the mod.
See [replanting-crops.json](./mods/replanting-crops.json) for an example of what a filled in mod file should look like.

```json5
{
  "name": "<mod_name>", // Name of the mod.
  "projectID": "<project_ID>", 
  // Optional giving the fileID when a different version rather than the newest is required. 
  // Default the newest file of the project is selected.
  "fileID":  "<file_ID>", 
  // Source is the name of the minecraft content distributor, like CurseForge or Modrinth.
  "source":  "<source_id>", // Options: curseforge, modrinth.
  // Side is whether the mod is run on the client side, server side or both.
  "side": "<side>" // Options: client, server, both.
}
```

### Data

The [data folder](./data) contains all additional files for your modpack like mod configuration.
These files will be added to your modpack as overrides.
