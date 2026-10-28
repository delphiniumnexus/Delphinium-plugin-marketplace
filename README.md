# Delphinium Beta Plugins

Start here: **[Reggie's Windows setup and first test](docs/REGGIE_START_HERE.md)**.

This marketplace distributes one opt-in **3DDDs Developer** beta package. The
package contains an activation skill, the existing Developer icon and a connection
to the hosted Developer service. Blender is planned next and is not included.

The marketplace is prepared for a public GitHub repository. Public visibility
lets anyone read and copy the distribution files; it does not grant GitHub write
access, Delphinium administration, access to a private development repository, or
access to another person's projects. Do not add Reggie as a repository collaborator
just to download this public package.

The hosted service authenticates separately. The service guide describes
account-owned project access; this has **not yet been verified with Reggie's
account**. The catalog is not an access-control layer and does not make the beta
exclusive to Reggie.

## Install after the owner makes this repository public

Use the current ChatGPT desktop app on Windows with Work or Codex and its plugin
browser. With a current Codex CLI and Git available in PowerShell:

```powershell
codex plugin marketplace add delphiniumnexus/Delphinium-plugin-marketplace --ref main
codex plugin marketplace list
```

Restart the desktop app, select **Delphinium Beta Plugins** in the Plugins
Directory, and install **3DDDs Developer**. Connect with your own account. The
package version is `1.0.3-marketplace.2`. Registering the marketplace alone does
not complete installation or authentication.

For a repeatable test, replace `main` with the full reviewed commit SHA. Follow
the [Windows guide](docs/REGGIE_START_HERE.md) for prerequisites, a download/local
fallback, troubleshooting, and the save/reopen test. A public GitHub repository
does not automatically create a listing in OpenAI's public plugin directory.

## Status and supporting notes

| Item | Status |
| --- | --- |
| Developer distribution package | Prepared; structural checks recorded |
| Developer guide through the existing owner connection | Read successfully on 2026-10-28 |
| Reggie's Windows installation and account access | Pending live test |
| Cross-account isolation | Pending controlled two-account test |
| Save, close and reopen | Pending on Reggie's disposable project |
| Blender package | Not included |

- [Installation and acceptance checks](docs/INSTALLATION.md)
- [Package provenance and compatibility](docs/PACKAGE.md)
- [Public distribution review](docs/PUBLIC_READINESS.md)
- [Sanitized test report template](docs/TEST_REPORT_TEMPLATE.md)
- [Adding Blender later](docs/ADDING_BLENDER.md)

The stable marketplace identifier remains `delphinium-private` for compatibility
with previously registered sources. Its display name is **Delphinium Beta Plugins**;
the identifier does not control GitHub visibility.

Installation instructions follow [OpenAI's package and marketplace documentation](https://developers.openai.com/plugins/build/plugins),
checked 2026-10-28. Account, plan, role and client support must be checked on the
tester's actual device.

