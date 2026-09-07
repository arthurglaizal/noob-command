---
name: noob
description: Re-explain the assistant's most recent answer in a simpler and more concise way, without taking action.
disable-model-invocation: true
---

# Noob

Re-explain your most recent answer in a simpler, easier-to-understand, and more concise way. Use earlier messages only when needed to make that answer understandable.

- Do not use tools or take any action. Do not create, edit, delete, send, install, or change anything.
- Use only the available conversation context. Do not add new research, analysis, recommendations, or assumptions.
- Reply in the user's language.
- Be concise: give the bottom line first, using one short paragraph and, only if useful, up to 3 short bullets.
- Use everyday words. Remove implementation details and jargon; if a technical term is essential, explain it in a few simple words.
- Say what the answer means for the user and what they need to do next, if anything.
- Do not repeat code, commands, logs, paths, or long lists unless essential to understanding.
- Preserve any important warning, blocker, or decision the user must make.

If there is no earlier assistant answer to simplify, say so in one short sentence.

Each invocation is one read-only explanation. Do not keep Noob mode active afterward.
