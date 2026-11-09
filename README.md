# Minecraft

Minecraft Config.


## packwiz

### Updating

To check for new mod versions and update your modpack, run the following command locally: 

```bash
packwiz update --all
```

### Migrating

When Minecraft or mod loader (Fabric) update to nev versions you need to migrate your modpack accordingly.

1. Make sure all the mods you want to include have been updated and are compatible with the new latest Minecraft version. You can find the update checkers on [Shroomlight.net](https://shroomlight.net/client/settings). Update checker usage:

	```bash
	sh "/path/to/ServerUpdates.sh" [MC_VERSION]
	```

2. Perform the migration:

	Minecraft:

	```bash
	packwiz migrate minecraft [NEW_VERSION]
	```

	Fabric:

	```bash
	packwiz migrate loader [NEW_VERSION|latest|recommended]
	```