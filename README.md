# Minecraft

Minecraft Config.


## packwiz

### Updating

1. To check for new mod versions and update your modpack, run the following command locally: 

	```bash
	packwiz update --all
	```

2. Push the changes:

	```bash
	git add -A && git commit -m "COMMIT_NAME" && git push
	```

3. Restart the server.

### Migrating

When Minecraft or mod loader (Fabric) update to new versions you need to migrate your modpack accordingly.

1. Make sure all the mods you want to include have been updated and are compatible with the new latest Minecraft version. You can find the update checkers on [Shroomlight.net](https://shroomlight.net/client/settings). Update checker usage:

	```bash
	sh "/path/to/ServerUpdates.sh" [MC_VERSION]
	```

2. Mods with no compatible release must be removed or the server will refuse to start:

	```bash
	packwiz remove [MOD_SLUG]
	```

3. Perform the migration:

	Minecraft:

	```bash
	packwiz migrate minecraft [NEW_VERSION]
	```

	Fabric:

	```bash
	packwiz migrate loader [NEW_VERSION|latest|recommended]
	```

4. Update the modpack index:

	```bash
	packwiz refresh
	```

5. Upgrade the server to the new version (e.g. `fabric-26.3.jar` -> `fabric-26.4.jar`) and update `start.sh` accordingly.

6. Push the changes:

	```bash
	git add -A && git commit -m "COMMIT_NAME" && git push
	```

7. Restart the server.