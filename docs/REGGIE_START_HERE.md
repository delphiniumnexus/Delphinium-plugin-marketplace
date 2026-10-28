# Reggie: Windows setup and first test

This first beta tests **3DDDs Developer**. Blender comes later.

Use your own ChatGPT account and your own 3DDDs service sign-in. You do not need
Shaq's account, Delphinium admin access or a GitHub collaborator invitation.

## 1. Check your setup

- Install or update to the **new ChatGPT desktop app for Windows** with Work or
  Codex and the Plugins Directory. ChatGPT Classic and a browser tab are not the
  target for this local-marketplace test.
- Check that your account can use the relevant desktop features.
- Install a current **Codex CLI** and **Git for Windows** if you use the
  registration command below. Follow the official
  [Codex CLI setup](https://developers.openai.com/codex/cli) and
  [Git for Windows](https://git-scm.com/downloads/win) instructions.
- In PowerShell, check:

```powershell
codex --version
git --version
```

If a command is missing, finish its setup and open a new PowerShell window. You
should not need a GitHub personal access token to read this repository after
Shaq makes it public.

## 2. Add the marketplace

After Shaq makes the repository public, run:

```powershell
codex plugin marketplace add delphiniumnexus/Delphinium-plugin-marketplace --ref main
codex plugin marketplace list
```

For a fixed test revision, use the full commit SHA Shaq supplies instead of
`main`. Confirm the marketplace identifier `delphinium-private` appears.

Fully quit and reopen ChatGPT. In Work or Codex, open the Plugins Directory,
choose **Delphinium Beta Plugins**, then open **3DDDs Developer** and select
**Install plugin**. Review the included skill and Developer connection. The
expected package version is **1.0.3-marketplace.2**.

If a source was already added, inspect `codex plugin marketplace list` first.
Refresh that registered Git source with:

```powershell
codex plugin marketplace upgrade delphinium-private
```

Then restart ChatGPT and use the plugin browser's supported update/reinstall
controls if needed. Refreshing a source alone does not prove the installed
cached plugin was updated. A source pinned to a commit stays on that commit;
register the intended revision using the CLI's supported controls when changing
the pin.

### Download/local alternative

On the public [repository page](https://github.com/delphiniumnexus/Delphinium-plugin-marketplace),
choose **Code > Download ZIP**, extract the whole repository, and keep its
`.agents` and `plugins` directories together. Open the extracted folder as the
project in a supported desktop Work/Codex client, restart the app and look for
the repo marketplace in the plugin browser.

If you already have the CLI, you can register the extracted root explicitly:

```powershell
codex plugin marketplace add "C:\Users\YOUR_WINDOWS_USER\Downloads\Delphinium-plugin-marketplace-main"
```

Replace the example path with the actual extracted root. This is a marketplace
folder, not a standalone plugin-upload ZIP. Do not upload the whole repository
to a single-plugin archive importer.

If this client does not discover the marketplace or lacks the required plugin
browser, record that as a client compatibility blocker. Do not edit account
configuration or copy Shaq's App binding to force it to work.

## 3. Connect your own account

Complete the host's connection flow using your own identity. Review the provider
and permissions before accepting. This package contains no tokens, API keys,
preset login or shared session.

The Developer endpoint is:

`https://ddd-rule-packs.grayv516.chatgpt.site/mcp`

If authorization fails, says the service is private, or requests unexpected
permissions, stop and send Shaq the sanitized error. A public repository does not
change the hosted service's access policy. Do not send passwords, OAuth links,
tokens, cookies or full account screenshots.

## 4. Run the first test

Start a fresh conversation with **3DDDs Developer** and paste:

> I am testing the 3DDDs Developer beta. First read the live Developer guide to
> confirm the connection. Do not open or change a project yet. Tell me whether
> the connection works and whether this is the Developer Pack.

If that succeeds, paste:

> I consent to saving one new disposable test project in the 3DDDs cloud under my
> own signed-in account. Its goal is: "Reggie beta test: plan a simple personal
> to-do page." Create only this test project. Start the supported guidance, let
> me answer one simple question, and save my real answer. Do not publish, deploy,
> connect a code repository or change another project. Stop after confirming
> the saved answer and tell me how to reopen this same project.

Answer the question yourself. The assistant must not invent your answer or an
approval. If an owner review or phase approval is required, use the service's
supported website controls for this test.

Then:

1. Open the service website from the returned project link using the same
   identity. Check that the test project and answer are present.
2. Keep that project link privately, close the conversation and quit ChatGPT.
3. Reopen ChatGPT, start a fresh Developer conversation, and ask it to resume
   **that same test project** using the saved link.
4. Confirm that the same answer, question state and progress return without
   creating another project or restarting the interview.
5. Report whether the inline card worked or the supported text/native fallback
   was used. A fallback must preserve the same saved question.

Only disposable test content should be used until isolation has been checked.
The owner runs the separate controlled two-account check; do not guess project
IDs or try opening anyone else's real work.

## 5. Report what happened

Send Shaq a short report using [this template](TEST_REPORT_TEMPLATE.md): client
and package versions, tested commit, which step passed, and a sanitized error
if one failed. Keep project links and account identifiers in a private exchange.
Do not put them in a public GitHub issue.

If it fails, stop at that step. You can disable/uninstall the candidate in the
plugin browser. Removing a marketplace source does not necessarily uninstall its
cached plugin or revoke a service connection; use the host's separate controls.

Official references, checked 2026-10-28:
[marketplace registration and desktop testing](https://developers.openai.com/plugins/build/plugins),
[new desktop app](https://help.openai.com/en/articles/20001276-moving-to-the-new-chatgpt-desktop-app),
[plugin availability](https://help.openai.com/en/articles/20001256-plugins-in-chatgpt).
