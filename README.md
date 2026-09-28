# agents

One `AGENTS.md` file. Every AI tool reads it. It survives every uninstall.

## What this is

A single file of working rules for coding agents: how to commit, how to plan,
how to write. It lives in its own folder and its own git repo, so no tool owns
it and no tool can lose it.

The rules cover five areas:

1. **Git commits** — never commit unless told. Conventional Commits. No trailers.
2. **Before you act** — read state first. Never break work that already runs. Scan for personal data before any commit.
3. **Writing style** — the Orwell rules from 1946, plus ASD-STE100 Simplified Technical English with countable limits.
4. **Never state what you have not checked** — run the command, then report the result.
5. **Replies** — result first. Cut every word that can go.

## Why it is not inside a tool folder

An `AGENTS.md` inside `~/.config/opencode/` dies with opencode. Nobody else can
read it. There is no history, so a bad edit has no way back.

So the file sits at `~/agents/AGENTS.md`, and each tool gets a link into its
own config folder. OpenCode reads the link and gets the same bytes. A new tool
needs one command:

```sh
ln -s ~/agents/AGENTS.md <tool-config-folder>/AGENTS.md
```

Some tools refuse to follow links. Copy the file for those.

## Why ASD-STE100

Aviation documentation cannot ask the reader a question, so it cannot afford a
sentence that reads two ways. ASD-STE100 is a controlled language built on that
idea: a fixed vocabulary of about 900 words and a set of countable rules.

The useful part is that the rules can be checked. Sentence length has a limit.
Verb tenses have a list. One word gets one meaning. A writer can test a draft
against them, not just read it and hope.

Orwell's 1946 rules say the same thing from the other end. Do not use a long
word where a short word will do. Cut the word if you can. Never hide the actor
behind a passive. Prefer the everyday word over the technical one, unless the
technical one is the exact name the code or API needs.

## Use it

Read [`AGENTS.md`](AGENTS.md). It is the whole product.

To take it:

```sh
git clone https://github.com/lxnre-codes/agents.git ~/agents
ln -s ~/agents/AGENTS.md ~/.config/opencode/AGENTS.md
```

Change what does not suit you. The file is yours once it is on your disk.

## Personal data

The rules forbid putting secrets, real names, employers, or employment history
into source, and require a scan before any commit. That rule exists because
publishing a working tool is a bad way to find out what a repository is
allowed to hold.

## License

MIT. See [`LICENSE`](LICENSE).

Copyright (c) 2026 lxnre-codes.
