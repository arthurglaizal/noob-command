Create a reusable command, skill, or equivalent called **Noob Command** for the current AI assistant.

Goal: let me invoke `noob` after a complex or long answer to receive a much simpler, shorter explanation without any action or modification.

First inspect the assistant's current native reusable-instruction mechanism. If personal/global and project-only installs both exist, ask which scope I want and wait. Prefer personal/global because this is a way of interacting with any project. Show the resolved path before writing, and never overwrite an existing installation without showing the difference and asking first.

Install this behavior:

```md
Re-explain your most recent answer in a simpler, easier-to-understand, and more concise way. Use earlier messages only when needed to make that answer understandable.

- Do not use tools or take any action. Do not create, edit, delete, send, install, or change anything.
- Use only the available conversation context. Do not add new research, analysis, recommendations, or assumptions.
- Reply in the user's language.
- Be concise: give the bottom line first, using one short paragraph and, only if useful, up to 3 short bullets.
- Use everyday words. Remove implementation details and jargon; explain any essential technical term in a few simple words.
- Say what the answer means for the user and what they need to do next, if anything.
- Do not repeat code, commands, logs, paths, or long lists unless essential.
- Preserve any important warning, blocker, or decision the user must make.

If there is no earlier assistant answer to simplify, say so in one short sentence. Each invocation is one read-only explanation; do not keep Noob mode active afterward.
```

Make it explicitly user-invoked if the assistant supports that. Keep it in the main conversation so it can read the preceding answer. Use the simplest current format, add no dependencies, and modify no unrelated files.

At the end, state what was created, where, how to invoke it, and whether read-only behavior is technically enforced or instruction-based.
