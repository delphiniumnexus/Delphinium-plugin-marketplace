# Delphinium private plugin marketplace

Local distribution candidate for Shaq's private marketplace. The initial catalog
contains **3DDDs Developer** as a connection/install test. Blender is the planned
next package for Reggie's work; it is not in this catalog yet.

This repository distributes a catalog, a small activation skill, the approved
Developer icon, and a remote MCP connection. It contains no service source,
credentials, account grants, owner projects, private doctrine, or internal handoffs.
Anyone with repository read access can read every bundled file. Keep it private.

The package is prepared locally. A schema pass does not prove installation,
authentication, account isolation, or save/reopen behavior.

## Contents

- `.agents/plugins/marketplace.json`: one opt-in `AVAILABLE` entry, with
  `ON_INSTALL` authentication policy.
- `plugins/dev-862eb19fb56c81918da6b3025e116337/`: portable Developer candidate.
- [Installation and acceptance gates](docs/INSTALLATION.md).
- [Package provenance and compatibility](docs/PACKAGE.md).
- [Adding Blender](docs/ADDING_BLENDER.md).

## After publication is explicitly approved

The owner must first approve the exact branch/diff for a private GitHub push.
No push or remote publication is part of this local preparation.

An eligible user with existing private-repository read access can then register
the reviewed source in a supported Codex client:

```powershell
codex plugin marketplace add delphiniumnexus/Delphinium-plugin-marketplace --ref <approved-commit>
```

Replace `<approved-commit>` with the full reviewed commit SHA that contains this
catalog. Do not use a placeholder or the initial README-only commit. The official
CLI registers the source; installation/testing uses the supported desktop plugin
browser. See the separate gates before proceeding. Repository access does not
grant MCP service access. No invitation or account permission change is implied.

For an approved local pilot, the equivalent registration uses the absolute path
of this repository as the marketplace root. This was not run during preparation,
because source registration changes client configuration and may initiate later
installation/authentication behavior.

Format source: [OpenAI's current package and marketplace documentation](https://developers.openai.com/plugins/build/plugins),
checked 2026-10-21. Availability varies by account and client surface.
