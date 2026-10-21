# Installation and acceptance gates

All gates below are separate. Local preparation passed no live install gate.
Record client/version, account used, reviewed commit/package version, UTC time,
observed result, and sanitized evidence for each gate. Keep tokens, email addresses,
project content, and owner identifiers out of this repository.

## 1. Private source and client installation

Status: pending. Reggie's account, client eligibility, and private-repo read access
are unverified. The owner has not authorized a push, invitation, or access change.

After the owner approves the exact local diff, push only the isolated branch to
the existing private repository. Choose a reviewed commit containing the catalog.
An eligible account with already authorized read access can register that exact
commit using the README command. Do not add a personal access token to a URL or
package. If access is absent, stop and request a separate access decision.

In the supported desktop plugin browser, confirm the marketplace title and the
single Developer entry. Review its package/permissions before installing. Confirm
the expected version, icon, activation skill, and named MCP connection load in a
fresh test conversation. Installation must be observed; CLI registration or valid
JSON is insufficient. Stop if the client drops the skill/server or needs unsupported
App bindings. Do not recreate the online listing to bypass that incompatibility.

## 2. Authentication and service authorization

Status: pending for this package and Reggie's account. A separate existing owner
connection returned its guide; this does not clear this gate.

Use only the intended tester's own existing authorized session. Inspect the
provider and requested scopes. Obtain explicit approval before creating any OAuth
grant, registering a client, entering credentials, or accepting additional scopes.
Never reuse the founder's tokens or cookies. Once authorized, read only
`gds_agent_guide` first and record success without touching projects. Stop on an
auth or entitlement failure; report the failing layer and sanitized error.

## 3. Data isolation

Status: unverified. Installation and successful authentication do not clear it.

With separately approved test identities and disposable fixtures, verify each
account can see only its own permitted projects/context. Attempt a bounded read of
a specifically approved foreign fixture identifier and confirm denial without
returning foreign content. Do not enumerate or probe real owner projects. Confirm
that caller IDs or ownership claims cannot expand access, and that a revoked or
disconnected session loses the affected access. Keep fixture identifiers and raw
responses in the private test evidence location, outside this distribution repo.
Do not perform this negative test until its identities/fixtures are authorized.

## 4. Save, close, and reopen

Status: unverified. This requires an expressly authorized write to a tester-owned
disposable project and must not use the founder's project as a shortcut.

Select that project, load current guide/methods/readiness/context, and render the
existing interaction. Save one genuine answer using the current revision and one
operation ID. Reread to verify the saved result. Close the chat/client and reopen
the same project in a fresh conversation. Confirm the same saved interaction,
answers, decisions, corrections, and revision persist without a restart or duplicate
question. Exercise permitted recovery with the original operation ID if a save is
uncertain. Observe card rendering or the guide's fallback controls. Human acceptance
stays with the owner on the website; a stored report is not independent verification.

## Recovery and rollback

For a failed pilot, record the exact action, target, reason, and last completed
gate. Stop the affected action. Remove the candidate through the host's supported
uninstall/source-removal UI or `codex plugin marketplace remove delphinium-private`
when removal is authorized. Revoking a grant is a separate account action. Do not
delete project data or alter the original App-bound listing. Local preparation can
be abandoned by retaining its branch/diff and returning to the untouched base.
