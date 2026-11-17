# Neon Siege remote config

Public, read-only kill switches the game client fetches at start (`game/src/shared/remote_config.gd`).
Nothing secret lives here.

| Key | Meaning |
|---|---|
| `min_protocol` | Clients with a lower `Proto.PROTOCOL_VERSION` get the update screen |
| `maintenance.on` / `message` / `eta` | Shows a maintenance message and blocks joining |
| `modes_disabled` | Mode ids to switch off without a build (e.g. `"br"`) |

**How to change:** edit `config.json` on `main` and commit. Clients cache the last good copy; the raw URL can take a few minutes to refresh.
Keep the JSON valid (a broken file is ignored and the cached copy is used).
