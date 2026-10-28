# Developer beta package provenance

## Source and identity

This distribution continues the existing marketplace candidate at
`57c093a2050fe8918996f3ffcc9792b3e99aed25` on
`codex/private-marketplace-setup`.

That candidate recorded the original private listing
`plugin_asdk_app_sites_862eb19fb56c81918da6b3025e116337`, release
`pluginrel_6ad8fd0e80388191a9bdf7e424cc7a43`, version `1.0.3`, checked on
2026-10-21. Its original App mapping was
`asdk_app_sites_862eb19fb56c81918da6b3025e116337`. Those identifiers are historical
provenance, not credentials or grants to another account. The original listing
and backend are not updated by this distribution preparation.

The portable package keeps its existing package name,
`dev-862eb19fb56c81918da6b3025e116337`, and advances from
`1.0.3-marketplace.1` to **`1.0.3-marketplace.2`** for the public-beta copy and
installation documentation. The marketplace keeps its stable
`delphinium-private` identifier, with the display name **Delphinium Beta Plugins**.

The existing activation skill, remote MCP configuration and icon are preserved.
The icon's recorded SHA-256 is:

```text
d15f90f128ee86e54ce89b5c9d0ce54d1d3af92867ec4cfffd1aab7156e6d896
```

## Connection and account boundary

The only remote MCP endpoint is the existing service:

`https://ddd-rule-packs.grayv516.chatgpt.site/mcp`

The package uses portable `mcp.json`, `streamable-http`, and provider/host
authentication discovery. It packages no authorization header, token, password,
client secret, preset client ID or registered App binding. Do not replace this
with authentication disabled or copy the owner's App binding to work around a
failed tester connection.

The prior candidate recorded an unauthenticated HTTP 401 OAuth challenge and
resource metadata for this endpoint on 2026-10-21. This does not establish that a
new host's OAuth flow can register/connect successfully.

On 2026-10-28, the existing authenticated owner connection returned
`gds_agent_guide`. It identifies Developer Pack `0.1.0`, an account-owned cloud
project workflow, and no repository access, file uploads or local sync. The
service's Pack version and the distribution package version are separate.

Only the connection guide was read. No project was listed, created or changed
during this preparation. No Reggie sign-in, new OAuth grant, account invitation,
admin-role change, backend edit or deployment was performed.

## Included files

- Root portable `plugin.json`.
- Root portable `mcp.json`.
- `skills/developer/SKILL.md`, a bootstrap to the current live guide.
- `assets/developer_compact_512.png`, the existing Developer icon.

The catalog resolves this contained directory through a local `./plugins/...`
path. There is no dependency on the private 3DDDs development repository. The
small bootstrap skill and public endpoint address are visible to every reader of
the repository. Required server methods are fetched from the service at runtime.

## Validation boundary

Preparation checks JSON syntax and documented field rules, one opt-in catalog
entry, path containment, referenced inventory, skill frontmatter, preserved
component hashes and common prohibited file/credential patterns. These checks
are not an official OpenAI ingestion result or a full backend security audit.

Live desktop ingestion, portable OAuth, second-account service access, card
rendering, controlled cross-account isolation and saved-session persistence
remain acceptance tests. See [installation checks](INSTALLATION.md) and
[public review](PUBLIC_READINESS.md).

