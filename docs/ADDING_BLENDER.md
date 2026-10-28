# Add Blender after the Developer pilot

Blender is intended for Reggie's 3D workflows after the Developer installation,
connection, account-isolation and save/reopen checks. It is not in this catalog.

The earlier candidate recorded this existing plugin and endpoint:

- Plugin: `plugin_asdk_app_sites_bcb806bbec148191bbb272710abeecd9`.
- MCP endpoint: `https://ddd-blender-pack.grayv516.chatgpt.site/mcp`.

Before adding Blender:

1. Inspect its current owned release and actual inventory, preserving the
   approved artwork and plugin identity. Verify the endpoint is still correct.
2. Read the current live Blender guide through an authorized connection.
   Establish its supported activation, methods, storage and resume behavior.
3. Package only customer-facing distribution files and a supported authenticated
   connection. Do not bundle backend source, credentials or private methods.
4. Add one opt-in `AVAILABLE` / `ON_INSTALL` entry in this marketplace, with its
   own contained plugin path and accurate metadata. Keep all other Packs out.
5. Validate the distribution and repeat the [acceptance checks](INSTALLATION.md)
   with the intended tester account/client.

A Developer pass does not prove Blender access, Blender application integration,
local filesystem permissions or Blender saved-work continuity. Those require
separate observed tests. The catalog alone provides no control of a local Blender
process. Leave Blender unavailable if the actual supported workflow cannot be
established; do not ship a placeholder.

