---
name: explain
description: Create a narrated, animated explanation of a topic that plays in the browser from a secret link. Use when the user asks to explain, visualize or teach something visually, or asks for an explainer video, rather than a text answer or a static diagram.
---

Create a narrated visual explanation of $ARGUMENTS with the chalkify MCP tools. When invoked automatically, explain the user's actual question, using any context they supplied.

1. Call `get_authoring_instructions` and follow them; use `get_scene_schema` for exact fields instead of guessing.
2. Call `create_explanation` and show the returned viewer link to the user immediately, before writing any scene. Keep working in the same turn while they watch.
3. Append one complete scene at a time with `append_scene`, starting with a short one-beat opener. If a scene is rejected, fix that same scene and resend it; if an append is interrupted, resend the identical scene.
4. Call `finalize_explanation` when every scene is accepted. Give the viewer link and mention any captions-only warning.

The first link is secret, not private: anyone who has it can watch, and it can't be withdrawn, so tell the user to keep it to themselves. If they want others to watch, call `share_explanation` and give them that link instead; `revoke_share` withdraws it.

If the tools are missing or the connection is refused, tell the user that chalkify needs an invite key in the `CHALKIFY_API_KEY` environment variable and that Claude Code must be restarted after setting it. Do not substitute a text answer.
