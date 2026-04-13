# r3d_adminmenu (QBCore)

## Install

1. Put `r3d_adminmenu` in your server `resources` folder.
2. Add this line to `server.cfg`:
   - `ensure r3d_adminmenu`
3. Restart the server.

## Open Menu

- Command: `/adminmenu`
- Default key: `F11`
- You can edit both in `config.lua`.

## Permissions (config.lua)

- `Config.UseQBCorePermissions = true`
- `Config.AllowedQbPermissions = { 'admin', 'god' }`
- Optional ACE fallback:
  - `Config.UseAcePermissions = true`
  - `Config.AcePermission = 'r3d.admin'`

## Features

You can enable/disable each feature from `Config.Features`:

- revive
- heal
- kill
- freeze
- gotoPlayer
- bringPlayer
- kickPlayer
- setJob
- vehicleFix
- vehicleClean
- vehicleDelete

## Notes

- This resource uses secure server-side checks before each action.
- For revive action, it triggers `hospital:client:Revive`.
- If your hospital script uses a different event, replace it in `server/main.lua`.
