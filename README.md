# Better Path

A skill for Claude that answers the question you asked, then offers the better option you did not know to ask about.

## The problem

Assistants are very good at answering inside the options you hand them. Ask whether Bubble or Lovable is better and you get a careful comparison of Bubble and Lovable, even when neither is the best way to reach what you were actually after. The advice is accurate and the outcome is still worse, because nobody looked outside the frame the question arrived in.

Every question carries a frame the asker already accepted. Better Path answers inside that frame first, then looks at the frame.

## Before and after

**Without the skill**

> **You:** How long should I put this broccoli in the microwave?
>
> **Claude:** About 5 minutes in the steamer bag, then let it sit for a minute before opening.

**With the skill**

> **You:** How long should I put this broccoli in the microwave?
>
> **Claude:** 5 minutes. If you have a little more time and would like another option, you could put the broccoli on a baking sheet with oil, salt, pepper, and garlic powder for 20 minutes. This gives the broccoli a great flavor with a little crunch.

The same move works at any scale. The size of the decision changes how much analysis it gets, not whether the second look happens.

## What it does

- Answers the question first, plainly, inside the frame it was asked in
- Offers one option, with what it costs and what it gives you
- Stays quiet when no genuinely better option exists
- Includes the argument against its own suggestion when there is one
- Verifies specifics rather than inventing products, prices, or features
- Stops advocating once you decide, and helps you do the thing you chose

## Installing

Clone the repo and copy the skill folder into your skills directory.

```bash
git clone https://github.com/bclaus9126/better-path.git
cp -r better-path/better-path ~/.claude/skills/
```

For a project rather than your whole account, copy it into `.claude/skills/` inside the project instead.

Restart Claude Code, or start a new session, and the skill will be available.

## Invoking it directly

The skill is written to activate on its own. To force it:

```
/better-path
```

Or ask for it in words: "run this through better-path before you answer."

## The trigger boundary

The trigger is deliberately wide. It fires on small questions as readily as large ones, because a cooking question can contain a better option just as a tech stack question can.

The control is the quality bar, not the trigger. An option is offered only when one is genuinely better, and only when its advantage is large enough to be worth the interruption. Most of the time the correct behavior is to answer the question and stop.

It stays out of the way entirely for emergencies, emotional support, execution tasks, constrained creative deliverables, and decisions you have already made and committed to.

`test/trigger-prompts.md` has the positive and negative cases, and the failure modes worth watching for.

## Supported environments

Written for Claude Code and Claude Desktop. The instructions are plain markdown with no tool dependencies, so it also works pasted into a project instruction or a custom system prompt, minus the reference file loading.

The `references/quantitative-decisions.md` file loads only when a decision turns on numbers, which keeps the main skill short.

## A note on third-party skills

Read any skill before you install it, including this one. A skill is instructions that shape how a model responds to you, and you should know what those instructions say. The whole thing is under 200 lines of markdown.

## License

MIT. See LICENSE.
