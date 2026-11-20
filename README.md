# LinkedIn Local

A personal Codex plugin for reading your LinkedIn profile, feed and saved items through the browser on the Mac mini.

This is a browser workflow, not a LinkedIn API connector. It uses existing Codex browser controls and the browser's sign-in session. The plugin contains no server or credential store. The read scope is an instruction to the agent, not a technical permission boundary on the browser.

## First connection

1. Unlock the Mac mini.
2. Enable local browser use in Codex's Work/computer-use settings. Use Codex's offered browser/extension setup if needed.
3. Select **LinkedIn Local** and say: **Connect to LinkedIn on this Mac and verify read access.**
4. Complete the browser's supported secure sign-in or manual handoff if offered. Keep passwords and verification codes out of chat.
5. Codex verifies the visible signed-in identity and separately checks the feed, profile and saved items.

Example requests:

- “Read my LinkedIn profile and summarize it.”
- “Summarize five visible posts from my feed.”
- “Summarize five of my saved LinkedIn posts.”

Reading content through Codex makes it part of the conversation. This setup does not provide ChatGPT web/mobile access. Browser sign-in can expire and is checked again when used.

## Connection verification status

The latest connection attempt was blocked by Codex's browser controls with: `Local browser access is unavailable for this chat`. An earlier attempt reported: `Local browser use is disabled in Work settings`.

LinkedIn did not open, Google sign-in did not start, and profile, feed, and saved posts/articles access remain unverified. The plugin is installed, but installation alone does not establish an account connection.

If the same error occurs, check local browser access in the desktop app and try a fresh local Work chat with **LinkedIn Local** selected. Complete sign-in and any verification directly in the browser once access is available. Do not bypass unavailable browser controls or copy browser sessions into another tool.

## Installation and removal

Source: `/Users/dharmesh/plugins/linkedin-local`

Personal marketplace: `/Users/dharmesh/.agents/plugins/marketplace.json`

Install after the marketplace is discovered:

```sh
codex plugin add linkedin-local@dharmesh-personal --json
```

Remove this workflow:

```sh
codex plugin remove linkedin-local@dharmesh-personal
```

Removal does not sign you out of LinkedIn or disable general browser controls. Sign out in the relevant browser or disable Codex browser access to revoke browser access.
