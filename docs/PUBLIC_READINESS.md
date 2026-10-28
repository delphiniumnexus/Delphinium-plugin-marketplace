# Public distribution review

Prepared on 2026-10-28 for a public marketplace and Reggie's first Developer test.

## What publication exposes

GitHub readers can inspect the catalog, plugin manifest, small activation skill,
icon, public endpoint address and these setup notes. Public visibility also
exposes repository history and Git commit metadata, including prior versions of
these files.

The two existing branches and the two-commit candidate history were inspected.
The initial commit contains a placeholder README; the candidate adds only the
distribution files described in [package provenance](PACKAGE.md). The unchanged
development branch still contains its older private-beta wording. Public visibility
applies to that branch too.

No service implementation, Delphinium administration code, packaged account
session, private project record or development-repository source is needed by this
distribution. Public repository read access gives no write role.

This is **public distribution with separate authenticated service access**, not a
Reggie-only GitHub beta. The marketplace's install policy is opt-in availability;
it does not restrict backend entitlement. If the service needs a tester allowlist
or invitation, configure and verify it through the supported service-owner
workflow separately. Publicizing this repository cannot supply that entitlement.

## Checks and remaining tests

| Check | Preparation result |
| --- | --- |
| Catalog and manifest JSON / documented field rules | Validated locally |
| One Developer entry with contained source path | Validated locally |
| Skill, MCP endpoint and icon preserved from candidate | Checked |
| No App binding, credential headers or local command server | Checked |
| Common secret/file-pattern scan of distribution text | No matches found |
| Existing owner connection can read the live guide | Observed 2026-10-28 |
| Reggie's actual Windows installation | Pending |
| Reggie's own OAuth and service access | Pending |
| Controlled two-account isolation | Pending |
| Disposable project save/reopen | Pending |
| Public visibility change | Owner action |

Structural validation and a credential-pattern scan have limited scope. They do
not certify backend security, prove host ingestion or replace the live tests.

## Owner handoff

1. Make only this marketplace repository public after reviewing its contents and
   history. Keep the main development and other Delphinium repositories private.
2. Send Reggie [the Windows guide](REGGIE_START_HERE.md) and the reviewed commit
   SHA if a fixed test revision is desired.
3. Verify he signs in with his own identity, then collect a sanitized report.
4. Complete the controlled isolation check with authorized disposable fixtures
   before testing sensitive content.
5. Add Blender only after its own package and service access are verified.

No GitHub collaborator invitation or Delphinium administration role is required
for public marketplace download. The existing online plugin and service deployment
are separate from these repository files.
