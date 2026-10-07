# Chalkify

Ask Claude Code to explain anything, and watch the explanation build itself in your browser: a narrated, animated
walkthrough with diagrams, tables, graphs and code, playing while Claude is still writing it. Share it with a link.

Chalkify is in private alpha. It runs on a hosted service and needs an invite key.

## Install

1. Put your invite key in your shell's environment, for example in `~/.zshrc`:

   ```sh
   export CHALKIFY_API_KEY=lg_...
   ```

   For fish: `set -gx CHALKIFY_API_KEY lg_...` in `~/.config/fish/config.fish`.

2. Restart Claude Code, then install the plugin:

   ```
   /plugin marketplace add oneryalcin/chalkify
   /plugin install chalkify@chalkify
   ```

Nothing else is needed: no checkout, no local server, no voice model.

If Claude says the chalkify server failed to connect with "No invite key", Claude Code was started without
`CHALKIFY_API_KEY`. Shell config is only read by terminals: the Claude desktop app and IDE extensions (VS Code,
JetBrains) don't see it unless you start them from a terminal that has it, and a terminal opened before you set the key
needs reopening. Set the key, then restart Claude Code.

## Use

```
/chalkify:explain how a hash table finds a key
```

Or just ask Claude to explain something visually. Claude shows a private link first; open it and the explanation
plays as each part is ready. Ask Claude to share it to get a separate link you can send to anyone, and to revoke that
link when you want.

## Good to know

- **Private by default.** Only people with the link can watch. A share link is separate and can be revoked.
- **Limits in the alpha.** Each explanation runs up to 3 minutes; each person gets 5 hours of narration a month.
  When narration runs out, explanations still play, with captions.
- **Audio is kept for 3 months after the last view.** After that the explanation still plays, with captions.
- Your invite key is a password: keep it out of chats, issues and repositories.
