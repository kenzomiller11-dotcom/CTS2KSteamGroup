# Project brief

## Project and source proposal

Working repository title: **What Players Value: Destiny 2 vs Warframe**.

The topic statement is titled *What Players Value: Comparing Recommended
and Non-Recommended MMORPG Steam Reviews*. Its motivating questions include
differences in monetization, gameplay and story discussions between review
recommendation groups.

## Scope decision for the group

Original broader question:

> How do discussions of monetization, gameplay, and story differ between
> recommended and non-recommended reviews?

Suggested narrower question that matches the current implemented analysis:

> How does spending-related language differ between recommended and
> not-recommended Steam reviews of Destiny 2 and Warframe, and what do
> contextual checks reveal about those keyword matches?

The narrower wording is a proposal, not a recorded group decision. Agree
either to narrow the final question or to finish the gameplay/story analysis.
Do not describe unimplemented themes as completed findings.

## Dataset and methods

- Two game files, 1,000 rows each, from Thomas Byers's Steam review dataset.
- Use review text and Steam's `voted_up` recommendation label.
- Drop missing review text, lowercase words, trim punctuation and remove
  the notebook's short stopword list.
- Count selected words and compare normalized frequencies.
- Compare the percentage of reviews mentioning spending keywords.
- Read examples in context and record manual complaint judgements.

Recommendation status is Steam's recommend/not-recommend label; the code
does not automatically classify every sentence's emotional sentiment.
This is descriptive analysis of a historical dataset, not proof of game
quality, review validity, player motivation, or internet culture's causal
influence. Those broader ideas need evidence beyond the current counts.

## Evidence locations

- Code: [working notebook](../notebooks/Steam_Reviews_D2_VS_Warframe.ipynb)
- Saved results and limitations: [current findings](current_findings.md)
- Task ownership: [task board](task_board.md)
- Original topic statement: supplied group document; upload the original
  separately if the team wants it in this repository.
