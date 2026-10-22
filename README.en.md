# ryoiki-tenkai (Domain Expansion)

English ｜ [繁體中文](README.md)

An agent skill that **expands** an idea, task or industry before any work starts, then converges it into an executable plan. Named after "Ryōiki Tenkai" (Domain Expansion) from *Jujutsu Kaisen*.

The process is adapted from the four dimensions in Felix Rieseberg's "How to be more ambitious: A tutorial for humans with models": altitude, depth, breadth and external judges. The order is always **diverge first, then converge**, and the conclusion is allowed to replace the original question.

The skill and prompt text are written in Traditional Chinese; the agent replies in the user's language.

## What it does

Eight steps, ending in a file and a YAML summary:

| Step | Content |
|---|---|
| 1. Raise the altitude | Ask "what should happen after this is done?" three times; write the literal, one-level-up and ultimate versions, and recommend one |
| 2. Describe it with verbs | Replace nouns like "report" or "app" with the 3–5 actions the work actually performs |
| 3. Diverge | One or two directions each from: another field, the inverse, a different audience, a different spot in the value chain, 10x better AI, an unreasonable goal |
| 4. Build a crew | 5–7 disciplines, at least 2 that insiders would not think of, always including a red team |
| 5. Challenge assumptions | List unstated assumptions, mark the 3 most fragile and the cheapest way to disprove each |
| 6. External judges | Executable checks, real-world data, real people; "the AI grades itself" does not count |
| 7. Converge | Score directions, pick a primary direction and a bold bet, split into workstreams, list the first 3 actions and kill criteria |
| 8. Rewrite the prompt | Turn the original task into a more ambitious, concrete instruction an agent can execute |

Key rules: no role-play; tag every claim as fact, estimate or to-be-checked; no advice that only does the same thing faster; delete any sentence that would still apply to a different field.

## Three modes

| You say | The agent |
|---|---|
| "領域展開" / "ryoiki tenkai" + a topic | Runs all eight steps, writes `docs/expansion-<name>-<date>.md`, replies with a summary |
| "quick" / "short version" | Answers four questions in the chat, then rewrites the prompt |
| "give me the prompt" | Returns `prompt.md` so you can paste it into another model or agent |

## Install

### Claude Code

```bash
git clone https://github.com/ailazytech/ryoiki-tenkai.git ~/.claude/skills/ryoiki-tenkai
```

Start a new session. Phrases like "領域展開", "ryoiki tenkai", "not ambitious enough" or "stuck on direction" trigger it.

### Other agents or models

Agents that read `SKILL.md`: put the folder in their skills directory. Others: paste the full or short prompt from `prompt.md`.

## Files

- `SKILL.md`: the skill instructions for agents (steps, rules, output format)
- `prompt.md`: ready-to-paste prompts (full and short)

## License

MIT
