# Developer distribution candidate

## Verified source

The existing private listing is
`plugin_asdk_app_sites_862eb19fb56c81918da6b3025e116337`, current release
`pluginrel_6ad8fd0e80388191a9bdf7e424cc7a43`, version `1.0.3`, checked 2026-10-21.
Its package has `plugin.json`, `.codex-plugin/plugin.json`, `.app.json`, and one
icon. It has no bundled skills or MCP file. The original App mapping is
`asdk_app_sites_862eb19fb56c81918da6b3025e116337`.

That mapping identifies an existing registered App. It does not prove that another
account can use it, nor that copying it transfers access. The original listing,
release, and binding remain unchanged. This separate distribution candidate uses
the verified remote MCP endpoint rather than shipping an unproved App dependency.
It retains the source package name and uses version `1.0.3-marketplace.1` to make
the local derivative distinguishable. It is not a new release of the online listing.

The icon is copied byte-for-byte from the verified release archive:

```text
assets/developer_compact_512.png
SHA-256 d15f90f128ee86e54ce89b5c9d0ce54d1d3af92867ec4cfffd1aab7156e6d896
```

Presentation changes are limited to a compliant short subtitle and accurate
Developer-only beta copy. No seven-Pack functionality is implied. The original
null default prompt is omitted; no replacement prompt or extra capabilities are
invented. No legacy overlay is needed by the targeted portable format; copying
the old overlay would retain the App dependency and misleading listing copy.

## Remote connection and instructions

`mcp.json` uses the documented `streamable-http` transport and verified URL:
`https://ddd-rule-packs.grayv516.chatgpt.site/mcp`.

A read-only unauthenticated GET returned HTTP 401 with an OAuth resource metadata
challenge. The advertised resource matches the exact MCP URL and names
`https://auth.openai.com` as its authorization server. The challenge named
`openid resource.invoke email`; metadata also advertises `offline_access` and
`profile`. No OAuth authorization, client registration, token request, credential
entry, or new grant was performed.

The portable connection leaves OAuth settings to supported host/provider
discovery. It supplies no client ID, registration mode, scopes, headers, or
credentials. Do not infer a portable OAuth flow works from the existing App
connection. Stop for approval before a new grant, new scope, registration, or
credential setup. Do not set authentication to `none` to work around a failure.

The downloaded Agent Plugins MCP 1.0.0 schema currently rejects extra server
properties, including `extensions`, while OpenAI's documentation describes
OpenAI auth extensions. This candidate uses only the common documented/schema
shape (`type` and `url`) and records OAuth separately here. Client ingestion and
OAuth compatibility remain live acceptance gates.

The current authenticated connection successfully returned `gds_agent_guide`
without accessing a project. The bundled skill requires this current live guide
and its required methods/readiness checks before work. It is a bootstrap contract,
not a copy of proprietary server methods or an invented replacement for them.
The guide reports Developer Pack `0.1.0`; package `1.0.3` is a separate version.

## Proof boundary

Local validation covers JSON schemas, catalog shape/path containment, instruction
presence and YAML, package inventory, asset integrity, and prohibited file/secret
patterns. The marketplace checks are derived from the official documentation;
they are not an official OpenAI marketplace schema or a host ingestion result.

It does not prove package tool ingestion, rich-card rendering, second-account
authentication, service entitlement, tenant isolation, or saved-session persistence.
The App-bound listing may remain the supported route on some surfaces. Do not
claim parity or replace that listing until a permitted pilot establishes it.
