# Installation and acceptance checks

Use [Reggie's Windows guide](REGGIE_START_HERE.md) for the installation steps.
These checks distinguish preparation from observed tester results.

Record the client/version, package version, tested commit, date, observed result
and sanitized evidence using [the report template](TEST_REPORT_TEMPLATE.md).
Store raw account and fixture details privately.

## 1. Distribution and desktop installation

**Pending on Reggie's Windows PC.**

The owner will make the marketplace repository public. The package is in the
same repository as the catalog, so installation needs no read access to a
separate private development repository and no collaborator invitation.

Register the source, restart the current ChatGPT desktop app, and verify the
marketplace and single Developer entry in the plugin browser. Inspect that the
expected version, existing icon, activation skill and Developer MCP connection
actually load. Valid JSON or successful source registration is not a live install
pass. Record missing components or unsupported client behavior as failures.

## 2. Authentication and service access

**Pending for Reggie's account and this portable package.**

Use only Reggie's own sign-in. Let the host/provider run the normal authorization
flow after he reviews its provider and permissions. Do not embed client secrets,
reuse owner sessions or disable authentication. Extra scopes or unexpected
providers require review by the person granting access.

Read only `gds_agent_guide` first. The existing owner's connection returned that
guide on 2026-10-28; that result does not prove portable OAuth, Reggie's
entitlement, rich-card rendering or project isolation. If the backend is
restricted to the owner, report that service-access blocker separately from a
repository or install error. Do not change the service's access policy as part
of a package test.

## 3. Controlled account isolation

**Unverified. Required before using sensitive project content.**

The service guide says only the authenticated caller's owned projects can be
read or changed. This is a declared contract, not an independently observed
isolation result.

Use two expressly authorized test accounts and disposable fixtures. Keep their
identifiers and raw responses in a private evidence location. Before testing,
define the exact fixtures both owners have authorized for this check.

- Create a disposable marker under each identity through supported owner flows.
- Confirm each identity can list/read its own marker and its own permitted
  projection; neither account should receive the other's marker in lists.
- With the fixture owners' authorization, request the exact other fixture ID.
  Expect a denied/not-found result containing no foreign project content.
- Confirm the public tools do not accept a caller/owner identity override that
  expands access. Do not probe real owner records or arbitrary identifiers.
- Using a connection the tester agrees to disconnect, verify it requires valid
  authentication again before another protected read. Check provider/host
  revocation behavior without assuming cached chat content will disappear.

Successful authentication alone does not pass this check. Reggie seeing his own
project is useful but is not proof that foreign IDs are rejected.

## 4. Save, close and reopen

**Pending on Reggie's disposable project.**

Reggie explicitly chooses cloud storage and authorizes one test project in the
Windows guide. Do not substitute an owner project or invent an answer. The Pack
must retrieve current context, methods and readiness before guiding work.

Save one genuine answer with the service's current revision and operation ID
contract, then read fresh context to confirm it. Close the chat/client. In a new
conversation, reopen the same saved project and confirm its question state,
answers, decisions, corrections and revision persist without another project or
a duplicate interview.

Recover an uncertain operation with its original ID before retrying. Preserve
the saved interaction if the host needs native controls or a text fallback.
Record actual card rendering separately from persistence. Human owner review
remains in the service website; a stored report is not independent verification.

## Recovery

Report the failing step and last completed check. Disable/uninstall the candidate
through the desktop plugin browser. If also removing the registered source:

```powershell
codex plugin marketplace remove delphinium-private
```

Source removal, cached-plugin removal and connection revocation are separate
actions. Use the host/provider controls for each intended action. Do not delete
test project data automatically or alter the original App-bound listing.

