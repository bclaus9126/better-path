# Trigger Test Prompts

Run these against the skill to check the activation boundary. The boundary is deliberately wide, because trivial questions often do contain a better option. The control is the quality bar, not the trigger: an option is offered only when one is genuinely better and its advantage clears the relevance threshold.

## Should produce an option

| Prompt | The option that should surface |
| --- | --- |
| "How long should I microwave this broccoli?" | Roasting, with the time cost stated |
| "What temperature should chicken reach?" | 165°F instantaneous is not the only safe answer. USDA time-temperature tables put 145°F held 8.9 minutes at equal lethality for lean chicken, with better texture |
| "Should I reduce the price or offer seller concessions?" | Whether price is the problem at all, before choosing between the two |
| "Would Bubble or Lovable be better for this app?" | Building it in code, with the setup and learning cost stated |
| "Should I put 20% down to avoid mortgage insurance?" | The right model, and the break-even at their hold period |
| "What's the fastest way to migrate this spreadsheet into a database?" | Whether it needs a database at all |
| "Which of these two laptops should I buy?" | Depends on the deciding fact, so ask for it |
| "I'm buying a riding mower with a 21 inch deck." | The spec does not match the category, which comes before any vendor comparison |

## Should not produce an option

| Prompt | Why |
| --- | --- |
| "Fix the grammar in this paragraph." | Execution task, no decision in it |
| "Who wrote The Republic?" | Settled fact, nothing outside the frame |
| "Write a condolence message." | Constrained creative deliverable, an option would interrupt finishing it |
| "Call 911 or drive to the emergency room?" | Emergency, answer only |
| "My dad passed last week and I'm trying to write something for the service." | Emotional support, not a decision problem |
| "I signed the contract yesterday, how do I set up the integration?" | Door is closed |
| "I already looked at the alternatives and I'm going with Postgres. How do I set up connection pooling?" | They said they considered it |
| "What does this Python error mean?" | Diagnostic question. An option is only warranted if a genuinely better approach exists, not by default |

## Failure modes to watch for

- **Manufactured options.** An alternative offered because the pattern expects one, not because it is better. Watch the "should not" list above.
- **The sting.** The option framed as a correction of what they asked, rather than as an option.
- **Invented specifics.** A product, price, feature, or plan limit stated without verification. The most common real-world failure.
- **Selling.** A line explaining why the suggestion is good. State it and stop.
- **Nagging.** Re-raising an option after the person declined it.
- **Density.** Every answer in a long session carrying a second paragraph. The pattern becomes noise regardless of the quality of any single instance.
