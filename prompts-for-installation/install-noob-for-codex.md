Install a reusable Codex skill called **Noob Command**.

Goal: give me `$noob`, a one-shot command that re-explains the assistant's latest answer in simpler, shorter language without using tools or changing anything.

## Before writing

1. Ask whether I want a **personal/global** install (recommended) or a **project-only** install, then wait for my answer.
2. Check the current official Codex skills documentation and my local environment. Resolve the current native format and exact path instead of relying on this prompt's paths.
3. Show every path you will create. Warn me if writing outside the workspace needs approval.
4. Check for an existing file, folder, or symbolic link. If one exists, show the difference and ask before replacing it.

## Skill to install

Use the current native Codex skill format. Name it `noob`, make it explicitly user-invoked only, and use this instruction body:

```md
# Noob

Re-explain your most recent answer in a simpler, easier-to-understand, and more concise way. Use earlier messages only when needed to make that answer understandable.

- Do not call tools or take any action. Do not create, edit, delete, send, install, or change anything.
- Use only the available conversation context. Do not add new research, analysis, recommendations, or assumptions.
- Reply in the user's language.
- Be concise: give the bottom line first, using one short paragraph and, only if useful, up to 3 short bullets.
- Use everyday words. Remove implementation details and jargon; if a technical term is essential, explain it in a few simple words.
- Say what the answer means for the user and what they need to do next, if anything.
- Do not repeat code, commands, logs, paths, or long lists unless essential to understanding.
- Preserve any important warning, blocker, or decision the user must make.

If there is no earlier assistant answer to simplify, say so in one short sentence.

Each invocation is one read-only explanation. Do not keep Noob mode active afterward.
```

Use this description if the format supports one:

```txt
Re-explain the assistant's most recent answer in a simpler, easier-to-understand, and more concise way, without taking action or changing anything. Use only when the user explicitly invokes `$noob`.
```

If supported, present it as **Noob Command**, use the short description `Explain the last answer simply and concisely.`, and disable implicit invocation. Do not create a legacy prompt unless I explicitly ask for it.

## Finish

Validate the files and metadata. Then tell me briefly what was installed, where, how to invoke `$noob`, whether a restart or new conversation is needed, and whether the read-only boundary is technically enforced or instruction-based.

Do not modify unrelated files, add dependencies, or change project configuration.
