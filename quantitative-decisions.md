# Quantitative Decisions

Read this when a recommendation turns on break-even timing, recurring versus one-time costs, opportunity cost, compounding, recoverable capital, or exit costs.

Picking the right model matters more than the arithmetic. A plausible calculation on the wrong model produces a specific, confident, backwards answer, which is worse than no number at all. State in one line what you are modeling and why that is the right frame, then run it.

## Modeling rules

- **Model only the delta.** What differs between the options, not the totals they share. If both paths carry the same base cost, that base is noise.
- **Include what the money or time would otherwise have earned.** Money not spent here earns something there. Hours saved are a gain only if those hours go somewhere that produces.
- **Include exit costs.** Selling costs, termination fees, migration, unwinding, severance. Short horizons fail here and it is the most commonly skipped input.
- **Give the break-even, not just the winner.** "Better after month 31" is more useful than "better."
- **Where an input is a guess, say so, and give the threshold where the answer flips.** A range with a tipping point beats false precision.
- **Check that the rule of thumb still holds at the actual numbers.** A heuristic that produces a strong answer at one input can produce a weak one at another. Pricing a home to cross a search filter break is a strong move at $415,000, where the nearest break is $16,000 down. At $430,000 the nearest break is $5,000 down, which is too small to function as a reduction. Say when you are at the edge of where the rule works.
- **Write code for anything with more than three moving parts.** Do not do compounding arithmetic in your head.

## Wrong models that produce confident, backwards answers

Check against these before trusting a calculation. Each one yields a specific, plausible number pointing the wrong way.

- **Recoverable capital treated as spent.** A down payment, a deposit, inventory, equity in anything. That money is not consumed, it comes back. The cost is the return it would have earned elsewhere, not the principal.
- **Opportunity cost of capital or time left out.** Compare against what the alternative use would have produced, not against zero.
- **Exit costs ignored.** See above. It is worth checking twice.
- **Totals compared when only the delta matters.**
- **Averages used where the spread decides.** A median says nothing about the specific case and hides the tail. When one tail is ruinous, the average is the wrong statistic entirely.
- **Recurring and one-time costs compared without a horizon.** $200 a month is $12,000 over five years. Put both on the same clock.
- **Taxes and inflation dropped from multi-year comparisons.** Deductibility and capital gains treatment can invert a pre-tax answer.
- **Compounding done linearly.** Interest, growth, amortization.
- **One observation turned into a pattern.** One deal from a channel is not a channel strategy. Ask how many observations sit behind a claim before it becomes a plan.
- **Survivors studied without the dead.** The customers who stayed, the listings that sold, the founders who made it. What is missing from the sample is usually where the answer is.

## Worked example: picking the wrong model

A buyer plans to put an extra $75,000 down on a house and sell in four years.

**The obvious model.** Divide the extra cash by the monthly payment savings and see how long it takes to recover. At roughly $675 a month saved, $75,000 takes over nine years to come back. Conclusion: never do it on a four year hold.

**Why it is wrong.** The $75,000 is not spent. It sits in equity and returns at closing. Treating recoverable capital as consumed is the single most common error in this category.

**The right model.** Compare what the $75,000 saves in interest and mortgage insurance against what it would have earned invested. Roughly $675 a month saved against roughly $280 a month forgone at a 4.5% return means the larger down payment wins from month one, not month one hundred and nine. Opposite conclusion from the same inputs.

**What neither version surfaced.** The real risk in a four year hold is that selling costs of seven to eight percent can exceed the equity built, which puts the low-down-payment buyer underwater at closing. That is the conversation worth having, and the original question did not contain it.

## Cost asymmetry

Errors are rarely symmetric, and people tune their behavior as if they are. Chasing a dead lead costs an hour. Missing a live one costs a commission. Shipping a bug costs a patch. Shipping late costs the quarter.

Say which direction is expensive and let it move the recommendation. When one error is cheap and reversible and the other is not, the answer is usually to take the cheap risk quickly rather than study it.

Pair this with reversibility. A decision that can be undone in a week deserves a fast call and a test. A decision that cannot deserves the full model.
