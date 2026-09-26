# The Shortlist

A Claude skill for actually deciding what to buy — not just comparing it.

Most shopping decisions don't stall for lack of options. They stall because there are too many options, the reviews contradict each other, and nothing tells you which factor actually matters for *your* situation. The Shortlist asks a few short questions about fit and use-case, weighs quality and durability alongside price instead of defaulting to price, and ends with one clear pick and a reason — not a table you still have to interpret yourself.

## What it does

1. Asks 2–3 quick questions about fit and use-case (not price) — and lets you give more than one answer when more than one applies (e.g. "sensitive *and* dry *and* breakout-prone" skin, all at once).
2. Asks about budget separately, as one input among several rather than the deciding factor.
3. Recommends 4–6 real, currently-sold options, weighing suitability, quality, and durability alongside price. Each option comes with what's good about it and what to watch out for.
4. Gives one clear pick, with reasoning tied directly to your answers.
5. Points you to a live search (never a guessed or possibly-stale link) so you can confirm today's actual price and stock before buying.

## Install

This is a [Claude Code](https://claude.com/claude-code) skill — a `SKILL.md` file that changes how Claude behaves in conversation, not a standalone app.

```bash
git clone https://github.com/<your-username>/the-shortlist.git
mkdir -p ~/.claude/skills
cp -r the-shortlist ~/.claude/skills/
```

Claude Code picks up skills from `~/.claude/skills/` automatically. Once it's there, just ask Claude something like the examples below — no separate registration step, and no extra tools or API keys required.

## Example

> **You:** Help me pick a pair of running shoes, I'm in the US, don't want to overspend.
>
> **Claude:** *(asks about terrain, weekly mileage, foot/gait notes)*
>
> **You:** *(answers)*
>
> **Claude:** *(asks budget, separately)*
>
> **You:** *(answers)*
>
> **Claude:** *(gives 4–6 real shoes, weighs support/durability/fit alongside price, picks one and explains why, points you to a live search to confirm current price and stock)*

## Why it's built this way

- **Questions before recommendations.** A recommendation is only as good as the fit it's based on — so nothing gets suggested until the skill knows what actually matters to you.
- **Multiple things can matter at once.** Real shopping criteria rarely reduce to one variable; the skill is written to treat several stated needs as simultaneous, not alternatives to pick between.
- **Price is a factor, not the sort key.** Cheapest-that-works and best-that-fits are often different answers, and this skill is built to give the second one.
- **Never a guessed link.** Product pages go stale, get discontinued, or never existed the way they're remembered. The skill only ever points to a live search (e.g. "search Amazon.in for '[exact product name]'"), never a specific URL typed from memory.

## Scope

Built for everyday consumer purchases — skincare, electronics, home goods, apparel, and similar. It works from general product knowledge, not a live price feed, so treat prices as typical ranges and always confirm exact price, stock, and current model name with the retailer before buying.

## License

MIT — see [LICENSE](LICENSE).
