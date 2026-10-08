# Chalkify

Ask Claude Code to explain anything, and watch the explanation build itself in your browser: a narrated, animated
walkthrough with diagrams, tables, graphs and code, playing while Claude is still writing it. Share it with a link.

Chalkify is in early alpha. It runs on a hosted service; you sign in with one click, no account needed.

## Install

```
/plugin marketplace add oneryalcin/chalkify
/plugin install chalkify@chalkify
```

Then sign in once: run `/mcp`, choose **chalkify** and **Authenticate**. A browser page opens; press **Continue**.
Claude Code keeps the sign-in, in the terminal, the desktop app and IDE extensions alike.

Nothing else is needed: no key, no checkout, no local server, no voice model.

If Claude says chalkify needs authentication, or the sign-in expired, run `/mcp` and Authenticate again.

## Use

```
/chalkify:explain how a hash table finds a key
```

Or just ask Claude to explain something visually. Claude shows your link first; open it and the explanation
plays as each part is ready. Ask Claude to share it to get a separate link you can send to anyone, and to revoke that
link when you want. A finished explanation has an **Export video** button (Chrome) that downloads an MP4.

## Good to know

- **Links are secret, not private.** Anyone who has a link can watch, without signing in, and nobody can guess one.
  Keep the first link Claude gives you to yourself: it can't be withdrawn. To show other people, ask Claude to share
  the explanation; that gives a separate link you can revoke at any time.
- **Limits in the alpha.** Each explanation runs up to 3 minutes, and a one-click sign-in includes 10 minutes of
  narration a month. When narration runs out, explanations still play, with captions.
- **Audio is kept for 30 days after the last view.** After that the explanation still plays, with captions.
- **Signing in again** (for example after `/mcp` → Authenticate) starts a new, separate sign-in: explanations made
  before still play from their links, but Claude can't add to them.

## Alpha testers with an invite key

Version 0.2 signs in instead of using `CHALKIFY_API_KEY`. Update with `/plugin update chalkify`, then run
`/reload-plugins` (or restart Claude Code) and sign in as above. Until the plugins reload you may see one
"Server rejected the configured Authorization header" message from the old version; it goes away. Explanations you made with your key still play from their links.
